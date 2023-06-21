# Windows弹性云服务器登录方式概述<a name="ZH-CN_TOPIC_0092494943"></a>

## 约束与限制<a name="section2984424226"></a>

-   只有运行中的云服务器才允许用户登录。
-   Windows操作系统用户名“Administrator”。
-   忘记密码，请先通过“重置密码”功能设置登录密码。

    重置密码：选中待重置密码的云服务器，并选择“操作”列下的“ 重置密码”。详细操作，请参见[在控制台重置弹性云服务器密码](在控制台重置弹性云服务器密码.md)。

-   对于密钥方式鉴权的弹性云服务器，需先通过管理控制台提供的获取密码功能，将创建弹性云服务器时使用的私钥文件解析为密码。
-   GPU实例中，部分G系列实例不支持云平台提供的远程登录功能，需要自行安装VNC Server进行登录。详细信息请参见[GPU加速型](https://support.huaweicloud.com/productdesc-ecs/ecs_01_0045.html)。推荐使用MSTSC方式登录弹性云服务器。
-   使用MSTSC方式访问GPU加速型弹性云服务器时，使用WDDM驱动程序模型的GPU将被替换为一个非加速的远程桌面显示驱动程序，造成GPU加速能力无法实现。因此，如果需要使用GPU加速能力，您必须使用不同的远程访问工具，如VNC工具。如果使用管理控制台提供的“远程登录”功能无法满足您的访问需求，请自行在弹性云服务器上安装符合要求的远程访问工具（如Tight VNC）。

    Tight VNC下载地址：[https://www.tightvnc.com/download.php](https://www.tightvnc.com/download.php)


## 登录方式概述<a name="section15582182172010"></a>

请根据需要选择登录方式，登录云服务器。

**表 1**  Windows云服务器登录方式一览

<a name="table12628192415452"></a>
<table><thead align="left"><tr id="row15628122474517"><th class="cellrowborder" valign="top" width="15.101510151015102%" id="mcps1.2.5.1.1"><p id="p166281424144510"><a name="p166281424144510"></a><a name="p166281424144510"></a><span id="text78465201196"><a name="text78465201196"></a><a name="text78465201196"></a>云服务器</span>操作系统</p>
</th>
<th class="cellrowborder" valign="top" width="14.4014401440144%" id="mcps1.2.5.1.2"><p id="p106281624174516"><a name="p106281624174516"></a><a name="p106281624174516"></a>本地主机操作系统</p>
</th>
<th class="cellrowborder" valign="top" width="45.604560456045604%" id="mcps1.2.5.1.3"><p id="p176280245459"><a name="p176280245459"></a><a name="p176280245459"></a>连接方法</p>
</th>
<th class="cellrowborder" valign="top" width="24.892489248924893%" id="mcps1.2.5.1.4"><p id="p31268429168"><a name="p31268429168"></a><a name="p31268429168"></a>条件</p>
</th>
</tr>
</thead>
<tbody><tr id="row716575515812"><td class="cellrowborder" rowspan="6" valign="top" width="15.101510151015102%" headers="mcps1.2.5.1.1 "><p id="p81651855380"><a name="p81651855380"></a><a name="p81651855380"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" width="14.4014401440144%" headers="mcps1.2.5.1.2 "><p id="p9165355081"><a name="p9165355081"></a><a name="p9165355081"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" width="45.604560456045604%" headers="mcps1.2.5.1.3 "><p id="p2971015171814"><a name="p2971015171814"></a><a name="p2971015171814"></a>（推荐使用）使用控制台提供的RDP文件登录<span id="text5811540161911"><a name="text5811540161911"></a><a name="text5811540161911"></a>云服务器</span>。</p>
<p id="p1816517551783"><a name="p1816517551783"></a><a name="p1816517551783"></a><a href="使用RDP文件登录Windows云服务器.md">使用RDP文件登录Windows云服务器</a>。</p>
</td>
<td class="cellrowborder" rowspan="5" valign="top" width="24.892489248924893%" headers="mcps1.2.5.1.4 "><p id="p196451914171"><a name="p196451914171"></a><a name="p196451914171"></a><span id="text173429117197"><a name="text173429117197"></a><a name="text173429117197"></a>云服务器</span>绑定<span id="text152848152188"><a name="text152848152188"></a><a name="text152848152188"></a>弹性公网IP</span></p>
<p id="p109678294370"><a name="p109678294370"></a><a name="p109678294370"></a>（通过内网登录<span id="text15207159121916"><a name="text15207159121916"></a><a name="text15207159121916"></a>云服务器</span>时可以不绑定弹性公网IP，例如VPN、云专线等内网网络连通场景。）</p>
</td>
</tr>
<tr id="row936071901815"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p2361319191814"><a name="p2361319191814"></a><a name="p2361319191814"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p6756423191411"><a name="p6756423191411"></a><a name="p6756423191411"></a>使用mstsc方式登录<span id="text12191134417192"><a name="text12191134417192"></a><a name="text12191134417192"></a>云服务器</span>。</p>
<p id="p16756723121413"><a name="p16756723121413"></a><a name="p16756723121413"></a>在本地主机单击“开始”菜单，输入<strong id="b14756102317142"><a name="b14756102317142"></a><a name="b14756102317142"></a>mstsc</strong>命令，打开远程桌面对话框。</p>
<p id="p3825173141916"><a name="p3825173141916"></a><a name="p3825173141916"></a><a href="远程桌面连接（MSTSC方式）.md">远程桌面连接（MSTSC方式）</a>。</p>
</td>
</tr>
<tr id="row675410233182"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1575442311815"><a name="p1575442311815"></a><a name="p1575442311815"></a>Linux</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p17754623141813"><a name="p17754623141813"></a><a name="p17754623141813"></a>安装远程连接工具，例如rdesktop，执行连接命令。</p>
<p id="p1116112813566"><a name="p1116112813566"></a><a name="p1116112813566"></a><a href="在Linux主机上登录Windows云服务器.md">在Linux主机上登录Windows云服务器</a>。</p>
</td>
</tr>
<tr id="row20754202301818"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p575416238183"><a name="p575416238183"></a><a name="p575416238183"></a>Mac OS系统</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p4953317122213"><a name="p4953317122213"></a><a name="p4953317122213"></a>安装远程连接工具，例如Microsoft Remote Desktop for Mac在Mac OS系统上登录。</p>
<p id="p2754523141820"><a name="p2754523141820"></a><a name="p2754523141820"></a><a href="Mac-OS系统登录Windows云服务器.md">Mac OS系统登录Windows云服务器</a>。</p>
</td>
</tr>
<tr id="row12754112311185"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1775462381810"><a name="p1775462381810"></a><a name="p1775462381810"></a>移动设备</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p20436453224"><a name="p20436453224"></a><a name="p20436453224"></a>安装远程连接工具，例如Microsoft Remote Desktop在移动设备上登录。</p>
<p id="p117543231189"><a name="p117543231189"></a><a name="p117543231189"></a><a href="在移动设备上登录Windows云服务器.md">在移动设备上登录Windows云服务器</a>。</p>
</td>
</tr>
<tr id="row11628142404520"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p5628324104515"><a name="p5628324104515"></a><a name="p5628324104515"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1628172413458"><a name="p1628172413458"></a><a name="p1628172413458"></a>使用管理控制台远程登录方式：<a href="Windows弹性云服务器管理控制台远程登录（VNC方式）.md">Windows弹性云服务器管理控制台远程登录（VNC方式）</a>。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p4667354174911"><a name="p4667354174911"></a><a name="p4667354174911"></a>不依赖<span id="text1436074610173"><a name="text1436074610173"></a><a name="text1436074610173"></a>弹性公网IP</span></p>
</td>
</tr>
</tbody>
</table>

## 相关链接<a name="section2826432183510"></a>

-   [忘记密码怎么办？](密码使用场景介绍.md)
-   [Windows云服务器如何配置多用户登录？](https://support.huaweicloud.com/trouble-ecs/ecs_trouble_0900.html)
-   [无法登录到Windows云服务器怎么办？](https://support.huaweicloud.com/ecs_faq/zh-cn_topic_0018073217.html)

