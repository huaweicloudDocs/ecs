# 安装qt CLI<a name="ecs_03_1417"></a>

如果您使用其他Linux镜像，请通过华为云擎天开源仓库进行编译安装。如果您使用Huawei Cloud EulerOS系统镜像时，通过以下命令直接安装：

```
yum install qingtian-tool
```

该rpm包中包含两个工具：

qt-enclave-env：提供资源隔离功能，擎天Enclave虚拟机创建之前需要隔离指定内存供enclave虚拟机使用，以保证擎天Enclave虚拟机空间的绝对安全。

qt CLI：是一个擎天命令行工具。您可以使用qt CLI制作擎天Enclave虚拟机启动所需要的EIF镜像，和管理擎天Enclave虚拟机生命周期。

注意：在使用qt CLI之前，您需要预先安装python3以及几个必要的python module : docker 和knack。可以参考以下命令进行安装：

```
pip3 install docker knack
```

