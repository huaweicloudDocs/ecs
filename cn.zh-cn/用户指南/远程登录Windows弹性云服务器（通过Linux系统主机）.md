# 远程登录Windows弹性云服务器（通过Linux系统主机）<a name="ecs_03_0191"></a>

## 操作场景<a name="zh-cn_topic_0017955381_section119451029135512"></a>

本节为您介绍如何在Linux操作系统主机上登录Windows云服务器。

## 前提条件<a name="zh-cn_topic_0017955381_section30111449112059"></a>

-   云服务器状态为“运行中”。
-   云服务器已经绑定弹性公网IP。

    使用MSTSC方式通过内网登录云服务器时可以不绑定弹性公网IP，例如VPN、云专线等内网网络连通场景。

-   所在安全组入方向已开放3389端口。
-   使用的登录工具与待登录的云服务器之间网络连通。例如，默认的3389端口没有被防火墙屏蔽。
-   云服务器开启远程桌面协议RDP（Remote Desktop Protocol）。使用公共镜像创建的云服务器默认已打开RDP。打开RDP方法请参考[开启远程桌面协议RDP](#section65216898112059)。

## 操作步骤<a name="section10475316119"></a>

如果本地主机为Linux操作系统，您可以使用远程连接工具（例如rdesktop）连接Windows实例。

1.  执行以下命令，检查云服务器是否安装rdesktop。

    **rdesktop**

    如果提示“command not found”说明未安装rdesktop。请参考[rdesktop工具官方](http://www.rdesktop.org/)获取rdesktop安装包安装rdesktop。

2.  输入以下命令登录云服务器。

    **rdesktop -u  _用户名_  -p  _密码_  -g  _分辨率_ _弹性公网IP地址_**

    例如：**rdesktop -u administrator -p password -g 1024\*720 121.xx.xx.xxx**

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
    <tr id="row7221133125617"><td class="cellrowborder" valign="top" width="18.85%" headers="mcps1.2.3.1.1 "><p id="p510920315586"><a name="p510920315586"></a><a name="p510920315586"></a><span id="text03581735143214"><a name="text03581735143214"></a><a name="text03581735143214"></a>弹性公网IP</span>地址</p>
    </td>
    <td class="cellrowborder" valign="top" width="81.15%" headers="mcps1.2.3.1.2 "><p id="p6109437589"><a name="p6109437589"></a><a name="p6109437589"></a>需要远程连接的服务器IP地址。需要替换为您的Windows实例的<span id="text89931542163215"><a name="text89931542163215"></a><a name="text89931542163215"></a>弹性公网IP</span>地址或 EIP 地址。</p>
    </td>
    </tr>
    </tbody>
    </table>

## 开启远程桌面协议RDP<a name="section65216898112059"></a>

首次登录弹性云服务器时，请先使用VNC方式登录弹性云服务器，打开RDP（Remote Desktop Protocol），然后再使用mstsc方式连接。

>![](public_sys-resources/icon-note.gif) **说明：** 
>使用公共镜像创建的云服务器，默认已打开RDP。

1.  VNC方式登录弹性云服务器。

    登录方法请参见[远程登录Windows弹性云服务器（VNC方式）](远程登录Windows弹性云服务器（VNC方式）.md)。

2.  单击“开始”菜单，选择“控制面板 \> 系统和安全 \> 系统 \> 远程设置”。

    系统进入“系统属性”页面。

    **图 1**  系统属性<a name="zh-cn_topic_0017955381_fig276023113838"></a>  
    ![](figures/系统属性.png "系统属性")

3.  选择“远程”页签，在“远程桌面”栏，选择“允许远程连接到此计算机”。
4.  单击“确定”。

