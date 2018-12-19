# 获取VNC远程登录地址（微版本2.5及以下）<a name="ZH-CN_TOPIC_0092906925"></a>

## 功能介绍<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section16588975"></a>

获取弹性云服务器VNC远程登录地址。

## URI<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section15083054"></a>

POST /v2/\{project\_id\}/servers/\{server\_id\}/action

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/action

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

该API将在微版本2.5后被废弃，使用此接口时，请指定微版本不高于2.5。

高于2.5版本请参考[获取VNC远程登录地址（微版本2.6及以上）](获取VNC远程登录地址（微版本2-6及以上）.md)。

## 请求消息<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section56802184"></a>

**请求参数**

请求参数如[表2](#zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_table44724688204850)所示。

**表 2**  请求参数

<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_table44724688204850"></a>
<table><thead align="left"><tr id="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_row1798761204850"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p39560242204918"><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p39560242204918"></a><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p39560242204918"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.35%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p50263001204918"><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p50263001204918"></a><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p50263001204918"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="12.22%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p44771301204918"><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p44771301204918"></a><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p44771301204918"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="46.43%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p2596798204918"><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p2596798204918"></a><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p2596798204918"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_row5848663204850"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0092803065_p38460826103157"><a name="zh-cn_topic_0092803065_p38460826103157"></a><a name="zh-cn_topic_0092803065_p38460826103157"></a>os-getVNCConsole</p>
</td>
<td class="cellrowborder" valign="top" width="16.35%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p1059631204933"><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p1059631204933"></a><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p1059631204933"></a>Dict</p>
</td>
<td class="cellrowborder" valign="top" width="12.22%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p18721296204933"><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p18721296204933"></a><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p18721296204933"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="46.43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p40030009204933"><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p40030009204933"></a><a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0058745339_p40030009204933"></a>弹性云服务器获取VNC远程登录地址。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  type参数信息

<a name="table16790921151610"></a>
<table><thead align="left"><tr id="row208009219163"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p19802521171618"><a name="p19802521171618"></a><a name="p19802521171618"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.35%" id="mcps1.2.5.1.2"><p id="p6804142171618"><a name="p6804142171618"></a><a name="p6804142171618"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="12.22%" id="mcps1.2.5.1.3"><p id="p1680642110166"><a name="p1680642110166"></a><a name="p1680642110166"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="46.43%" id="mcps1.2.5.1.4"><p id="p19808182161617"><a name="p19808182161617"></a><a name="p19808182161617"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row98101721201615"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p681432171617"><a name="p681432171617"></a><a name="p681432171617"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="16.35%" headers="mcps1.2.5.1.2 "><p id="p28155213162"><a name="p28155213162"></a><a name="p28155213162"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="12.22%" headers="mcps1.2.5.1.3 "><p id="p208187210164"><a name="p208187210164"></a><a name="p208187210164"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="46.43%" headers="mcps1.2.5.1.4 "><p id="p1081882101612"><a name="p1081882101612"></a><a name="p1081882101612"></a>获取对象，请将type配置为“novnc”。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section41457614"></a>

不涉及。

## 示例<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section37574207"></a>

-   请求示例

    ```
    POST /v2/9c53a566cb3443ab910cf0daebca90c4/servers/47e9be4e-a7b9-471f-92d9-ffc83814e07a/action
    POST /v2.1/9c53a566cb3443ab910cf0daebca90c4/servers/47e9be4e-a7b9-471f-92d9-ffc83814e07a/action
    {
       "os-getVNCConsole" : {
            "type" : "novnc"
        }
    }
    ```

-   响应示例

    ```
    {
        "console":{"url": "https://nova-novncproxy.az21.dc1.domainname.com:8002/vnc.auto.html?token=80fa7c8d-37fe-451e-8b08-bfbd9fb6a4df&lang=EN","type":"novnc"}
    }
    ```


## 返回值<a name="zh-cn_topic_0092803065_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="zh-cn_topic_0092803065_zh-cn_topic_0067161469_zh-cn_topic_0057973179_section23611955"></a>

请参考[错误码说明](错误码说明.md)。

