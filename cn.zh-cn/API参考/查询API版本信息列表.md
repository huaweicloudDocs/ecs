# 查询API版本信息列表<a name="ecs_03_0101"></a>

## 功能介绍<a name="section54478915181842"></a>

返回Nova当前所有可用的版本。

为了支持功能不断扩展，Nova API支持版本号区分。Nova中有两种形式的版本号：

-   "主版本号": 具有独立的url。
-   "微版本号": 通过Http请求头X-OpenStack-Nova-API-Version来使用，从 2.27 版本开始支持新的微版本头：OpenStack-API-Version。

## URI<a name="section53791107181842"></a>

GET /

## 请求消息<a name="section108201017144216"></a>

无

## 响应消息<a name="section89511024194216"></a>

响应参数如表1所示。

**表 1**  响应参数

<a name="table1456520231001"></a>
<table><thead align="left"><tr id="row25656239015"><th class="cellrowborder" valign="top" width="23.54235423542354%" id="mcps1.2.4.1.1"><p id="p45658231201"><a name="p45658231201"></a><a name="p45658231201"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.772477247724773%" id="mcps1.2.4.1.2"><p id="p125655231308"><a name="p125655231308"></a><a name="p125655231308"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="51.68516851685169%" id="mcps1.2.4.1.3"><p id="p056515231709"><a name="p056515231709"></a><a name="p056515231709"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row456582314010"><td class="cellrowborder" valign="top" width="23.54235423542354%" headers="mcps1.2.4.1.1 "><p id="p115651723008"><a name="p115651723008"></a><a name="p115651723008"></a>versions</p>
</td>
<td class="cellrowborder" valign="top" width="24.772477247724773%" headers="mcps1.2.4.1.2 "><p id="p8565122310019"><a name="p8565122310019"></a><a name="p8565122310019"></a><span>Object</span></p>
</td>
<td class="cellrowborder" valign="top" width="51.68516851685169%" headers="mcps1.2.4.1.3 "><p id="p125121301517"><a name="p125121301517"></a><a name="p125121301517"></a>API版本信息列表，详情请参见<a href="#table16114143917">表2</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  versions字段数据结构说明

<a name="table16114143917"></a>
<table><thead align="left"><tr id="row511412437116"><th class="cellrowborder" valign="top" width="23.32233223322332%" id="mcps1.2.4.1.1"><p id="p311454313119"><a name="p311454313119"></a><a name="p311454313119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.782478247824784%" id="mcps1.2.4.1.2"><p id="p91141643018"><a name="p91141643018"></a><a name="p91141643018"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="51.8951895189519%" id="mcps1.2.4.1.3"><p id="p181143437120"><a name="p181143437120"></a><a name="p181143437120"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row411414312112"><td class="cellrowborder" valign="top" width="23.32233223322332%" headers="mcps1.2.4.1.1 "><p id="p8114943715"><a name="p8114943715"></a><a name="p8114943715"></a><span>id</span></p>
</td>
<td class="cellrowborder" valign="top" width="24.782478247824784%" headers="mcps1.2.4.1.2 "><p id="p21141343213"><a name="p21141343213"></a><a name="p21141343213"></a><span>string</span></p>
</td>
<td class="cellrowborder" valign="top" width="51.8951895189519%" headers="mcps1.2.4.1.3 "><p id="p1260613411515"><a name="p1260613411515"></a><a name="p1260613411515"></a>所讨论的版本的通用名称，仅仅是信息性的，它没有真正的语义。</p>
</td>
</tr>
<tr id="row477413141835"><td class="cellrowborder" valign="top" width="23.32233223322332%" headers="mcps1.2.4.1.1 "><p id="p167749141234"><a name="p167749141234"></a><a name="p167749141234"></a><span>links</span></p>
</td>
<td class="cellrowborder" valign="top" width="24.782478247824784%" headers="mcps1.2.4.1.2 "><p id="p117741414039"><a name="p117741414039"></a><a name="p117741414039"></a><span>Object</span></p>
</td>
<td class="cellrowborder" valign="top" width="51.8951895189519%" headers="mcps1.2.4.1.3 "><p id="p65342421414"><a name="p65342421414"></a><a name="p65342421414"></a>版本相关标记快捷链接信息，详情请参见<a href="#table1586318199718">表3</a>。</p>
</td>
</tr>
<tr id="row4774151417318"><td class="cellrowborder" valign="top" width="23.32233223322332%" headers="mcps1.2.4.1.1 "><p id="p077414142318"><a name="p077414142318"></a><a name="p077414142318"></a><span>min_version</span></p>
</td>
<td class="cellrowborder" valign="top" width="24.782478247824784%" headers="mcps1.2.4.1.2 "><p id="p137741814033"><a name="p137741814033"></a><a name="p137741814033"></a><span>string</span></p>
</td>
<td class="cellrowborder" valign="top" width="51.8951895189519%" headers="mcps1.2.4.1.3 "><a name="ul46761225713"></a><a name="ul46761225713"></a><ul id="ul46761225713"><li>如果API的这个版本支持微版本，则支持最小的微版本。</li><li>如果不支持微版本，这将是空字符串。</li></ul>
</td>
</tr>
<tr id="row107969153318"><td class="cellrowborder" valign="top" width="23.32233223322332%" headers="mcps1.2.4.1.1 "><p id="p17961015939"><a name="p17961015939"></a><a name="p17961015939"></a><span>status</span></p>
</td>
<td class="cellrowborder" valign="top" width="24.782478247824784%" headers="mcps1.2.4.1.2 "><p id="p1579713151538"><a name="p1579713151538"></a><a name="p1579713151538"></a><span>string</span></p>
</td>
<td class="cellrowborder" valign="top" width="51.8951895189519%" headers="mcps1.2.4.1.3 "><p id="p8717131862"><a name="p8717131862"></a><a name="p8717131862"></a>API版本的状态。</p>
<a name="ul6651646766"></a><a name="ul6651646766"></a><ul id="ul6651646766"><li>CURRENT，这是使用的API的首选版本</li><li>SUPPORTED，这是一个较老的，但仍然支持的API版本。</li><li>DEPRECATED，一个被废弃的API版本，该版本将被删除。</li></ul>
</td>
</tr>
<tr id="row1449716334"><td class="cellrowborder" valign="top" width="23.32233223322332%" headers="mcps1.2.4.1.1 "><p id="p144918166312"><a name="p144918166312"></a><a name="p144918166312"></a><span>version</span></p>
</td>
<td class="cellrowborder" valign="top" width="24.782478247824784%" headers="mcps1.2.4.1.2 "><p id="p17449716136"><a name="p17449716136"></a><a name="p17449716136"></a><span>string</span></p>
</td>
<td class="cellrowborder" valign="top" width="51.8951895189519%" headers="mcps1.2.4.1.3 "><a name="ul10933101420711"></a><a name="ul10933101420711"></a><ul id="ul10933101420711"><li>如果API的这个版本支持微版本，则支持最大的微版本。</li><li>如果不支持微版本，这将是空字符串。</li></ul>
</td>
</tr>
<tr id="row1488912161131"><td class="cellrowborder" valign="top" width="23.32233223322332%" headers="mcps1.2.4.1.1 "><p id="p9889151613314"><a name="p9889151613314"></a><a name="p9889151613314"></a><span>updated</span></p>
</td>
<td class="cellrowborder" valign="top" width="24.782478247824784%" headers="mcps1.2.4.1.2 "><p id="p88897161032"><a name="p88897161032"></a><a name="p88897161032"></a><span>string</span></p>
</td>
<td class="cellrowborder" valign="top" width="51.8951895189519%" headers="mcps1.2.4.1.3 "><p id="p82093545426"><a name="p82093545426"></a><a name="p82093545426"></a>一个有特定值的字符串。</p>
<p id="p088916161838"><a name="p088916161838"></a><a name="p088916161838"></a>API版本为2.0时，值为2011-01-21T11:33:21Z，API版本是2.1时，值为 2013-07-23T11:33:21Z。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  links字段数据结构说明

