# 查询指定API版本信息<a name="ecs_03_0102"></a>

## 功能介绍<a name="section553655182144"></a>

返回指定版本的信息。

为了支持功能不断扩展，Nova API支持版本号区分。Nova中有两种形式的版本号：

-   "主版本号": 具有独立的url。
-   "微版本号": 通过Http请求头X-OpenStack-Nova-API-Version来使用，从 2.27 版本开始支持新的微版本头：OpenStack-API-Version。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >如果使用OpenStack-API-Version的请求头，version对应的value取值格式为 compute 微版本号。
    >例如：key为OpenStack-API-Version的时候value需要填compute 2.27。

## 调试<a name="section926243314015"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=ECS&api=NovaShowVersion)中调试该接口。

## URI<a name="section961608182144"></a>

GET /\{api\_version\}

参数说明请参见[表1](#table46110007)。

**表 1**  参数说明

<a name="table46110007"></a>
<table><thead align="left"><tr id="row14148614"><th class="cellrowborder" valign="top" width="20.74%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.99%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.27%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17201924"><td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.1 "><p id="p51178607"><a name="p51178607"></a><a name="p51178607"></a>api_version</p>
</td>
<td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.2 "><p id="p51826478"><a name="p51826478"></a><a name="p51826478"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="59.27%" headers="mcps1.2.4.1.3 "><p id="p37195178"><a name="p37195178"></a><a name="p37195178"></a>API版本号。例如: v2</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section108201017144216"></a>

无

## 响应消息<a name="section89511024194216"></a>

响应参数如表2所示。

**表 2**  响应参数

<a name="table1456520231001"></a>
<table><thead align="left"><tr id="row25656239015"><th class="cellrowborder" valign="top" width="21.69216921692169%" id="mcps1.2.4.1.1"><p id="p45658231201"><a name="p45658231201"></a><a name="p45658231201"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.14211421142114%" id="mcps1.2.4.1.2"><p id="p125655231308"><a name="p125655231308"></a><a name="p125655231308"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="57.165716571657164%" id="mcps1.2.4.1.3"><p id="p056515231709"><a name="p056515231709"></a><a name="p056515231709"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row456582314010"><td class="cellrowborder" valign="top" width="21.69216921692169%" headers="mcps1.2.4.1.1 "><p id="p115651723008"><a name="p115651723008"></a><a name="p115651723008"></a>versions</p>
</td>
<td class="cellrowborder" valign="top" width="21.14211421142114%" headers="mcps1.2.4.1.2 "><p id="p8565122310019"><a name="p8565122310019"></a><a name="p8565122310019"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="57.165716571657164%" headers="mcps1.2.4.1.3 "><p id="p125121301517"><a name="p125121301517"></a><a name="p125121301517"></a>指定版本信息，详情请参见<a href="#table1970522313484">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  versions字段数据结构说明

<a name="table1970522313484"></a>
<table><thead align="left"><tr id="row11705723114815"><th class="cellrowborder" valign="top" width="22.132213221322132%" id="mcps1.2.4.1.1"><p id="p770515232485"><a name="p770515232485"></a><a name="p770515232485"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.8020802080208%" id="mcps1.2.4.1.2"><p id="p177051223184810"><a name="p177051223184810"></a><a name="p177051223184810"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="57.065706570657056%" id="mcps1.2.4.1.3"><p id="p7705112374819"><a name="p7705112374819"></a><a name="p7705112374819"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row127051723154815"><td class="cellrowborder" valign="top" width="22.132213221322132%" headers="mcps1.2.4.1.1 "><p id="p155331243134911"><a name="p155331243134911"></a><a name="p155331243134911"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.2 "><p id="p17051623154814"><a name="p17051623154814"></a><a name="p17051623154814"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="57.065706570657056%" headers="mcps1.2.4.1.3 "><p id="p6251730155117"><a name="p6251730155117"></a><a name="p6251730155117"></a>所讨论的版本的通用名称。仅仅是信息性的，它没有真正的语义。</p>
</td>
</tr>
<tr id="row13161133211483"><td class="cellrowborder" valign="top" width="22.132213221322132%" headers="mcps1.2.4.1.1 "><p id="p20162193264816"><a name="p20162193264816"></a><a name="p20162193264816"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.2 "><p id="p101624324488"><a name="p101624324488"></a><a name="p101624324488"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="57.065706570657056%" headers="mcps1.2.4.1.3 "><p id="p168341639155116"><a name="p168341639155116"></a><a name="p168341639155116"></a>链接到资源的问题。有关更多信息，请参见<a href="https://developer.openstack.org/api-guide/compute/links_and_references.html" target="_blank" rel="noopener noreferrer">OpenStack Documentation</a>。</p>
<p id="p97381735319"><a name="p97381735319"></a><a name="p97381735319"></a>详情请参见<a href="#table1586318199718">表4</a>。</p>
</td>
</tr>
<tr id="row161541434114814"><td class="cellrowborder" valign="top" width="22.132213221322132%" headers="mcps1.2.4.1.1 "><p id="p61541434154814"><a name="p61541434154814"></a><a name="p61541434154814"></a>media-types</p>
</td>
<td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.2 "><p id="p14154153424815"><a name="p14154153424815"></a><a name="p14154153424815"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="57.065706570657056%" headers="mcps1.2.4.1.3 "><p id="p15390144665112"><a name="p15390144665112"></a><a name="p15390144665112"></a>媒体类型。详情请参见<a href="#table1242753025619">表5</a>。</p>
</td>
</tr>
<tr id="row1866313454811"><td class="cellrowborder" valign="top" width="22.132213221322132%" headers="mcps1.2.4.1.1 "><p id="p2663734104815"><a name="p2663734104815"></a><a name="p2663734104815"></a>min_version</p>
</td>
<td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.2 "><p id="p666313345481"><a name="p666313345481"></a><a name="p666313345481"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="57.065706570657056%" headers="mcps1.2.4.1.3 "><a name="ul343720140818"></a><a name="ul343720140818"></a><ul id="ul343720140818"><li>如果API的这个版本支持微版本，则支持最小的微版本。</li><li>如果不支持微版本，这将是空字符串。</li></ul>
</td>
</tr>
<tr id="row1178133544820"><td class="cellrowborder" valign="top" width="22.132213221322132%" headers="mcps1.2.4.1.1 "><p id="p157810358483"><a name="p157810358483"></a><a name="p157810358483"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.2 "><p id="p1578143511481"><a name="p1578143511481"></a><a name="p1578143511481"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="57.065706570657056%" headers="mcps1.2.4.1.3 "><p id="p18269115975114"><a name="p18269115975114"></a><a name="p18269115975114"></a>API版本的状态：</p>
<a name="ul5520141712813"></a><a name="ul5520141712813"></a><ul id="ul5520141712813"><li>CURRENT这是使用的API的首选版本；</li><li>SUPPORTED：这是一个较老的，但仍然支持的API版本；</li><li>DEPRECATED：一个被废弃的API版本，该版本将被删除</li></ul>
</td>
</tr>
<tr id="row18470235174818"><td class="cellrowborder" valign="top" width="22.132213221322132%" headers="mcps1.2.4.1.1 "><p id="p1947063511481"><a name="p1947063511481"></a><a name="p1947063511481"></a>updated</p>
</td>
<td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.2 "><p id="p147033519489"><a name="p147033519489"></a><a name="p147033519489"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="57.065706570657056%" headers="mcps1.2.4.1.3 "><p id="p13546378525"><a name="p13546378525"></a><a name="p13546378525"></a>一个有特定值的字符串。API版本为2.0时，值为2011-01-21T11:33:21Z ，API版本是2.1时，值为2013-07-23T11:33:21Z。</p>
</td>
</tr>
<tr id="row57011535174817"><td class="cellrowborder" valign="top" width="22.132213221322132%" headers="mcps1.2.4.1.1 "><p id="p6702113515482"><a name="p6702113515482"></a><a name="p6702113515482"></a>version</p>
</td>
<td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.2 "><p id="p2070273594817"><a name="p2070273594817"></a><a name="p2070273594817"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="57.065706570657056%" headers="mcps1.2.4.1.3 "><a name="ul81689446815"></a><a name="ul81689446815"></a><ul id="ul81689446815"><li>如果API的这个版本支持微版本，则支持最大的微版本。</li><li>如果不支持微版本，这将是空字符串。</li></ul>
</td>
</tr>
</tbody>
</table>

**表 4**  links字段数据结构说明

<a name="table1586318199718"></a>
<table><thead align="left"><tr id="row19863719071"><th class="cellrowborder" valign="top" width="22.132213221322132%" id="mcps1.2.4.1.1"><p id="p38643193712"><a name="p38643193712"></a><a name="p38643193712"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.8020802080208%" id="mcps1.2.4.1.2"><p id="p1186420191678"><a name="p1186420191678"></a><a name="p1186420191678"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="57.065706570657056%" id="mcps1.2.4.1.3"><p id="p118647191972"><a name="p118647191972"></a><a name="p118647191972"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1886419192713"><td class="cellrowborder" valign="top" width="22.132213221322132%" headers="mcps1.2.4.1.1 "><p id="p48646193713"><a name="p48646193713"></a><a name="p48646193713"></a>href</p>
</td>
<td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.2 "><p id="p786471915713"><a name="p786471915713"></a><a name="p786471915713"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="57.065706570657056%" headers="mcps1.2.4.1.3 "><p id="p55689555719"><a name="p55689555719"></a><a name="p55689555719"></a>相应资源的链接。</p>
</td>
</tr>
<tr id="row178649191472"><td class="cellrowborder" valign="top" width="22.132213221322132%" headers="mcps1.2.4.1.1 "><p id="p386411192074"><a name="p386411192074"></a><a name="p386411192074"></a>rel</p>
</td>
<td class="cellrowborder" valign="top" width="20.8020802080208%" headers="mcps1.2.4.1.2 "><p id="p68646190716"><a name="p68646190716"></a><a name="p68646190716"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="57.065706570657056%" headers="mcps1.2.4.1.3 "><a name="ul06311647387"></a><a name="ul06311647387"></a><ul id="ul06311647387"><li>self：自助链接包含版本链接的资源。立即链接后使用这些链接。</li><li>bookmark：书签链接提供了一个永久资源的永久链接，该链接适合于长期存储。</li><li>alternate：备用链接可以包含资源的替换表示形式。例如，OpenStack计算映像可能在OpenStack映像服务中有一个替代表示。</li></ul>
</td>
</tr>
</tbody>
</table>

**表 5**  media-types字段数据结构说明

<a name="table1242753025619"></a>
<table><thead align="left"><tr id="row342713010569"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p44276309569"><a name="p44276309569"></a><a name="p44276309569"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p04277305564"><a name="p04277305564"></a><a name="p04277305564"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p14427153011563"><a name="p14427153011563"></a><a name="p14427153011563"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1342719303565"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p742733065617"><a name="p742733065617"></a><a name="p742733065617"></a>base</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p4427193017566"><a name="p4427193017566"></a><a name="p4427193017566"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p9874125215560"><a name="p9874125215560"></a><a name="p9874125215560"></a>基础类型。</p>
</td>
</tr>
<tr id="row44271330135612"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p742753019564"><a name="p742753019564"></a><a name="p742753019564"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p1142743085619"><a name="p1142743085619"></a><a name="p1142743085619"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p13427113095613"><a name="p13427113095613"></a><a name="p13427113095613"></a>媒体类型。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section19667838182144"></a>

查询指定API的版本信息。

```
GET https://{endpoint}/v2.1
```

## 响应示例<a name="section20327115469"></a>

```
{
    "version":{
        "min_version":"2.1",
        "media-types":[
            {
                "type":"application/vnd.openstack.compute+json;version=2.1",
                "base":"application/json"
            }
        ],
        "links":[
            {
                "rel":"self",
                "href":"https://{endpoint}/v2.1/"
            },
            {
                "rel":"describedby",
                "href":"http://docs.openstack.org/",
                "type":"text/html"
            }
        ],
        "id":"v2.1",
        "updated":"2013-07-23T11:33:21Z",
        "version":"2.60",
        "status":"CURRENT"
    }
}
```

## 返回值<a name="section12571834"></a>

请参考[通用请求返回值](通用请求返回值.md)。

