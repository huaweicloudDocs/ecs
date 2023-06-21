# Linux系统上擎天Enclave应用的开发<a name="ecs_03_1415"></a>

## 擎天Enclave SDK<a name="zh-cn_topic_0000001409393257_section12691146193814"></a>

擎天Enclave SDK由一系列开源库组成，以便您开发自己的擎天Enclave应用程序。此外，SDK集成了KMS接口，该接口内置了获取证明文档及调用华为云KMS相关服务的功能。在典型使用案例里，我们描述了在擎天Enclave调用KMS解密接口的实例。

## Vsock通信实例<a name="zh-cn_topic_0000001409393257_section688618101393"></a>

本节主要通过vsock实例来指导如何在Linux环境下开发擎天Enclave应用程序。本节中提供的vsock程序只支持在Linux环境下运行。

通过该vsock程序，可以帮助开发者了解到父虚拟机和擎天Enclave间如何进行消息传递从而实现双方交互。该vsock程序带有Server和Client参数，通过指定该参数可以指定父虚拟机或者擎天Enclave虚拟机扮演相应角色。在该vsock程序中，客户端程序会发送一段简单的文本信息通过vsock通道传递给服务端程序，同时服务端程序会监听相应的vsock通道，一旦收到来自客户端的消息后，会将其收到的消息打印在终端界面上。

在下面介绍中，我们将说明如何让擎天Enclave扮演服务端等待并接收来自客户端父虚拟机的hello world信息：

1.  编写一个SocketCommunication.py程序：

```
#!/usr/local/env python3
import argparse
import socket
import sys
​
CID_DEFAULT = 3
PORT_DEFAULT = 9999
TIMEOUT = 5
BLACKLOG_DEFAULT = 5
​
class Client:
    def __init__(self, cid, port):
        self.clientAddr = (cid, port)
        self.connect()
​
    def connect(self):
        self.socket = socket.socket(socket.AF_VSOCK, socket.SOCK_STREAM)
        self.socket.settimeout(TIMEOUT)
        print("connecting to the server")
        try:
            self.socket.connect(self.clientAddr)
        except socket.error:
            print("client's socket connection err")
            sys.exit(1)
​
    def send(self, msg):
        print("client sends hello to the server")
        self.socket.sendall(msg)
​
    def disconnect(self):
        self.socket.close()
​
    def receiveData(self):
        while True:
            try:
                message = self.socket.recv().decode()
            except (socket.error, UnicodeDecodeError):
                break
            if message:
                print(message, end = " ", flush = True)
        print()
​
def clientHandler(args):
    client = Client(args.cid, args.port)
    message = "Hello world"
    client.send(message.encode())
    client.disconnect()
​
class Server:
    def __init__(self, port):
        self.socket = socket.socket(socket.AF_VSOCK, socket.SOCK_STREAM)
        self.serverAddr = (socket.VMADDR_CID_ANY, port)
        self.socket.bind(self.serverAddr)
        self.socket.listen(BLACKLOG_DEFAULT)
​
    def receiveData(self):
        while True:
            print("waiting for a connection")
            (conn, clientAddr) = self.socket.accept()
            try:
                print("connection from ", clientAddr)
                while True:
                    try: 
                        data = conn.recv(256).decode()
                    except (socket.error, UnicodeDecodeError):
                        break
                    if data:
                        print("data: ", data)
                    else:
                        print("connection close")
                        break
            finally:
                conn.close()
​
def serverHandler(args):
    server = Server(args.port)
    server.receiveData()
​
​
def main():
    parser = argparse.ArgumentParser(description = "Hello world demo", prog='SocketCommunication')
    subparsers = parser.add_subparsers(description = "Communication roles")
    parserClient = subparsers.add_parser("Client", description = "Client",
                                        help = "Communicate with server using a given cid and port.")
    parserClient.add_argument("-c", "--cid", default = CID_DEFAULT, type = int, help = "Client's Cid")
    parserClient.add_argument("-p", "--port", default = PORT_DEFAULT, type = int, help = "Client's port")
    parserClient.set_defaults(func = clientHandler)
    parserServer = subparsers.add_parser("Server", description = "Server", help = "Listen on a given port")
    parserServer.add_argument("-p", "--port", default = PORT_DEFAULT, type = int, help = "Server's Port")
    parserServer.set_defaults(func = serverHandler)
    if len(sys.argv) < 2:
        parser.print_usage()
        sys.exit(1)
    args = parser.parse_args()
    args.func(args)
​
​
if __name__ == "__main__":
    main()
```

1.  创建一个Dockerfile文件，内容如下：

```
#start the Docker image from ubuntu
FROM ubuntu AS base-img
WORKDIR /home/builder
# COPY vsocket example
COPY . vsocket
# install relative dependencies
RUN apt-get update && \
    apt-get install python3 -y && \
    apt-get install gcc -y && \
    apt-get install gawk -y
# Launch a client
CMD ["python3", "/home/builder/vsocket/SocketCommunication.py","Server","-p 9999"]
```

1.  构建docker镜像：

```
sudo docker build -t vsock-sample-client -f Dockerfile .
```

1.  将docker镜像转化为擎天Enclave镜像：

```
qt enclave make-img --docker-uri vsock-sample-client --eif vsock_sample.eif
```

1.  使用vsock\_sample.eif以debug模式启动擎天Enclave:

```
qt enclave start --cpus 2 --mem 4096 --eif vsock_sample.eif --debug-mode --cid 4
```

然后使用qt enclave console命令查看擎天Enclave内只读终端输出：

```
qt enclave console --enclave-id 0
waiting for a connection
```

1.  然后另起一个父虚拟机终端，启动客户端程序：

```
Python3 SocketCommunication.py Client -c 4 -p 9999
```

1.  当服务端程序收到来着vsock的消息后，会打印如下消息到终端上：

```
connection from  (3, 4180219645)
data:  Hello world
connection close
waiting for a connection
```

