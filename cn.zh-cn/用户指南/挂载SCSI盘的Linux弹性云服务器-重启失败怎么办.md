# 挂载SCSI盘的Linux弹性云服务器，重启失败怎么办？<a name="ZH-CN_TOPIC_0087382187"></a>

## 问题描述<a name="section3414486317516"></a>

对于挂载了SCSI类型云硬盘的Linux弹性云服务器，如果在/etc/fstab中配置了SCSI磁盘开机自动挂载，且使用的是磁盘的盘符（如/dev/sdb）进行配置，弹性云服务器可能重启失败。

## 可能原因<a name="section20153596175411"></a>

SCSI磁盘的分配与磁盘的槽位号、弹性云服务器中可用的盘符有关。弹性云服务器内部，每加载一个磁盘都按顺序分配空闲的盘符。弹性云服务器启动时，按照槽位号顺序加载磁盘，所以槽位号和盘符的顺序是一一对应的。

在线卸载弹性云服务器的SCSI磁盘后，磁盘的槽位号顺序有可能发生改变，导致重启后磁盘的盘符也发生改变，槽位号和盘符无法对应，重启失败。

## 处理方法<a name="section17730319204351"></a>

1.  以root用户登录Linux弹性云服务器。
2.  <a name="li2064141120446"></a>执行以下命令，根据SCSI盘的盘符，查询对应的SCSI ID。

    **ll /dev/disk/by-id/|grep** _磁盘盘符_

    假设SCSI磁盘的盘符为/dev/sdb，则命令行如下：

    **ll /dev/disk/by-id/|grep sdb**

    ```
    CNA64_22:/opt/galax/eucalyptus/ecs_scripts # ll /dev/disk/by-id/|grep sdb
    lrwxrwxrwx 1 root root  9 Dec  6 11:26 scsi-3688860300001436b005014f890338280 -> ../../sdb
    lrwxrwxrwx 1 root root  9 Dec  6 11:26 wwn-0x688860300001436b005014f890338280 -> ../../sdb
    ```

3.  修改/etc/fstab文件，将SCSI盘的盘符（如/dev/sdb）修改为对应的SCSI ID。

    **/dev/disk/by-id/**_SCSI ID_

    假设[2](#li2064141120446)中查询到的SCSI ID为scsi-3688860300001436b005014f890338280，则用以下内容替换/dev/sdb：

    **/dev/disk/by-id/scsi-3688860300001436b005014f890338280**


