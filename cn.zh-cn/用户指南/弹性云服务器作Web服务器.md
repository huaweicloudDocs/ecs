# 弹性云服务器作Web服务器<a name="ZH-CN_TOPIC_0140323158"></a>

-   场景举例：

    如果您在弹性云服务器上部署了网站，即弹性云服务器作Web服务器用，希望用户能通过HTTP或HTTPS服务访问到您的网站，您需要在弹性云服务器所在安全组中添加以下安全组规则。

-   安全组配置方法：

    <a name="zh-cn_topic_0118534017_table30323767195135"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0118534017_row15770184195135"><th class="cellrowborder" valign="top" width="28.93%" id="mcps1.1.5.1.1"><p id="zh-cn_topic_0118534017_p2316559195135"><a name="zh-cn_topic_0118534017_p2316559195135"></a><a name="zh-cn_topic_0118534017_p2316559195135"></a>协议</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.27%" id="mcps1.1.5.1.2"><p id="zh-cn_topic_0118534017_p53423553195135"><a name="zh-cn_topic_0118534017_p53423553195135"></a><a name="zh-cn_topic_0118534017_p53423553195135"></a>方向</p>
    </th>
    <th class="cellrowborder" valign="top" width="28.349999999999998%" id="mcps1.1.5.1.3"><p id="zh-cn_topic_0118534017_p32340552195135"><a name="zh-cn_topic_0118534017_p32340552195135"></a><a name="zh-cn_topic_0118534017_p32340552195135"></a>端口范围</p>
    </th>
    <th class="cellrowborder" valign="top" width="25.45%" id="mcps1.1.5.1.4"><p id="zh-cn_topic_0118534017_p2339084195135"><a name="zh-cn_topic_0118534017_p2339084195135"></a><a name="zh-cn_topic_0118534017_p2339084195135"></a>源地址</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0118534017_row55248116195135"><td class="cellrowborder" valign="top" width="28.93%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0118534017_p45912425195135"><a name="zh-cn_topic_0118534017_p45912425195135"></a><a name="zh-cn_topic_0118534017_p45912425195135"></a>TCP</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.27%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0118534017_p27918930195135"><a name="zh-cn_topic_0118534017_p27918930195135"></a><a name="zh-cn_topic_0118534017_p27918930195135"></a>入方向</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.349999999999998%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0118534017_p46840856195135"><a name="zh-cn_topic_0118534017_p46840856195135"></a><a name="zh-cn_topic_0118534017_p46840856195135"></a>80（HTTP）</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.45%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0118534017_p36012962195135"><a name="zh-cn_topic_0118534017_p36012962195135"></a><a name="zh-cn_topic_0118534017_p36012962195135"></a>0.0.0.0/0</p>
    </td>
    </tr>
    <tr id="zh-cn_topic_0118534017_row5566305020026"><td class="cellrowborder" valign="top" width="28.93%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0118534017_p3120540920026"><a name="zh-cn_topic_0118534017_p3120540920026"></a><a name="zh-cn_topic_0118534017_p3120540920026"></a>TCP</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.27%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0118534017_p4461017620026"><a name="zh-cn_topic_0118534017_p4461017620026"></a><a name="zh-cn_topic_0118534017_p4461017620026"></a>入方向</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.349999999999998%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0118534017_p5665449220026"><a name="zh-cn_topic_0118534017_p5665449220026"></a><a name="zh-cn_topic_0118534017_p5665449220026"></a>443（HTTPS）</p>
    </td>
    <td class="cellrowborder" valign="top" width="25.45%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0118534017_p2561110020026"><a name="zh-cn_topic_0118534017_p2561110020026"></a><a name="zh-cn_topic_0118534017_p2561110020026"></a>0.0.0.0/0</p>
    </td>
    </tr>
    </tbody>
    </table>


