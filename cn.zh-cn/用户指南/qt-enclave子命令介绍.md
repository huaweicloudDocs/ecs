# qt enclave子命令介绍<a name="ecs_03_1419"></a>

qt为一级命令，其下目前包含enclave一个二级子命令:

```
[root@localhost ~]# qt 
  ____  _          _______ _ 
 / __ \(_)        |__   __(_) 
| |  | |_ _ __   __ _| |   _  __ _ _ __ 
| |  | | | '_ \ / _` | |  | |/ _` | '_ \ 
| |__| | | | | | (_| | |  | | (_| | | | | 
 \___\_\_|_| |_|\__, |_|  |_|\__,_|_| |_| 
                 __/ | 
                |___/ 
 
Welcome to the cool QingTian new CLI! 
 
    enclave : Enclave life-circle management.
```

qt enclave中提供enclave相关的镜像制作，拉起、销毁、查询擎天Enclave等子命令：

```
[root@localhost ~]# qt enclave
usage: qt enclave [-h] {make-img,start,stop,query,console} ...
qt enclave: error: the following arguments are required: _subcommand
enclave command line interface
[root@localhost ~]# qt enclave -h
​
Group
  qt enclave : Enclave life-circle management.
​
Commands:
  console  : Console an enclave via the enclave-id while debugging.
  make-img : Make an eif image from a docker image.
  query   : Query an enclave via the enclave-id or query all enclaves.
  start   : Start an enclave via an eif image.
  stop   : Stop an enclave via the enclave-id.
```

## qt enclave make-img<a name="zh-cn_topic_0000001409233153_section1754984025717"></a>

该命令用于将用户制作好的docker镜像转换为擎天Enclave虚拟机可用的镜像，命令格式如下：

```
[root@localhost ~]# qt enclave make-img -h

Command
    qt enclave make-img : Make an eif image from a docker image.

Arguments
    --docker-uri [Required]
    --eif        [Required]
    --private-key
    --signing-certificate

Global Arguments
    --debug                 : Increase logging verbosity to show all debug logs.
    --help -h               : Show this help message and exit.
    --only-show-errors      : Only show errors, suppressing warnings.
    --output -o             : Output format.  Allowed values: json, jsonc, none, table, tsv, yaml,
                              yamlc.  Default: json.
    --query                 : JMESPath query string. See http://jmespath.org/ for more information
                              and examples.
    --verbose               : Increase logging verbosity. Use --debug for full debug logs.

Examples
    Given docker-uri and eif to make an eif image
        qt enclave make-img --docker-uri [DOCKER-URI] --eif [EIF]

    Make an eif image with private-key and signing-certificate
        qt enclave make-img --docker-uri [DOCKER-URI] --eif [EIF] --private-key [PRIVATE-KEY]
        --signing-certificate [SIGNING-CERTIFICATE]
```

必选项：--docker-uri，指定Docker存储库中Docker映像的统一资源标识符（URI）。可以通过docker image ls命令查询当前本地镜像uri。

必选项：--eif，提供路径名称用于存放生成后的EIF镜像

可选项：--private-key，提供对擎天Enclave镜像进行签名的私钥绝对路径，如果指定了PRIVATE-KEY， 要求必须同时指定签名密钥SIGNING-CERTIFICATE；

可选项：--signing-certificate，提供对擎天Enclave镜像进行签名的秘钥绝对路径，如果指定了SIGNING-CERTIFICATE， 如要同时指定签名密钥PRIVATE-KEY；

命令行返回值：如果配置了以上两项证书可选项，必须保证证书有效。证书有效情况下命令输出将包括额外的PCR0，PCR8散列值用于。证书无效，镜像创建失败。

创建镜像命令示例：

```
[root@localhost docker]# qt enclave make-img --docker-uri ubuntu --eif /home/docker/ubuntu.eif --private-key  /home/docker/private-key.pem --signing-certificate /home/docker/server.pem
{
    "digest":       "SHA384",
    "PCR0": "b8c59692da8a5bcb739a83d15a0ceca670bd78da06cb2250ec70548f72254e674419e9888db9c0364a9b88dd58017a62"  
    "PCR8": "dbf4a7f9fab7f18619b5899c407081981ad6762fb9a809da78548821b5021965423181584acd7b201703376f1133a546"
}
```

## qt enclave start<a name="zh-cn_topic_0000001409233153_section7188009592"></a>

该命令用于创建擎天Enclave虚拟机，命令格式如下：

```
[root@localhost ~]# qt enclave start -h
​
Command
  qt enclave start : Start an enclave via an eif image.
​
Arguments
  --cid  [Required]
  --eif  [Required]
  --cpus       : Default: 2.
  --debug-mode
  --mem        : Default: 1024.
​
Global Arguments
  --debug       : Increase logging verbosity to show all debug logs.
  --help -h      : Show this help message and exit.
  --only-show-errors : Only show errors, suppressing warnings.
  --output -o     : Output format.  Allowed values: json, jsonc, none, table, tsv, yaml, yamlc.
             Default: json.
  --query       : JMESPath query string. See http://jmespath.org/ for more information and
             examples.
  --verbose      : Increase logging verbosity. Use --debug for full debug logs.
​
Examples
  Given an eif image, an unused cid, the number of cpus and memory needed
    qt enclave start  [--cpus CPUS] [--mem MEM] --eif EIF [--cid CID]
```

可选项：--cpus，指定要分配给enclave虚拟机的vCPU数量，不能大于隔离的cpu数目， 未配置使用默认值2；

可选项：--mem，指定分配给擎天Enclave虚拟机的内存大小（MB），不能大于隔离内存大小，需大于擎天Enclave镜像大小，未配置使用默认值1024MB；

必选项：--eif，指定EIF镜像路径；

