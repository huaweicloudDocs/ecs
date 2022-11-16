# KVM实例变更为擎天实例（Linux）<a name="ecs_03_0179"></a>

## 操作场景<a name="section925916342463"></a>

本节介绍将Linux操作系统的KVM实例变更为擎天架构实例的操作步骤。

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   KVM实例：参考[规格清单](https://support.huaweicloud.com/productdesc-ecs/zh-cn_topic_0159822360.html)，查询对应规格的虚拟化类型。
>-   擎天架构实例：选择“通用计算增强型C7”、“内存优化型M7”。

## 约束与限制<a name="section156669511419"></a>

-   变更规格时不支持修改网络类型。
-   Linux操作系统云服务器的系统盘和数据盘如果存在由多个物理卷组成的LVM逻辑卷或组建了RAID磁盘阵列，均不支持变更规格，否则可能会导致数据丢失。

-   擎天实例仅支持使用SCSI磁盘模式挂载磁盘，不支持使用VBD磁盘模式挂载磁盘。即磁盘标识为wwn。
-   支持将“KVM实例”变更为“擎天实例”，不支持将“擎天实例”变更为“KVM实例”。
-   不支持“XEN” 实例变更为“擎天实例”。

## 操作流程<a name="section565123943212"></a>

KVM实例变更为擎天实例的操作流程如[图1](#fig10268287430)所示。

**图 1**  Linux云服务器变更流程<a name="fig10268287430"></a>  
![](figures/Linux云服务器变更流程.png "Linux云服务器变更流程")

**表 1**  KVM实例变更为擎天实例

<a name="table53651941115913"></a>
<table><thead align="left"><tr id="row183651341145918"><th class="cellrowborder" valign="top" width="33.29%" id="mcps1.2.3.1.1"><p id="p8365144115919"><a name="p8365144115919"></a><a name="p8365144115919"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="66.71000000000001%" id="mcps1.2.3.1.2"><p id="p4365124113595"><a name="p4365124113595"></a><a name="p4365124113595"></a>任务</p>
</th>
</tr>
</thead>
<tbody><tr id="row19366941115915"><td class="cellrowborder" valign="top" width="33.29%" headers="mcps1.2.3.1.1 "><p id="p1242122753517"><a name="p1242122753517"></a><a name="p1242122753517"></a>步骤1</p>
</td>
<td class="cellrowborder" valign="top" width="66.71000000000001%" headers="mcps1.2.3.1.2 "><p id="p1542162717357"><a name="p1542162717357"></a><a name="p1542162717357"></a><a href="#section3197492350">步骤1：制作系统盘快照</a></p>
</td>
</tr>
<tr id="row18696165154411"><td class="cellrowborder" valign="top" width="33.29%" headers="mcps1.2.3.1.1 "><p id="p103202566448"><a name="p103202566448"></a><a name="p103202566448"></a>步骤2</p>
</td>
<td class="cellrowborder" valign="top" width="66.71000000000001%" headers="mcps1.2.3.1.2 "><p id="p569695119445"><a name="p569695119445"></a><a name="p569695119445"></a><a href="#section69761823194217">步骤2：执行规格变更优化脚本</a></p>
</td>
</tr>
<tr id="row1136644155912"><td class="cellrowborder" valign="top" width="33.29%" headers="mcps1.2.3.1.1 "><p id="ecs_03_0161_p236624118593"><a name="ecs_03_0161_p236624118593"></a><a name="ecs_03_0161_p236624118593"></a>步骤3</p>
</td>
<td class="cellrowborder" valign="top" width="66.71000000000001%" headers="mcps1.2.3.1.2 "><p id="ecs_03_0161_p12366104118596"><a name="ecs_03_0161_p12366104118596"></a><a name="ecs_03_0161_p12366104118596"></a><a href="#section1815152131917">步骤3：变更规格</a></p>
</td>
</tr>
<tr id="row03661441165910"><td class="cellrowborder" valign="top" width="33.29%" headers="mcps1.2.3.1.1 "><p id="ecs_03_0161_p93661441145912"><a name="ecs_03_0161_p93661441145912"></a><a name="ecs_03_0161_p93661441145912"></a>步骤4</p>
</td>
<td class="cellrowborder" valign="top" width="66.71000000000001%" headers="mcps1.2.3.1.2 "><p id="ecs_03_0161_p123666411590"><a name="ecs_03_0161_p123666411590"></a><a name="ecs_03_0161_p123666411590"></a><a href="#section2625525131519">（可选）步骤4：检查磁盘挂载状态</a></p>
</td>
</tr>
</tbody>
</table>

## 步骤1：制作系统盘快照<a name="section3197492350"></a>

如果云服务器未安装驱动就执行了变更规格的操作，云服务器无法正常使用，需要重装操作系统才能恢复，可能造成您的系统盘数据丢失。因此，建议您先制作系统盘快照，防止数据丢失。

1.  制作系统盘快照前请对云服务器完成自检**。**

    对云服务器执行关机、开机操作，确保云服务器重启后业务可以正常运行。再启动制作系统盘快照。

2.  制作系统盘快照的操作，请参见《云硬盘用户指南》的“用户指南 \>  [创建快照](https://support.huaweicloud.com/usermanual-evs/zh-cn_topic_0066615262.html)”章节。

>![](public_sys-resources/icon-note.gif) **说明：** 
>变更规格完成后，如已确认业务恢复正常，请在快照页面手动删除快照。

## 步骤2：执行规格变更优化脚本<a name="section69761823194217"></a>

1.  远程登录弹性云服务器。
2.  执行以下命令，将规格变更优化下载到root目录下。

    **curl  _URL_  \> \~/offload\_check\_blockdevice.sh**

    其中，URL为规格变更优化脚本的下载地址。

    下载地址：

    -   华东-上海一：[https://sdi-resize-check-cn-east-3.obs.cn-east-3.myhuaweicloud.com:443/offload\_check\_blockdevice.sh](https://sdi-resize-check-cn-east-3.obs.cn-east-3.myhuaweicloud.com:443/offload_check_blockdevice.sh)
    -   华北-北京四：[https://sdi-resize-check-cn-north-4.obs.cn-north-4.myhuaweicloud.com:443/offload\_check\_blockdevice.sh](https://sdi-resize-check-cn-north-4.obs.cn-north-4.myhuaweicloud.com:443/offload_check_blockdevice.sh)
    -   华南-广州：[https://sdi-resize-check-cn-south-1.obs.cn-south-1.myhuaweicloud.com:443/offload\_check\_blockdevice.sh](https://sdi-resize-check-cn-south-1.obs.cn-south-1.myhuaweicloud.com:443/offload_check_blockdevice.sh)
    -   乌兰察布一：[https://sdi-resize-check-cn-north-9.obs.cn-north-9.myhuaweicloud.com:443/offload\_check\_blockdevice.sh](https://sdi-resize-check-cn-north-9.obs.cn-north-9.myhuaweicloud.com:443/offload_check_blockdevice.sh)
    -   西南-贵阳一：[https://sdi-resize-check-cn-southwest-2.obs.cn-southwest-2.myhuaweicloud.com:443/offload\_check\_blockdevice.sh](https://sdi-resize-check-cn-southwest-2.obs.cn-southwest-2.myhuaweicloud.com:443/offload_check_blockdevice.sh)

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >若回显异常，请检查云服务器是否绑定弹性公网IP。除上述区域外，绑定弹性公网IP后才能获取脚本。

3.  执行以下命令，运行规格变更优化脚本，该脚本会自动检查云服务器是否可以变更为擎天实例。

    **bash offload\_check\_blockdevice.sh**

    **图 2**  运行脚本<a name="fig12977105264911"></a>  
    ![](figures/运行脚本-14.png "运行脚本-14")

    请耐心等待脚本运行结束。如果回显提示“fstab file looks fine”，表示规格变更优化脚本执行成功，云服务器可以变更擎天实例。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >请务必确保云服务器配置成功，否则，可能会导致变更规格后的弹性云服务器不可用。


## 步骤3：变更规格<a name="section1815152131917"></a>

1.  登录控制台。
2.  单击“![](figures/service-list.jpg)”，选择“计算 \> 弹性云服务器”。
3.  在弹性云服务器列表，查询待变更弹性云服务器状态。

    如果不是关机状态，单击“操作”列下的“更多 \> 关机”。

4.  单击“操作”列下的“更多 \> 变更规格”。

    系统进入“云服务器变更规格”页面。

5.  根据界面提示，选择变更后的云服务器类型、vCPU和内存。
6.  （可选）选择“专属主机”。

    对于在专属主机上创建的弹性云服务器，系统支持更换云服务器所在的专属主机。

    此时，您可以单击下拉列表，选择更换专属主机。如果下拉列表中无可用的专属主机，说明专属主机所剩资源不足，不能用于创建变更规格后的弹性云服务器。

7.  勾选复选框“我确认已完成对弹性云服务器的配置”，确认已完成“配置弹性云服务器”操作。
8.  单击“确定”。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >-   单击“确定”后云平台自动为您制作系统盘快照。变更规格完成后，如已确认业务恢复正常，请在快照页面手动删除快照。
    >-   如果变更规格失败后，弹性云服务器无法使用，可能会需要重装操作系统来恢复云服务器，请注意重装操作系统会清除系统盘数据，但不影响数据盘的数据。


## （可选）步骤4：检查磁盘挂载状态<a name="section2625525131519"></a>

KVM实例变更为擎天实例时，可能会发生磁盘挂载失败的情况，因此，变更规格后，需检查磁盘挂载状态是否正常。如果正常，则变更成功。

-   Linux弹性云服务器

    详细操作请参考[Linux云服务器变更规格后数据盘脱机怎么办？](https://support.huaweicloud.com/ecs_faq/ecs_faq_0619.html)


## 后续处理<a name="section7460163511720"></a>

如果控制台上云服务器列表页，显示弹性云服务器已变更规格成功，但是远程登录云服务器后，操作系统无法启动，此时，请联系客服进行恢复，或重装操作系统进行恢复。重装系统的操作指导，请参见[重装操作系统](重装操作系统.md)。

>![](public_sys-resources/icon-note.gif) **说明：** 
>重装操作系统会清除系统盘数据，但不影响数据盘的数据。

变更规格完成后，如已确认业务恢复正常，请在快照页面手动删除快照。

