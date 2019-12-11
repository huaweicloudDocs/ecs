# 远程桌面连接（MSTSC方式）<a name="ZH-CN_TOPIC_0017955381"></a>

## 操作场景<a name="section119451029135512"></a>

本节为您介绍如何在本机使用远程登录工具MSTSC登录Windows弹性云服务器。

## 前提条件<a name="section30111449112059"></a>

-   云服务器状态为“运行中”。
-   如果弹性云服务器采用密钥方式鉴权，已获取Windows弹性云服务器的密码，获取方式请参见[获取Windows弹性云服务器的密码](获取Windows弹性云服务器的密码.md)。
-   弹性云服务器已经绑定弹性公网IP，绑定方式请参见[绑定弹性公网IP](绑定弹性公网IP.md)。

-   所在安全组入方向已开放3389端口，配置方式请参见[配置安全组规则](配置安全组规则.md)。
-   使用的登录工具与待登录的弹性云服务器之间网络连通。例如，默认的3389端口没有被防火墙屏蔽。
-   弹性云服务器开启远程桌面协议RDP（Remote Desktop Protocol）。使用公共镜像创建的云服务器默认已打开RDP。打开RDP方法请参考[开启远程桌面协议RDP](#section65216898112059)。

## 使用MSTSC方式登录Windows弹性云服务器<a name="section1011913410314"></a>

本地主机为Windows操作系统，那么可以使用Windows自带的远程桌面连接工具MSTSC登录Windows弹性云服务器。

1.  在本地主机单击“开始”菜单。
2.  在“搜索程序和文件”中，输入“mstsc”，单击mstsc打开远程桌面连接工具。
3.  在“远程桌面连接”的对话框中，单击“选项”。

    **图 1**  显示选项<a name="zh-cn_topic_0027290684_fig22996848191913"></a>  
    ![](figures/显示选项.png "显示选项")

4.  输入待登录的弹性云服务器的弹性公网IP和用户名，默认为Administrator。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >如需再次登录时不再重复输入用户名和密码，可勾选“允许我保存凭据”。  

    **图 2**  远程桌面链接<a name="fig61897111106"></a>  
    ![](figures/远程桌面链接.png "远程桌面链接")

5.  （可选）如需在远程会话中使用本地主机的资源，请单击“本地资源”选项卡完成如下配置。
    -   如需从本地主机复制到云服务器中，请勾选“剪贴板”。

        **图 3**  勾选剪贴板<a name="fig5308424112111"></a>  
        ![](figures/勾选剪贴板.png "勾选剪贴板")

        -   如需从本地主机复制文件到云服务器中，单击“详细信息”，勾选“驱动器”和相应的磁盘。

            **图 4**  勾选驱动器<a name="fig2016145215213"></a>  
            ![](figures/勾选驱动器.png "勾选驱动器")


6.  （可选）如需调整远程桌面窗口的大小，可以选择“显示”选项卡，再调整窗口大小。

    **图 5**  调整窗口大小<a name="fig45767599405"></a>  
    ![](figures/调整窗口大小.png "调整窗口大小")

7.  单击“确定”，根据提示输入云服务器密码，登录弹性云服务器。

    为安全起见，首次登录弹性云服务器，需更改密码。

    **图 6**  输入云服务器密码<a name="fig1975358193111"></a>  
    ![](figures/输入云服务器密码.png "输入云服务器密码")

8.  （可选）通过远程桌面连接（Remote Desktop Protocol, RDP）方式登录弹性云服务器后，如果需要使用RDP提供的“剪切板”功能，将本地的大文件（文件大小超过2GB）复制粘贴至远端的Windows弹性云服务器中，由于Windows系统的限制，会导致操作失败。

    具体的解决方法，请参见[https://support.microsoft.com/en-us/help/2258090/copying-files-larger-than-2-gb-over-a-remote-desktop-services-or-terminal-services-session-by-using-clipboard-redirection-copy-and-paste-fails-silently](https://support.microsoft.com/en-us/help/2258090/copying-files-larger-than-2-gb-over-a-remote-desktop-services-or-terminal-services-session-by-using-clipboard-redirection-copy-and-paste-fails-silently)。


## 本地Linux操作系统登录Windows云服务器<a name="section10475316119"></a>

如果本地主机为Linux操作系统，您可以使用远程连接工具（例如rdesktop）连接Windows实例。

1.  在本地主机下载并安装rdesktop工具。

    **yum -y install rdesktop**

2.  输入以下命令登录云服务器。

    **rdesktop -u  _用户名_  -p  _密码_  -g  _分辨率_ _弹性公网IP地址_**

    例如：**rdesktop -u administrator -p password -g 1024\*720 192.168.x.x**

    **表 1**  远程登录命令参数

    <a name="table522016385618"></a>
    <table><thead align="left"><tr id="row10220131567"><th class="cellrowborder" valign="top" width="18.85%" id="mcps1.2.3.1.1"><p id="p1422063175611"><a name="p1422063175611"></a><a name="p1422063175611"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="81.15%" id="mcps1.2.3.1.2"><p id="p22201931564"><a name="p22201931564"></a><a name="p22201931564"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row422018365611"><td class="cellrowborder" valign="top" width="18.85%" headers="mcps1.2.3.1.1 "><p id="p151081031580"><a name="p151081031580"></a><a name="p151081031580"></a>-u</p>
    </td>
    <td class="cellrowborder" valign="top" width="81.15%" headers="mcps1.2.3.1.2 "><p id="p181082375811"><a name="p181082375811"></a><a name="p181082375811"></a>用户名，Windows实例默认用户名是Administrator。</p>
    </td>
    </tr>
    <tr id="row922117310569"><td class="cellrowborder" valign="top" width="18.85%" headers="mcps1.2.3.1.1 "><p id="p12108331586"><a name="p12108331586"></a><a name="p12108331586"></a>-p</p>
    </td>
    <td class="cellrowborder" valign="top" width="81.15%" headers="mcps1.2.3.1.2 "><p id="p1410893145811"><a name="p1410893145811"></a><a name="p1410893145811"></a>登录Windows实例的密码。</p>
    </td>
    </tr>
    <tr id="row92211335563"><td class="cellrowborder" valign="top" width="18.85%" headers="mcps1.2.3.1.1 "><p id="p201086395817"><a name="p201086395817"></a><a name="p201086395817"></a>-f</p>
    </td>
    <td class="cellrowborder" valign="top" width="81.15%" headers="mcps1.2.3.1.2 "><p id="p210810325811"><a name="p210810325811"></a><a name="p210810325811"></a>默认全屏，需要用 Ctrl+Alt+Enter 组合键进行全屏模式切换。</p>
    </td>
    </tr>
    <tr id="row122215314561"><td class="cellrowborder" valign="top" width="18.85%" headers="mcps1.2.3.1.1 "><p id="p201091033582"><a name="p201091033582"></a><a name="p201091033582"></a>-g</p>
    </td>
    <td class="cellrowborder" valign="top" width="81.15%" headers="mcps1.2.3.1.2 "><p id="p141098317582"><a name="p141098317582"></a><a name="p141098317582"></a>分辨率，中间用星号（*）连接，可省略，省略后默认为全屏显示。例如：<strong id="b10895163017715"><a name="b10895163017715"></a><a name="b10895163017715"></a>1024*720</strong></p>
    </td>
    </tr>
    <tr id="row7221133125617"><td class="cellrowborder" valign="top" width="18.85%" headers="mcps1.2.3.1.1 "><p id="p510920315586"><a name="p510920315586"></a><a name="p510920315586"></a>弹性公网IP地址</p>
    </td>
    <td class="cellrowborder" valign="top" width="81.15%" headers="mcps1.2.3.1.2 "><p id="p6109437589"><a name="p6109437589"></a><a name="p6109437589"></a>需要远程连接的服务器IP地址。需要替换为您的Windows实例的弹性公网IP地址或 EIP 地址。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 开启远程桌面协议RDP<a name="section65216898112059"></a>

首次登录弹性云服务器时，请先使用VNC方式登录弹性云服务器，打开RDP（Remote Desktop Protocol），然后再使用mstsc方式连接。

>![](public_sys-resources/icon-note.gif) **说明：**   
>使用公共镜像创建的云服务器，默认已打开RDP。  

1.  VNC方式登录弹性云服务器。

    登录方法请参见[Windows弹性云服务器管理控制台远程登录（VNC方式）](Windows弹性云服务器管理控制台远程登录（VNC方式）.md)。

2.  单击“开始”菜单，选择“控制面板 \> 系统和安全 \> 系统 \> 远程设置”。

    系统进入“系统属性”页面。

    **图 7**  系统属性<a name="fig276023113838"></a>  
    ![](figures/系统属性.png "系统属性")

3.  选择“远程”页签，在“远程桌面”栏，选择“允许远程连接到此计算机”。
4.  单击“确定”。

## 相关链接<a name="section2826432183510"></a>

-   [云服务器登录前的准备工作有哪些？](https://support.huaweicloud.com/ecs_faq/zh-cn_topic_0163540201.html)
-   [无法登录到Windows云服务器怎么办？](https://support.huaweicloud.com/ecs_faq/zh-cn_topic_0018073217.html)

