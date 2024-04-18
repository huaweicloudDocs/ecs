# Linux系统上QingTian Enclave应用的开发<a name="ecs_03_1415"></a>

## QingTian Enclave SDK<a name="zh-cn_topic_0000001409393257_section12691146193814"></a>

QingTian Enclave SDK由一系列开源库组成，以便您开发自己的QingTian Enclave应用程序。其中包括QingTian安全模块（QingTian Security Module，QTSM）提供的qtsm-lib函数库。此外，SDK集成了KMS接口，该接口内置了获取证明文档及调用华为云KMS相关服务的功能。在典型使用案例里，我们描述了在QingTian Enclave调用KMS解密接口的实例。

**表 1**  接口介绍

<a name="table11323191018384"></a>
<table><thead align="left"><tr id="row3324610163818"><th class="cellrowborder" valign="top" width="14.2%" id="mcps1.2.4.1.1"><p id="p4671106103918"><a name="p4671106103918"></a><a name="p4671106103918"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.56%" id="mcps1.2.4.1.2"><p id="p1132412105386"><a name="p1132412105386"></a><a name="p1132412105386"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="46.239999999999995%" id="mcps1.2.4.1.3"><p id="p8324201013383"><a name="p8324201013383"></a><a name="p8324201013383"></a>接口描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row732461083815"><td class="cellrowborder" rowspan="7" valign="top" width="14.2%" headers="mcps1.2.4.1.1 "><p id="p188417754113"><a name="p188417754113"></a><a name="p188417754113"></a>libqtsm接口</p>
</td>
<td class="cellrowborder" valign="top" width="39.56%" headers="mcps1.2.4.1.2 "><p id="p77341213394"><a name="p77341213394"></a><a name="p77341213394"></a>qtsm_describe_pcr</p>
</td>
<td class="cellrowborder" valign="top" width="46.239999999999995%" headers="mcps1.2.4.1.3 "><p id="p18324610123818"><a name="p18324610123818"></a><a name="p18324610123818"></a>查询指定index的PCR数据信息</p>
</td>
</tr>
<tr id="row1770842612381"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p4709192633815"><a name="p4709192633815"></a><a name="p4709192633815"></a>qtsm_extend_pcr</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p970932673813"><a name="p970932673813"></a><a name="p970932673813"></a>扩展指定index对应的PCR值</p>
</td>
</tr>
<tr id="row1470912610386"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1570919265383"><a name="p1570919265383"></a><a name="p1570919265383"></a>qtsm_lock_pcr</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1370912264384"><a name="p1370912264384"></a><a name="p1370912264384"></a>锁定指定index的PCR数据信息</p>
</td>
</tr>
<tr id="row1070912269387"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p177091926113819"><a name="p177091926113819"></a><a name="p177091926113819"></a>qtsm_lock_pcrs</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1171062613810"><a name="p1171062613810"></a><a name="p1171062613810"></a>批量锁定指定index对应的PCR值</p>
</td>
</tr>
<tr id="row19710112614385"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1171042615384"><a name="p1171042615384"></a><a name="p1171042615384"></a>qtsm_get_describe</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p7710132603818"><a name="p7710132603818"></a><a name="p7710132603818"></a>获取qtsm信息</p>
</td>
</tr>
<tr id="row17101326153810"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p732154263214"><a name="p732154263214"></a><a name="p732154263214"></a>qtsm_get_attestation</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p10710192613387"><a name="p10710192613387"></a><a name="p10710192613387"></a>获取Attestation Doc</p>
</td>
</tr>
<tr id="row1749175283116"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p632642173218"><a name="p632642173218"></a><a name="p632642173218"></a>qtsm_get_random</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p84911152193118"><a name="p84911152193118"></a><a name="p84911152193118"></a>获取硬件随机数</p>
</td>
</tr>
<tr id="row19324151063818"><td class="cellrowborder" rowspan="6" valign="top" width="14.2%" headers="mcps1.2.4.1.1 "><p id="p183311211154111"><a name="p183311211154111"></a><a name="p183311211154111"></a>KMS接口</p>
</td>
<td class="cellrowborder" valign="top" width="39.56%" headers="mcps1.2.4.1.2 "><p id="p133751244203316"><a name="p133751244203316"></a><a name="p133751244203316"></a>kms_generate_datakey_blocking</p>
</td>
<td class="cellrowborder" valign="top" width="46.239999999999995%" headers="mcps1.2.4.1.3 "><p id="p832491017381"><a name="p832491017381"></a><a name="p832491017381"></a>生成新的密钥对，获取公钥与私钥</p>
</td>
</tr>
<tr id="row032420106385"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p537684403320"><a name="p537684403320"></a><a name="p537684403320"></a>kms_generate_datakey_blocking_with_proxy</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p177245863316"><a name="p177245863316"></a><a name="p177245863316"></a>集成qtproxy代理的密钥对获取接口</p>
</td>
</tr>
<tr id="row1332512102387"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p10376204483318"><a name="p10376204483318"></a><a name="p10376204483318"></a>kms_gen_random_blocking</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1072105817332"><a name="p1072105817332"></a><a name="p1072105817332"></a>获取随机数</p>
</td>
</tr>
<tr id="row334602293318"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p53761544183314"><a name="p53761544183314"></a><a name="p53761544183314"></a>kms_gen_random_blocking_with_proxy</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p972175833318"><a name="p972175833318"></a><a name="p972175833318"></a>集成qtproxy代理的随机数获取接口</p>
</td>
</tr>
<tr id="row814192719339"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p11376944143311"><a name="p11376944143311"></a><a name="p11376944143311"></a>kms_decrypt_data_blocking</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p77235810337"><a name="p77235810337"></a><a name="p77235810337"></a>解密数据</p>
</td>
</tr>
<tr id="row20709182483318"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p83761344103319"><a name="p83761344103319"></a><a name="p83761344103319"></a>kms_decrypt_data_blocking_with_proxy</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p572125893319"><a name="p572125893319"></a><a name="p572125893319"></a>集成qtproxy代理的解密数据接口</p>
</td>
</tr>
</tbody>
</table>

