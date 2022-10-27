# 管理虚拟IP地址<a name="ecs_03_0506"></a>

## 操作场景<a name="section152499465387"></a>

虚拟IP地址用于为网卡提供第二个IP地址，同时支持与多个弹性云服务器的网卡绑定，从而实现多个弹性云服务器之间的高可用性。

## 操作步骤<a name="section9994956183811"></a>

1.  登录管理控制台。
2.  单击“![](figures/service-list.jpg)”，选择“计算 \> 弹性云服务器”。
3.  在弹性云服务器列表中，单击待绑定虚拟IP地址的弹性云服务器名称。

    系统跳转至该弹性云服务器详情页面。

4.  选择“弹性网卡”页签，单击“管理虚拟IP地址”。
5.  选择“IP地址管理”页签，在需要绑定弹性公网IP或者弹性云服务器的虚拟IP地址所在行的操作列下，单击“绑定弹性公网IP”或者“绑定弹性云服务器”。

    多个主备部署的弹性云服务器可以在绑定虚拟IP地址时选择同一个虚拟IP地址，增强容灾性能。

6.  单击“确定”。
7.  为已绑定虚拟IP的弹性云服务器手工配置虚拟IP地址。

    弹性云服务器的网卡绑定虚拟IP地址后，需要在弹性云服务器上手工配置虚拟IP地址。

    **Linux系统**（本文以“CentOS 7.2 64bit”为例，其他规格请参考对应官网帮助文档）

    1.  <a name="zh-cn_topic_0118499077_li528316578916"></a>执行以下命令，查看并记录需要绑定虚拟IP的网卡及对应连接。

        **nmcli connection**

        回显类似如下信息：

        ![](figures/zh-cn_image_0000001281210233.png)

        本示例的回显信息说明如下：

        -   **DEVICE**列的**eth0**为需要绑定虚拟IP的网卡。
        -   **NAME**列的**Wired connection 1**为网卡对应的连接。

    2.  <a name="zh-cn_topic_0118499077_li20283257695"></a>执行以下命令，在目标连接中添加虚拟IP。

        **nmcli connection modify "**_CONNECTION_**" ipv4.addresses** _VIP_

        参数说明如下：

        -   CONNECTION：为[7.a](#zh-cn_topic_0118499077_li528316578916)中查到的网卡对应的连接。
        -   VIP：待添加的虚拟IP地址。
            -   如果一次添加多个虚拟IP地址，多个虚拟IP地址之间用“,”隔开。
            -   如果已有虚拟IP地址，此时还需要新增虚拟IP地址，那么命令中除了包含新的虚拟IP地址，也需要包含原有虚拟IP地址。

        命令示例：

        -   添加单个虚拟IP：**nmcli connection modify "Wired connection 1" ipv4.addresses 172.16.0.125**
        -   添加多个虚拟IP：**nmcli connection modify "Wired connection 1" ipv4.addresses 172.16.0.125,172.16.0.126**

    3.  执行以下命令，使[7.b](#zh-cn_topic_0118499077_li20283257695)的配置生效。

        **nmcli connection up "**_CONNECTION_**"**

        命令示例：

        **nmcli connection up "Wired connection 1"**

        回显类似如下信息：

        ![](figures/zh-cn_image_0000001237328110.png)

    4.  执行以下命令，检查虚拟IP配置是否成功。

        **ip a**

        回显类似如下信息，可以看到eth0网卡下存在虚拟IP地址，为**172.16.0.125**。

        ![](figures/zh-cn_image_0000001237013856.png)

    **Windows系统**（本文以“Windows Server”为例）

    1.  在“控制面板 \> 网络和共享中心”路径下，单击对应的本地连接。
    2.  在打开的本地连接页面中，单击“属性”。
    3.  在“网络”页签中选择“Internet 协议版本 4 （TCP/IPv4）”。
    4.  单击“属性”。
    5.  选择“使用下面的IP地址”，IP地址配置为弹性云服务器的私有IP地址，例如：10.0.0.101。

        **图 1**  配置私有IP地址<a name="zh-cn_topic_0118499077_fig1228662717417"></a>  
        ![](figures/配置私有IP地址.png "配置私有IP地址")

    6.  单击“高级”。
    7.  在“IP设置”页签内“IP地址”区域，单击“添加”。

        添加虚拟IP地址，例如：10.0.0.154。

        **图 2**  配置虚拟IP地址<a name="zh-cn_topic_0118499077_fig528642717417"></a>  
        ![](figures/配置虚拟IP地址.png "配置虚拟IP地址")

    8.  单击“确定”，保存更改。
    9.  在“开始”菜单中打开Windows命令行窗口，执行以下命令确认是否配置了虚拟IP地址。

        **ipconfig /all**

        回显样例中IPv4 Address包含虚拟IP地址10.0.0.154，表示弹性云服务器内部网卡的虚拟IP地址配置正常。



## 相关操作<a name="section69073354463"></a>

当不再使用虚拟IP时，可以删除虚拟IP地址，详细内容，请参考[删除虚拟IP地址](https://support.huaweicloud.com/usermanual-vpc/vpc_vip_0009.html)。

弹性云服务器的网卡解绑并删除虚拟IP地址后，需要在弹性云服务器上手工删除虚拟IP地址。

**Linux系统**（本文以“CentOS 7.2 64bit”为例，其他规格请参考对应官网帮助文档）

1.  <a name="li14751815122511"></a>执行以下命令，查看并记录需要删除虚拟IP的网卡及对应连接。

    **nmcli connection**

    回显类似如下信息：

    ![](figures/zh-cn_image_0000001326291534.png)

    本示例的回显信息说明如下：

    -   **DEVICE**列的**eth0**为需要删除虚拟IP的网卡。
    -   **NAME**列的**Wired connection 1**为网卡对应的连接。

2.  执行以下命令，在目标连接中删除虚拟IP。

    **nmcli connection delete "**_CONNECTION_**" ipv4.addresses** _VIP_

    参数说明如下：

    -   CONNECTION：为步骤[1](#li14751815122511)中查到的网卡对应的连接。
    -   VIP：待删除的虚拟IP地址。

3.  执行以下命令，使配置生效。

    **nmcli connection up "**_CONNECTION_**"**

    命令示例：

    **nmcli connection up "Wired connection 1"**

4.  执行以下命令，检查虚拟IP配置是否成功。

    **ip a**

    可以看到eth0网卡下已经不存在添加的虚拟IP地址。


