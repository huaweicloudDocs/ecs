# Linux云服务器登录方式概述<a name="ZH-CN_TOPIC_0013771089"></a>

只有运行中的弹性云服务器才允许用户登录。

登录Linux弹性云服务器的方式有：VNC登录、SSH方式登录。

-   VNC方式登录

    未绑定弹性公网IP的弹性云服务器可通过管理控制台提供的远程登录方式直接登录。

-   SSH方式登录

    仅适用于Linux弹性云服务器。您可以使用远程登录工具（例如PuTTY），登录弹性云服务器。此时，弹性云服务器需绑定弹性公网IP。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >包括SSH密钥方式和SSH密码方式。  


**表 1**  Linux云服务器登录方式一览

<a name="table61081657112611"></a>
<table><thead align="left"><tr id="row191096571265"><th class="cellrowborder" valign="top" width="20.8020802080208%" id="mcps1.2.4.1.1"><p id="p1110985719266"><a name="p1110985719266"></a><a name="p1110985719266"></a>是否绑定EIP</p>
</th>
<th class="cellrowborder" valign="top" width="18.24182418241824%" id="mcps1.2.4.1.2"><p id="p9109175712263"><a name="p9109175712263"></a><a name="p9109175712263"></a>本地设备操作系统</p>
</th>
<th class="cellrowborder" valign="top" width="60.956095609560954%" id="mcps1.2.4.1.3"><p id="p101093571265"><a name="p101093571265"></a><a name="p101093571265"></a>连接方法</p>
</th>
</tr>
</thead>
<tbody><tr id="row1109257152618"><td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.1 "><p id="p31093573261"><a name="p31093573261"></a><a name="p31093573261"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18.24182418241824%" headers="mcps1.2.4.1.2 "><p id="p710918576262"><a name="p710918576262"></a><a name="p710918576262"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top" width="60.956095609560954%" headers="mcps1.2.4.1.3 "><p id="p852021613318"><a name="p852021613318"></a><a name="p852021613318"></a>使用PuTTY、Xshell等远程登录工具：</p>
<a name="ul7459195253114"></a><a name="ul7459195253114"></a><ul id="ul7459195253114"><li>密码方式鉴权：<a href="SSH密码方式登录.md">SSH密码方式登录</a>的“客户端使用Windows系统”。</li><li>密钥方式鉴权：<a href="SSH密钥方式登录.md">SSH密钥方式登录</a>的<a href="SSH密钥方式登录.md#section47918167111724">本地使用Windows操作系统</a>。</li></ul>
</td>
</tr>
<tr id="row5621130122920"><td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.1 "><p id="p186221930202910"><a name="p186221930202910"></a><a name="p186221930202910"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18.24182418241824%" headers="mcps1.2.4.1.2 "><p id="p66221308296"><a name="p66221308296"></a><a name="p66221308296"></a>Linux</p>
</td>
<td class="cellrowborder" valign="top" width="60.956095609560954%" headers="mcps1.2.4.1.3 "><p id="p10622330122919"><a name="p10622330122919"></a><a name="p10622330122919"></a>使用命令连接：</p>
<a name="ul877312810369"></a><a name="ul877312810369"></a><ul id="ul877312810369"><li>密码方式鉴权：<a href="SSH密码方式登录.md">SSH密码方式登录</a>的“客户端使用Linux系统”。</li><li>密钥方式鉴权：<a href="SSH密钥方式登录.md">SSH密钥方式登录</a>的<a href="SSH密钥方式登录.md#section3666784111724">本地使用Linux操作系统</a>。</li></ul>
</td>
</tr>
<tr id="row1010913573268"><td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.1 "><p id="p810935742618"><a name="p810935742618"></a><a name="p810935742618"></a>是/否</p>
</td>
<td class="cellrowborder" valign="top" width="18.24182418241824%" headers="mcps1.2.4.1.2 "><p id="p12109165719267"><a name="p12109165719267"></a><a name="p12109165719267"></a>Windows或者Linux</p>
</td>
<td class="cellrowborder" valign="top" width="60.956095609560954%" headers="mcps1.2.4.1.3 "><p id="p6109757112613"><a name="p6109757112613"></a><a name="p6109757112613"></a>使用远程登录方式：<a href="Linux云服务器远程登录（VNC方式）.md">Linux云服务器远程登录（VNC方式）</a></p>
</td>
</tr>
</tbody>
</table>

