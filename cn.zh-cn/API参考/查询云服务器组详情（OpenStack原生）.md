# 查询云服务器组详情<a name="ecs_03_1403"></a>

## 功能介绍<a name="zh-cn_topic_0057973159_section30240326"></a>

查询云服务器组详情。

## URI<a name="zh-cn_topic_0057973159_section3727484"></a>

GET /v2.1/\{project\_id\}/os-server-groups/\{server\_group\_id\}

参数说明请参见[表1](#table1773113411618)。

**表 1**  参数说明

<a name="table1773113411618"></a>
<table><thead align="left"><tr id="row2073173419165"><th class="cellrowborder" valign="top" width="23.342334233423344%" id="mcps1.2.4.1.1"><p id="p1734664216169"><a name="p1734664216169"></a><a name="p1734664216169"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.202120212021203%" id="mcps1.2.4.1.2"><p id="p11346124271610"><a name="p11346124271610"></a><a name="p11346124271610"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.45554555455545%" id="mcps1.2.4.1.3"><p id="p11346104220163"><a name="p11346104220163"></a><a name="p11346104220163"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1773534141610"><td class="cellrowborder" valign="top" width="23.342334233423344%" headers="mcps1.2.4.1.1 "><p id="p83465429162"><a name="p83465429162"></a><a name="p83465429162"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.202120212021203%" headers="mcps1.2.4.1.2 "><p id="p63461542141612"><a name="p63461542141612"></a><a name="p63461542141612"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.45554555455545%" headers="mcps1.2.4.1.3 "><p id="p18346124231612"><a name="p18346124231612"></a><a name="p18346124231612"></a>项目ID。</p>
<p id="p11346114211166"><a name="p11346114211166"></a><a name="p11346114211166"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row1373153419161"><td class="cellrowborder" valign="top" width="23.342334233423344%" headers="mcps1.2.4.1.1 "><p id="p193461542111617"><a name="p193461542111617"></a><a name="p193461542111617"></a>server_group_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.202120212021203%" headers="mcps1.2.4.1.2 "><p id="p734764214164"><a name="p734764214164"></a><a name="p734764214164"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.45554555455545%" headers="mcps1.2.4.1.3 "><p id="p1034714281618"><a name="p1034714281618"></a><a name="p1034714281618"></a><span id="text1334713429164"><a name="text1334713429164"></a><a name="text1334713429164"></a>弹性云服务器</span>组UUID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section7947182095214"></a>

无

## 响应消息<a name="zh-cn_topic_0057973159_section28398296"></a>

响应参数如[表2](#table176896216171)所示。

**表 2**  响应参数

<a name="table176896216171"></a>
<table><thead align="left"><tr id="row136891322172"><th class="cellrowborder" valign="top" width="27.792779277927792%" id="mcps1.2.4.1.1"><p id="p18622612101716"><a name="p18622612101716"></a><a name="p18622612101716"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="27.342734273427343%" id="mcps1.2.4.1.2"><p id="p76221812141711"><a name="p76221812141711"></a><a name="p76221812141711"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.86448644864487%" id="mcps1.2.4.1.3"><p id="p462291231718"><a name="p462291231718"></a><a name="p462291231718"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row468942121713"><td class="cellrowborder" valign="top" width="27.792779277927792%" headers="mcps1.2.4.1.1 "><p id="p1622161215175"><a name="p1622161215175"></a><a name="p1622161215175"></a>server_group</p>
</td>
<td class="cellrowborder" valign="top" width="27.342734273427343%" headers="mcps1.2.4.1.2 "><p id="p11622171219171"><a name="p11622171219171"></a><a name="p11622171219171"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="44.86448644864487%" headers="mcps1.2.4.1.3 "><p id="p12622131215171"><a name="p12622131215171"></a><a name="p12622131215171"></a><span id="text1562213126175"><a name="text1562213126175"></a><a name="text1562213126175"></a>弹性云服务器</span>组信息，参考<a href="#zh-cn_topic_0057973159_table5520021">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  server\_group参数信息

<a name="zh-cn_topic_0057973159_table5520021"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973159_row52947946"><th class="cellrowborder" valign="top" width="30.09%" id="mcps1.2.4.1.1"><p id="p14850105762611"><a name="p14850105762611"></a><a name="p14850105762611"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.09%" id="mcps1.2.4.1.2"><p id="p1685014574266"><a name="p1685014574266"></a><a name="p1685014574266"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.82%" id="mcps1.2.4.1.3"><p id="p168651757112614"><a name="p168651757112614"></a><a name="p168651757112614"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973159_row5110742"><td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973159_p11316939"><a name="zh-cn_topic_0057973159_p11316939"></a><a name="zh-cn_topic_0057973159_p11316939"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973159_p44256881"><a name="zh-cn_topic_0057973159_p44256881"></a><a name="zh-cn_topic_0057973159_p44256881"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.82%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973159_p56454382"><a name="zh-cn_topic_0057973159_p56454382"></a><a name="zh-cn_topic_0057973159_p56454382"></a><span id="text1090613491423"><a name="text1090613491423"></a><a name="text1090613491423"></a>弹性云服务器</span>组UUID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973159_row38327398"><td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973159_p17511496"><a name="zh-cn_topic_0057973159_p17511496"></a><a name="zh-cn_topic_0057973159_p17511496"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973159_p9145087"><a name="zh-cn_topic_0057973159_p9145087"></a><a name="zh-cn_topic_0057973159_p9145087"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.82%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973159_p5596939"><a name="zh-cn_topic_0057973159_p5596939"></a><a name="zh-cn_topic_0057973159_p5596939"></a><span id="text1255410502213"><a name="text1255410502213"></a><a name="text1255410502213"></a>弹性云服务器</span>组名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973159_row50372456"><td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973159_p53637170"><a name="zh-cn_topic_0057973159_p53637170"></a><a name="zh-cn_topic_0057973159_p53637170"></a>policies</p>
</td>
<td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973159_p49643541"><a name="zh-cn_topic_0057973159_p49643541"></a><a name="zh-cn_topic_0057973159_p49643541"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="39.82%" headers="mcps1.2.4.1.3 "><div class="p" id="zh-cn_topic_0057973159_p31957059"><a name="zh-cn_topic_0057973159_p31957059"></a><a name="zh-cn_topic_0057973159_p31957059"></a><span id="text1212315519217"><a name="text1212315519217"></a><a name="text1212315519217"></a>弹性云服务器</span>组类型。包括：<a name="zh-cn_topic_0057973153_ul1237514118527"></a><a name="zh-cn_topic_0057973153_ul1237514118527"></a><ul id="zh-cn_topic_0057973153_ul1237514118527"><li>anti-affinity：此组中的<span id="text108531141105410"><a name="text108531141105410"></a><a name="text108531141105410"></a>云服务器</span>必须安排到不同的主机。</li><li>affinity：此组中的<span id="text45441542205412"><a name="text45441542205412"></a><a name="text45441542205412"></a>云服务器</span>必须安排在同一主机上。</li><li>soft-anti-affinity：如果可能，应将此组中的<span id="text19269184312543"><a name="text19269184312543"></a><a name="text19269184312543"></a>云服务器</span>尽量安排到不同的主机上，但如果无法实现，则仍应安排它们，而不是导致生成失败。</li><li>soft-affinity：如果可能，应将此组中的<span id="text146184418540"><a name="text146184418540"></a><a name="text146184418540"></a>云服务器</span>尽量安排在同一主机上， 但如果无法实现，则仍应安排它们，而不是导致生成失败。</li></ul>
</div>
<div class="note" id="note3999145219471"><a name="note3999145219471"></a><a name="note3999145219471"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1199975212476"><a name="p1199975212476"></a><a name="p1199975212476"></a>当前仅支持反亲和性anti-affinity策略。不建议使用其他策略。如果使用其他策略云服务器组可能会创建失败。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0057973159_row19178079"><td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973159_p9920603"><a name="zh-cn_topic_0057973159_p9920603"></a><a name="zh-cn_topic_0057973159_p9920603"></a>members</p>
</td>
<td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973159_p65371346"><a name="zh-cn_topic_0057973159_p65371346"></a><a name="zh-cn_topic_0057973159_p65371346"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="39.82%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973159_p8656215"><a name="zh-cn_topic_0057973159_p8656215"></a><a name="zh-cn_topic_0057973159_p8656215"></a><span id="text990715511124"><a name="text990715511124"></a><a name="text990715511124"></a>弹性云服务器</span>组中包含的<span id="text1063465220219"><a name="text1063465220219"></a><a name="text1063465220219"></a>弹性云服务器</span>列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973159_row10797076"><td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973159_p2147930"><a name="zh-cn_topic_0057973159_p2147930"></a><a name="zh-cn_topic_0057973159_p2147930"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973159_p39764641"><a name="zh-cn_topic_0057973159_p39764641"></a><a name="zh-cn_topic_0057973159_p39764641"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="39.82%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973159_p43657808"><a name="zh-cn_topic_0057973159_p43657808"></a><a name="zh-cn_topic_0057973159_p43657808"></a><span id="text1752319533215"><a name="text1752319533215"></a><a name="text1752319533215"></a>弹性云服务器</span>组元数据。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973159_row57375958"><td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973159_p16941010"><a name="zh-cn_topic_0057973159_p16941010"></a><a name="zh-cn_topic_0057973159_p16941010"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973159_p30044530"><a name="zh-cn_topic_0057973159_p30044530"></a><a name="zh-cn_topic_0057973159_p30044530"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.82%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973159_p23428799"><a name="zh-cn_topic_0057973159_p23428799"></a><a name="zh-cn_topic_0057973159_p23428799"></a><span id="text12666541218"><a name="text12666541218"></a><a name="text12666541218"></a>弹性云服务器</span>组所属租户ID，UUID格式。</p>
<p id="p1873011156514"><a name="p1873011156514"></a><a name="p1873011156514"></a>微版本2.13及以上版本支持。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973159_row975381085117"><td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973159_p187549109517"><a name="zh-cn_topic_0057973159_p187549109517"></a><a name="zh-cn_topic_0057973159_p187549109517"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="30.09%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973159_p090181716517"><a name="zh-cn_topic_0057973159_p090181716517"></a><a name="zh-cn_topic_0057973159_p090181716517"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.82%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973159_p39217176512"><a name="zh-cn_topic_0057973159_p39217176512"></a><a name="zh-cn_topic_0057973159_p39217176512"></a><span id="text16860173512312"><a name="text16860173512312"></a><a name="text16860173512312"></a>弹性云服务器</span>组所属用户ID，UUID格式。</p>
<p id="p01189312816"><a name="p01189312816"></a><a name="p01189312816"></a>微版本2.13及以上版本支持。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0057973159_section54258073"></a>

```
GET https://{endpoint}/v2.1/9c53a566cb3443ab910cf0daebca90c4/os-server-groups/5bbcc3c4-1da2-4437-a48a-66f15b1b13f9
```

## 响应示例<a name="section8761640135117"></a>

```
{
    "server_group": {
        "id": "5bbcc3c4-1da2-4437-a48a-66f15b1b13f9",
        "name": "test",
        "policies": ["anti-affinity"],
        "members": [],
        "metadata": {},
        "project_id": "9c53a566cb3443ab910cf0daebca90c4"
    }
}
```

## 返回值<a name="zh-cn_topic_0057973159_section32827787"></a>

请参考[通用请求返回值](通用请求返回值.md)。

