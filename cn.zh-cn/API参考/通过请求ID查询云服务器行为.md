# 通过请求ID查询云服务器行为<a name="ZH-CN_TOPIC_0065817693"></a>

## 功能介绍<a name="zh-cn_topic_0057973179_section16588975"></a>

查询弹性云服务器的某个请求行为。

## URI<a name="zh-cn_topic_0057973179_section15083054"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/os-instance-actions/\{request\_id\}

参数说明请参见[表1](#zh-cn_topic_0057973179_table55945983)。

**表 1**  参数说明

<a name="zh-cn_topic_0057973179_table55945983"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973179_row11302482"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="47%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973179_row49888896"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973179_p14468758"><a name="zh-cn_topic_0057973179_p14468758"></a><a name="zh-cn_topic_0057973179_p14468758"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973179_p31118786"><a name="zh-cn_topic_0057973179_p31118786"></a><a name="zh-cn_topic_0057973179_p31118786"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row613736410235"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973179_p2736446410235"><a name="zh-cn_topic_0057973179_p2736446410235"></a><a name="zh-cn_topic_0057973179_p2736446410235"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973179_p192907210235"><a name="zh-cn_topic_0057973179_p192907210235"></a><a name="zh-cn_topic_0057973179_p192907210235"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973179_p2203711610235"><a name="zh-cn_topic_0057973179_p2203711610235"></a><a name="zh-cn_topic_0057973179_p2203711610235"></a><span id="text68264416318"><a name="text68264416318"></a><a name="text68264416318"></a>弹性云服务器</span>ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row172751639164211"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973179_p1927610391427"><a name="zh-cn_topic_0057973179_p1927610391427"></a><a name="zh-cn_topic_0057973179_p1927610391427"></a>request_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973179_p1727693974213"><a name="zh-cn_topic_0057973179_p1727693974213"></a><a name="zh-cn_topic_0057973179_p1727693974213"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973179_p4276839114210"><a name="zh-cn_topic_0057973179_p4276839114210"></a><a name="zh-cn_topic_0057973179_p4276839114210"></a>请求ID</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057973179_section56802184"></a>

无

## 响应消息<a name="zh-cn_topic_0057973179_section41457614"></a>

响应参数如[表2](#zh-cn_topic_0057973153_table55529076)所示。

**表 2**  响应参数

<a name="zh-cn_topic_0057973153_table55529076"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973153_row53394154"><th class="cellrowborder" valign="top" width="28.79%" id="mcps1.2.4.1.1"><p id="p32821024102610"><a name="p32821024102610"></a><a name="p32821024102610"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.79%" id="mcps1.2.4.1.2"><p id="p202822024132618"><a name="p202822024132618"></a><a name="p202822024132618"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="42.42%" id="mcps1.2.4.1.3"><p id="p10298192442612"><a name="p10298192442612"></a><a name="p10298192442612"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973153_row43894534"><td class="cellrowborder" valign="top" width="28.79%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973153_p65796329"><a name="zh-cn_topic_0057973153_p65796329"></a><a name="zh-cn_topic_0057973153_p65796329"></a>instanceAction</p>
</td>
<td class="cellrowborder" valign="top" width="28.79%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973153_p27902470"><a name="zh-cn_topic_0057973153_p27902470"></a><a name="zh-cn_topic_0057973153_p27902470"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="42.42%" headers="mcps1.2.4.1.3 "><p id="p24702645"><a name="p24702645"></a><a name="p24702645"></a><span id="text107516360550"><a name="text107516360550"></a><a name="text107516360550"></a>云服务器</span>操作行为，详情请参见<a href="#zh-cn_topic_0057973179_table42003011">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  instanceAction字段数据结构说明

<a name="zh-cn_topic_0057973179_table42003011"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973179_row4203326"><th class="cellrowborder" valign="top" width="21.16%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0057973179_p4925089"><a name="zh-cn_topic_0057973179_p4925089"></a><a name="zh-cn_topic_0057973179_p4925089"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.8%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0057973179_p34151611"><a name="zh-cn_topic_0057973179_p34151611"></a><a name="zh-cn_topic_0057973179_p34151611"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.990000000000002%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0057973179_p63387966"><a name="zh-cn_topic_0057973179_p63387966"></a><a name="zh-cn_topic_0057973179_p63387966"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="37.05%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0057973179_p14817088"><a name="zh-cn_topic_0057973179_p14817088"></a><a name="zh-cn_topic_0057973179_p14817088"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973179_row59333494"><td class="cellrowborder" valign="top" width="21.16%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p41283716"><a name="zh-cn_topic_0057973179_p41283716"></a><a name="zh-cn_topic_0057973179_p41283716"></a>action</p>
</td>
<td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p11092043"><a name="zh-cn_topic_0057973179_p11092043"></a><a name="zh-cn_topic_0057973179_p11092043"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.990000000000002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p55646739"><a name="zh-cn_topic_0057973179_p55646739"></a><a name="zh-cn_topic_0057973179_p55646739"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p26040275"><a name="zh-cn_topic_0057973179_p26040275"></a><a name="zh-cn_topic_0057973179_p26040275"></a>行为动作</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row33035884"><td class="cellrowborder" valign="top" width="21.16%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p58660976"><a name="zh-cn_topic_0057973179_p58660976"></a><a name="zh-cn_topic_0057973179_p58660976"></a>instance_uuid</p>
</td>
<td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p5331789"><a name="zh-cn_topic_0057973179_p5331789"></a><a name="zh-cn_topic_0057973179_p5331789"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.990000000000002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p53918616"><a name="zh-cn_topic_0057973179_p53918616"></a><a name="zh-cn_topic_0057973179_p53918616"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p29221750"><a name="zh-cn_topic_0057973179_p29221750"></a><a name="zh-cn_topic_0057973179_p29221750"></a><span id="text155414220319"><a name="text155414220319"></a><a name="text155414220319"></a>弹性云服务器</span>ID，UUID格式</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row61669162"><td class="cellrowborder" valign="top" width="21.16%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p29146205"><a name="zh-cn_topic_0057973179_p29146205"></a><a name="zh-cn_topic_0057973179_p29146205"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p35098404"><a name="zh-cn_topic_0057973179_p35098404"></a><a name="zh-cn_topic_0057973179_p35098404"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.990000000000002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p12032376"><a name="zh-cn_topic_0057973179_p12032376"></a><a name="zh-cn_topic_0057973179_p12032376"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p24398472"><a name="zh-cn_topic_0057973179_p24398472"></a><a name="zh-cn_topic_0057973179_p24398472"></a>行为完成状态信息</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row18259663"><td class="cellrowborder" valign="top" width="21.16%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p2637755"><a name="zh-cn_topic_0057973179_p2637755"></a><a name="zh-cn_topic_0057973179_p2637755"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p59338465"><a name="zh-cn_topic_0057973179_p59338465"></a><a name="zh-cn_topic_0057973179_p59338465"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.990000000000002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p12331636"><a name="zh-cn_topic_0057973179_p12331636"></a><a name="zh-cn_topic_0057973179_p12331636"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p41686379"><a name="zh-cn_topic_0057973179_p41686379"></a><a name="zh-cn_topic_0057973179_p41686379"></a>项目ID</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row39633094"><td class="cellrowborder" valign="top" width="21.16%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p56164037"><a name="zh-cn_topic_0057973179_p56164037"></a><a name="zh-cn_topic_0057973179_p56164037"></a>request_id</p>
</td>
<td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p64588638"><a name="zh-cn_topic_0057973179_p64588638"></a><a name="zh-cn_topic_0057973179_p64588638"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.990000000000002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p52993173"><a name="zh-cn_topic_0057973179_p52993173"></a><a name="zh-cn_topic_0057973179_p52993173"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p64297159"><a name="zh-cn_topic_0057973179_p64297159"></a><a name="zh-cn_topic_0057973179_p64297159"></a>请求ID</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row41803519"><td class="cellrowborder" valign="top" width="21.16%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p30641851"><a name="zh-cn_topic_0057973179_p30641851"></a><a name="zh-cn_topic_0057973179_p30641851"></a>start_time</p>
</td>
<td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p50142074"><a name="zh-cn_topic_0057973179_p50142074"></a><a name="zh-cn_topic_0057973179_p50142074"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.990000000000002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p66070892"><a name="zh-cn_topic_0057973179_p66070892"></a><a name="zh-cn_topic_0057973179_p66070892"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p34976204"><a name="zh-cn_topic_0057973179_p34976204"></a><a name="zh-cn_topic_0057973179_p34976204"></a>行为开始时间</p>
</td>
</tr>
<tr id="row419219211572"><td class="cellrowborder" valign="top" width="21.16%" headers="mcps1.2.5.1.1 "><p id="p13192421165713"><a name="p13192421165713"></a><a name="p13192421165713"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.2.5.1.2 "><p id="p2019272113571"><a name="p2019272113571"></a><a name="p2019272113571"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.990000000000002%" headers="mcps1.2.5.1.3 "><p id="p1419252175710"><a name="p1419252175710"></a><a name="p1419252175710"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="p31920211578"><a name="p31920211578"></a><a name="p31920211578"></a>用户ID</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row46350387"><td class="cellrowborder" valign="top" width="21.16%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p63393830"><a name="zh-cn_topic_0057973179_p63393830"></a><a name="zh-cn_topic_0057973179_p63393830"></a>events</p>
</td>
<td class="cellrowborder" valign="top" width="20.8%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p53294688"><a name="zh-cn_topic_0057973179_p53294688"></a><a name="zh-cn_topic_0057973179_p53294688"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.990000000000002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p34626643"><a name="zh-cn_topic_0057973179_p34626643"></a><a name="zh-cn_topic_0057973179_p34626643"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p21902453"><a name="zh-cn_topic_0057973179_p21902453"></a><a name="zh-cn_topic_0057973179_p21902453"></a>事件信息，详情参见<a href="#zh-cn_topic_0057973179_table12745176">表4</a></p>
</td>
</tr>
</tbody>
</table>

**表 4**  events字段数据结构说明

<a name="zh-cn_topic_0057973179_table12745176"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973179_row62655484"><th class="cellrowborder" valign="top" width="21.9%" id="mcps1.2.5.1.1"><p id="p955611101542"><a name="p955611101542"></a><a name="p955611101542"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.349999999999998%" id="mcps1.2.5.1.2"><p id="p755691019545"><a name="p755691019545"></a><a name="p755691019545"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.7%" id="mcps1.2.5.1.3"><p id="p1255681015541"><a name="p1255681015541"></a><a name="p1255681015541"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="37.05%" id="mcps1.2.5.1.4"><p id="p1957112100545"><a name="p1957112100545"></a><a name="p1957112100545"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973179_row66711197"><td class="cellrowborder" valign="top" width="21.9%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p34897906"><a name="zh-cn_topic_0057973179_p34897906"></a><a name="zh-cn_topic_0057973179_p34897906"></a>event</p>
</td>
<td class="cellrowborder" valign="top" width="20.349999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p56831198"><a name="zh-cn_topic_0057973179_p56831198"></a><a name="zh-cn_topic_0057973179_p56831198"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p8158160"><a name="zh-cn_topic_0057973179_p8158160"></a><a name="zh-cn_topic_0057973179_p8158160"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p39924292"><a name="zh-cn_topic_0057973179_p39924292"></a><a name="zh-cn_topic_0057973179_p39924292"></a>行为动作名称</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row23774312"><td class="cellrowborder" valign="top" width="21.9%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p46671110"><a name="zh-cn_topic_0057973179_p46671110"></a><a name="zh-cn_topic_0057973179_p46671110"></a>result</p>
</td>
<td class="cellrowborder" valign="top" width="20.349999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p58518640"><a name="zh-cn_topic_0057973179_p58518640"></a><a name="zh-cn_topic_0057973179_p58518640"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p22263569"><a name="zh-cn_topic_0057973179_p22263569"></a><a name="zh-cn_topic_0057973179_p22263569"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p42389388"><a name="zh-cn_topic_0057973179_p42389388"></a><a name="zh-cn_topic_0057973179_p42389388"></a>执行结果</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row45960172"><td class="cellrowborder" valign="top" width="21.9%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p31786413"><a name="zh-cn_topic_0057973179_p31786413"></a><a name="zh-cn_topic_0057973179_p31786413"></a>traceback</p>
</td>
<td class="cellrowborder" valign="top" width="20.349999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p43418025"><a name="zh-cn_topic_0057973179_p43418025"></a><a name="zh-cn_topic_0057973179_p43418025"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p24562655"><a name="zh-cn_topic_0057973179_p24562655"></a><a name="zh-cn_topic_0057973179_p24562655"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p27199156"><a name="zh-cn_topic_0057973179_p27199156"></a><a name="zh-cn_topic_0057973179_p27199156"></a>异常信息</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row43465817"><td class="cellrowborder" valign="top" width="21.9%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p31070312"><a name="zh-cn_topic_0057973179_p31070312"></a><a name="zh-cn_topic_0057973179_p31070312"></a>start_time</p>
</td>
<td class="cellrowborder" valign="top" width="20.349999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p42699947"><a name="zh-cn_topic_0057973179_p42699947"></a><a name="zh-cn_topic_0057973179_p42699947"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p33667339"><a name="zh-cn_topic_0057973179_p33667339"></a><a name="zh-cn_topic_0057973179_p33667339"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p36143663"><a name="zh-cn_topic_0057973179_p36143663"></a><a name="zh-cn_topic_0057973179_p36143663"></a>事件开始时间</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973179_row56857514"><td class="cellrowborder" valign="top" width="21.9%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973179_p42055936"><a name="zh-cn_topic_0057973179_p42055936"></a><a name="zh-cn_topic_0057973179_p42055936"></a>finish_time</p>
</td>
<td class="cellrowborder" valign="top" width="20.349999999999998%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973179_p44459997"><a name="zh-cn_topic_0057973179_p44459997"></a><a name="zh-cn_topic_0057973179_p44459997"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.7%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973179_p51087662"><a name="zh-cn_topic_0057973179_p51087662"></a><a name="zh-cn_topic_0057973179_p51087662"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973179_p44490037"><a name="zh-cn_topic_0057973179_p44490037"></a><a name="zh-cn_topic_0057973179_p44490037"></a>事件结束时间</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0057973179_section37574207"></a>

```
GET https://{endpoint}/v2.1/89655fe61c4c4a08b9f3e7f9095441b8/servers/e723eb40-f56e-40f9-8c8c-caa517fe06ba/os-instance-actions/req-5a429946-c9cc-45cc-b5bd-68864209e5c
```

## 响应示例<a name="section18542154625318"></a>

```
{
    "instanceAction": {
        "instance_uuid": "e723eb40-f56e-40f9-8c8c-caa517fe06ba",
        "user_id": "752be40780484291a9cc7ae50fff3e6d",
        "start_time": "2014-12-11T02:17:49.000000",
        "request_id": "req-5a429946-c9cc-45cc-b5bd-68864209e5cc",
        "action": "create",
        "message": null,
        "project_id": "89655fe61c4c4a08b9f3e7f9095441b8",
        "events": [
            {
                "finish_time": "2014-12-11T02:17:58.000000",
                "start_time": "2014-12-11T02:17:50.000000",
                "traceback": null,
                "event": "compute_build_and_run_instance",
                "result": "Success"
            }
        ]
    }
}
```

## 返回值<a name="zh-cn_topic_0057973179_section1642564"></a>

请参考[通用请求返回值](通用请求返回值.md)。