<a name="table1586318199718"></a>
<table><thead align="left"><tr id="row19863719071"><th class="cellrowborder" valign="top" width="23.2023202320232%" id="mcps1.2.4.1.1"><p id="p38643193712"><a name="p38643193712"></a><a name="p38643193712"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.342434243424343%" id="mcps1.2.4.1.2"><p id="p1186420191678"><a name="p1186420191678"></a><a name="p1186420191678"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.45524552455245%" id="mcps1.2.4.1.3"><p id="p118647191972"><a name="p118647191972"></a><a name="p118647191972"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1886419192713"><td class="cellrowborder" valign="top" width="23.2023202320232%" headers="mcps1.2.4.1.1 "><p id="p48646193713"><a name="p48646193713"></a><a name="p48646193713"></a><span>href</span></p>
</td>
<td class="cellrowborder" valign="top" width="24.342434243424343%" headers="mcps1.2.4.1.2 "><p id="p786471915713"><a name="p786471915713"></a><a name="p786471915713"></a><span>string</span></p>
</td>
<td class="cellrowborder" valign="top" width="52.45524552455245%" headers="mcps1.2.4.1.3 "><p id="p55689555719"><a name="p55689555719"></a><a name="p55689555719"></a>相应资源的链接。</p>
</td>
</tr>
<tr id="row178649191472"><td class="cellrowborder" valign="top" width="23.2023202320232%" headers="mcps1.2.4.1.1 "><p id="p386411192074"><a name="p386411192074"></a><a name="p386411192074"></a><span>rel</span></p>
</td>
<td class="cellrowborder" valign="top" width="24.342434243424343%" headers="mcps1.2.4.1.2 "><p id="p68646190716"><a name="p68646190716"></a><a name="p68646190716"></a><span>string</span></p>
</td>
<td class="cellrowborder" valign="top" width="52.45524552455245%" headers="mcps1.2.4.1.3 "><a name="ul83106471713"></a><a name="ul83106471713"></a><ul id="ul83106471713"><li>self：自助链接包含版本链接的资源。立即链接后使用这些链接。</li><li>bookmark：书签链接提供了一个永久资源的永久链接，该链接适合于长期存储。</li><li>alternate：备用链接可以包含资源的替换表示形式。<p id="p103164310816"><a name="p103164310816"></a><a name="p103164310816"></a>例如，OpenStack计算映像可能在OpenStack映像服务中有一个替代表示。</p>
</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section39878380181842"></a>

```
GET https://{endpoint}/
```

## 响应示例<a name="section569124244211"></a>

```
{
 "versions": [{
  "links": [{
   "rel": "self",
   "href": "https://ecs.service.domain.com:443/v2/"
  }],
  "id": "v2.0",
  "updated": "2001-09-21T12:33:21Z",
  "status": "SUPPORTED"
 }]
}
```

## 返回值<a name="section12571834"></a>

请参考[通用请求返回值](通用请求返回值.md)。

