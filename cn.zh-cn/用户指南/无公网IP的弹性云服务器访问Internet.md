# 无公网IP的弹性云服务器访问Internet<a name="ZH-CN_TOPIC_0027157850"></a>

## 操作场景<a name="section6427533194453"></a>

为保证安全和节省公网IP资源，通常只为特定的弹性云服务器配置公网IP，可直接访问Internet，其他弹性云服务器只配置私网IP，无法直接访问Internet。因此，当只配置了私网IP的弹性云服务器需要访问Internet，执行软件升级、给系统打补丁或者其它需求时，可选择一台绑定了公网IP的弹性云服务器作为代理弹性云服务器，为其他无公网IP的云服务器提供访问通道，正常访问Internet。

>![](public_sys-resources/icon-note.gif) **说明：**   
>优先推荐您使用NAT（NAT Gateway）网关服务。NAT网关能够为VPC内的弹性云服务器提供SNAT和DNAT功能，通过灵活简易的配置，即可轻松构建VPC的公网出入口。了解更多请参考[NAT网关](https://support.huaweicloud.com/natgateway/index.html)。  

## 前提条件<a name="section2608915610029"></a>

-   已拥有一台绑定了公网IP的弹性云服务器作为代理弹性云服务器。

    本节操作中，以代理弹性云服务器的操作系统是CentOS 6.5为例。

-   代理弹性云服务器和其他需要访问Internet的弹性云服务器均处于同一网段，并且在同一安全组内。

## 操作步骤<a name="section6907807103042"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/icon-region.png)，选择区域和项目。
3.  选择“计算 \> 弹性云服务器”。
4.  在弹性云服务器列表中的右上角，输入代理云服务器名称进行搜索。
5.  单击代理弹性云服务器的名称，查看详情。
6.  在代理弹性云服务器详情页面，选择“网卡”页签，并展开![](figures/icon-dropdown.jpg)，将“源/目的检查”选项设置为“OFF”。

    默认情况下，“源/目的检查”状态为“启用”，系统会检查弹性云服务器发送的报文中源IP地址是否正确，否则不允许弹性云服务器发送该报文。这有助于防止伪装报文攻击，提升安全性。但在该场景中，这种保护机制会导致报文的发送者无法接收到返回的报文。因此，需设置“源/目的检查”状态为禁用。

7.  登录代理弹性云服务器。

    详细操作方法请参见[Linux弹性云服务器登录方式概述](Linux弹性云服务器登录方式概述.md)。

8.  执行以下命令，检测代理弹性云服务器是否可以正常连接Internet。

    **ping www.baidu.com**

    回显包含类似如下信息时，表示代理弹性云服务器可正常连接Internet。

    **图 1**  检测是否可以正常连接Internet<a name="fig932219254813"></a>  
    ![](figures/检测是否可以正常连接Internet.png "检测是否可以正常连接Internet")

9.  执行以下命令，查看代理弹性云服务器的IP转发功能是否开启。

    **cat /proc/sys/net/ipv4/ip\_forward**

    -   回显为“0”表示关闭，请执行[10](#li51820417113959)。
    -   回显为“1”表示开启，请执行[16](#li49419571113959)。

10. <a name="li51820417113959"></a>执行以下命令，打开IP转发功能配置文件。

    **vi /etc/sysctl.conf**

11. 按“i”，进入编辑模式。
12. 修改如下参数的值。

    将参数“net.ipv4.ip\_forward ”的值修改为“1”。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >如果“sysctl.conf”文件中不存在参数“net.ipv4.ip\_forward ”，执行以下命令进行添加：  
    >**echo net.ipv4.ip\_forward=1 \>\> /etc/sysctl.conf**  

13. 按“Esc”，输入**:wq**，按“Enter”。

    保存设置并退出vi编辑器。

14. <a name="li61723653113959"></a>执行以下命令，使配置文件修改生效。

    **sysctl -p /etc/sysctl.conf**

15. 执行以下命令，清除原有iptables规则。

    **iptables -F**

16. <a name="li49419571113959"></a>执行以下命令，配置SNAT，使代理弹性云服务器所在的网段内其他弹性云服务器可通过代理弹性云服务器访问Internet。

    **iptables -t nat -A POSTROUTING -o eth0 -s** _**subnet/netmask-bits**_ **-j SNAT --to** _**nat-instance-ip**_

    假设代理弹性云服务器所在的网段为192.168.125.0，子网掩码为24位，私网IP地址为192.168.125.4，则执行如下命令。

    **iptables -t nat -A POSTROUTING -o eth0 -s** _**192.168.125.0/24**_ **-j SNAT --to 192.168.125.4**

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >为了确保重启后上述规则不丢失，可以执行**vi /etc/rc.local**编辑**rc.local**文件，将[14](#li61723653113959)中的规则复制到**rc.local**文件，按“ESC”退出编辑模式，输入“:wq”保存并退出。  

17. 执行以下命令，查看SNAT配置是否成功。

    **iptables -t nat --list**

    回显类似如[图2](#fig27598108113959)所示时，表示SNAT配置成功。

    **图 2**  SNAT配置成功<a name="fig27598108113959"></a>  
    ![](figures/SNAT配置成功.png "SNAT配置成功")

18. 添加自定义路由。
    1.  登录控制台。
    2.  单击管理控制台左上角的![](figures/icon-region.png)，选择区域和项目。
    3.  选择“网络 \> 虚拟私有云”。
    4.  选择需要添加路由表的虚拟私有云，在“路由表”页面，单击“添加路由信息”。
    5.  根据界面提示，填写路由信息。
        -   目的地址：是目的网段，默认是0.0.0.0/0。
        -   下一跳地址：是SNAT弹性云服务器的私有IP地址。

            您可以在弹性云服务器页面，查看该弹性云服务器的私有IP地址。




## 后续处理<a name="section1977851205413"></a>

如需删除添加的iptables规则，需执行以下命令：

**iptables -t nat -D POSTROUTING -o eth0 -s** _**subnet/netmask-bits**_ **-j SNAT --to** _**nat-instance-ip**_

假设代理弹性云服务器所在的网段为192.168.125.0，子网掩码为24位，私网IP地址为192.168.125.4，则执行如下命令。

**iptables -t nat -D POSTROUTING -o eth0 -s 192.168.125.0/24 -j SNAT --to 192.168.125.4**

