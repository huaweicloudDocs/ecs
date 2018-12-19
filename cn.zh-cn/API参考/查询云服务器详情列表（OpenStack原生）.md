# 查询云服务器详情列表<a name="ZH-CN_TOPIC_0020212689"></a>

## 功能介绍<a name="section33716833"></a>

查询云服务器详情信息列表。

## URI<a name="section35016046"></a>

GET /v2/\{project\_id\}/servers/detail\{?changes-since,image,flavor,name,status,limit,marker,not-tags,reservation\_id,ip\}

GET /v2.1/\{project\_id\}/servers/detail\{?changes-since,image,flavor,name,status,limit,marker,not-tags,reservation\_id,ip\}

参数说明请参见[表1](#table31251786)。

**表 1**  参数说明

<a name="table31251786"></a>
<table><thead align="left"><tr id="row43455040"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="48%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row41845253"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p34022319"><a name="p34022319"></a><a name="p34022319"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.4.1.2 "><p id="p4344474"><a name="p4344474"></a><a name="p4344474"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section52316204200"></a>

**请求参数**

请求参数如[表2](#table49939793)所示。

**表 2**  请求参数

<a name="table49939793"></a>
<table><thead align="left"><tr id="row40936054"><th class="cellrowborder" valign="top" width="19%" id="mcps1.2.5.1.1"><p id="p83031738192710"><a name="p83031738192710"></a><a name="p83031738192710"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p11776988"><a name="p11776988"></a><a name="p11776988"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.5.1.3"><p id="p14412003"><a name="p14412003"></a><a name="p14412003"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="56.99999999999999%" id="mcps1.2.5.1.4"><p id="p37367427"><a name="p37367427"></a><a name="p37367427"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row762524"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p61764512"><a name="p61764512"></a><a name="p61764512"></a>changes-since</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p36869576"><a name="p36869576"></a><a name="p36869576"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p33645693"><a name="p33645693"></a><a name="p33645693"></a>String:DateTime</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p32975066"><a name="p32975066"></a><a name="p32975066"></a>云服务器上次更新状态的时间戳信息。时间戳为UTC格式。</p>
</td>
</tr>
<tr id="row29801224315"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p1098119240115"><a name="p1098119240115"></a><a name="p1098119240115"></a>ip</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p18981172412115"><a name="p18981172412115"></a><a name="p18981172412115"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p59817240117"><a name="p59817240117"></a><a name="p59817240117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p798132410120"><a name="p798132410120"></a><a name="p798132410120"></a>IPv4地址过滤结果。</p>
</td>
</tr>
<tr id="row28340140"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p13849974"><a name="p13849974"></a><a name="p13849974"></a>image</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p48106092"><a name="p48106092"></a><a name="p48106092"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p4279416"><a name="p4279416"></a><a name="p4279416"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p48648256163653"><a name="p48648256163653"></a><a name="p48648256163653"></a>镜像ID。</p>
<p id="p32686589"><a name="p32686589"></a><a name="p32686589"></a>在使用image作为条件过滤时，不能同时支持其他过滤条件和分页条件。如果同时指定image及其他条件，则以image条件为准；当条件不含image时，接口功能不受限制。</p>
</td>
</tr>
<tr id="row25743851"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p4877220"><a name="p4877220"></a><a name="p4877220"></a>flavor</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p59510545"><a name="p59510545"></a><a name="p59510545"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p55624859"><a name="p55624859"></a><a name="p55624859"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p16768629"><a name="p16768629"></a><a name="p16768629"></a>云服务器规格ID。</p>
</td>
</tr>
<tr id="row16699940"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p10517875"><a name="p10517875"></a><a name="p10517875"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p46641535"><a name="p46641535"></a><a name="p46641535"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p19867951"><a name="p19867951"></a><a name="p19867951"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p55330634"><a name="p55330634"></a><a name="p55330634"></a>云服务器名称。</p>
</td>
</tr>
<tr id="row28213660"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p3605162"><a name="p3605162"></a><a name="p3605162"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p23582716"><a name="p23582716"></a><a name="p23582716"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p31151867"><a name="p31151867"></a><a name="p31151867"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p26915331"><a name="p26915331"></a><a name="p26915331"></a>云服务器状态。</p>
<p id="p13233363305"><a name="p13233363305"></a><a name="p13233363305"></a>取值范围：</p>
<p id="p7325133614307"><a name="p7325133614307"></a><a name="p7325133614307"></a>ACTIVE， BUILD，ERROR，HARD_REBOOT，MIGRATING，REBOOT，RESIZE，REVERT_RESIZE，SHELVED，SHELVED_OFFLOADED，SHUTOFF，VERIFY_RESIZE</p>
<p id="p168361158173715"><a name="p168361158173715"></a><a name="p168361158173715"></a>直到2.37微版本，非上面范围的status字段将返回空列表，2.38之后的微版本，将返回400错误。</p>
</td>
</tr>
<tr id="row63147504"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p14674162"><a name="p14674162"></a><a name="p14674162"></a>limit</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p47756489"><a name="p47756489"></a><a name="p47756489"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p43070429"><a name="p43070429"></a><a name="p43070429"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p58503618"><a name="p58503618"></a><a name="p58503618"></a>查询返回云服务器数量限制。</p>
</td>
</tr>
<tr id="row56770522"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p35009555"><a name="p35009555"></a><a name="p35009555"></a>marker</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p17201705"><a name="p17201705"></a><a name="p17201705"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p51160835"><a name="p51160835"></a><a name="p51160835"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p50829401"><a name="p50829401"></a><a name="p50829401"></a>从marker指定的云服务器ID的下一条数据开始查询。</p>
</td>
</tr>
<tr id="row3418391114343"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p1743343514343"><a name="p1743343514343"></a><a name="p1743343514343"></a>not-tags</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p282213114343"><a name="p282213114343"></a><a name="p282213114343"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p2726607214343"><a name="p2726607214343"></a><a name="p2726607214343"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p1490634313912"><a name="p1490634313912"></a><a name="p1490634313912"></a>受微版本2.26限制</p>
<p id="p497882461442"><a name="p497882461442"></a><a name="p497882461442"></a>查询tag字段中不包含该值的云服务器，值为标签的Key。</p>
<div class="note" id="note124521913175616"><a name="note124521913175616"></a><a name="note124521913175616"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0020212688_p1745221311560"><a name="zh-cn_topic_0020212688_p1745221311560"></a><a name="zh-cn_topic_0020212688_p1745221311560"></a>系统近期对标签功能进行了升级。如果之前添加的Tag为“Key.Value”的形式，则查询的时候需要使用“Key”来查询。</p>
<p id="zh-cn_topic_0020212688_p213418685710"><a name="zh-cn_topic_0020212688_p213418685710"></a><a name="zh-cn_topic_0020212688_p213418685710"></a>例如：之前添加的tag为“a.b”,则升级后，查询时需使用“not-tags=a”。</p>
</div></div>
</td>
</tr>
<tr id="row15964135162918"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p151431598259"><a name="p151431598259"></a><a name="p151431598259"></a>reservation_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p11452059192515"><a name="p11452059192515"></a><a name="p11452059192515"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p0145165992515"><a name="p0145165992515"></a><a name="p0145165992515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p191452591254"><a name="p191452591254"></a><a name="p191452591254"></a>批量创建弹性云服务器时，指定返回的ID，用于查询本次批量创建的弹性云服务器。</p>
</td>
</tr>
<tr id="row2066412186"><td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.1 "><p id="p1066412283"><a name="p1066412283"></a><a name="p1066412283"></a>sort_key</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p15661012780"><a name="p15661012780"></a><a name="p15661012780"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p158210121988"><a name="p158210121988"></a><a name="p158210121988"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.5.1.4 "><p id="p576212355010"><a name="p576212355010"></a><a name="p576212355010"></a>查询结果按弹性云服务器属性排序，默认排序顺序为create_at逆序。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section17727455"></a>

**响应参数**

响应参数如[表3](#table61256692)所示。

**表 3**  响应参数

<a name="table61256692"></a>
<table><thead align="left"><tr id="row16697504"><th class="cellrowborder" valign="top" width="20.177982201779823%" id="mcps1.2.4.1.1"><p id="p151881852192720"><a name="p151881852192720"></a><a name="p151881852192720"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="31.26687331266873%" id="mcps1.2.4.1.2"><p id="p429128"><a name="p429128"></a><a name="p429128"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.555144485551445%" id="mcps1.2.4.1.3"><p id="p34759433"><a name="p34759433"></a><a name="p34759433"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row64050727"><td class="cellrowborder" valign="top" width="20.177982201779823%" headers="mcps1.2.4.1.1 "><p id="p20726409"><a name="p20726409"></a><a name="p20726409"></a>servers</p>
</td>
<td class="cellrowborder" valign="top" width="31.26687331266873%" headers="mcps1.2.4.1.2 "><p id="p23416123"><a name="p23416123"></a><a name="p23416123"></a>列表数据结构</p>
</td>
<td class="cellrowborder" valign="top" width="48.555144485551445%" headers="mcps1.2.4.1.3 "><p id="p24702645"><a name="p24702645"></a><a name="p24702645"></a>查询云服务器信息列表，详情请参见<a href="#table1549812072413">表4</a>。</p>
</td>
</tr>
<tr id="row5635120017432"><td class="cellrowborder" valign="top" width="20.177982201779823%" headers="mcps1.2.4.1.1 "><p id="p104447017432"><a name="p104447017432"></a><a name="p104447017432"></a>servers_links</p>
</td>
<td class="cellrowborder" valign="top" width="31.26687331266873%" headers="mcps1.2.4.1.2 "><p id="p1749328217432"><a name="p1749328217432"></a><a name="p1749328217432"></a>列表数据结构</p>
</td>
<td class="cellrowborder" valign="top" width="48.555144485551445%" headers="mcps1.2.4.1.3 "><p id="p766970517432"><a name="p766970517432"></a><a name="p766970517432"></a>分页查询时，查询下一页数据链接，详情请参见<a href="#table16539321">表7</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  servers字段数据结构说明

<a name="table1549812072413"></a>
<table><thead align="left"><tr id="row1548112082413"><th class="cellrowborder" valign="top" width="28.000000000000004%" id="mcps1.2.4.1.1"><p id="p17285123172813"><a name="p17285123172813"></a><a name="p17285123172813"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17%" id="mcps1.2.4.1.2"><p id="p83011731182817"><a name="p83011731182817"></a><a name="p83011731182817"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.00000000000001%" id="mcps1.2.4.1.3"><p id="p1230114317281"><a name="p1230114317281"></a><a name="p1230114317281"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1548212052418"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p7482120192416"><a name="p7482120192416"></a><a name="p7482120192416"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p948210207248"><a name="p948210207248"></a><a name="p948210207248"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p34821220112420"><a name="p34821220112420"></a><a name="p34821220112420"></a>云服务器名称。</p>
</td>
</tr>
<tr id="row174821720142411"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p6482320202414"><a name="p6482320202414"></a><a name="p6482320202414"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p1348242010244"><a name="p1348242010244"></a><a name="p1348242010244"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p548272092414"><a name="p548272092414"></a><a name="p548272092414"></a>云服务器唯一标识ID。</p>
</td>
</tr>
<tr id="row19483920182415"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p1482520122415"><a name="p1482520122415"></a><a name="p1482520122415"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p11483162010242"><a name="p11483162010242"></a><a name="p11483162010242"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p7483620172414"><a name="p7483620172414"></a><a name="p7483620172414"></a>云服务器当前状态信息。</p>
<p id="p15483172014245"><a name="p15483172014245"></a><a name="p15483172014245"></a>取值范围：</p>
<p id="p248332062411"><a name="p248332062411"></a><a name="p248332062411"></a>ACTIVE， BUILD，DELETED，ERROR，HARD_REBOOT，MIGRATING，REBOOT，RESIZE，REVERT_RESIZE，SHELVED，SHELVED_OFFLOADED，SHUTOFF，UNKNOWN，VERIFY_RESIZE</p>
</td>
</tr>
<tr id="row204831920202413"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p1148362014246"><a name="p1148362014246"></a><a name="p1148362014246"></a>created</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p9483112019245"><a name="p9483112019245"></a><a name="p9483112019245"></a>String:DateTime</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p9483120172419"><a name="p9483120172419"></a><a name="p9483120172419"></a>云服务器创建时间。</p>
</td>
</tr>
<tr id="row948452042410"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p12483202082411"><a name="p12483202082411"></a><a name="p12483202082411"></a>updated</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p124849201244"><a name="p124849201244"></a><a name="p124849201244"></a>String:DateTime</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p184846209241"><a name="p184846209241"></a><a name="p184846209241"></a>云服务器上一次更新时间。</p>
</td>
</tr>
<tr id="row1748412052419"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p1848482062410"><a name="p1848482062410"></a><a name="p1848482062410"></a>flavor</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p1484202016247"><a name="p1484202016247"></a><a name="p1484202016247"></a>字典数据结构</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p448472092419"><a name="p448472092419"></a><a name="p448472092419"></a>云服务器对应云服务器规格信息。</p>
<p id="p1089830141117"><a name="p1089830141117"></a><a name="p1089830141117"></a>详情请参见<a href="#table19588408">表5</a>。</p>
</td>
</tr>
<tr id="row4485152072417"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p548452052412"><a name="p548452052412"></a><a name="p548452052412"></a>image</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p19484620132419"><a name="p19484620132419"></a><a name="p19484620132419"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p248452052410"><a name="p248452052410"></a><a name="p248452052410"></a>云服务器镜像信息。</p>
<p id="p1485162013249"><a name="p1485162013249"></a><a name="p1485162013249"></a>对于镜像创建的弹性云服务器属性通常返回镜像ID和链接，对于卷创建的弹性云服务器，该属性为空字符串。</p>
<p id="p648512072420"><a name="p648512072420"></a><a name="p648512072420"></a>要获取镜像信息，请使用metadata中相关属性。</p>
</td>
</tr>
<tr id="row154851208245"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p10485220202414"><a name="p10485220202414"></a><a name="p10485220202414"></a>tenant_id</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p648512014246"><a name="p648512014246"></a><a name="p648512014246"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p10485182017246"><a name="p10485182017246"></a><a name="p10485182017246"></a>云服务器所属租户ID。</p>
</td>
</tr>
<tr id="row13486320172411"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p5485122042411"><a name="p5485122042411"></a><a name="p5485122042411"></a>key_name</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p11485202072415"><a name="p11485202072415"></a><a name="p11485202072415"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p1485120202420"><a name="p1485120202420"></a><a name="p1485120202420"></a>SSH密钥名称。</p>
</td>
</tr>
<tr id="row1548692072411"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p204861320122415"><a name="p204861320122415"></a><a name="p204861320122415"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p1448642072417"><a name="p1448642072417"></a><a name="p1448642072417"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p1448682020243"><a name="p1448682020243"></a><a name="p1448682020243"></a>云服务器所属用户ID。</p>
</td>
</tr>
<tr id="row748782022420"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p448611202242"><a name="p448611202242"></a><a name="p448611202242"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p848662017248"><a name="p848662017248"></a><a name="p848662017248"></a>字典数据结构</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p64871620152419"><a name="p64871620152419"></a><a name="p64871620152419"></a>云服务器元数据。</p>
</td>
</tr>
<tr id="row448720203246"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p4487122082413"><a name="p4487122082413"></a><a name="p4487122082413"></a>hostId</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p18487620152413"><a name="p18487620152413"></a><a name="p18487620152413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p9487112020247"><a name="p9487112020247"></a><a name="p9487112020247"></a>云服务器对应的主机ID。</p>
</td>
</tr>
<tr id="row9488102018244"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p5487182092415"><a name="p5487182092415"></a><a name="p5487182092415"></a>addresses</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p104877201246"><a name="p104877201246"></a><a name="p104877201246"></a>字典数据结构</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p548802020243"><a name="p548802020243"></a><a name="p548802020243"></a>云服务器对应的网络地址信息。</p>
<p id="p11732124819142"><a name="p11732124819142"></a><a name="p11732124819142"></a>详情请参见<a href="#table3730161">表6</a>。</p>
</td>
</tr>
<tr id="row7488142016248"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p148872020247"><a name="p148872020247"></a><a name="p148872020247"></a>security_groups</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p154882201243"><a name="p154882201243"></a><a name="p154882201243"></a>列表数据结构</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p1648872013244"><a name="p1648872013244"></a><a name="p1648872013244"></a>云服务器所属安全组列表。</p>
<p id="p14944151210151"><a name="p14944151210151"></a><a name="p14944151210151"></a>详情请参见<a href="#table761507165933">表10</a></p>
</td>
</tr>
<tr id="row15488820152416"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p548811201248"><a name="p548811201248"></a><a name="p548811201248"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p7488620102418"><a name="p7488620102418"></a><a name="p7488620102418"></a>列表数据结构</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p1488122019249"><a name="p1488122019249"></a><a name="p1488122019249"></a>云服务器相关快捷链接信息。</p>
<p id="p1359134614158"><a name="p1359134614158"></a><a name="p1359134614158"></a>详情请参见<a href="#table16539321">表7</a></p>
</td>
</tr>
<tr id="row104894203243"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p1448882052415"><a name="p1448882052415"></a><a name="p1448882052415"></a>OS-DCF:diskConfig</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p14488820122413"><a name="p14488820122413"></a><a name="p14488820122413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p2048819204245"><a name="p2048819204245"></a><a name="p2048819204245"></a>扩展属性，磁盘配置方式。对镜像启动云服务器生效。</p>
<p id="p13489132012240"><a name="p13489132012240"></a><a name="p13489132012240"></a>取值范围：</p>
<a name="ul948972012249"></a><a name="ul948972012249"></a><ul id="ul948972012249"><li>AUTO: API使用单个分区构建目标磁盘大小的云服务器。 API会自动调整文件系统以适应整个分区。</li><li>MANUAL：API使用源映像中的分区方案和文件系统构建服务器。如果目标磁盘较大，则API不分区剩余的磁盘空间。</li></ul>
</td>
</tr>
<tr id="row17489142082419"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p2489132011245"><a name="p2489132011245"></a><a name="p2489132011245"></a>OS-EXT-AZ:availability_zone</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p11489320152410"><a name="p11489320152410"></a><a name="p11489320152410"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p144898207242"><a name="p144898207242"></a><a name="p144898207242"></a>扩展属性，可用分区编码。</p>
</td>
</tr>
<tr id="row13490320112416"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p12489162013248"><a name="p12489162013248"></a><a name="p12489162013248"></a>OS-EXT-SRV-ATTR:host</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p1749010206242"><a name="p1749010206242"></a><a name="p1749010206242"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p20490172020241"><a name="p20490172020241"></a><a name="p20490172020241"></a>扩展属性，云服务器宿主名称。</p>
</td>
</tr>
<tr id="row44918205242"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p17490162014240"><a name="p17490162014240"></a><a name="p17490162014240"></a>OS-EXT-SRV-ATTR:hypervisor_hostname</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p1749015202242"><a name="p1749015202242"></a><a name="p1749015202242"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p7490020162410"><a name="p7490020162410"></a><a name="p7490020162410"></a>扩展属性，hypervisor主机名。</p>
</td>
</tr>
<tr id="row2491420172417"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p1949113206248"><a name="p1949113206248"></a><a name="p1949113206248"></a>OS-EXT-SRV-ATTR:instance_name</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p1149192022415"><a name="p1149192022415"></a><a name="p1149192022415"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p104919201241"><a name="p104919201241"></a><a name="p104919201241"></a>扩展属性，云服务器实例ID。</p>
</td>
</tr>
<tr id="row14492520122419"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p5491142013241"><a name="p5491142013241"></a><a name="p5491142013241"></a>OS-EXT-STS:power_state</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p9491120132410"><a name="p9491120132410"></a><a name="p9491120132410"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p149116209246"><a name="p149116209246"></a><a name="p149116209246"></a>扩展属性，云服务器电源状态。</p>
<p id="p1749162013245"><a name="p1749162013245"></a><a name="p1749162013245"></a>取值范围：0，1，2，3，4</p>
<a name="ul154921920112413"></a><a name="ul154921920112413"></a><ul id="ul154921920112413"><li>0 : pending</li><li>1 : running</li><li>2 : paused</li><li>3 : shutdown</li><li>4 : crashed</li></ul>
</td>
</tr>
<tr id="row12492182018247"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p16492142014240"><a name="p16492142014240"></a><a name="p16492142014240"></a>OS-EXT-STS:task_state</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p12492132082410"><a name="p12492132082410"></a><a name="p12492132082410"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p6492120102416"><a name="p6492120102416"></a><a name="p6492120102416"></a>扩展属性，云服务器任务状态。</p>
<p id="p549218206246"><a name="p549218206246"></a><a name="p549218206246"></a>取值范围：</p>
<p id="p849272012416"><a name="p849272012416"></a><a name="p849272012416"></a>SHOUTOFF，RESIZE，REBUILD，VERIFY_RESIZE，REVERT_RESIZE，PAUSED，MIGRATING，SUSPENDED，RESCUE，ERROR,DELETED,SHELVED,SHELVED_OFFLOADED</p>
</td>
</tr>
<tr id="row104922209248"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p154927206241"><a name="p154927206241"></a><a name="p154927206241"></a>OS-EXT-STS:vm_state</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p204926207240"><a name="p204926207240"></a><a name="p204926207240"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p14492112013243"><a name="p14492112013243"></a><a name="p14492112013243"></a>扩展属性，云服务器状态。</p>
<p id="p184927203240"><a name="p184927203240"></a><a name="p184927203240"></a>取值范围：</p>
<p id="p1149222082418"><a name="p1149222082418"></a><a name="p1149222082418"></a>ACTIVE,BUILDING,STOPPED,PAUSED,SUSPENDED,RESCUED,ERROR,DELETED,SOFT_DELETED,SHELVED,SHELVED_OFFLOADED</p>
</td>
</tr>
<tr id="row6492220132410"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p194926206240"><a name="p194926206240"></a><a name="p194926206240"></a>OS-SRV-USG:launched_at</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p04925208249"><a name="p04925208249"></a><a name="p04925208249"></a>String:DateTime</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p1649212011249"><a name="p1649212011249"></a><a name="p1649212011249"></a>扩展属性，云服务器启动时间。</p>
</td>
</tr>
<tr id="row7493120142419"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p7492202012241"><a name="p7492202012241"></a><a name="p7492202012241"></a>OS-SRV-USG:terminated_at</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p11492122013248"><a name="p11492122013248"></a><a name="p11492122013248"></a>String:DateTime</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p849212201243"><a name="p849212201243"></a><a name="p849212201243"></a>扩展属性，云服务器关闭时间。</p>
</td>
</tr>
<tr id="row1749342013247"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p15493172092417"><a name="p15493172092417"></a><a name="p15493172092417"></a>os-extended-volumes:volumes_attached</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p149302062415"><a name="p149302062415"></a><a name="p149302062415"></a>列表数据结构</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p18493102022412"><a name="p18493102022412"></a><a name="p18493102022412"></a>云服务器挂载的云磁盘信息。</p>
<p id="p382215381616"><a name="p382215381616"></a><a name="p382215381616"></a>详情请参见<a href="#table20591095122442">表9</a>。</p>
</td>
</tr>
<tr id="row949312017246"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p749372082418"><a name="p749372082418"></a><a name="p749372082418"></a>tags</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p14493420142420"><a name="p14493420142420"></a><a name="p14493420142420"></a>String列表</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p1149310203247"><a name="p1149310203247"></a><a name="p1149310203247"></a>云服务器的标签列表。</p>
<div class="p" id="p7300949059"><a name="p7300949059"></a><a name="p7300949059"></a>系统近期对标签功能进行了升级，升级后，返回的tag值遵循如下规则：<a name="ul871515496611"></a><a name="ul871515496611"></a><ul id="ul871515496611"><li>key与value使用“=”连接，如“key=value”。</li><li>如果value为空字符串，则仅返回key。</li></ul>
</div>
</td>
</tr>
<tr id="row1264933513916"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p1253710242210"><a name="p1253710242210"></a><a name="p1253710242210"></a>locked</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p1653720241521"><a name="p1653720241521"></a><a name="p1653720241521"></a>boolean</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p18537624422"><a name="p18537624422"></a><a name="p18537624422"></a>当云服务器被锁时为True，否则为False。</p>
<p id="p10742257355"><a name="p10742257355"></a><a name="p10742257355"></a>微版本2.9后支持</p>
</td>
</tr>
<tr id="row249416203244"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p1149317202246"><a name="p1149317202246"></a><a name="p1149317202246"></a>accessIPv4</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p3493182016241"><a name="p3493182016241"></a><a name="p3493182016241"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p449319209247"><a name="p449319209247"></a><a name="p449319209247"></a>预留属性。</p>
</td>
</tr>
<tr id="row1249422052417"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p749492020246"><a name="p749492020246"></a><a name="p749492020246"></a>accessIPv6</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p1249442052418"><a name="p1249442052418"></a><a name="p1249442052418"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p12494132010248"><a name="p12494132010248"></a><a name="p12494132010248"></a>预留属性。</p>
</td>
</tr>
<tr id="row24951820172418"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p19494420102411"><a name="p19494420102411"></a><a name="p19494420102411"></a>config_drive</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p194951720152416"><a name="p194951720152416"></a><a name="p194951720152416"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p184951720102410"><a name="p184951720102410"></a><a name="p184951720102410"></a>预留属性。</p>
</td>
</tr>
<tr id="row549602016244"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p249562062415"><a name="p249562062415"></a><a name="p249562062415"></a>evsOpts</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p64951620142416"><a name="p64951620142416"></a><a name="p64951620142416"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p1749562012412"><a name="p1749562012412"></a><a name="p1749562012412"></a>预留属性。</p>
</td>
</tr>
<tr id="row194969205247"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p1349618206247"><a name="p1349618206247"></a><a name="p1349618206247"></a>hyperThreadAffinity</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p14496152013243"><a name="p14496152013243"></a><a name="p14496152013243"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p14496182010242"><a name="p14496182010242"></a><a name="p14496182010242"></a>预留属性。</p>
</td>
</tr>
<tr id="row17497162042414"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p5496102012419"><a name="p5496102012419"></a><a name="p5496102012419"></a>numaOpts</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p2496720152410"><a name="p2496720152410"></a><a name="p2496720152410"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p1149619205242"><a name="p1149619205242"></a><a name="p1149619205242"></a>预留属性。</p>
</td>
</tr>
<tr id="row4497132062416"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p84971020122411"><a name="p84971020122411"></a><a name="p84971020122411"></a>progress</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p11497132082416"><a name="p11497132082416"></a><a name="p11497132082416"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p6497142015243"><a name="p6497142015243"></a><a name="p6497142015243"></a>预留属性。</p>
</td>
</tr>
<tr id="row7498420162414"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="p1049792012412"><a name="p1049792012412"></a><a name="p1049792012412"></a>vcpuAffinity</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.2 "><p id="p14497820182417"><a name="p14497820182417"></a><a name="p14497820182417"></a>Integer列表结构</p>
</td>
<td class="cellrowborder" valign="top" width="55.00000000000001%" headers="mcps1.2.4.1.3 "><p id="p94971820112410"><a name="p94971820112410"></a><a name="p94971820112410"></a>预留属性。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  flavor字段数据结构说明

<a name="table19588408"></a>
<table><thead align="left"><tr id="row65668512"><th class="cellrowborder" valign="top" width="21.37%" id="mcps1.2.4.1.1"><p id="p2743203852915"><a name="p2743203852915"></a><a name="p2743203852915"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.2%" id="mcps1.2.4.1.2"><p id="p3743193822918"><a name="p3743193822918"></a><a name="p3743193822918"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.43%" id="mcps1.2.4.1.3"><p id="p147431638122913"><a name="p147431638122913"></a><a name="p147431638122913"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row54114449"><td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.4.1.1 "><p id="p21194271"><a name="p21194271"></a><a name="p21194271"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="30.2%" headers="mcps1.2.4.1.2 "><p id="p6046963"><a name="p6046963"></a><a name="p6046963"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.43%" headers="mcps1.2.4.1.3 "><p id="p20041994"><a name="p20041994"></a><a name="p20041994"></a>云服务器类型ID。</p>
</td>
</tr>
<tr id="row46160221"><td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.4.1.1 "><p id="p47990424"><a name="p47990424"></a><a name="p47990424"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="30.2%" headers="mcps1.2.4.1.2 "><p id="p57492083"><a name="p57492083"></a><a name="p57492083"></a>列表数据结构</p>
</td>
<td class="cellrowborder" valign="top" width="48.43%" headers="mcps1.2.4.1.3 "><p id="p35797372"><a name="p35797372"></a><a name="p35797372"></a>云服务器类型相关快捷链接信息，详情请参见<a href="#table16539321">表7</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  addresses字段数据结构说明

<a name="table3730161"></a>
<table><thead align="left"><tr id="row20014316"><th class="cellrowborder" valign="top" width="21.497850214978502%" id="mcps1.2.4.1.1"><p id="p8834164002918"><a name="p8834164002918"></a><a name="p8834164002918"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.947005299470053%" id="mcps1.2.4.1.2"><p id="p6834340112912"><a name="p6834340112912"></a><a name="p6834340112912"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.555144485551445%" id="mcps1.2.4.1.3"><p id="p18491640162916"><a name="p18491640162916"></a><a name="p18491640162916"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row57432766"><td class="cellrowborder" valign="top" width="21.497850214978502%" headers="mcps1.2.4.1.1 "><p id="p2057412833316"><a name="p2057412833316"></a><a name="p2057412833316"></a>弹性云服务器所属网络的名称。</p>
</td>
<td class="cellrowborder" valign="top" width="29.947005299470053%" headers="mcps1.2.4.1.2 "><p id="p4439518115623"><a name="p4439518115623"></a><a name="p4439518115623"></a>列表数据结构</p>
</td>
<td class="cellrowborder" valign="top" width="48.555144485551445%" headers="mcps1.2.4.1.3 "><p id="p19891184119819"><a name="p19891184119819"></a><a name="p19891184119819"></a>弹性云服务器所属网络信息。</p>
<a name="ul1197110522819"></a><a name="ul1197110522819"></a><ul id="ul1197110522819"><li>key为网络名名称，如“demo_net”。</li><li>value为网络详细信息。</li></ul>
<p id="p204137567134"><a name="p204137567134"></a><a name="p204137567134"></a>详情请参见<a href="#table1656029015527">表8</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  servers\_links、links字段数据结构说明

<a name="table16539321"></a>
<table><thead align="left"><tr id="row4585366"><th class="cellrowborder" valign="top" width="21.61216121612161%" id="mcps1.2.4.1.1"><p id="p1475445290"><a name="p1475445290"></a><a name="p1475445290"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.073007300730076%" id="mcps1.2.4.1.2"><p id="p14634442298"><a name="p14634442298"></a><a name="p14634442298"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.31483148314831%" id="mcps1.2.4.1.3"><p id="p36312446294"><a name="p36312446294"></a><a name="p36312446294"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row14455526"><td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.4.1.1 "><p id="p30046962"><a name="p30046962"></a><a name="p30046962"></a>rel</p>
</td>
<td class="cellrowborder" valign="top" width="30.073007300730076%" headers="mcps1.2.4.1.2 "><p id="p39387099"><a name="p39387099"></a><a name="p39387099"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.31483148314831%" headers="mcps1.2.4.1.3 "><p id="p36238473"><a name="p36238473"></a><a name="p36238473"></a>快捷链接标记名称。</p>
</td>
</tr>
<tr id="row57710802"><td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.4.1.1 "><p id="p44063391"><a name="p44063391"></a><a name="p44063391"></a>href</p>
</td>
<td class="cellrowborder" valign="top" width="30.073007300730076%" headers="mcps1.2.4.1.2 "><p id="p62035831"><a name="p62035831"></a><a name="p62035831"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.31483148314831%" headers="mcps1.2.4.1.3 "><p id="p58846418"><a name="p58846418"></a><a name="p58846418"></a>对应快捷链接。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  弹性云服务器所属网络信息数据结构说明

<a name="table1656029015527"></a>
<table><thead align="left"><tr id="row2645284715527"><th class="cellrowborder" valign="top" width="36.720000000000006%" id="mcps1.2.4.1.1"><p id="p99491446132918"><a name="p99491446132918"></a><a name="p99491446132918"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.719999999999999%" id="mcps1.2.4.1.2"><p id="p49641746132913"><a name="p49641746132913"></a><a name="p49641746132913"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.559999999999995%" id="mcps1.2.4.1.3"><p id="p896474622910"><a name="p896474622910"></a><a name="p896474622910"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5009697415527"><td class="cellrowborder" valign="top" width="36.720000000000006%" headers="mcps1.2.4.1.1 "><p id="p3132311415527"><a name="p3132311415527"></a><a name="p3132311415527"></a>addr</p>
</td>
<td class="cellrowborder" valign="top" width="14.719999999999999%" headers="mcps1.2.4.1.2 "><p id="p5414433915527"><a name="p5414433915527"></a><a name="p5414433915527"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.559999999999995%" headers="mcps1.2.4.1.3 "><p id="p2361534415527"><a name="p2361534415527"></a><a name="p2361534415527"></a>IP地址信息。</p>
</td>
</tr>
<tr id="row1121151015527"><td class="cellrowborder" valign="top" width="36.720000000000006%" headers="mcps1.2.4.1.1 "><p id="p3571711715527"><a name="p3571711715527"></a><a name="p3571711715527"></a>version</p>
</td>
<td class="cellrowborder" valign="top" width="14.719999999999999%" headers="mcps1.2.4.1.2 "><p id="p740535615527"><a name="p740535615527"></a><a name="p740535615527"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="48.559999999999995%" headers="mcps1.2.4.1.3 "><p id="p6296298815527"><a name="p6296298815527"></a><a name="p6296298815527"></a>IP地址类型，值为4或6。</p>
<a name="ul2979598615527"></a><a name="ul2979598615527"></a><ul id="ul2979598615527"><li>4：IP地址类型是IPv4</li><li>6：IP地址类型是IPv6</li></ul>
</td>
</tr>
<tr id="row3913338616494"><td class="cellrowborder" valign="top" width="36.720000000000006%" headers="mcps1.2.4.1.1 "><p id="p37919028165012"><a name="p37919028165012"></a><a name="p37919028165012"></a>OS-EXT-IPS-MAC:mac_addr</p>
</td>
<td class="cellrowborder" valign="top" width="14.719999999999999%" headers="mcps1.2.4.1.2 "><p id="p51542402165012"><a name="p51542402165012"></a><a name="p51542402165012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.559999999999995%" headers="mcps1.2.4.1.3 "><p id="p14185000165012"><a name="p14185000165012"></a><a name="p14185000165012"></a>扩展属性，MAC地址。</p>
</td>
</tr>
<tr id="row5993434716495"><td class="cellrowborder" valign="top" width="36.720000000000006%" headers="mcps1.2.4.1.1 "><p id="p6100298165012"><a name="p6100298165012"></a><a name="p6100298165012"></a>OS-EXT-IPS:type</p>
</td>
<td class="cellrowborder" valign="top" width="14.719999999999999%" headers="mcps1.2.4.1.2 "><p id="p24362133165012"><a name="p24362133165012"></a><a name="p24362133165012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.559999999999995%" headers="mcps1.2.4.1.3 "><p id="p27175732165012"><a name="p27175732165012"></a><a name="p27175732165012"></a>扩展属性，分配IP地址方式。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  os-extended-volumes:volumes\_attached字段数据结构说明

<a name="table20591095122442"></a>
<table><thead align="left"><tr id="row46969160122442"><th class="cellrowborder" valign="top" width="36.533653365336534%" id="mcps1.2.4.1.1"><p id="p8475185013292"><a name="p8475185013292"></a><a name="p8475185013292"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.781378137813782%" id="mcps1.2.4.1.2"><p id="p849025062918"><a name="p849025062918"></a><a name="p849025062918"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.684968496849685%" id="mcps1.2.4.1.3"><p id="p6490750122918"><a name="p6490750122918"></a><a name="p6490750122918"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row22997982122442"><td class="cellrowborder" valign="top" width="36.533653365336534%" headers="mcps1.2.4.1.1 "><p id="p50897247122442"><a name="p50897247122442"></a><a name="p50897247122442"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="13.781378137813782%" headers="mcps1.2.4.1.2 "><p id="p29036308122442"><a name="p29036308122442"></a><a name="p29036308122442"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.684968496849685%" headers="mcps1.2.4.1.3 "><p id="p3130725122442"><a name="p3130725122442"></a><a name="p3130725122442"></a>云磁盘ID。</p>
</td>
</tr>
</tbody>
</table>

**表 10**  security\_groups字段数据结构说明

<a name="table761507165933"></a>
<table><thead align="left"><tr id="row29958070165933"><th class="cellrowborder" valign="top" width="36.533653365336534%" id="mcps1.2.4.1.1"><p id="p1550320527296"><a name="p1550320527296"></a><a name="p1550320527296"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.781378137813782%" id="mcps1.2.4.1.2"><p id="p650355252917"><a name="p650355252917"></a><a name="p650355252917"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.684968496849685%" id="mcps1.2.4.1.3"><p id="p14518145202914"><a name="p14518145202914"></a><a name="p14518145202914"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row29572324165933"><td class="cellrowborder" valign="top" width="36.533653365336534%" headers="mcps1.2.4.1.1 "><p id="p46548026165933"><a name="p46548026165933"></a><a name="p46548026165933"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="13.781378137813782%" headers="mcps1.2.4.1.2 "><p id="p12293798165933"><a name="p12293798165933"></a><a name="p12293798165933"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.684968496849685%" headers="mcps1.2.4.1.3 "><p id="p52012230"><a name="p52012230"></a><a name="p52012230"></a>安全组名称或者uuid。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section1630232142117"></a>

-   响应示例

    ```
    {
        "servers": [
            {
                "addresses": {
                    "68269e6e-4a27-441b-8029-35373ad50bd9": [
                        {
                            "addr": "192.168.0.3", 
                            "version": 4
                        }
                    ]
                }, 
                "created": "2012-09-07T16:56:37Z", 
                "flavor": {
                    "id": "1", 
                    "links": [
                        {
                            "href": "http://openstack.example.com/openstack/flavors/1", 
                            "rel": "bookmark"
                        }
                    ]
                }, 
                "hostId": "16d193736a5cfdb60c697ca27ad071d6126fa13baeb670fc9d10645e", 
                "id": "05184ba3-00ba-4fbc-b7a2-03b62b884931", 
                "image": "", 
                "links": [
                    {
                        "href": "http://openstack.example.com/v2/openstack/servers/05184ba3-00ba-4fbc-b7a2-03b62b884931", 
                        "rel": "self"
                    }, 
                    {
                        "href": "http://openstack.example.com/openstack/servers/05184ba3-00ba-4fbc-b7a2-03b62b884931", 
                        "rel": "bookmark"
                    }
                ], 
                "metadata": {},                         
                "name": "new-server-test", 
                "progress": 0, 
                "status": "ACTIVE", 
                "tenant_id": "openstack", 
                "updated": "2012-09-07T16:56:37Z", 
                "user_id": "fake"
            }
        ]
    }
    ```


## 返回值<a name="section25329374"></a>

请参考[通用请求返回值](通用请求返回值.md)。