可选项：--cid，设置擎天Enclave虚拟机cid，用于指定父虚拟机与擎天Enclave虚拟机间vsock通信的socket IP。可用的cid范围为：4-4294967294，未配置使用默认值4；

可选项：--debug-mode，指定是否在调试模式下启动擎天Enclave实例，该模式下使用全部为0的PCR散列值，可以收集打印擎天Enclave虚拟机内部日志；

命令行返回值：创建成功后输出创建的擎天Enclave虚拟机详细信息。

Enclave虚拟机启动命令示例：

```
qt enclave start --cpus 2 --mem 1024 --eif /home/docker/ubuntu.eif --cid 4
```

## qt enclave query<a name="zh-cn_topic_0000001409233153_section1519411261101"></a>

该命令用于在父虚拟机内查询当前已创建的擎天Enclave虚拟机信息，命令格式如下：

```
[root@localhost ~]# qt enclave query -h
​
Command
  qt enclave query : Query an enclave via the enclave-id or query all enclaves.
​
Arguments
  --enclave-id
​
Global Arguments
  --debug       : Increase logging verbosity to show all debug logs.
  --help -h      : Show this help message and exit.
  --only-show-errors : Only show errors, suppressing warnings.
  --output -o     : Output format.  Allowed values: json, jsonc, none, table, tsv, yaml, yamlc.
             Default: json.
  --query       : JMESPath query string. See http://jmespath.org/ for more information and
             examples.
  --verbose      : Increase logging verbosity. Use --debug for full debug logs.
​
Examples
  Given an enclave-id to query an enclave
      qt enclave query --enclave-id [ENCLAVE-ID]
​
  Query all enclaves without enclave-id
    qt enclave query
```

可选项：--enclave-id，query时带此参数则查询指定擎天Enclave虚拟机信息，否则查询全部当前已存在擎天Enclave虚拟机信息；

命令行返回值，查询到的擎天Enclave虚拟机信息：

-   EnclaveID：擎天Enclave虚拟机的id号；

-   ProcessID：父实例中持有擎天Enclave资源的进程的进程号PID；

-   EnclaveCID：擎天Enclave虚拟机与父虚拟机通信使用的vsock socket id；

-   NumberOfCPUs：从父虚拟机分配给擎天Enclave虚拟机的vCPU个数；

-   MemoryMiB：从父虚拟机分配给擎天Enclave虚拟机的内存大小\(MB\)；

擎天Enclave虚拟机查询命令示例：

```
[root@localhost ~]#qt enclave query
[{
        "EnclaveID":    0,
        "ProcessID":    29990,
        "EnclaveCID":   4,
        "NumberOfCPUs": 2,
        "MemoryMiB":    1024,
        "LaunchMode":   "debug"
    }]
```

若当前无擎天Enclave虚拟机存在，则该命令查询返回空；

带--enclave-id参数查询场景，若指定enclave-id的擎天Enclave虚拟机不存在， 查询命令返回空。

## qt enclave stop<a name="zh-cn_topic_0000001409233153_section17553194211114"></a>

该命令用于在父虚拟机内销毁已创建的擎天Enclave虚拟机，命令格式如下：

```
[root@localhost ~]# qt enclave stop -h
​
Command
  qt enclave stop : Stop an enclave via the enclave-id.
​
Arguments
  --enclave-id [Required]
​
Global Arguments
  --debug         : Increase logging verbosity to show all debug logs.
  --help -h        : Show this help message and exit.
  --only-show-errors    : Only show errors, suppressing warnings.
  --output -o       : Output format.  Allowed values: json, jsonc, none, table, tsv, yaml,
               yamlc.  Default: json.
  --query         : JMESPath query string. See http://jmespath.org/ for more information
               and examples.
  --verbose        : Increase logging verbosity. Use --debug for full debug logs.
​
Examples
  Given an enclave-id to stop an enclave
   qt enclave stop --enclave-id [ENCLAVE-ID]
```

必选项：--enclave-id，指定需要销毁的擎天Enclave虚拟机的enclave-id

命令行返回值：成功返回销毁成功，销毁失败无返回。

擎天Enclave虚拟机销毁命令示例：

```
[root@localhost ~]# qt enclave stop --enclave-id 1
stop 1 success
```

## qt enclave console<a name="zh-cn_topic_0000001409233153_section31371042185915"></a>

在启动擎天Enclave时，指定为debug-mode时，用于在父虚拟机中查看擎天Enclave中的只读控制台输出，命令格式如下：

```
[root@localhost ~]# qt enclave console -h
 
Command
    qt enclave console : Console an enclave via the enclave-id while debugging.
 
Arguments
    --enclave-id [Required]
 
Global Arguments
    --debug                 : Increase logging verbosity to show all debug logs.
    --help -h               : Show this help message and exit.
    --only-show-errors      : Only show errors, suppressing warnings.
    --output -o             : Output format.  Allowed values: json, jsonc, none, table, tsv, yaml,
                              yamlc.  Default: json.
    --query                 : JMESPath query string. See http://jmespath.org/ for more information
                              and examples.
    --verbose               : Increase logging verbosity. Use --debug for full debug logs.
 
Examples
    Given an enclave-id to console an enclave
        qt enclave console --enclave-id [ENCLAVE-ID]
```

必选项：--enclave-id，指定需要获取只读控制台输出的擎天Enclave虚拟机的enclave-id。

命令行执行成功后，会打印擎天Enclave虚拟机的只读控制台输出，如下所示：

```
hello enclave! 
hello enclave! 
hello enclave! 
hello enclave!
```

您可以使用ctrl+c的方式退出该命令。需要注意的是，在同一时间我们只允许一个qt enclave console命令作用于一个指定的擎天Enclave实例。

