# 使用FTP上传或下载文件<a name="ZH-CN_TOPIC_0140323160"></a>

-   场景举例：

    如果您需要使用FTP软件向弹性云服务器上传或下载文件，您需要添加安全组规则。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >您需要在弹性云服务器上先安装FTP服务器程序，再查看20、21端口是否正常工作。安装FTP服务器的操作请参见[搭建FTP站点（Windows）](https://support.huaweicloud.com/bestpractice-ecs/zh-cn_topic_0109733866.html)、[搭建FTP站点（Linux）](https://support.huaweicloud.com/bestpractice-ecs/zh-cn_topic_0115828034.html)。  

-   安全组配置方法：

    <a name="zh-cn_topic_0118534019_table8479153013395"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0118534019_row1518203013392"><th class="cellrowborder" valign="top" width="28.57%" id="mcps1.1.5.1.1"><p id="zh-cn_topic_0118534019_p1651819306397"><a name="zh-cn_topic_0118534019_p1651819306397"></a><a name="zh-cn_topic_0118534019_p1651819306397"></a>协议</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.349999999999998%" id="mcps1.1.5.1.2"><p id="zh-cn_topic_0118534019_p13518730193918"><a name="zh-cn_topic_0118534019_p13518730193918"></a><a name="zh-cn_topic_0118534019_p13518730193918"></a>方向</p>
    </th>
    <th class="cellrowborder" valign="top" width="28.57%" id="mcps1.1.5.1.3"><p id="zh-cn_topic_0118534019_p175183303395"><a name="zh-cn_topic_0118534019_p175183303395"></a><a name="zh-cn_topic_0118534019_p175183303395"></a>端口范围</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.509999999999998%" id="mcps1.1.5.1.4"><p id="zh-cn_topic_0118534019_p3518163053913"><a name="zh-cn_topic_0118534019_p3518163053913"></a><a name="zh-cn_topic_0118534019_p3518163053913"></a>源地址</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0118534019_row4519143013399"><td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0118534019_p10519113063920"><a name="zh-cn_topic_0118534019_p10519113063920"></a><a name="zh-cn_topic_0118534019_p10519113063920"></a>FTP</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.349999999999998%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0118534019_p13519123013393"><a name="zh-cn_topic_0118534019_p13519123013393"></a><a name="zh-cn_topic_0118534019_p13519123013393"></a>入方向</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.57%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0118534019_p5519930193917"><a name="zh-cn_topic_0118534019_p5519930193917"></a><a name="zh-cn_topic_0118534019_p5519930193917"></a>20-21</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.509999999999998%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0118534019_p13519630123910"><a name="zh-cn_topic_0118534019_p13519630123910"></a><a name="zh-cn_topic_0118534019_p13519630123910"></a>0.0.0.0/0</p>
    </td>
    </tr>
    </tbody>
    </table>


