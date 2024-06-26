# QingTian Enclave概念<a name="ecs_03_1403"></a>

-   QingTian Enclave

    QingTian Enclave是完全隔离的虚拟机，它的内存和CPU来自于其父虚拟机被预先隔离出来的资源。QingTian Enclave既没有外部网络，也没有持久化存储。父虚拟机内的进程、应用程序、内核或者用户都无法访问QingTian Enclave中的资源。

-   父虚拟机

    父虚拟机是一个能够将其CPU及内存资源隔离分配给QingTian Enclave的ECS实例。这些资源能够在QingTian Enclave的生存周期内被其使用。启动QingTian Enclave成功后，该QingTian Enclave只能与其父虚拟机进行安全通信。

-   QingTian Enclave镜像文件

    QingTian Enclave镜像文件（.eif）提供了启动QingTian Enclave并在其中运行QingTian Enclave应用程序所需的系统信息，包括Linux操作系统、其他第三方库和QingTian Enclave应用程序。镜像创建详情见[Linux系统上QingTian Enclave应用的开发](Linux系统上QingTian-Enclave应用的开发.md)。

-   QingTian命令行工具

    作为华为云QingTian命令行工具（qt CLI），在QingTian Enclave使用场景中，qt CLI可以用于创建、关闭和查询QingTian Enclave信息。qt CLI必须在父虚拟机上安装和使用。详情见[QingTian CLI（qt CLI）](QingTian-CLI（qt-CLI）.md)。

-   Enclave SDK

    Enclave SDK由一系列开源库组成，以便用户开发自己的QingTian Enclave应用程序。它集成了一些与华为云KMS交互的接口，例如加解密和产生随机数等，并为远程证明提供了内在支持。

-   QingTian密码学证明

    QingTian密码学证明是QingTian Enclave在与KMS服务交互时证明自己合法性的过程。它依赖QingTianHypervisor产生的具有数字签名的证明文档。一个QingTian Enclave证明文档内包含的具体信息可以作为第三方服务认证及鉴权的条件。您可以在IAM服务中使用kms:RecipientAttestation相关条件键值（condition key）来控制对KMS服务特定接口操作的访问权限，例如生成随机数或者加解密操作。

-   证明文档

    证明文档（Attestation Document）由QingTianHypervisor产生并签名，其文件内容为QingTian Enclave的信息，包括PCR、密码摘要以及用户声明。外部服务可以通过证明文件来验证QingTian Enclave的身份是否可信。用户可以利用证明文档构建自己的可信系统，也可以与KMS交互时使用。详情可见[证明文档](证明文档.md)。

-   qt-proxy

    qt-proxy是一个运行在父虚拟机上的网络代理服务。用户可以使用这个服务，使父虚拟机转发来自于QingTian Enclave的网络包，实现QingTian Enclave与外界进行通信。这是QingTian Enclave用来与外部服务交互的唯一通信渠道。

-   PCR

    平台配置寄存器（Platform configuration registers，PCRs）是QingTian Enclave独有的可信度量值。一部分在QingTian Enclave创建时自动产生，用于验证QingTian Enclave自创建以来的完整性，另一部分可以由用户自己定义以确保QingTian Enclave能够运行在他所希望执行的平台上。另外，Attestation Document包含了相关的PCR，用户可以使用PCR作为IAM访问控制策略的条件键（condition key），以实现更为更严格的访问控制。详情可见[PCR简介](PCR简介.md)。

-   本地连接通道

    本地连接通道（Local Vsock Connection）是QingTian Enclave实例与父虚拟机之间唯一的，安全的本地通信通道。

-   QingTian安全模块

    QingTian安全模块（QingTian Security Module，QTSM）整体由qtsm-lib函数库和qtsm-server服务组成。您可以在您的QingTian Enclave 应用程序中调用qtsm-lib用户态接口，qtsm-server会处理具体的QTSM请求并将返回相应结果。qtsm-lib提供的用户态接口包括获取指定index对应的PCR值（qtsm\_describe\_pcr），扩展指定index的PCR值（qtsm\_extend\_pcr），锁定指定index的PCR值（qtsm\_lock\_pcr），批量锁定指定index的PCR值（qtsm\_lock\_pcrs），获取QTSM信息（qtsm\_get\_describe）和获取已签名的证明文档（qtsm\_get\_attestation）。

