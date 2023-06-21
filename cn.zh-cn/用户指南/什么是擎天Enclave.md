# 什么是擎天Enclave<a name="ecs_03_1402"></a>

-   在现有的基于擎天架构的虚拟机产品中，我们增加了一个置于其内部的，安全的、完全隔离的虚拟机，这个虚拟机我们称之为擎天Enclave虚拟机，外部对这个擎天Enclave虚拟机具备所有权的虚拟机，我们称之为父虚拟机。擎天Enclave是完全独立的虚拟机，无持久化存储、交互式访问或外部网络连接。父虚拟机与擎天Enclave之间通过安全的本地通道进行通信。即使是父虚拟机上的root用户，也不能访问擎天Enclave或通过 SSH 连接到擎天Enclave。
-   擎天Hypervisor可以将擎天Enclave的CPU 和内存与父虚拟机的CPU和内存资源隔离开，提供给您一个完全隔离的可执行环境，显著减少了攻击面。因此，使用擎天Enclave，您能保护敏感的核心数据和应用程序，为您在擎天Enclave中运行的服务增加安全保障。
-   擎天Enclave还提供了证明（Attestation）的功能，您可以通过该功能验证擎天Enclave实例的可信度量值。[华为云密钥管理服务（Key management Service，简称KMS）](https://support.huaweicloud.com/productdesc-dew/dew_01_0001.html)为擎天证明功能提供了内在支持，您能限制应用程序必须在预期的擎天Enclave运行环境中才能调用KMS API处理敏感数据。

![](figures/最新（擎天enclave介绍图）.png)

## 约束条件<a name="zh-cn_topic_0000001359553230_section194467418515"></a>

擎天Enclave有以下约束：

<a name="zh-cn_topic_0000001359553230_table5447131115718"></a>
<table><thead align="left"><tr id="zh-cn_topic_0000001359553230_row5447141117713"><th class="cellrowborder" valign="top" width="21.17%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0000001359553230_p327715251175"><a name="zh-cn_topic_0000001359553230_p327715251175"></a><a name="zh-cn_topic_0000001359553230_p327715251175"></a>虚拟机名称</p>
</th>
<th class="cellrowborder" valign="top" width="78.83%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0000001359553230_p1427722518718"><a name="zh-cn_topic_0000001359553230_p1427722518718"></a><a name="zh-cn_topic_0000001359553230_p1427722518718"></a>限制要求</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0000001359553230_row184478119718"><td class="cellrowborder" valign="top" width="21.17%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0000001359553230_p102774250718"><a name="zh-cn_topic_0000001359553230_p102774250718"></a><a name="zh-cn_topic_0000001359553230_p102774250718"></a>父虚拟机（主虚拟机）</p>
</td>
<td class="cellrowborder" valign="top" width="78.83%" headers="mcps1.1.3.1.2 "><a name="ol172445553589"></a><a name="ol172445553589"></a><ol id="ol172445553589"><li>至少预留2个vCPU，至少预留512M内存空间。</li><li>必须为Linux操作系统。</li></ol>
</td>
</tr>
<tr id="zh-cn_topic_0000001359553230_row744761111710"><td class="cellrowborder" valign="top" width="21.17%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0000001359553230_p6278172510718"><a name="zh-cn_topic_0000001359553230_p6278172510718"></a><a name="zh-cn_topic_0000001359553230_p6278172510718"></a>擎天Enclave（从虚拟机）</p>
</td>
<td class="cellrowborder" valign="top" width="78.83%" headers="mcps1.1.3.1.2 "><a name="ol11676712596"></a><a name="ol11676712596"></a><ol id="ol11676712596"><li>裸金属实例不支持擎天Enclave。</li><li>必须为Linux操作系统。</li><li>启动擎天Enclave最低内存规格为128M，并且不能小于Enclave镜像文件（Enclave Image File，简称EIF）文件大小的4倍。</li><li>当在配置文件中，为擎天Enclave配置2M大页的内存管理方式时，擎天Enclave启动支持的最大内存为512M。</li><li>当在配置文件中，为擎天Enclave配置1G大页的内存管理方式时，擎天Enclave最大内存为256G。</li><li>擎天Enclave所使用的内存和CPU都必须隔离自同一个NUMA节点。</li><li>vcpu数量配置需要为偶数，最高不超过父虚拟机单NUMA node cpu数量减 2；总数量最高不超过62。</li><li>在擎天Enclave中运行的应用程序需要和OS（内核，ramdisk，init程序）一起被打包成擎天Enclave镜像。</li></ol>
</td>
</tr>
</tbody>
</table>

父虚拟机和擎天Enclave关系：

1.  每个父虚拟机可以创建最多两个擎天Enclave。
2.  不支持与父虚拟机共物理内核。
3.  只有在父虚拟机处于运行状态时，擎天Enclave才处于运行状态。如果父虚拟机被停止或终止，则擎天Enclave被终止。
4.  擎天Enclave分配的资源（内存和CPU等），都是从父虚拟机中分割出来的，内存区间要求是2M/1G对齐的连续物理区间。

另外还需要注意：

1.  支持擎天Enclave特性的父虚拟机规格： c7t

    c7t规格还处于公测阶段，请通过[提交工单](https://console.huaweicloud.com/ticket/#/ticketindex/createIndex)联系客服申请公测。

2.  支持擎天Enclave特性的局点： 华东-上海一
3.  如果您在擎天Enclave中的业务被意外终止，您需要手动重新运行该业务
4.  擎天Enclave的默认配置为使用1G大页，具有1G内存，2vcpu

## 计费标准<a name="zh-cn_topic_0000001359553230_section14278101414106"></a>

在公测期间，使用擎天Enclave并不会收取额外费用，您只需要支付ECS的购买费用。

## 相关服务<a name="zh-cn_topic_0000001359553230_section12415364108"></a>

擎天Enclave与以下华为云服务集成：

1.  密钥管理服务

    密钥管理服务（KMS）是华为云数据加密服务族中的一个核心服务。KMS提供可用性高的密钥生成、存储、管理和审计解决方案。KMS密钥由硬件安全模块HSM保护，并与许多华为云数据存储服务集成。您可以借此服务开发自己的安全的数据应用。

2.  华为统一身份认证服务

    统一身份认证（Identity and Access Management，简称IAM）是华为云提供权限管理的基础服务，可以帮助您安全地控制华为云服务和资源的访问权限。


