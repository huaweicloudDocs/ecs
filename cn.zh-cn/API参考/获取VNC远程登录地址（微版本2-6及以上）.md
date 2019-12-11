# 获取VNC远程登录地址（微版本2.6及以上）<a name="ZH-CN_TOPIC_0142763126"></a>

## 功能介绍<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section16588975"></a>

获取弹性云服务器VNC远程登录地址。

## URI<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section15083054"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/remote-consoles

参数说明请参见[表1](#zh-cn_topic_0092803065_table55945983)。

**表 1**  参数说明

<a name="zh-cn_topic_0092803065_table55945983"></a>
<table><thead align="left"><tr id="zh-cn_topic_0092803065_row11302482"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="43%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0092803065_row49888896"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0092803065_p14468758"><a name="zh-cn_topic_0092803065_p14468758"></a><a name="zh-cn_topic_0092803065_p14468758"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0092803065_p31118786"><a name="zh-cn_topic_0092803065_p31118786"></a><a name="zh-cn_topic_0092803065_p31118786"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0092803065_row613736410235"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0092803065_p2736446410235"><a name="zh-cn_topic_0092803065_p2736446410235"></a><a name="zh-cn_topic_0092803065_p2736446410235"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0092803065_p192907210235"><a name="zh-cn_topic_0092803065_p192907210235"></a><a name="zh-cn_topic_0092803065_p192907210235"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="43%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0092803065_p2203711610235"><a name="zh-cn_topic_0092803065_p2203711610235"></a><a name="zh-cn_topic_0092803065_p2203711610235"></a>弹性云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 接口约束<a name="zh-cn_topic_0092803065_section56676316111458"></a>

-   使用此接口时，请指定微版本不低于2.6。
-   获取的登录地址有效时间10min，超过10min请重新获取。

## 请求消息<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section56802184"></a>

**表 2**  请求参数

<a name="table2421133916364"></a>
<table><thead align="left"><tr id="row15425153973610"><th class="cellrowborder" valign="top" width="18.27817218278172%" id="mcps1.2.5.1.1"><p id="p1542663953616"><a name="p1542663953616"></a><a name="p1542663953616"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.268373162683734%" id="mcps1.2.5.1.2"><p id="p16512193593516"><a name="p16512193593516"></a><a name="p16512193593516"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.04829517048295%" id="mcps1.2.5.1.3"><p id="p11427173918366"><a name="p11427173918366"></a><a name="p11427173918366"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.40515948405159%" id="mcps1.2.5.1.4"><p id="p1842973903611"><a name="p1842973903611"></a><a name="p1842973903611"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row16430153914363"><td class="cellrowborder" valign="top" width="18.27817218278172%" headers="mcps1.2.5.1.1 "><p id="p498319273719"><a name="p498319273719"></a><a name="p498319273719"></a>remote_console</p>
</td>
<td class="cellrowborder" valign="top" width="16.268373162683734%" headers="mcps1.2.5.1.2 "><p id="p105121035103517"><a name="p105121035103517"></a><a name="p105121035103517"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.04829517048295%" headers="mcps1.2.5.1.3 "><p id="p898215212374"><a name="p898215212374"></a><a name="p898215212374"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48.40515948405159%" headers="mcps1.2.5.1.4 "><p id="p9978132133714"><a name="p9978132133714"></a><a name="p9978132133714"></a>弹性云服务器获取VNC远程登录地址。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  type参数信息

<a name="table19959184318164"></a>
<table><thead align="left"><tr id="row129653435167"><th class="cellrowborder" valign="top" width="18.17818218178182%" id="mcps1.2.5.1.1"><p id="p1296704318169"><a name="p1296704318169"></a><a name="p1296704318169"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.368363163683632%" id="mcps1.2.5.1.2"><p id="p1149238163514"><a name="p1149238163514"></a><a name="p1149238163514"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.04829517048295%" id="mcps1.2.5.1.3"><p id="p109701443181618"><a name="p109701443181618"></a><a name="p109701443181618"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.40515948405159%" id="mcps1.2.5.1.4"><p id="p597624311615"><a name="p597624311615"></a><a name="p597624311615"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row39781443181610"><td class="cellrowborder" valign="top" width="18.17818218178182%" headers="mcps1.2.5.1.1 "><p id="p10980144310164"><a name="p10980144310164"></a><a name="p10980144310164"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="16.368363163683632%" headers="mcps1.2.5.1.2 "><p id="p6149203820355"><a name="p6149203820355"></a><a name="p6149203820355"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.04829517048295%" headers="mcps1.2.5.1.3 "><p id="p189829437166"><a name="p189829437166"></a><a name="p189829437166"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.40515948405159%" headers="mcps1.2.5.1.4 "><p id="p1498612438166"><a name="p1498612438166"></a><a name="p1498612438166"></a>远程登录的类型，请将type配置为“novnc”。</p>
</td>
</tr>
<tr id="row11987144391610"><td class="cellrowborder" valign="top" width="18.17818218178182%" headers="mcps1.2.5.1.1 "><p id="p2098904311617"><a name="p2098904311617"></a><a name="p2098904311617"></a>protocol</p>
</td>
<td class="cellrowborder" valign="top" width="16.368363163683632%" headers="mcps1.2.5.1.2 "><p id="p614923863516"><a name="p614923863516"></a><a name="p614923863516"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.04829517048295%" headers="mcps1.2.5.1.3 "><p id="p599184312166"><a name="p599184312166"></a><a name="p599184312166"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.40515948405159%" headers="mcps1.2.5.1.4 "><p id="p599510433169"><a name="p599510433169"></a><a name="p599510433169"></a>远程登录协议，请将protocol配置为“vnc”。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section41457614"></a>

响应参数如[表4](#table8420447171011)所示。

**表 4**  响应参数

<a name="table8420447171011"></a>
<table><thead align="left"><tr id="row19425134710106"><th class="cellrowborder" valign="top" width="28.48%" id="mcps1.2.4.1.1"><p id="p1542644714106"><a name="p1542644714106"></a><a name="p1542644714106"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.63%" id="mcps1.2.4.1.2"><p id="p2426104761014"><a name="p2426104761014"></a><a name="p2426104761014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.89%" id="mcps1.2.4.1.3"><p id="p204289475101"><a name="p204289475101"></a><a name="p204289475101"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row20429447201017"><td class="cellrowborder" valign="top" width="28.48%" headers="mcps1.2.4.1.1 "><p id="p743019477102"><a name="p743019477102"></a><a name="p743019477102"></a>remote_console</p>
</td>
<td class="cellrowborder" valign="top" width="18.63%" headers="mcps1.2.4.1.2 "><p id="p343116478104"><a name="p343116478104"></a><a name="p343116478104"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="52.89%" headers="mcps1.2.4.1.3 "><p id="p44331647131017"><a name="p44331647131017"></a><a name="p44331647131017"></a>弹性云服务器获取远程登录地址。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  type参数信息

<a name="table12434194718104"></a>
<table><thead align="left"><tr id="row11437194781018"><th class="cellrowborder" valign="top" width="28.48%" id="mcps1.2.4.1.1"><p id="p10438104701020"><a name="p10438104701020"></a><a name="p10438104701020"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.63%" id="mcps1.2.4.1.2"><p id="p644124714100"><a name="p644124714100"></a><a name="p644124714100"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.89%" id="mcps1.2.4.1.3"><p id="p1044224771012"><a name="p1044224771012"></a><a name="p1044224771012"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row44421547151015"><td class="cellrowborder" valign="top" width="28.48%" headers="mcps1.2.4.1.1 "><p id="p16443114712101"><a name="p16443114712101"></a><a name="p16443114712101"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="18.63%" headers="mcps1.2.4.1.2 "><p id="p154442475107"><a name="p154442475107"></a><a name="p154442475107"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.89%" headers="mcps1.2.4.1.3 "><p id="p13445747131013"><a name="p13445747131013"></a><a name="p13445747131013"></a>远程登录的类型。</p>
</td>
</tr>
<tr id="row194475479107"><td class="cellrowborder" valign="top" width="28.48%" headers="mcps1.2.4.1.1 "><p id="p1044764712103"><a name="p1044764712103"></a><a name="p1044764712103"></a>protocol</p>
</td>
<td class="cellrowborder" valign="top" width="18.63%" headers="mcps1.2.4.1.2 "><p id="p20448447111014"><a name="p20448447111014"></a><a name="p20448447111014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.89%" headers="mcps1.2.4.1.3 "><p id="p64491447131016"><a name="p64491447131016"></a><a name="p64491447131016"></a>远程登录的协议。</p>
</td>
</tr>
<tr id="row112741544151614"><td class="cellrowborder" valign="top" width="28.48%" headers="mcps1.2.4.1.1 "><p id="p627404410168"><a name="p627404410168"></a><a name="p627404410168"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="18.63%" headers="mcps1.2.4.1.2 "><p id="p92741044141612"><a name="p92741044141612"></a><a name="p92741044141612"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.89%" headers="mcps1.2.4.1.3 "><p id="p10274544151617"><a name="p10274544151617"></a><a name="p10274544151617"></a>远程登录的url。</p>
<p id="p18426544113918"><a name="p18426544113918"></a><a name="p18426544113918"></a>该url有效时间10min，超过10min请重新获取。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section37574207"></a>

```
POST https://{endpoint}/v2.1/13c67a214ced4afb88d911ae4bd5721a/servers/47bc79ae-df61-4ade-9197-283a74e5d70e/remote-consoles
```

```
{
   "remote_console" : {
        "type" : "novnc",
        "protocol": "vnc"
    }
}
```

## 响应示例<a name="section1713910142558"></a>

```
{
	"remote_console": {
		"url": "https://nova-novncproxy.az21.dc1.domainname.com:8002/vnc.auto.html?token=80fa7c8d-37fe-451e-8b08-bfbd9fb6a4df&lang=EN",
		"type": "novnc",
		"protocol": "vnc"
	}
}
```

## 返回值<a name="zh-cn_topic_0092803065_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section23611955"></a>

请参考[错误码说明](错误码说明.md)。

