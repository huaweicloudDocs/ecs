# 管理虚拟IP地址<a name="ecs_03_0506"></a>

## 操作场景<a name="section152499465387"></a>

虚拟IP地址用于为网卡提供第二个IP地址，同时支持与多个的网卡绑定，从而实现多个弹性云服务器之间的高可用性。

## 绑定虚拟IP地址<a name="section9994956183811"></a>

1.  登录管理控制台。
2.  单击“![](figures/service-list.jpg)”，选择“计算 \> 弹性云服务器”。
3.  在弹性云服务器列表中，单击待绑定虚拟IP地址的弹性云服务器名称。

    系统跳转至该弹性云服务器详情页面。

4.  选择“弹性网卡”页签，单击“管理虚拟IP地址”。
5.  选择“IP地址管理”页签，在需要绑定弹性公网IP或者弹性云服务器的虚拟IP地址所在行的操作列下，单击“绑定弹性公网IP”或者“绑定服务器”。

    多个主备部署的弹性云服务器可以在绑定虚拟IP地址时选择同一个虚拟IP地址，增强容灾性能。

6.  单击“确定”。

## 登录弹性云服务器配置虚拟IP地址<a name="section134093255615"></a>

参考以下章节，为已绑定虚拟IP的弹性云服务器手工配置虚拟IP地址。

本文提供以下操作系统的配置示例，其他操作系统，请您参考对应官网帮助文档进行配置。

-   Linux系统：CentOS 7.2 64bit、Ubuntu 22.04 server 64bit
-   Windows系统：Windows Server

**Linux系统（以下配置以“CentOS 7.2 64bit”为例）**

1.  <a name="zh-cn_topic_0118499077_li528316578916"></a>执行以下命令，查看并记录需要绑定虚拟IP的网卡及对应连接。

    **nmcli connection**

    回显类似如下信息：

    ![](figures/zh-cn_image_0000001281210233.png)

    本示例的回显信息说明如下：

    -   **DEVICE**列的**eth0**为需要绑定虚拟IP的网卡。
    -   **NAME**列的**Wired connection 1**为网卡对应的连接。