源码可以在开源仓库[https://gitee.com/HuaweiCloudDeveloper/huawei-qingtian/tree/master/enclave](https://gitee.com/HuaweiCloudDeveloper/huawei-qingtian/tree/master/enclave)免费获取，您可以基于测试示例开发自己的QingTian Enclave应用程序。

## Vsock通信实例<a name="zh-cn_topic_0000001409393257_section688618101393"></a>

本节主要通过vsock示例来介绍如何在Linux环境下开发QingTian Enclave应用程序。本节中提供的vsock程序只支持在Linux环境下运行。

通过该vsock程序，可以帮助开发者了解到父虚拟机和QingTian Enclave间如何进行消息传递从而实现双方交互。该vsock程序带有Server和Client参数，通过指定该参数可以指定父虚拟机或者QingTian Enclave虚拟机扮演相应角色。在该vsock程序中，客户端程序会发送一段简单的文本信息通过vsock通道传递给服务端程序，同时服务端程序会监听相应的vsock通道，一旦收到来自客户端的消息后，会将其收到的消息打印在终端界面上。

在下面介绍中，我们将说明如何让QingTian Enclave扮演服务端等待并接收来自客户端父虚拟机的hello world信息：

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

1.  将docker镜像转化为QingTian Enclave镜像：

    ```
    qt enclave make-img --docker-uri vsock-sample-client --eif vsock_sample.eif
    ```

1.  使用vsock\_sample.eif以debug模式启动QingTian Enclave:

    ```
    qt enclave start --cpus 2 --mem 4096 --eif vsock_sample.eif --debug-mode --cid 4
    ```

    然后使用qt enclave console命令查看QingTian Enclave内只读终端输出：

    ```
    qt enclave console --enclave-id 0
    waiting for a connection
    ```

1.  然后另起一个父虚拟机终端，启动客户端程序：

    ```
    python3 SocketCommunication.py Client -c 4 -p 9999
    ```

1.  当服务端程序收到来着vsock的消息后，会打印如下消息到终端上：

    ```
    connection from  (3, 4180219645)
    data:  Hello world
    connection close
    waiting for a connection
    ```

## libqtsm与SDK使用示例<a name="section17711125894317"></a>

本节主要基于开源示例代码来介绍如何在QingTian Enclave应用程序中使用libqtsm与SDK接口。本节中提供的示例程序只支持在Linux环境下运行。

1.  安装libqtsm开发包：

    **yum install libqtsm-devel**

1.  获取开源示例代码，拷贝至enclave镜像创建环境中，地址如下：

    [https://gitee.com/HuaweiCloudDeveloper/huawei-qingtian/tree/master/enclave/qtsm](https://gitee.com/HuaweiCloudDeveloper/huawei-qingtian/tree/master/enclave/qtsm)

1.  创建一个Dockerfile文件，内容如下：

    ```
    # start the Docker image from ubuntu
    FROM ubuntu AS base-img
    WORKDIR /home/builder
    # COPY libqtsm example
    COPY ./qtsm qtsm_tests/
    # install relative dependencies
    RUN apt-get update && \
        apt-get install gcc -y && \
        apt-get install make -y && \
        apt-get install libssl-dev -y && \
        apt-get install libglib2.0-dev -y && \
        apt-get install curl -y && \
        apt-get install libcurl4-openssl-dev –y  && \
        apt-get install -y libcbor-dev && \
        apt-get install -y libjson-c-dev
    # build a test demo
    RUN cd qtsm_tests/tests/ && \
           make
    RUN cp /home/builder/qtsm_tests/tests/gtest_libqtsm /root/
    # Launch a client
    CMD "/root/gtest_libqtsm"
    ```

1.  构建docker镜像，将docker镜像装换为enclave镜像并启动enclave。
2.  获取SDK接口的开源示例代码，地址如下：

    <u>[https://gitee.com/HuaweiCloudDeveloper/huawei-qingtian/tree/master/enclave/qtsm-sdk-c/samples](https://gitee.com/HuaweiCloudDeveloper/huawei-qingtian/tree/master/enclave/qtsm-sdk-c/samples)</u>

