# Linux弹性云服务器登录方式概述<a name="ZH-CN_TOPIC_0013771089"></a>

## 约束与限制<a name="section15584113212291"></a>

-   只有运行中的弹性云服务器才允许用户登录。
-   Linux操作系统用户名“root”。
-   忘记密码，请先通过“重置密码”功能设置登录密码。

    重置密码：选中待重置密码的云服务器，并选择“操作”列下的“ 重置密码”。详细操作，请参见[在控制台重置弹性云服务器密码](在控制台重置弹性云服务器密码.md)。


## 登录方式概述<a name="section95820318444"></a>

请根据需要选择登录方式，登录云服务器。

**表 1**  Linux云服务器登录方式一览

<a name="table12628192415452"></a>
<table><thead align="left"><tr id="row15628122474517"><th class="cellrowborder" valign="top" width="12.58125812581258%" id="mcps1.2.5.1.1"><p id="p166281424144510"><a name="p166281424144510"></a><a name="p166281424144510"></a>云服务器操作系统</p>
</th>
<th class="cellrowborder" valign="top" width="15.191519151915193%" id="mcps1.2.5.1.2"><p id="p106281624174516"><a name="p106281624174516"></a><a name="p106281624174516"></a>本地主机操作系统</p>
</th>
<th class="cellrowborder" valign="top" width="43.154315431543154%" id="mcps1.2.5.1.3"><p id="p176280245459"><a name="p176280245459"></a><a name="p176280245459"></a>连接方法</p>
</th>
<th class="cellrowborder" valign="top" width="29.072907290729074%" id="mcps1.2.5.1.4"><p id="p31268429168"><a name="p31268429168"></a><a name="p31268429168"></a>条件</p>
</th>
</tr>
</thead>
<tbody><tr id="row716575515812"><td class="cellrowborder" rowspan="7" valign="top" width="12.58125812581258%" headers="mcps1.2.5.1.1 "><p id="p81651855380"><a name="p81651855380"></a><a name="p81651855380"></a>Linux</p>
</td>
<td class="cellrowborder" valign="top" width="15.191519151915193%" headers="mcps1.2.5.1.2 "><p id="p9165355081"><a name="p9165355081"></a><a name="p9165355081"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" width="43.154315431543154%" headers="mcps1.2.5.1.3 "><p id="p2971015171814"><a name="p2971015171814"></a><a name="p2971015171814"></a>（推荐使用）使用控制台提供的CloudShell登录云服务器。</p>
<p id="p1816517551783"><a name="p1816517551783"></a><a name="p1816517551783"></a><a href="使用CloudShell登录云服务器.md">使用CloudShell登录云服务器</a>。</p>
</td>
<td class="cellrowborder" rowspan="6" valign="top" width="29.072907290729074%" headers="mcps1.2.5.1.4 "><p id="p196451914171"><a name="p196451914171"></a><a name="p196451914171"></a>云服务器绑定弹性公网IP。</p>
<p id="p109678294370"><a name="p109678294370"></a><a name="p109678294370"></a>（通过内网登录云服务器时可以不绑定弹性公网IP，例如VPN、云专线等内网网络连通场景。）</p>
<p id="p109224635614"><a name="p109224635614"></a><a name="p109224635614"></a></p>
</td>
</tr>
<tr id="row20754202301818"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p575416238183"><a name="p575416238183"></a><a name="p575416238183"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p322813265319"><a name="p322813265319"></a><a name="p322813265319"></a>使用PuTTY、Xshell等远程登录工具：</p>
<a name="ul1922818322536"></a><a name="ul1922818322536"></a><ul id="ul1922818322536"><li>密码方式鉴权：<a href="SSH密码方式登录.md#section62068112020">SSH密码方式登录（本地使用Windows操作系统）</a>。</li><li>密钥方式鉴权：<a href="SSH密钥方式登录.md#section47918167111724">SSH密钥方式登录（本地使用Windows操作系统）</a>。</li></ul>
</td>
</tr>
<tr id="row158119153539"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1258151511530"><a name="p1258151511530"></a><a name="p1258151511530"></a>Linux</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p916813541539"><a name="p916813541539"></a><a name="p916813541539"></a>使用命令连接：</p>
<a name="ul4168165465311"></a><a name="ul4168165465311"></a><ul id="ul4168165465311"><li>密码方式鉴权：<a href="SSH密码方式登录.md#section20811823174313">SSH密码方式登录（本地使用Linux操作系统）</a>。</li><li>密钥方式鉴权：<a href="SSH密钥方式登录.md#section3666784111724">SSH密钥方式登录（本地使用Linux操作系统）</a>。</li></ul>
</td>
</tr>
<tr id="row12754112311185"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p1775462381810"><a name="p1775462381810"></a><a name="p1775462381810"></a>移动设备</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p20436453224"><a name="p20436453224"></a><a name="p20436453224"></a>使用Termius、JuiceSSH等SSH客户端工具登录云服务器。</p>
<p id="p117543231189"><a name="p117543231189"></a><a name="p117543231189"></a><a href="在移动设备上登录Linux云服务器.md">在移动设备上登录Linux云服务器</a>。</p>
</td>
</tr>
<tr id="row168129165611"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p108452042564"><a name="p108452042564"></a><a name="p108452042564"></a>移动设备</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p28456415616"><a name="p28456415616"></a><a name="p28456415616"></a>下载华为云APP连接云服务器。</p>
<p id="p188451941565"><a name="p188451941565"></a><a name="p188451941565"></a><a href="使用华为云APP连接Linux云服务器.md">使用华为云APP连接Linux云服务器</a>。</p>
</td>
</tr>
<tr id="row12926465567"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p5922469560"><a name="p5922469560"></a><a name="p5922469560"></a>macOS系统</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p792124655616"><a name="p792124655616"></a><a name="p792124655616"></a>使用系统自带的终端（Terminal）：</p>
<p id="p12492045155716"><a name="p12492045155716"></a><a name="p12492045155716"></a><a href="macOS系统登录Linux弹性云服务器.md">macOS系统登录Linux弹性云服务器</a>。</p>
</td>
</tr>
<tr id="row11628142404520"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p5628324104515"><a name="p5628324104515"></a><a name="p5628324104515"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1628172413458"><a name="p1628172413458"></a><a name="p1628172413458"></a>使用管理控制台远程登录方式：<a href="Linux弹性云服务器远程登录（VNC方式）.md">Linux弹性云服务器远程登录（VNC方式）</a>。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.5.1.3 "><p id="p4667354174911"><a name="p4667354174911"></a><a name="p4667354174911"></a>不依赖弹性公网IP。</p>
</td>
</tr>
</tbody>
</table>

## 相关链接<a name="section2826432183510"></a>

-   [忘记密码怎么办？](密码使用场景介绍.md)
-   [无法登录到Linux云服务器怎么办？](https://support.huaweicloud.com/ecs_faq/zh-cn_topic_0105127983.html)

