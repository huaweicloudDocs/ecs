# Windows弹性云服务器登录方式概述<a name="ZH-CN_TOPIC_0092494943"></a>

## 约束与限制<a name="section109631817183419"></a>

-   只有运行中的弹性云服务器才允许用户登录。
-   对于密钥方式鉴权的弹性云服务器，需先通过管理控制台提供的获取密码功能，将创建弹性云服务器时使用的私钥文件解析为密码。
-   GPU实例中，G5不支持云平台提供的远程登录功能，如果需要VNC登录，则用户需要在镜像制作时安装VNC Server（VNC Server由用户自己提供），否则会导致弹性云服务器无法VNC登录。

    您可以用MSTSC方式登录弹性云服务器，登录方法请参见[远程桌面连接（MSTSC方式）](远程桌面连接（MSTSC方式）.md)。

-   GPU实例中，G3不支持公有云平台提供的远程登录功能，如果需要VNC登录，则用户需要在镜像制作时安装VNC Server（VNC Server由用户自己提供），否则会导致弹性云服务器无法VNC登录。

    您可以用MSTSC方式登录弹性云服务器，登录方法请参见[远程桌面连接（MSTSC方式）](远程桌面连接（MSTSC方式）.md)。

-   G1型弹性云服务器、规格为g1.2xlarge.8的弹性云服务器，不支持公有云平台提供的远程登录功能，需要自行安装VNC Server进行登录，VNC Server由用户自己提供。
-   MSTSC方式仅适用于Windows弹性云服务器。
-   MSTSC方式要求该弹性云服务器已绑定弹性公网IP。
-   使用控制台提供的RDP文件登录云服务器要求该弹性云服务器已绑定弹性公网IP。
-   使用移动设备登录要求该弹性云服务器已绑定弹性公网IP。
-   使用Mac OS系统登录要求该弹性云服务器已绑定弹性公网IP。
-   使用MSTSC方式访问GPU加速型弹性云服务器时，使用WDDM驱动程序模型的GPU将被替换为一个非加速的远程桌面显示驱动程序，造成GPU加速能力无法实现。因此，如果需要使用GPU加速能力，您必须使用不同的远程访问工具，如VNC工具。如果使用管理控制台提供的“远程登录”功能无法满足您的访问需求，请自行在弹性云服务器上安装符合要求的远程访问工具（如Tight VNC）。

    Tight VNC下载地址：[https://www.tightvnc.com/download.php](https://www.tightvnc.com/download.php)


## 登录方式概述<a name="section15582182172010"></a>

只有运行中的弹性云服务器才允许用户登录。

请根据需要选择登录方式，登录弹性云服务器。Windows操作系统用户名“Administrator”。

**表 1**  Windows云服务器登录方式一览

<a name="table61081657112611"></a>
<table><thead align="left"><tr id="row191096571265"><th class="cellrowborder" valign="top" width="16.13161316131613%" id="mcps1.2.4.1.1"><p id="p1110985719266"><a name="p1110985719266"></a><a name="p1110985719266"></a>是否绑定EIP</p>
</th>
<th class="cellrowborder" valign="top" width="20.882088208820885%" id="mcps1.2.4.1.2"><p id="p9109175712263"><a name="p9109175712263"></a><a name="p9109175712263"></a>本地设备操作系统</p>
</th>
<th class="cellrowborder" valign="top" width="62.98629862986299%" id="mcps1.2.4.1.3"><p id="p101093571265"><a name="p101093571265"></a><a name="p101093571265"></a>连接方法</p>
</th>
</tr>
</thead>
<tbody><tr id="row1735573445420"><td class="cellrowborder" valign="top" width="16.13161316131613%" headers="mcps1.2.4.1.1 "><p id="p810935742618"><a name="p810935742618"></a><a name="p810935742618"></a>VNC登录对EIP无依赖</p>
</td>
<td class="cellrowborder" valign="top" width="20.882088208820885%" headers="mcps1.2.4.1.2 "><p id="p12109165719267"><a name="p12109165719267"></a><a name="p12109165719267"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" width="62.98629862986299%" headers="mcps1.2.4.1.3 "><p id="p6109757112613"><a name="p6109757112613"></a><a name="p6109757112613"></a>使用管理控制台远程登录方式：<a href="Windows弹性云服务器管理控制台远程登录（VNC方式）.md">Windows弹性云服务器管理控制台远程登录（VNC方式）</a>。</p>
</td>
</tr>
<tr id="row334382365716"><td class="cellrowborder" valign="top" width="16.13161316131613%" headers="mcps1.2.4.1.1 "><p id="p3123112416576"><a name="p3123112416576"></a><a name="p3123112416576"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.882088208820885%" headers="mcps1.2.4.1.2 "><p id="p15123172410572"><a name="p15123172410572"></a><a name="p15123172410572"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" width="62.98629862986299%" headers="mcps1.2.4.1.3 "><p id="p412342416572"><a name="p412342416572"></a><a name="p412342416572"></a>使用控制台提供的RDP文件登录云服务器：<a href="使用RDP文件登录Windows云服务器.md">使用RDP文件登录Windows云服务器</a>。</p>
</td>
</tr>
<tr id="row1109257152618"><td class="cellrowborder" valign="top" width="16.13161316131613%" headers="mcps1.2.4.1.1 "><p id="p31093573261"><a name="p31093573261"></a><a name="p31093573261"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.882088208820885%" headers="mcps1.2.4.1.2 "><p id="p710918576262"><a name="p710918576262"></a><a name="p710918576262"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" width="62.98629862986299%" headers="mcps1.2.4.1.3 "><p id="p852021613318"><a name="p852021613318"></a><a name="p852021613318"></a>使用远程桌面连接MSTSC方式：<a href="远程桌面连接（MSTSC方式）.md">远程桌面连接（MSTSC方式）</a>。</p>
<p id="p12883234183414"><a name="p12883234183414"></a><a name="p12883234183414"></a>（使用MSTSC方式通过内网登录云服务器时可以不绑定弹性公网IP，例如VPN、云专线等内网网络连通场景。）</p>
</td>
</tr>
<tr id="row1970731303"><td class="cellrowborder" valign="top" width="16.13161316131613%" headers="mcps1.2.4.1.1 "><p id="p697115333019"><a name="p697115333019"></a><a name="p697115333019"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.882088208820885%" headers="mcps1.2.4.1.2 "><p id="p897112317306"><a name="p897112317306"></a><a name="p897112317306"></a>移动设备</p>
</td>
<td class="cellrowborder" valign="top" width="62.98629862986299%" headers="mcps1.2.4.1.3 "><p id="p159711393011"><a name="p159711393011"></a><a name="p159711393011"></a>在移动设备上登录：<a href="在移动设备上登录Windows弹性云服务器.md">在移动设备上登录Windows弹性云服务器</a>。</p>
</td>
</tr>
<tr id="row1236541865117"><td class="cellrowborder" valign="top" width="16.13161316131613%" headers="mcps1.2.4.1.1 "><p id="p18664192410513"><a name="p18664192410513"></a><a name="p18664192410513"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.882088208820885%" headers="mcps1.2.4.1.2 "><p id="p46641324205111"><a name="p46641324205111"></a><a name="p46641324205111"></a>Mac OS系统</p>
</td>
<td class="cellrowborder" valign="top" width="62.98629862986299%" headers="mcps1.2.4.1.3 "><p id="p186641524125115"><a name="p186641524125115"></a><a name="p186641524125115"></a>在Mac OS系统上登录：<a href="Mac-OS系统登录Windows弹性云服务器.md">Mac OS系统登录Windows弹性云服务器</a>。</p>
</td>
</tr>
</tbody>
</table>

## 相关链接<a name="section2826432183510"></a>

-   [云服务器登录前的准备工作有哪些？](https://support.huaweicloud.com/ecs_faq/zh-cn_topic_0163540201.html)
-   [无法登录到Windows云服务器怎么办？](https://support.huaweicloud.com/ecs_faq/zh-cn_topic_0018073217.html)

