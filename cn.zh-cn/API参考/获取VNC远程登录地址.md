# 获取VNC远程登录地址<a name="ecs_02_0208"></a>

## 功能介绍<a name="zh-cn_topic_0092803065_ecs_03_0601_zh-cn_topic_0057973179_section16588975"></a>

获取弹性云服务器VNC远程登录地址。

## 调试<a name="section926243314015"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=ECS&api=ShowServerRemoteConsole)中调试该接口。

## URI<a name="zh-cn_topic_0092803065_ecs_03_0601_zh-cn_topic_0057973179_section15083054"></a>

POST /v1/\{project\_id\}/cloudservers/\{server\_id\}/remote\_console

参数说明请参见[表1](#zh-cn_topic_0092803065_table55945983)。

**表 1**  参数说明

<a name="zh-cn_topic_0092803065_table55945983"></a>
<table><thead align="left"><tr id="zh-cn_topic_0092803065_row11302482"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0092803065_p43085863"><a name="zh-cn_topic_0092803065_p43085863"></a><a name="zh-cn_topic_0092803065_p43085863"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="32%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0092803065_p294000"><a name="zh-cn_topic_0092803065_p294000"></a><a name="zh-cn_topic_0092803065_p294000"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="35%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0092803065_p23814038"><a name="zh-cn_topic_0092803065_p23814038"></a><a name="zh-cn_topic_0092803065_p23814038"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0092803065_row49888896"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0092803065_p14468758"><a name="zh-cn_topic_0092803065_p14468758"></a><a name="zh-cn_topic_0092803065_p14468758"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0092803065_p31118786"><a name="zh-cn_topic_0092803065_p31118786"></a><a name="zh-cn_topic_0092803065_p31118786"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0092803065_row613736410235"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0092803065_p2736446410235"><a name="zh-cn_topic_0092803065_p2736446410235"></a><a name="zh-cn_topic_0092803065_p2736446410235"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0092803065_p192907210235"><a name="zh-cn_topic_0092803065_p192907210235"></a><a name="zh-cn_topic_0092803065_p192907210235"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="35%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0092803065_p2203711610235"><a name="zh-cn_topic_0092803065_p2203711610235"></a><a name="zh-cn_topic_0092803065_p2203711610235"></a><span id="text12901157172414"><a name="text12901157172414"></a><a name="text12901157172414"></a>云服务器</span>ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0092803065_ecs_03_0601_zh-cn_topic_0057973179_section56802184"></a>

**请求参数**

请求参数如[表2](#table1559505991313)所示。

**表 2**  请求参数

<a name="table1559505991313"></a>
<table><thead align="left"><tr id="row14595959131317"><th class="cellrowborder" valign="top" width="20.4%" id="mcps1.2.5.1.1"><p id="p1747519171416"><a name="p1747519171416"></a><a name="p1747519171416"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.28%" id="mcps1.2.5.1.2"><p id="p2747181919149"><a name="p2747181919149"></a><a name="p2747181919149"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.52%" id="mcps1.2.5.1.3"><p id="p1574712199145"><a name="p1574712199145"></a><a name="p1574712199145"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.8%" id="mcps1.2.5.1.4"><p id="p17477195149"><a name="p17477195149"></a><a name="p17477195149"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1459518594134"><td class="cellrowborder" valign="top" width="20.4%" headers="mcps1.2.5.1.1 "><p id="p174711919148"><a name="p174711919148"></a><a name="p174711919148"></a>remote_console</p>
</td>
<td class="cellrowborder" valign="top" width="13.28%" headers="mcps1.2.5.1.2 "><p id="p15747151971419"><a name="p15747151971419"></a><a name="p15747151971419"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.52%" headers="mcps1.2.5.1.3 "><p id="p18747161919147"><a name="p18747161919147"></a><a name="p18747161919147"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48.8%" headers="mcps1.2.5.1.4 "><p id="p16747191918144"><a name="p16747191918144"></a><a name="p16747191918144"></a>弹性云服务器获取远程登录地址，详情见<a href="#zh-cn_topic_0092803065_table47368008105952">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  remote\_console参数信息

<a name="zh-cn_topic_0092803065_table47368008105952"></a>
<table><thead align="left"><tr id="zh-cn_topic_0092803065_row53555469105952"><th class="cellrowborder" valign="top" width="22.577742225777424%" id="mcps1.2.5.1.1"><p id="p1826194311472"><a name="p1826194311472"></a><a name="p1826194311472"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.968803119688031%" id="mcps1.2.5.1.2"><p id="p1247593616353"><a name="p1247593616353"></a><a name="p1247593616353"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.04829517048295%" id="mcps1.2.5.1.3"><p id="p1926117436472"><a name="p1926117436472"></a><a name="p1926117436472"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.40515948405159%" id="mcps1.2.5.1.4"><p id="p72618434479"><a name="p72618434479"></a><a name="p72618434479"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0092803065_row23505526105952"><td class="cellrowborder" valign="top" width="22.577742225777424%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0092803065_p24899443105952"><a name="zh-cn_topic_0092803065_p24899443105952"></a><a name="zh-cn_topic_0092803065_p24899443105952"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="11.968803119688031%" headers="mcps1.2.5.1.2 "><p id="p747523613355"><a name="p747523613355"></a><a name="p747523613355"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.04829517048295%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0092803065_p3588984105952"><a name="zh-cn_topic_0092803065_p3588984105952"></a><a name="zh-cn_topic_0092803065_p3588984105952"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.40515948405159%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0092803065_p59226044105952"><a name="zh-cn_topic_0092803065_p59226044105952"></a><a name="zh-cn_topic_0092803065_p59226044105952"></a>远程登录的类型，请将type配置为“novnc”。</p>
</td>
</tr>
<tr id="row03959196408"><td class="cellrowborder" valign="top" width="22.577742225777424%" headers="mcps1.2.5.1.1 "><p id="p193963199407"><a name="p193963199407"></a><a name="p193963199407"></a>protocol</p>
</td>
<td class="cellrowborder" valign="top" width="11.968803119688031%" headers="mcps1.2.5.1.2 "><p id="p1847518369351"><a name="p1847518369351"></a><a name="p1847518369351"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.04829517048295%" headers="mcps1.2.5.1.3 "><p id="p16396171994014"><a name="p16396171994014"></a><a name="p16396171994014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.40515948405159%" headers="mcps1.2.5.1.4 "><p id="p103961419184018"><a name="p103961419184018"></a><a name="p103961419184018"></a>远程登录协议，请将protocol配置为“vnc”。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0092803065_ecs_03_0601_zh-cn_topic_0057973179_section41457614"></a>

**响应参数**

响应参数如[表4](#table8420447171011)所示。

**表 4**  响应参数

<a name="table8420447171011"></a>
<table><thead align="left"><tr id="row19425134710106"><th class="cellrowborder" valign="top" width="28.48%" id="mcps1.2.4.1.1"><p id="p1542644714106"><a name="p1542644714106"></a><a name="p1542644714106"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.63%" id="mcps1.2.4.1.2"><p id="p2426104761014"><a name="p2426104761014"></a><a name="p2426104761014"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.89%" id="mcps1.2.4.1.3"><p id="p204289475101"><a name="p204289475101"></a><a name="p204289475101"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row20429447201017"><td class="cellrowborder" valign="top" width="28.48%" headers="mcps1.2.4.1.1 "><p id="p743019477102"><a name="p743019477102"></a><a name="p743019477102"></a>remote_console</p>
</td>
<td class="cellrowborder" valign="top" width="18.63%" headers="mcps1.2.4.1.2 "><p id="p343116478104"><a name="p343116478104"></a><a name="p343116478104"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="52.89%" headers="mcps1.2.4.1.3 "><p id="p44331647131017"><a name="p44331647131017"></a><a name="p44331647131017"></a>弹性云服务器获取远程登录地址，详情参见<a href="#table12434194718104">表5</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  remote\_console数据结构说明

<a name="table12434194718104"></a>
<table><thead align="left"><tr id="row11437194781018"><th class="cellrowborder" valign="top" width="28.48%" id="mcps1.2.4.1.1"><p id="p10438104701020"><a name="p10438104701020"></a><a name="p10438104701020"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.63%" id="mcps1.2.4.1.2"><p id="p644124714100"><a name="p644124714100"></a><a name="p644124714100"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.89%" id="mcps1.2.4.1.3"><p id="p1044224771012"><a name="p1044224771012"></a><a name="p1044224771012"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row44421547151015"><td class="cellrowborder" valign="top" width="28.48%" headers="mcps1.2.4.1.1 "><p id="p16443114712101"><a name="p16443114712101"></a><a name="p16443114712101"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="18.63%" headers="mcps1.2.4.1.2 "><p id="p154442475107"><a name="p154442475107"></a><a name="p154442475107"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.89%" headers="mcps1.2.4.1.3 "><p id="p13445747131013"><a name="p13445747131013"></a><a name="p13445747131013"></a>远程登录的类型</p>
</td>
</tr>
<tr id="row194475479107"><td class="cellrowborder" valign="top" width="28.48%" headers="mcps1.2.4.1.1 "><p id="p1044764712103"><a name="p1044764712103"></a><a name="p1044764712103"></a>protocol</p>
</td>
<td class="cellrowborder" valign="top" width="18.63%" headers="mcps1.2.4.1.2 "><p id="p20448447111014"><a name="p20448447111014"></a><a name="p20448447111014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.89%" headers="mcps1.2.4.1.3 "><p id="p64491447131016"><a name="p64491447131016"></a><a name="p64491447131016"></a>远程登录的协议</p>
</td>
</tr>
<tr id="row112741544151614"><td class="cellrowborder" valign="top" width="28.48%" headers="mcps1.2.4.1.1 "><p id="p627404410168"><a name="p627404410168"></a><a name="p627404410168"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="18.63%" headers="mcps1.2.4.1.2 "><p id="p92741044141612"><a name="p92741044141612"></a><a name="p92741044141612"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.89%" headers="mcps1.2.4.1.3 "><p id="p10274544151617"><a name="p10274544151617"></a><a name="p10274544151617"></a>远程登录的url</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0092803065_ecs_03_0601_zh-cn_topic_0057973179_section37574207"></a>

```
POST https://{endpoint}/v1/13c67a214ced4afb88d911ae4bd5721a/cloudservers/47bc79ae-df61-4ade-9197-283a74e5d70e/remote_console
```

```
{
    "remote_console": {
        "protocol": "vnc",
        "type": "novnc"
    }
}
```

## 响应示例<a name="section1671118351481"></a>

```
{
   "remote_console": {
        "type": "novnc",
        "protocol": "vnc",
        "url": "https://nova-novncproxy.az1.dc1.domainname.com:8002/vnc_auto.html?token=0fda3eca-8232-4249-a69f-44ce8ab31be6&lang=EN&tLength=70"
    }
}
```

## 返回值<a name="zh-cn_topic_0092803065_ecs_03_0202_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="zh-cn_topic_0092803065_ecs_03_0601_zh-cn_topic_0057973179_section23611955"></a>

请参考[错误码](错误码.md)。

