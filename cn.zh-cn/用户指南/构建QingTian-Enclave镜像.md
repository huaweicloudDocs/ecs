# 构建QingTian Enclave镜像<a name="ecs_03_1407"></a>

在开发人员开发完成一个QingTian Enclave应用程序后，还需要在一个可信赖的环境中构建QingTian Enclave镜像文件（.eif）。该镜像文件提供了启动QingTian Enclave实例所需要的所有信息，包括应用程序代码、运行时依赖、操作系统和文件系统等。在本节我们将说明如何创建QingTian Enclave镜像文件。

1.  制作docker源镜像

    用户将开发好的enclave应用程序及其相关的执行环境打包成docker镜像。详情可见[Linux系统上QingTian Enclave应用的开发](Linux系统上QingTian-Enclave应用的开发.md)。

2.  获取镜像库中的镜像

    本章将使用docker仓中提供的ubuntu镜像为例。从docker中获取镜像源（虚拟机内需要配置网络才可查询）。查询镜像源命令：

    ```
    docker search ubuntu
    ```

    将ubuntu镜像pull到本地：

    ```
    docker pull ubuntu
    ```

    镜像pull到本地后可以通过以下命令查询到:

    ```
    docker image ls
    ```

    如果您使用本地docker镜像，可以直接进行步骤3镜像转换。

3.  镜像转换

    接下来，您需要将docker镜像转换为QingTian Enclave镜像，转换前可以通过（openssl或其他工具）创建私钥（private-key.pem）和证书（server.pem）。生成私钥和证书为可选项。**_\*qt make-img\*_**命令中的必要参数为docker源镜像和创建后生成的QingTian Enclave目标镜像。

    ```
    # qt enclave make-img --docker-uri ubuntu --eif  /home/docker/ubuntu.eif --
    private-key  /home/docker/private-key.pem--signing-certificate  
    /home/docker/server.pem
    {     
         "digest":       "SHA384", 
         "PCR0": "b8c59692da8a5bcb739a83d15a0ceca670bd78da06cb2250ec70548f72254e674419e9888db9c0364a9b88dd58017a62"
         "PCR8": "dbf4a7f9fab7f18619b5899c407081981ad6762fb9a809da78548821b5021965423181584acd7b201703376f1133a546"
    }
    ```

    至此，QingTian Enclave可用的EIF镜像已制作完成。您会获得一组散列PCR0和PCR8，这些散列值用作预期的Enclave度量值，它们可用于IAM授权策略中的条件键，以实现对KMS API的条件访问控制。详情可见[PCR简介](PCR简介.md)。

