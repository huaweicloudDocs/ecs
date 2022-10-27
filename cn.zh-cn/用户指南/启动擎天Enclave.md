# 启动擎天Enclave<a name="ecs_03_1408"></a>

## 资源隔离<a name="zh-cn_topic_0000001409273457_section2901123412225"></a>

启动擎天Enclave虚拟机之前，您首先要在父虚拟机内隔离资源供擎天Enclave虚拟机使用。隔离的资源包括cpu个数和内存大小，可以通过在虚拟机内访问修改**\*/etc/qiangtian/enclave/qt-enclave-env.conf\***配置文件指定需要隔离的资源：

```
#1G大页  
hugepage_size:1024  
#内存1G.  
memory_mib:1024  
# cpu个数  
cpu_count:2  
# cpu列表  
# cpu_list:2,3
```

我们建议您最好不要反复启动资源隔离服务，否则将会出现大页内存不足，导致擎天Enclave无法正常启动或者隔离服务无法正常启动。本教程中保持默认值不变，使用1G大页，隔离2个vCPU和1G内存。确认配置文件参数之后执行以下命令：

```
systemctl restart qt-enclave-env.service
```

其中**\*/etc/qiangtian/enclave/qt-enclave-env.conf\***配置文件中的配置项之间有约束条件，详情可见[qt-enclave-env服务介绍](qt-enclave-env工具介绍.md)。

## 启动擎天Enclave<a name="zh-cn_topic_0000001409273457_section18881215132415"></a>

在父虚拟机内，使用**\*qt enclave start\***命令创建擎天Enclave虚拟机，该命令中需要指定擎天Enclave虚拟机镜像文件。在擎天Enclave虚拟机启动后，擎天Enclave应用程序及其依赖项会被从该镜像文件中引导到擎天Enclave虚拟机中。这里以创建一个拥有2个vCPU，1G内存，CID为4的擎天Enclave虚拟机为例：

```
[root@localhost ~]# qt enclave start --cpus 2 --mem 1024 --eif /home/docker/ubuntu.eif --cid 4
Started enclave with EnclaveID : 0, EnclaveCID : 4, NumberOfCPUs : 2, MemoryMiB : 1024
{
    "EnclaveID":    0,
    "EnclaveCID":   4,
    "NumberOfCPUs": 2,
    "MemoryMiB":    1024,
    "LaunchMode":   "debug"
}
```

在该实例中，原镜像ubuntu中的CMD语句为/bin/bash，因此擎天Enclave启动之后将会执行该语句，执行完成后将退出并关闭。

