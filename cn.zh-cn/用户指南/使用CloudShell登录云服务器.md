# 使用CloudShell登录云服务器<a name="ZH-CN_TOPIC_0269825629"></a>

## 操作场景<a name="section193261132111117"></a>

本节为您介绍通过控制台提供的CloudShell登录云服务器的操作步骤。

登录成功后，如需使用CloudShell界面提供的复制、粘贴功能，请参见[CloudShell常用操作](#section1537822813216)。

## 前提条件<a name="section58260650112020"></a>

-   云服务器状态为“运行中”。

-   请确保安全组已开放登录端口，默认使用22端口，如需使用其他端口可登录云服务器后重新设置。

    修改远程登录端口请参考[修改远程登录端口](https://support.huaweicloud.com/ecs_faq/ecs_faq_0530.html)。配置安全组规则请参考[配置安全组规则](配置安全组规则.md)。

-   云服务器已绑定弹性公网IP。
-   如果在创建云服务器时未设置密码，请先重置密码后再登录云服务器。

## 操作步骤<a name="section1969153812313"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/icon-region.png)，选择区域和项目。
3.  选择“计算 \> 弹性云服务器”。
4.  选择要登录的云服务器，单击“操作”列下的“远程登录”。
5.  在弹出的“登录Linux云服务器”窗口中，单击“使用CloudShell登录”。
6.  在CloudShell界面配置云服务器信息。

    首次登录，默认会打开CloudShell配置向导。在CloudShell配置向导中输入云服务器的弹性公网IP、端口（默认22）、用户名和密码，单击“连接”登录云服务器。

    如果点击“连接”没有反应，可能是云服务器未设置登录密码或密码错误，请重置密码后重新登录。

    **图 1**  CloudShell配置向导<a name="fig85517479715"></a>  
    ![](figures/CloudShell配置向导.png "CloudShell配置向导")

7.  连接成功后，CloudShell界面提示如下。

    **图 2**  配置向导<a name="fig97321742133019"></a>  
    ![](figures/配置向导.png "配置向导")


## CloudShell常用操作<a name="section1537822813216"></a>

-   **新建远程终端**

    单击“远程终端 \> 新建远程终端”，即可用当前配置再打开一个终端。

-   **新建会话**

    选择“远程终端 \> 切换会话”，即可配置新的连接会话。

-   **快捷键**

    您可以使用快捷键编辑输入的命令。

    **表 1**  CloudShell快捷键

    <a name="table7625145793711"></a>
    <table><thead align="left"><tr id="row36251357193712"><th class="cellrowborder" valign="top" width="32.47%" id="mcps1.2.3.1.1"><p id="p06254579377"><a name="p06254579377"></a><a name="p06254579377"></a>快捷键</p>
    </th>
    <th class="cellrowborder" valign="top" width="67.53%" id="mcps1.2.3.1.2"><p id="p862516575376"><a name="p862516575376"></a><a name="p862516575376"></a>功能</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row4625195733713"><td class="cellrowborder" valign="top" width="32.47%" headers="mcps1.2.3.1.1 "><p id="p16625857173715"><a name="p16625857173715"></a><a name="p16625857173715"></a>Ctrl+L</p>
    </td>
    <td class="cellrowborder" valign="top" width="67.53%" headers="mcps1.2.3.1.2 "><p id="p176251457193714"><a name="p176251457193714"></a><a name="p176251457193714"></a>将当前行移到第一行</p>
    </td>
    </tr>
    <tr id="row06251575375"><td class="cellrowborder" valign="top" width="32.47%" headers="mcps1.2.3.1.1 "><p id="p362585714376"><a name="p362585714376"></a><a name="p362585714376"></a>Ctrl+U</p>
    </td>
    <td class="cellrowborder" valign="top" width="67.53%" headers="mcps1.2.3.1.2 "><p id="p962525713379"><a name="p962525713379"></a><a name="p962525713379"></a>清除当前行</p>
    </td>
    </tr>
    <tr id="row176251574376"><td class="cellrowborder" valign="top" width="32.47%" headers="mcps1.2.3.1.1 "><p id="p062515773716"><a name="p062515773716"></a><a name="p062515773716"></a>Ctrl+H</p>
    </td>
    <td class="cellrowborder" valign="top" width="67.53%" headers="mcps1.2.3.1.2 "><p id="p12625185719377"><a name="p12625185719377"></a><a name="p12625185719377"></a>向前删除一个字符</p>
    </td>
    </tr>
    <tr id="row136251557103717"><td class="cellrowborder" valign="top" width="32.47%" headers="mcps1.2.3.1.1 "><p id="p9625105710370"><a name="p9625105710370"></a><a name="p9625105710370"></a>Ctrl+A</p>
    </td>
    <td class="cellrowborder" valign="top" width="67.53%" headers="mcps1.2.3.1.2 "><p id="p862525753719"><a name="p862525753719"></a><a name="p862525753719"></a>光标移动到句首</p>
    </td>
    </tr>
    <tr id="row462525753711"><td class="cellrowborder" valign="top" width="32.47%" headers="mcps1.2.3.1.1 "><p id="p1625057123717"><a name="p1625057123717"></a><a name="p1625057123717"></a>Ctrl+E</p>
    </td>
    <td class="cellrowborder" valign="top" width="67.53%" headers="mcps1.2.3.1.2 "><p id="p26258578371"><a name="p26258578371"></a><a name="p26258578371"></a>光标移动到句末</p>
    </td>
    </tr>
    </tbody>
    </table>

-   **复制、粘贴**

    CloudShell支持直接在终端中进行复制粘贴。您既可以通过右键来复制粘贴，也可以直接用“Ctrl+C”、“Ctrl+V”等快捷键实现。

-   **浏览输出历史**

    对于跨屏内容，可以滚动终端查看历史输出。默认情况下，终端只会记录最近1000行输出，但是您可以在设置中修改这一值。

-   **多终端分区布局**

    您可以在同一个页面中创建多个CloudShell终端，并可以直接拖动窗口，随意组合成您喜欢的布局。


