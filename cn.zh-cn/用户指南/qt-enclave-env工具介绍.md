# qt-enclave-env工具介绍<a name="ecs_03_1418"></a>

qt-enclave-env是一个service，service启动后从qt-enclave-env.conf配置文件中读取需要隔离的资源信息，并执行资源隔离操作。隔离操作需要在创建擎天Enclave虚拟机之前执行。接下来我们将介绍该服务的配置文件/etc/qingtian/enclave/ qt-enclave-env.conf：

```
#enclave虚拟机隔离大页内存类型，可配置2或1024，分别表示2M大页或1G大页 
hugepage_size:1024 
# 配置需要隔离的内存大小，数值需要为hugepage_size的整数倍. 
memory_mib:1024 
# 配置需要隔离的cpu个数， 该配置项与cpu_list互斥，二者只能配置一个，否则service启动失败 
cpu_count:2 
# 配置需要隔离的cpu列表，可填入0以外的其他cpu id，该配置项与cpu_count互斥，二者只能配置一个，否则service启动失败 
# cpu_list:2,3
```

需要注意的是：qt-enclave-env服务预留大页内存是否成功受父虚拟机本身内存碎片化影响，系统长时间运行或者反复重启qt-enclave-env可能导致无法预留出足够的大页内存。推荐的使用方式是在系统刚启动时，启动一次qt-enclave-env预留足够的内存即可。

