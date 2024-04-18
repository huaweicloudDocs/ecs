# QingTian Enclave应用开发<a name="ecs_03_1414"></a>

一个功能完备的QingTian Enclave应用程序至少包括如下两个部分：

1.  一个运行在父虚拟机内安全不敏感的应用程序。
2.  一个运行在Enclave环境中安全敏感的应用程序。

由于QingTian Enclave环境的独立性，QingTian Enclave环境中的应用程序和运行在父虚拟机中的应用程序间只能通过唯一的vsock通道进行通信。

-   **[Linux系统上QingTian Enclave应用的开发](Linux系统上QingTian-Enclave应用的开发.md)**  