2.  <a name="zh-cn_topic_0118499077_li20283257695"></a>执行以下命令，在目标网卡连接中添加虚拟IP。

    **nmcli connection modify "**_网卡对应的连接名称_**" +ipv4.addresses** _虚拟IP地址_

    参数说明如下：

    -   网卡对应的连接名称：为[1](#zh-cn_topic_0118499077_li528316578916)中查到的网卡对应的连接，本示例中为**Wired connection 1**。
    -   虚拟IP地址：待添加的虚拟IP地址，如果一次添加多个虚拟IP地址，多个虚拟IP地址之间用“,”隔开。

    命令示例：

    -   添加单个虚拟IP：**nmcli connection modify "Wired connection 1" +ipv4.addresses 172.16.0.125**
    -   添加多个虚拟IP：**nmcli connection modify "Wired connection 1" +ipv4.addresses 172.16.0.125,172.16.0.126**

3.  <a name="zh-cn_topic_0118499077_li11209933188"></a>执行以下命令，使[2](#zh-cn_topic_0118499077_li20283257695)的配置生效。

    **nmcli connection up "**_网卡对应的连接名称_**"**

    命令示例：

    **nmcli connection up "Wired connection 1"**

    回显类似如下信息：

    ![](figures/zh-cn_image_0000001237328110.png)

4.  执行以下命令，检查虚拟IP配置是否成功。

    **ip a**

    回显类似如下信息，可以看到eth0网卡下存在虚拟IP地址，为**172.16.0.125**。

    ![](figures/zh-cn_image_0000001237013856.png)

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >如果您需要删除已添加的虚拟IP，可以使用以下方法：
    >1.  在目标网卡连接中删除虚拟IP。
    >    **nmcli connection modify "**_网卡对应的连接名称_**" -ipv4.addresses** _虚拟IP地址_
    >    一次删除多个虚拟IP地址时，多个IP之间用“,”隔开，命令示例：
    >    -   删除单个虚拟IP：**nmcli connection modify "Wired connection 1" -ipv4.addresses 172.16.0.125**
    >    -   删除多个虚拟IP：**nmcli connection modify "Wired connection 1" -ipv4.addresses 172.16.0.125,172.16.0.126**
    >2.  参考[3](#zh-cn_topic_0118499077_li11209933188)，使删除操作生效。

**Linux系统（以下配置以“Ubuntu 22.04 server 64bit ”为例）**

当弹性云服务器的操作系统为**Ubuntu 22**和**Ubuntu 20**时，请参考以下方法进行配置。

1.  执行以下命令，查看并记录需要绑定虚拟IP的网卡。

    **ifconfig**

    回显类似如下信息，本示例中绑定虚拟IP的网卡名称为**eth0**。

    ```
    root@ecs-X-ubantu:~# ifconfig
    eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
            inet 172.16.0.210  netmask 255.255.255.0  broadcast 172.16.0.255
            inet6 fe80::f816:3eff:fe01:f1c3  prefixlen 64  scopeid 0x20<link>
            ether fa:16:3e:01:f1:c3  txqueuelen 1000  (Ethernet)
            RX packets 43915  bytes 63606486 (63.6 MB)
            RX errors 0  dropped 0  overruns 0  frame 0
            TX packets 3364  bytes 455617 (455.6 KB)
            TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
    ...
    ```

2.  执行以下命令，进入“/etc/netplan”目录。

    **cd /etc/netplan**

3.  <a name="zh-cn_topic_0118499077_li1244016171484"></a>执行以下命令，为目标网卡添加虚拟IP地址。
    1.  执行以下命令，打开配置文件“01-netcfg.yaml”。

        **vim 01-netcfg.yaml**

    2.  按i进入编辑模式。
    3.  在对应网卡配置区域内，添加虚拟IP地址。

        本示例为**eth0**添加虚拟IP地址，待添加内容如下：

        **addresses:**

        **- 172.16.0.26/32**

        添加后文件内容如下：

        ```
        network:
            version: 2
            renderer: NetworkManager
            ethernets:
                eth0:
                    dhcp4: true
                    addresses:
                    - 172.16.0.26/32
                eth1:
                    dhcp4: true
                eth2:
                    dhcp4: true
                eth3:
                    dhcp4: true
                eth4:
                    dhcp4: true
        ```

    4.  添加完成后，按“ESC”，并输入“:wq!”，保存后退出文件。

4.  <a name="zh-cn_topic_0118499077_li1071922334218"></a>执行以下命令，使[3](#zh-cn_topic_0118499077_li1244016171484)的配置生效。

    **netplan apply**

5.  执行以下命令，检查虚拟IP配置是否成功。

    **ip a**

    回显类似如下信息，可以看到eth0网卡下存在虚拟IP地址，为**172.16.0.26**。

    ```
    root@ecs-X-ubantu:/etc/netplan# ip a
    ...
    2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
        link/ether fa:16:3e:01:f1:c3 brd ff:ff:ff:ff:ff:ff
        altname enp0s3
        altname ens3
        inet 172.16.0.26/32 scope global noprefixroute eth0
           valid_lft forever preferred_lft forever
        inet 172.16.0.210/24 brd 172.16.0.255 scope global dynamic noprefixroute eth0
           valid_lft 107999971sec preferred_lft 107999971sec
        inet6 fe80::f816:3eff:fe01:f1c3/64 scope link 
           valid_lft forever preferred_lft forever
    ```

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >如果您需要删除已添加的虚拟IP，可以使用以下方法：
    >1.  参考[3](#zh-cn_topic_0118499077_li1244016171484)，打开配置文件“01-netcfg.yaml”，并删除对应网卡下虚拟IP的地址。
    >2.  参考[4](#zh-cn_topic_0118499077_li1071922334218)，使删除操作生效。

**Windows系统（本文以“Windows Server”为例）**

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

