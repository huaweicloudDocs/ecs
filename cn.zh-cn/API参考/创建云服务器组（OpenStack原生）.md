# 创建云服务器组<a name="ZH-CN_TOPIC_0065817720"></a>

## 功能介绍<a name="zh-cn_topic_0057973153_section31887518"></a>

创建云服务器组。

## 接口约束<a name="zh-cn_topic_0057973153_section32752180"></a>

当前只支持反亲和性组。

## URI<a name="zh-cn_topic_0057973153_section18552212"></a>

POST /v2.1/\{project\_id\}/os-server-groups

参数说明请参见[表1](#zh-cn_topic_0057973153_zh-cn_topic_0020212650_table62669527)。

**表 1**  参数说明

<a name="zh-cn_topic_0057973153_zh-cn_topic_0020212650_table62669527"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973153_zh-cn_topic_0020212650_row33894570"><th class="cellrowborder" valign="top" width="20.74%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.05%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.209999999999994%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973153_zh-cn_topic_0020212650_row8419032"><td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973153_zh-cn_topic_0020212650_p10852974"><a name="zh-cn_topic_0057973153_zh-cn_topic_0020212650_p10852974"></a><a name="zh-cn_topic_0057973153_zh-cn_topic_0020212650_p10852974"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.05%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973153_zh-cn_topic_0020212650_p6675738"><a name="zh-cn_topic_0057973153_zh-cn_topic_0020212650_p6675738"></a><a name="zh-cn_topic_0057973153_zh-cn_topic_0020212650_p6675738"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="60.209999999999994%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057973153_section35680930"></a>

请求参数如[表2](#zh-cn_topic_0057973153_table57386915)所示。

**表 2**  请求参数

<a name="zh-cn_topic_0057973153_table57386915"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973153_row22108653"><th class="cellrowborder" valign="top" width="17.41%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0057972670_p57733603"><a name="zh-cn_topic_0057972670_p57733603"></a><a name="zh-cn_topic_0057972670_p57733603"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.34%" id="mcps1.2.5.1.2"><p id="p6694732133016"><a name="p6694732133016"></a><a name="p6694732133016"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="26.22%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0057972670_p45910260"><a name="zh-cn_topic_0057972670_p45910260"></a><a name="zh-cn_topic_0057972670_p45910260"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.03%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0057972670_p32634650"><a name="zh-cn_topic_0057972670_p32634650"></a><a name="zh-cn_topic_0057972670_p32634650"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973153_row62192793"><td class="cellrowborder" valign="top" width="17.41%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973153_p4451468"><a name="zh-cn_topic_0057973153_p4451468"></a><a name="zh-cn_topic_0057973153_p4451468"></a>server_group</p>
</td>
<td class="cellrowborder" valign="top" width="17.34%" headers="mcps1.2.5.1.2 "><p id="p1069423223018"><a name="p1069423223018"></a><a name="p1069423223018"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="26.22%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973153_p25024636"><a name="zh-cn_topic_0057973153_p25024636"></a><a name="zh-cn_topic_0057973153_p25024636"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="39.03%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973153_p38357105"><a name="zh-cn_topic_0057973153_p38357105"></a><a name="zh-cn_topic_0057973153_p38357105"></a><span id="text91094251724"><a name="text91094251724"></a><a name="text91094251724"></a>弹性云服务器</span>组信息。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  server\_group参数信息

<a name="zh-cn_topic_0057973153_table19917766"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973153_row59878934"><th class="cellrowborder" valign="top" width="17.32%" id="mcps1.2.5.1.1"><p id="p115851920182615"><a name="p115851920182615"></a><a name="p115851920182615"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.11%" id="mcps1.2.5.1.2"><p id="p375944953017"><a name="p375944953017"></a><a name="p375944953017"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="25.480000000000004%" id="mcps1.2.5.1.3"><p id="p1560210202260"><a name="p1560210202260"></a><a name="p1560210202260"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.09%" id="mcps1.2.5.1.4"><p id="p10602192016264"><a name="p10602192016264"></a><a name="p10602192016264"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973153_row28765213"><td class="cellrowborder" valign="top" width="17.32%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973153_p48280896"><a name="zh-cn_topic_0057973153_p48280896"></a><a name="zh-cn_topic_0057973153_p48280896"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.5.1.2 "><p id="p137591249173010"><a name="p137591249173010"></a><a name="p137591249173010"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25.480000000000004%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973153_p18438475"><a name="zh-cn_topic_0057973153_p18438475"></a><a name="zh-cn_topic_0057973153_p18438475"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.09%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973153_p44665147"><a name="zh-cn_topic_0057973153_p44665147"></a><a name="zh-cn_topic_0057973153_p44665147"></a><span id="text35902295214"><a name="text35902295214"></a><a name="text35902295214"></a>弹性云服务器</span>组名称，长度大于0小于256字节。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973153_row66442010"><td class="cellrowborder" valign="top" width="17.32%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973153_p13093750"><a name="zh-cn_topic_0057973153_p13093750"></a><a name="zh-cn_topic_0057973153_p13093750"></a>policies</p>
</td>
<td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.5.1.2 "><p id="p12759104943011"><a name="p12759104943011"></a><a name="p12759104943011"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="25.480000000000004%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973153_p53960863"><a name="zh-cn_topic_0057973153_p53960863"></a><a name="zh-cn_topic_0057973153_p53960863"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="39.09%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973153_p173471532155519"><a name="zh-cn_topic_0057973153_p173471532155519"></a><a name="zh-cn_topic_0057973153_p173471532155519"></a>与<span id="text184750158545"><a name="text184750158545"></a><a name="text184750158545"></a>云服务器</span>组关联的策略名称列表。包括：</p>
<a name="zh-cn_topic_0057973153_ul1237514118527"></a><a name="zh-cn_topic_0057973153_ul1237514118527"></a><ul id="zh-cn_topic_0057973153_ul1237514118527"><li>anti-affinity：此组中的<span id="text317320315213"><a name="text317320315213"></a><a name="text317320315213"></a>弹性云服务器</span>必须安排到不同的主机。</li><li>affinity：此组中的<span id="text48051032928"><a name="text48051032928"></a><a name="text48051032928"></a>弹性云服务器</span>必须安排在同一主机上。</li><li>soft-anti-affinity：如果可能，应将此组中的<span id="text11579101912541"><a name="text11579101912541"></a><a name="text11579101912541"></a>云服务器</span>尽量安排到不同的主机上，但如果无法实现，则仍应安排它们，而不是导致生成失败。</li><li>soft-affinity：如果可能，应将此组中的<span id="text46698341928"><a name="text46698341928"></a><a name="text46698341928"></a>弹性云服务器</span>尽量安排在同一主机上， 但如果无法实现，则仍应安排它们，而不是导致生成失败。</li></ul>
<div class="note" id="note156714496517"><a name="note156714496517"></a><a name="note156714496517"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1856715491058"><a name="p1856715491058"></a><a name="p1856715491058"></a>当前仅支持反亲和性anti-affinity策略。为兼容原生接口，保留其他三种策略，但使用其他三种策略创建的<span id="text16411172285420"><a name="text16411172285420"></a><a name="text16411172285420"></a>云服务器</span>组策略不生效。</p>
<p id="p356719491458"><a name="p356719491458"></a><a name="p356719491458"></a>推荐使用<a href="创建云服务器组.md">创建云服务器组</a>。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0057973153_section52692922"></a>

响应参数如[表4](#zh-cn_topic_0057973153_table55529076)所示。

**表 4**  响应参数

<a name="zh-cn_topic_0057973153_table55529076"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973153_row53394154"><th class="cellrowborder" valign="top" width="28.79%" id="mcps1.2.4.1.1"><p id="p32821024102610"><a name="p32821024102610"></a><a name="p32821024102610"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.79%" id="mcps1.2.4.1.2"><p id="p202822024132618"><a name="p202822024132618"></a><a name="p202822024132618"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="42.42%" id="mcps1.2.4.1.3"><p id="p10298192442612"><a name="p10298192442612"></a><a name="p10298192442612"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973153_row43894534"><td class="cellrowborder" valign="top" width="28.79%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973153_p65796329"><a name="zh-cn_topic_0057973153_p65796329"></a><a name="zh-cn_topic_0057973153_p65796329"></a>server_group</p>
</td>
<td class="cellrowborder" valign="top" width="28.79%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973153_p27902470"><a name="zh-cn_topic_0057973153_p27902470"></a><a name="zh-cn_topic_0057973153_p27902470"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="42.42%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973153_p62235912"><a name="zh-cn_topic_0057973153_p62235912"></a><a name="zh-cn_topic_0057973153_p62235912"></a><span id="text1918214365217"><a name="text1918214365217"></a><a name="text1918214365217"></a>弹性云服务器</span>组信息</p>
</td>
</tr>
</tbody>
</table>

**表 5**  server\_group参数信息

<a name="zh-cn_topic_0057973153_table7944126"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973153_row9238701"><th class="cellrowborder" valign="top" width="26.597340265973408%" id="mcps1.2.4.1.1"><p id="p177470268263"><a name="p177470268263"></a><a name="p177470268263"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.148085191480853%" id="mcps1.2.4.1.2"><p id="p167471026112613"><a name="p167471026112613"></a><a name="p167471026112613"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="54.25457454254574%" id="mcps1.2.4.1.3"><p id="p67471426112617"><a name="p67471426112617"></a><a name="p67471426112617"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973153_row60872190"><td class="cellrowborder" valign="top" width="26.597340265973408%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973153_p31700356"><a name="zh-cn_topic_0057973153_p31700356"></a><a name="zh-cn_topic_0057973153_p31700356"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="19.148085191480853%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973153_p17592014"><a name="zh-cn_topic_0057973153_p17592014"></a><a name="zh-cn_topic_0057973153_p17592014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.25457454254574%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973153_p61068496"><a name="zh-cn_topic_0057973153_p61068496"></a><a name="zh-cn_topic_0057973153_p61068496"></a><span id="text969412371220"><a name="text969412371220"></a><a name="text969412371220"></a>弹性云服务器</span>组UUID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973153_row12745552"><td class="cellrowborder" valign="top" width="26.597340265973408%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973153_p25756821"><a name="zh-cn_topic_0057973153_p25756821"></a><a name="zh-cn_topic_0057973153_p25756821"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="19.148085191480853%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973153_p5927779"><a name="zh-cn_topic_0057973153_p5927779"></a><a name="zh-cn_topic_0057973153_p5927779"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.25457454254574%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973153_p36126903"><a name="zh-cn_topic_0057973153_p36126903"></a><a name="zh-cn_topic_0057973153_p36126903"></a><span id="text71902391320"><a name="text71902391320"></a><a name="text71902391320"></a>弹性云服务器</span>组名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973153_row56706675"><td class="cellrowborder" valign="top" width="26.597340265973408%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973153_p29837953"><a name="zh-cn_topic_0057973153_p29837953"></a><a name="zh-cn_topic_0057973153_p29837953"></a>policies</p>
</td>
<td class="cellrowborder" valign="top" width="19.148085191480853%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973153_p955132"><a name="zh-cn_topic_0057973153_p955132"></a><a name="zh-cn_topic_0057973153_p955132"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="54.25457454254574%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973153_p18801115810585"><a name="zh-cn_topic_0057973153_p18801115810585"></a><a name="zh-cn_topic_0057973153_p18801115810585"></a>与服务器组关联的策略名称列表。当前有效的策略名称为:</p>
<p id="zh-cn_topic_0057973153_p1380255810580"><a name="zh-cn_topic_0057973153_p1380255810580"></a><a name="zh-cn_topic_0057973153_p1380255810580"></a>anti-affinity -此组中的服务器必须安排到不同的主机；</p>
<p id="zh-cn_topic_0057973153_p138031158195815"><a name="zh-cn_topic_0057973153_p138031158195815"></a><a name="zh-cn_topic_0057973153_p138031158195815"></a>affinity -此组中的服务器必须安排在同一主机上.</p>
<p id="zh-cn_topic_0057973153_p68041058195811"><a name="zh-cn_topic_0057973153_p68041058195811"></a><a name="zh-cn_topic_0057973153_p68041058195811"></a>soft-anti-affinity –如果可能, 应将此组中的服务器安排到不同的主机, 但如果无法实现, 则仍应安排它们, 而不是导致生成失败。</p>
<p id="zh-cn_topic_0057973153_p680565816581"><a name="zh-cn_topic_0057973153_p680565816581"></a><a name="zh-cn_topic_0057973153_p680565816581"></a>soft-affinity -如果可能, 应将此组中的服务器安排在同一主机上, 但如果无法实现, 则仍应安排它们, 而不是导致生成失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973153_row28154895"><td class="cellrowborder" valign="top" width="26.597340265973408%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973153_p65953984"><a name="zh-cn_topic_0057973153_p65953984"></a><a name="zh-cn_topic_0057973153_p65953984"></a>members</p>
</td>
<td class="cellrowborder" valign="top" width="19.148085191480853%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973153_p40672482"><a name="zh-cn_topic_0057973153_p40672482"></a><a name="zh-cn_topic_0057973153_p40672482"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="54.25457454254574%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973153_p27313303"><a name="zh-cn_topic_0057973153_p27313303"></a><a name="zh-cn_topic_0057973153_p27313303"></a><span id="text5197174013216"><a name="text5197174013216"></a><a name="text5197174013216"></a>弹性云服务器</span>组中包含的<span id="text1712634116218"><a name="text1712634116218"></a><a name="text1712634116218"></a>弹性云服务器</span>列表</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973153_row44493140"><td class="cellrowborder" valign="top" width="26.597340265973408%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973153_p47174611"><a name="zh-cn_topic_0057973153_p47174611"></a><a name="zh-cn_topic_0057973153_p47174611"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="19.148085191480853%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973153_p63047142"><a name="zh-cn_topic_0057973153_p63047142"></a><a name="zh-cn_topic_0057973153_p63047142"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="54.25457454254574%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973153_p60373738"><a name="zh-cn_topic_0057973153_p60373738"></a><a name="zh-cn_topic_0057973153_p60373738"></a><span id="text16114213212"><a name="text16114213212"></a><a name="text16114213212"></a>弹性云服务器</span>组元数据</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973153_row1034716141596"><td class="cellrowborder" valign="top" width="26.597340265973408%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973153_p56149379"><a name="zh-cn_topic_0057973153_p56149379"></a><a name="zh-cn_topic_0057973153_p56149379"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.148085191480853%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973153_p51805857"><a name="zh-cn_topic_0057973153_p51805857"></a><a name="zh-cn_topic_0057973153_p51805857"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.25457454254574%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973153_p58946952"><a name="zh-cn_topic_0057973153_p58946952"></a><a name="zh-cn_topic_0057973153_p58946952"></a><span id="text784594217211"><a name="text784594217211"></a><a name="text784594217211"></a>弹性云服务器</span>组所属租户ID，UUID格式。</p>
<div class="note" id="zh-cn_topic_0057973153_note122131644114517"><a name="zh-cn_topic_0057973153_note122131644114517"></a><a name="zh-cn_topic_0057973153_note122131644114517"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0057973153_p1521344417459"><a name="zh-cn_topic_0057973153_p1521344417459"></a><a name="zh-cn_topic_0057973153_p1521344417459"></a>微版本2.13新增参数。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0057973153_row6492733"><td class="cellrowborder" valign="top" width="26.597340265973408%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973153_p172856208593"><a name="zh-cn_topic_0057973153_p172856208593"></a><a name="zh-cn_topic_0057973153_p172856208593"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.148085191480853%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973153_p14286172095912"><a name="zh-cn_topic_0057973153_p14286172095912"></a><a name="zh-cn_topic_0057973153_p14286172095912"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="54.25457454254574%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973153_p728822045918"><a name="zh-cn_topic_0057973153_p728822045918"></a><a name="zh-cn_topic_0057973153_p728822045918"></a><span id="text189901143224"><a name="text189901143224"></a><a name="text189901143224"></a>弹性云服务器</span>组所属用户ID，UUID格式。</p>
<div class="note" id="zh-cn_topic_0057973153_note19831155154515"><a name="zh-cn_topic_0057973153_note19831155154515"></a><a name="zh-cn_topic_0057973153_note19831155154515"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0057973153_p1983195594518"><a name="zh-cn_topic_0057973153_p1983195594518"></a><a name="zh-cn_topic_0057973153_p1983195594518"></a>微版本2.13新增参数。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0057973153_section4474257"></a>

```
POST https://{endpoint}/v2.1/9c53a566cb3443ab910cf0daebca90c4/os-server-groups
```

```
{
    "server_group": {
        "name": "test",
        "policies": ["anti-affinity"]
    }
}
```

## 响应示例<a name="section4844134018500"></a>

```
{
    "server_group": {
        "id": "5bbcc3c4-1da2-4437-a48a-66f15b1b13f9",
        "name": "test",
        "policies": [
            "anti-affinity"
        ],
        "members": [],
        "metadata": {}
    }
}
```

## 返回值<a name="zh-cn_topic_0057973153_section17661930132114"></a>

请参考[通用请求返回值](通用请求返回值.md)。

