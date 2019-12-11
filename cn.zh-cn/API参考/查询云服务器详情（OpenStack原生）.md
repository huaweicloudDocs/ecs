# 查询云服务器详情<a name="ZH-CN_TOPIC_0020212690"></a>

## 功能介绍<a name="section11242227"></a>

根据云服务器ID，查询云服务器的详细信息。

## URI<a name="section34071180"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}

参数说明请参见[表1](#table32475667)。

**表 1**  参数说明

<a name="table32475667"></a>
<table><thead align="left"><tr id="row44937496"><th class="cellrowborder" valign="top" width="22.24%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.87%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.88999999999999%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1664874"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="p637140"><a name="p637140"></a><a name="p637140"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="p51608407"><a name="p51608407"></a><a name="p51608407"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row41565035"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="p11324657"><a name="p11324657"></a><a name="p11324657"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="p44882061"><a name="p44882061"></a><a name="p44882061"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="p11568292"><a name="p11568292"></a><a name="p11568292"></a>云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section38205169"></a>

无

## 响应消息<a name="section8302201"></a>

响应参数如[表2](#table44736746)所示。

**表 2**  响应参数

<a name="table44736746"></a>
<table><thead align="left"><tr id="row8242429"><th class="cellrowborder" valign="top" width="21.11%" id="mcps1.2.4.1.1"><p id="p63657004"><a name="p63657004"></a><a name="p63657004"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.39%" id="mcps1.2.4.1.2"><p id="p35147813"><a name="p35147813"></a><a name="p35147813"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.5%" id="mcps1.2.4.1.3"><p id="p28400574"><a name="p28400574"></a><a name="p28400574"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row18745119"><td class="cellrowborder" valign="top" width="21.11%" headers="mcps1.2.4.1.1 "><p id="p41959665"><a name="p41959665"></a><a name="p41959665"></a>server</p>
</td>
<td class="cellrowborder" valign="top" width="29.39%" headers="mcps1.2.4.1.2 "><p id="p16804102"><a name="p16804102"></a><a name="p16804102"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="49.5%" headers="mcps1.2.4.1.3 "><p id="p36377578"><a name="p36377578"></a><a name="p36377578"></a>云服务器信息，详情请参见<a href="#table26210179">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  server字段数据结构说明

<a name="table26210179"></a>
<table><thead align="left"><tr id="row30559396"><th class="cellrowborder" valign="top" width="24.752475247524753%" id="mcps1.2.4.1.1"><p id="p59391972"><a name="p59391972"></a><a name="p59391972"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.762376237623762%" id="mcps1.2.4.1.2"><p id="p36664945"><a name="p36664945"></a><a name="p36664945"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="51.48514851485149%" id="mcps1.2.4.1.3"><p id="p17070607"><a name="p17070607"></a><a name="p17070607"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row19417740"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p29333120"><a name="p29333120"></a><a name="p29333120"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p53487552"><a name="p53487552"></a><a name="p53487552"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p37524445"><a name="p37524445"></a><a name="p37524445"></a>云服务器名称。</p>
</td>
</tr>
<tr id="row2175687"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p42012952"><a name="p42012952"></a><a name="p42012952"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p30874046"><a name="p30874046"></a><a name="p30874046"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p17769829"><a name="p17769829"></a><a name="p17769829"></a>云服务器唯一标识。</p>
</td>
</tr>
<tr id="row25710733"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p2194613"><a name="p2194613"></a><a name="p2194613"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p37560342"><a name="p37560342"></a><a name="p37560342"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p22488863"><a name="p22488863"></a><a name="p22488863"></a>云服务器当前状态信息。</p>
<p id="p17952198145121"><a name="p17952198145121"></a><a name="p17952198145121"></a>取值范围：</p>
<p id="p53652898145152"><a name="p53652898145152"></a><a name="p53652898145152"></a>ACTIVE、BUILD、DELETED、ERROR、HARD_REBOOT、MIGRATING、PAUSED、REBOOT、REBUILD、RESIZE、REVERT_RESIZE、SHUTOFF、SHELVED、SHELVED_OFFLOADED、SOFT_DELETED、SUSPENDED、VERIFY_RESIZE</p>
<p id="p5103192105518"><a name="p5103192105518"></a><a name="p5103192105518"></a>弹性云服务器状态说明请参考<a href="云服务器状态.md">云服务器状态</a>。</p>
</td>
</tr>
<tr id="row1073183"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p19818984"><a name="p19818984"></a><a name="p19818984"></a>created</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p42487544"><a name="p42487544"></a><a name="p42487544"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p18939022"><a name="p18939022"></a><a name="p18939022"></a>云服务器创建时间。时间格式例如：2019-05-22T07:48:19Z</p>
</td>
</tr>
<tr id="row36233478"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p49230602"><a name="p49230602"></a><a name="p49230602"></a>updated</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p7022941"><a name="p7022941"></a><a name="p7022941"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p31987323"><a name="p31987323"></a><a name="p31987323"></a>云服务器上一次更新时间。时间格式例如：2019-05-22T07:48:19Z</p>
</td>
</tr>
<tr id="row19450451"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p31982717"><a name="p31982717"></a><a name="p31982717"></a>flavor</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p56299846"><a name="p56299846"></a><a name="p56299846"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p39071968"><a name="p39071968"></a><a name="p39071968"></a>云服务器规格信息，详情请参见<a href="#table29241163">表4</a>。</p>
</td>
</tr>
<tr id="row16103393"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p29306417"><a name="p29306417"></a><a name="p29306417"></a>image</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p12507614"><a name="p12507614"></a><a name="p12507614"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p58354673"><a name="p58354673"></a><a name="p58354673"></a>云服务器镜像信息，对镜像创的弹性云服务器该属性通常返回镜像id和链接。</p>
<p id="p5571104842212"><a name="p5571104842212"></a><a name="p5571104842212"></a>详情请参见<a href="#table1080891111402">表5</a>。</p>
</td>
</tr>
<tr id="row55430014"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p60646173"><a name="p60646173"></a><a name="p60646173"></a>tenant_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p11089280"><a name="p11089280"></a><a name="p11089280"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p25816468"><a name="p25816468"></a><a name="p25816468"></a>云服务器所属租户ID。即项目id，和project_id表示的是一个概念。</p>
</td>
</tr>
<tr id="row289486817056"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p4349571017124"><a name="p4349571017124"></a><a name="p4349571017124"></a>key_name</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p3349163017124"><a name="p3349163017124"></a><a name="p3349163017124"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p2846749017124"><a name="p2846749017124"></a><a name="p2846749017124"></a>SSH密钥名称。</p>
</td>
</tr>
<tr id="row31021623"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p29723549"><a name="p29723549"></a><a name="p29723549"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p64958874"><a name="p64958874"></a><a name="p64958874"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p27177474"><a name="p27177474"></a><a name="p27177474"></a>云服务器所属用户ID。</p>
</td>
</tr>
<tr id="row43270676"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p15263883"><a name="p15263883"></a><a name="p15263883"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p19916823"><a name="p19916823"></a><a name="p19916823"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p23849822"><a name="p23849822"></a><a name="p23849822"></a>云服务器元数据。</p>
</td>
</tr>
<tr id="row13321813"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p5325067"><a name="p5325067"></a><a name="p5325067"></a>hostId</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p41156139"><a name="p41156139"></a><a name="p41156139"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p45312999"><a name="p45312999"></a><a name="p45312999"></a>云服务器对应的主机ID。</p>
</td>
</tr>
<tr id="row5163807"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p15615252"><a name="p15615252"></a><a name="p15615252"></a>addresses</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p43546944"><a name="p43546944"></a><a name="p43546944"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p3229562"><a name="p3229562"></a><a name="p3229562"></a>云服务器对应的网络地址信息，详情请参见<a href="#table36337966">表6</a>。</p>
</td>
</tr>
<tr id="row2817586217053"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p2741526417147"><a name="p2741526417147"></a><a name="p2741526417147"></a>security_groups</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p604393417147"><a name="p604393417147"></a><a name="p604393417147"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p4395185217147"><a name="p4395185217147"></a><a name="p4395185217147"></a>云服务器所属安全组列表，详情请参见<a href="#table2053207517233">表10</a>。</p>
</td>
</tr>
<tr id="row29066061"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p5540732"><a name="p5540732"></a><a name="p5540732"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p46852469"><a name="p46852469"></a><a name="p46852469"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p64147070"><a name="p64147070"></a><a name="p64147070"></a>云服务器相关标记快捷链接信息，详情请参见<a href="#table35230296">表7</a>。</p>
</td>
</tr>
<tr id="row5544204718389"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p749372082418"><a name="p749372082418"></a><a name="p749372082418"></a>tags</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p14493420142420"><a name="p14493420142420"></a><a name="p14493420142420"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p1620274611333"><a name="p1620274611333"></a><a name="p1620274611333"></a>云服务器的标签列表。</p>
<p id="p1149310203247"><a name="p1149310203247"></a><a name="p1149310203247"></a>微版本2.26，如果不使用微版本查询，响应中无tags字段。</p>
<div class="p" id="p7300949059"><a name="p7300949059"></a><a name="p7300949059"></a>系统近期对标签功能进行了升级，升级后，返回的tag值遵循如下规则：<a name="zh-cn_topic_0020212689_ul871515496611"></a><a name="zh-cn_topic_0020212689_ul871515496611"></a><ul id="zh-cn_topic_0020212689_ul871515496611"><li>key与value使用“=”连接，如“key=value”。</li><li>如果value为空字符串，则仅返回key。</li></ul>
</div>
</td>
</tr>
<tr id="row65689897121119"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p19281432121119"><a name="p19281432121119"></a><a name="p19281432121119"></a>OS-DCF:diskConfig</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p18292184121119"><a name="p18292184121119"></a><a name="p18292184121119"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p5271953121119"><a name="p5271953121119"></a><a name="p5271953121119"></a>扩展属性，磁盘配置方式。对镜像启动弹性云服务器生效。</p>
<p id="p978417418171"><a name="p978417418171"></a><a name="p978417418171"></a>取值范围：</p>
<p id="p12130413131719"><a name="p12130413131719"></a><a name="p12130413131719"></a>AUTO: API使用单个分区构建目标磁盘大小的弹性云服务器。 API会自动调整文件系统以适应整个分区。</p>
<p id="p156451257181916"><a name="p156451257181916"></a><a name="p156451257181916"></a>MANUAL:API使用源映像中的分区方案和文件系统构建服务器。如果目标磁盘较大，则API不分区剩余的磁盘空间。</p>
</td>
</tr>
<tr id="row26985914121125"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p38375386121125"><a name="p38375386121125"></a><a name="p38375386121125"></a>OS-EXT-AZ:availability_zone</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p21398534121125"><a name="p21398534121125"></a><a name="p21398534121125"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p55559719121125"><a name="p55559719121125"></a><a name="p55559719121125"></a>扩展属性，可用区编码。</p>
</td>
</tr>
<tr id="row8927030121127"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p52000861121127"><a name="p52000861121127"></a><a name="p52000861121127"></a>OS-EXT-SRV-ATTR:host</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p51320175121127"><a name="p51320175121127"></a><a name="p51320175121127"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p63293526121127"><a name="p63293526121127"></a><a name="p63293526121127"></a>扩展属性，云服务器宿主名称。</p>
</td>
</tr>
<tr id="row15809615121127"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p5510414121127"><a name="p5510414121127"></a><a name="p5510414121127"></a>OS-EXT-SRV-ATTR:hypervisor_hostname</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p43690378121127"><a name="p43690378121127"></a><a name="p43690378121127"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p49259690121127"><a name="p49259690121127"></a><a name="p49259690121127"></a>扩展属性，hypervisor主机名。</p>
</td>
</tr>
<tr id="row20844277121128"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p10664873121128"><a name="p10664873121128"></a><a name="p10664873121128"></a>OS-EXT-SRV-ATTR:instance_name</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p58548414121128"><a name="p58548414121128"></a><a name="p58548414121128"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p44801116121128"><a name="p44801116121128"></a><a name="p44801116121128"></a>扩展属性，云服务器ID。</p>
</td>
</tr>
<tr id="row66679123121128"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p32299911121128"><a name="p32299911121128"></a><a name="p32299911121128"></a>OS-EXT-STS:power_state</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p66155999121128"><a name="p66155999121128"></a><a name="p66155999121128"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p57035716121128"><a name="p57035716121128"></a><a name="p57035716121128"></a>扩展属性，云服务器电源状态。</p>
<p id="p2689123602310"><a name="p2689123602310"></a><a name="p2689123602310"></a>取值范围：0 , 1 , 2 , 3 , 4</p>
<a name="ul934453312193"></a><a name="ul934453312193"></a><ul id="ul934453312193"><li>0 : pending</li><li>1 : running</li><li>2 : paused</li><li>3 : shutdown</li><li>4 : crashed</li></ul>
</td>
</tr>
<tr id="row19260742121226"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p16616235121226"><a name="p16616235121226"></a><a name="p16616235121226"></a>OS-EXT-STS:task_state</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p3737772121226"><a name="p3737772121226"></a><a name="p3737772121226"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p34324147121226"><a name="p34324147121226"></a><a name="p34324147121226"></a>扩展属性，云服务器任务状态。</p>
<p id="p13922047162612"><a name="p13922047162612"></a><a name="p13922047162612"></a>取值范围请参考<a href="云服务器状态.md">云服务器状态</a>表3。</p>
</td>
</tr>
<tr id="row11298969121227"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p42801278121227"><a name="p42801278121227"></a><a name="p42801278121227"></a>OS-EXT-STS:vm_state</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p44351508121227"><a name="p44351508121227"></a><a name="p44351508121227"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p9331154012376"><a name="p9331154012376"></a><a name="p9331154012376"></a>扩展属性，云服务器状态。</p>
<p id="p35702402121227"><a name="p35702402121227"></a><a name="p35702402121227"></a>取值范围：</p>
<p id="p15276846381"><a name="p15276846381"></a><a name="p15276846381"></a>ACTIVE,BUILDING,STOPPED,RESIZED,PAUSED,SUSPENDED,RESCUED,ERROR,DELETED,SOFT_DELETED,SHELVED,SHELVED_OFFLOADED</p>
<p id="p69818711559"><a name="p69818711559"></a><a name="p69818711559"></a>弹性云服务器状态说明请参考<a href="云服务器状态.md">云服务器状态</a>。</p>
</td>
</tr>
<tr id="row59870257121227"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p17652642121227"><a name="p17652642121227"></a><a name="p17652642121227"></a>OS-SRV-USG:launched_at</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p20577863121227"><a name="p20577863121227"></a><a name="p20577863121227"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p56194184121227"><a name="p56194184121227"></a><a name="p56194184121227"></a>扩展属性，云服务器启动时间。时间格式例如：2019-05-22T07:48:19.000000</p>
</td>
</tr>
<tr id="row58808453121228"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p65864237121228"><a name="p65864237121228"></a><a name="p65864237121228"></a>OS-SRV-USG:terminated_at</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p33402957121228"><a name="p33402957121228"></a><a name="p33402957121228"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p21285006121228"><a name="p21285006121228"></a><a name="p21285006121228"></a>扩展属性，云服务器删除时间。时间格式例如：2019-05-22T07:48:19.000000</p>
</td>
</tr>
<tr id="row22845263122110"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p29403502122828"><a name="p29403502122828"></a><a name="p29403502122828"></a>os-extended-volumes:volumes_attached</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p32873451122828"><a name="p32873451122828"></a><a name="p32873451122828"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p6881526122828"><a name="p6881526122828"></a><a name="p6881526122828"></a>云服务器挂载的云磁盘信息，详情请参见<a href="#table10024873122234">表9</a>。</p>
</td>
</tr>
<tr id="row161046711504"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p43095310"><a name="zh-cn_topic_0057972887_p43095310"></a><a name="zh-cn_topic_0057972887_p43095310"></a>fault</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p1059226"><a name="zh-cn_topic_0057972887_p1059226"></a><a name="zh-cn_topic_0057972887_p1059226"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p37371779"><a name="zh-cn_topic_0057972887_p37371779"></a><a name="zh-cn_topic_0057972887_p37371779"></a>弹性云服务器故障信息。</p>
<p id="p14777766535"><a name="p14777766535"></a><a name="p14777766535"></a>可选参数，在弹性云服务器状态为ERROR且存在异常的情况下返回。</p>
<p id="p1688015424530"><a name="p1688015424530"></a><a name="p1688015424530"></a>详情参见 <a href="#table1075312230549">表11 fault字段数据结构说明</a>。</p>
</td>
</tr>
<tr id="row107959146481"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p57463526"><a name="zh-cn_topic_0057972887_p57463526"></a><a name="zh-cn_topic_0057972887_p57463526"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p24034004"><a name="zh-cn_topic_0057972887_p24034004"></a><a name="zh-cn_topic_0057972887_p24034004"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p48379233"><a name="zh-cn_topic_0057972887_p48379233"></a><a name="zh-cn_topic_0057972887_p48379233"></a>弹性云服务器的描述信息。</p>
<p id="p28201545155518"><a name="p28201545155518"></a><a name="p28201545155518"></a>微版本2.19后支持。</p>
</td>
</tr>
<tr id="row456252015488"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p58332432"><a name="zh-cn_topic_0057972887_p58332432"></a><a name="zh-cn_topic_0057972887_p58332432"></a>host_status</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p27306569"><a name="zh-cn_topic_0057972887_p27306569"></a><a name="zh-cn_topic_0057972887_p27306569"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p44841923"><a name="zh-cn_topic_0057972887_p44841923"></a><a name="zh-cn_topic_0057972887_p44841923"></a>nova-compute状态。</p>
<a name="zh-cn_topic_0057972887_ul924126"></a><a name="zh-cn_topic_0057972887_ul924126"></a><ul id="zh-cn_topic_0057972887_ul924126"><li>UP：服务正常</li><li>UNKNOWN：状态未知</li><li>DOWN：服务异常</li><li>MAINTENANCE：维护状态</li><li>空字符串：弹性云服务器无主机信息</li></ul>
<p id="p9178121814561"><a name="p9178121814561"></a><a name="p9178121814561"></a>微版本2.16后支持。</p>
</td>
</tr>
<tr id="row1043718233485"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p7131169"><a name="zh-cn_topic_0057972887_p7131169"></a><a name="zh-cn_topic_0057972887_p7131169"></a>OS-EXT-SRV-ATTR:hostname</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p40753854"><a name="zh-cn_topic_0057972887_p40753854"></a><a name="zh-cn_topic_0057972887_p40753854"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p24324288"><a name="zh-cn_topic_0057972887_p24324288"></a><a name="zh-cn_topic_0057972887_p24324288"></a>弹性云服务器的主机名。</p>
<p id="p3479627194317"><a name="p3479627194317"></a><a name="p3479627194317"></a>微版本2.3后支持。</p>
</td>
</tr>
<tr id="row1843752316486"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p6779396"><a name="zh-cn_topic_0057972887_p6779396"></a><a name="zh-cn_topic_0057972887_p6779396"></a>OS-EXT-SRV-ATTR:reservation_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p12260243"><a name="zh-cn_topic_0057972887_p12260243"></a><a name="zh-cn_topic_0057972887_p12260243"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p43041107"><a name="zh-cn_topic_0057972887_p43041107"></a><a name="zh-cn_topic_0057972887_p43041107"></a>批量创建场景，弹性云服务器的预留ID。</p>
<p id="p18137583436"><a name="p18137583436"></a><a name="p18137583436"></a>微版本2.3后支持。</p>
</td>
</tr>
<tr id="row12424182718489"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p54550808"><a name="zh-cn_topic_0057972887_p54550808"></a><a name="zh-cn_topic_0057972887_p54550808"></a>OS-EXT-SRV-ATTR:launch_index</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p56539341"><a name="zh-cn_topic_0057972887_p56539341"></a><a name="zh-cn_topic_0057972887_p56539341"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p43927036"><a name="zh-cn_topic_0057972887_p43927036"></a><a name="zh-cn_topic_0057972887_p43927036"></a>批量创建场景，弹性云服务器的启动顺序。</p>
<p id="p12601191124414"><a name="p12601191124414"></a><a name="p12601191124414"></a>微版本2.3后支持。</p>
</td>
</tr>
<tr id="row14424927204815"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p22853796"><a name="zh-cn_topic_0057972887_p22853796"></a><a name="zh-cn_topic_0057972887_p22853796"></a>OS-EXT-SRV-ATTR:kernel_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p39218184"><a name="zh-cn_topic_0057972887_p39218184"></a><a name="zh-cn_topic_0057972887_p39218184"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p15126299"><a name="zh-cn_topic_0057972887_p15126299"></a><a name="zh-cn_topic_0057972887_p15126299"></a>若使用AMI格式的镜像，则表示kernel image的UUID；否则，留空。</p>
<p id="p196273244466"><a name="p196273244466"></a><a name="p196273244466"></a>微版本2.3后支持。</p>
</td>
</tr>
<tr id="row1842472711482"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p40968939"><a name="zh-cn_topic_0057972887_p40968939"></a><a name="zh-cn_topic_0057972887_p40968939"></a>OS-EXT-SRV-ATTR:ramdisk_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p30149753"><a name="zh-cn_topic_0057972887_p30149753"></a><a name="zh-cn_topic_0057972887_p30149753"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p11808112215493"><a name="p11808112215493"></a><a name="p11808112215493"></a>若使用AMI格式镜像，则表示ramdisk image的UUID；否则，留空。</p>
<p id="zh-cn_topic_0057972887_p42710723"><a name="zh-cn_topic_0057972887_p42710723"></a><a name="zh-cn_topic_0057972887_p42710723"></a>微版本2.3后支持。</p>
</td>
</tr>
<tr id="row5425122710481"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p7284856"><a name="zh-cn_topic_0057972887_p7284856"></a><a name="zh-cn_topic_0057972887_p7284856"></a>OS-EXT-SRV-ATTR:root_device_name</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p53202458"><a name="zh-cn_topic_0057972887_p53202458"></a><a name="zh-cn_topic_0057972887_p53202458"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p28127439"><a name="zh-cn_topic_0057972887_p28127439"></a><a name="zh-cn_topic_0057972887_p28127439"></a>弹性云服务器系统盘的设备名称。</p>
<p id="p11804132124618"><a name="p11804132124618"></a><a name="p11804132124618"></a>微版本2.3后支持。</p>
</td>
</tr>
<tr id="row11445163194818"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p61864358"><a name="zh-cn_topic_0057972887_p61864358"></a><a name="zh-cn_topic_0057972887_p61864358"></a>OS-EXT-SRV-ATTR:user_data</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p44957139"><a name="zh-cn_topic_0057972887_p44957139"></a><a name="zh-cn_topic_0057972887_p44957139"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p20334069"><a name="zh-cn_topic_0057972887_p20334069"></a><a name="zh-cn_topic_0057972887_p20334069"></a>创建弹性云服务器时指定的user_data。</p>
<p id="p1815314834617"><a name="p1815314834617"></a><a name="p1815314834617"></a>微版本2.3后支持。</p>
</td>
</tr>
<tr id="row8537324827"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p1253710242210"><a name="p1253710242210"></a><a name="p1253710242210"></a>locked</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p1653720241521"><a name="p1653720241521"></a><a name="p1653720241521"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p18537624422"><a name="p18537624422"></a><a name="p18537624422"></a>当云服务器被锁时为True，否则为False。</p>
<p id="p13993454402"><a name="p13993454402"></a><a name="p13993454402"></a>微版本2.9后支持。</p>
</td>
</tr>
<tr id="row4211297017037"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p4431131717046"><a name="p4431131717046"></a><a name="p4431131717046"></a>accessIPv4</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p3244692017046"><a name="p3244692017046"></a><a name="p3244692017046"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p1095487217046"><a name="p1095487217046"></a><a name="p1095487217046"></a>预留属性。</p>
</td>
</tr>
<tr id="row5854487717038"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p14705517046"><a name="p14705517046"></a><a name="p14705517046"></a>accessIPv6</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p1191150917046"><a name="p1191150917046"></a><a name="p1191150917046"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p2530817917046"><a name="p2530817917046"></a><a name="p2530817917046"></a>预留属性。</p>
</td>
</tr>
<tr id="row3362467117038"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p6183447417046"><a name="p6183447417046"></a><a name="p6183447417046"></a>config_drive</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p4253646017046"><a name="p4253646017046"></a><a name="p4253646017046"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p2290125117046"><a name="p2290125117046"></a><a name="p2290125117046"></a>预留属性。</p>
</td>
</tr>
<tr id="row6528865417041"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p6381535217046"><a name="p6381535217046"></a><a name="p6381535217046"></a>progress</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p166104217046"><a name="p166104217046"></a><a name="p166104217046"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p32670417046"><a name="p32670417046"></a><a name="p32670417046"></a>预留属性。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  flavor字段数据结构说明

<a name="table29241163"></a>
<table><thead align="left"><tr id="row10599309"><th class="cellrowborder" valign="top" width="20.677932206779325%" id="mcps1.2.4.1.1"><p id="p08351422143212"><a name="p08351422143212"></a><a name="p08351422143212"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.887011298870114%" id="mcps1.2.4.1.2"><p id="p158351922123214"><a name="p158351922123214"></a><a name="p158351922123214"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.43505649435057%" id="mcps1.2.4.1.3"><p id="p8835192210324"><a name="p8835192210324"></a><a name="p8835192210324"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1202807"><td class="cellrowborder" valign="top" width="20.677932206779325%" headers="mcps1.2.4.1.1 "><p id="p30318520"><a name="p30318520"></a><a name="p30318520"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p9142577"><a name="p9142577"></a><a name="p9142577"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p2351288"><a name="p2351288"></a><a name="p2351288"></a>云服务器类型ID。</p>
</td>
</tr>
<tr id="row21161599"><td class="cellrowborder" valign="top" width="20.677932206779325%" headers="mcps1.2.4.1.1 "><p id="p36367968"><a name="p36367968"></a><a name="p36367968"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p38229923"><a name="p38229923"></a><a name="p38229923"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p19435912"><a name="p19435912"></a><a name="p19435912"></a>云服务器类型相关标记快捷链接信息。</p>
<p id="p580410263265"><a name="p580410263265"></a><a name="p580410263265"></a>详情请参见<a href="#table35230296">表7</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  image字段数据结构说明

<a name="table1080891111402"></a>
<table><thead align="left"><tr id="row5852711204015"><th class="cellrowborder" valign="top" width="20.93%" id="mcps1.2.4.1.1"><p id="p2098102533210"><a name="p2098102533210"></a><a name="p2098102533210"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.57%" id="mcps1.2.4.1.2"><p id="p1498192513327"><a name="p1498192513327"></a><a name="p1498192513327"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.5%" id="mcps1.2.4.1.3"><p id="p41141025113214"><a name="p41141025113214"></a><a name="p41141025113214"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row149223117400"><td class="cellrowborder" valign="top" width="20.93%" headers="mcps1.2.4.1.1 "><p id="p109391611134017"><a name="p109391611134017"></a><a name="p109391611134017"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="29.57%" headers="mcps1.2.4.1.2 "><p id="p7960411104018"><a name="p7960411104018"></a><a name="p7960411104018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.5%" headers="mcps1.2.4.1.3 "><p id="p19699157104820"><a name="p19699157104820"></a><a name="p19699157104820"></a>镜像ID。</p>
</td>
</tr>
<tr id="row119931361483"><td class="cellrowborder" valign="top" width="20.93%" headers="mcps1.2.4.1.1 "><p id="p99936664813"><a name="p99936664813"></a><a name="p99936664813"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="29.57%" headers="mcps1.2.4.1.2 "><p id="p5994196144811"><a name="p5994196144811"></a><a name="p5994196144811"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="49.5%" headers="mcps1.2.4.1.3 "><p id="p1399417684820"><a name="p1399417684820"></a><a name="p1399417684820"></a>镜像相关标记快捷链接信息，详情请参见<a href="#table35230296">表7</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  addresses字段数据结构说明

<a name="table36337966"></a>
<table><thead align="left"><tr id="row66136932"><th class="cellrowborder" valign="top" width="20.93%" id="mcps1.2.4.1.1"><p id="p8152204019329"><a name="p8152204019329"></a><a name="p8152204019329"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.57%" id="mcps1.2.4.1.2"><p id="p1515294016327"><a name="p1515294016327"></a><a name="p1515294016327"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.5%" id="mcps1.2.4.1.3"><p id="p1515284010326"><a name="p1515284010326"></a><a name="p1515284010326"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row66161841"><td class="cellrowborder" valign="top" width="20.93%" headers="mcps1.2.4.1.1 "><p id="p2057412833316"><a name="p2057412833316"></a><a name="p2057412833316"></a>弹性云服务器所属网络的名称</p>
</td>
<td class="cellrowborder" valign="top" width="29.57%" headers="mcps1.2.4.1.2 "><p id="p4439518115623"><a name="p4439518115623"></a><a name="p4439518115623"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="49.5%" headers="mcps1.2.4.1.3 "><p id="p1534202613277"><a name="p1534202613277"></a><a name="p1534202613277"></a>弹性云服务器所属网络信息。其中，</p>
<a name="ul1556425242710"></a><a name="ul1556425242710"></a><ul id="ul1556425242710"><li>key为网络名称，如“demo_net”。</li><li>value为网络详细信息。</li></ul>
<p id="p8364776268"><a name="p8364776268"></a><a name="p8364776268"></a>详情请参见<a href="#table1972725101724">表8</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  links字段数据结构说明

<a name="table35230296"></a>
<table><thead align="left"><tr id="row22264835"><th class="cellrowborder" valign="top" width="20.932093209320936%" id="mcps1.2.4.1.1"><p id="p112383444325"><a name="p112383444325"></a><a name="p112383444325"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.382938293829387%" id="mcps1.2.4.1.2"><p id="p14238944103219"><a name="p14238944103219"></a><a name="p14238944103219"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.684968496849685%" id="mcps1.2.4.1.3"><p id="p1023811445320"><a name="p1023811445320"></a><a name="p1023811445320"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row35493489"><td class="cellrowborder" valign="top" width="20.932093209320936%" headers="mcps1.2.4.1.1 "><p id="p56400342"><a name="p56400342"></a><a name="p56400342"></a>rel</p>
</td>
<td class="cellrowborder" valign="top" width="29.382938293829387%" headers="mcps1.2.4.1.2 "><p id="p4372186"><a name="p4372186"></a><a name="p4372186"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.684968496849685%" headers="mcps1.2.4.1.3 "><p id="p18602825"><a name="p18602825"></a><a name="p18602825"></a>快捷链接标记名称。</p>
</td>
</tr>
<tr id="row33207705"><td class="cellrowborder" valign="top" width="20.932093209320936%" headers="mcps1.2.4.1.1 "><p id="p5469547"><a name="p5469547"></a><a name="p5469547"></a>href</p>
</td>
<td class="cellrowborder" valign="top" width="29.382938293829387%" headers="mcps1.2.4.1.2 "><p id="p49569014"><a name="p49569014"></a><a name="p49569014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.684968496849685%" headers="mcps1.2.4.1.3 "><p id="p55667198"><a name="p55667198"></a><a name="p55667198"></a>对应快捷链接。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  弹性云服务器所属网络信息的数据结构说明

<a name="table1972725101724"></a>
<table><thead align="left"><tr id="row12506860101724"><th class="cellrowborder" valign="top" width="21.22%" id="mcps1.2.4.1.1"><p id="p1370316476325"><a name="p1370316476325"></a><a name="p1370316476325"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.78%" id="mcps1.2.4.1.2"><p id="p370334723212"><a name="p370334723212"></a><a name="p370334723212"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="p0703347163220"><a name="p0703347163220"></a><a name="p0703347163220"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row12641738101724"><td class="cellrowborder" valign="top" width="21.22%" headers="mcps1.2.4.1.1 "><p id="p65254077101750"><a name="p65254077101750"></a><a name="p65254077101750"></a>addr</p>
</td>
<td class="cellrowborder" valign="top" width="28.78%" headers="mcps1.2.4.1.2 "><p id="p51088888101750"><a name="p51088888101750"></a><a name="p51088888101750"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p44559239101750"><a name="p44559239101750"></a><a name="p44559239101750"></a>IP地址信息。</p>
</td>
</tr>
<tr id="row21763795101724"><td class="cellrowborder" valign="top" width="21.22%" headers="mcps1.2.4.1.1 "><p id="p2995307101750"><a name="p2995307101750"></a><a name="p2995307101750"></a>version</p>
</td>
<td class="cellrowborder" valign="top" width="28.78%" headers="mcps1.2.4.1.2 "><p id="p41293276101750"><a name="p41293276101750"></a><a name="p41293276101750"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p32665092151024"><a name="p32665092151024"></a><a name="p32665092151024"></a>IP地址类型，值为4或6。</p>
<a name="ul25550372151024"></a><a name="ul25550372151024"></a><ul id="ul25550372151024"><li>4：IP地址类型是IPv4</li><li>6：IP地址类型是IPv6</li></ul>
</td>
</tr>
<tr id="row5677238512196"><td class="cellrowborder" valign="top" width="21.22%" headers="mcps1.2.4.1.1 "><p id="p3516049812196"><a name="p3516049812196"></a><a name="p3516049812196"></a>OS-EXT-IPS-MAC:mac_addr</p>
</td>
<td class="cellrowborder" valign="top" width="28.78%" headers="mcps1.2.4.1.2 "><p id="p2942812812196"><a name="p2942812812196"></a><a name="p2942812812196"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p3486817812196"><a name="p3486817812196"></a><a name="p3486817812196"></a>扩展属性，MAC地址。</p>
</td>
</tr>
<tr id="row211654712196"><td class="cellrowborder" valign="top" width="21.22%" headers="mcps1.2.4.1.1 "><p id="p3722265012196"><a name="p3722265012196"></a><a name="p3722265012196"></a>OS-EXT-IPS:type</p>
</td>
<td class="cellrowborder" valign="top" width="28.78%" headers="mcps1.2.4.1.2 "><p id="p6224463612196"><a name="p6224463612196"></a><a name="p6224463612196"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p865077112196"><a name="p865077112196"></a><a name="p865077112196"></a>扩展属性，分配IP地址方式。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  os-extended-volumes:volumes\_attached字段数据结构说明

<a name="table10024873122234"></a>
<table><thead align="left"><tr id="row57520332122234"><th class="cellrowborder" valign="top" width="21%" id="mcps1.2.4.1.1"><p id="p141714507323"><a name="p141714507323"></a><a name="p141714507323"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.999999999999996%" id="mcps1.2.4.1.2"><p id="p1433115012326"><a name="p1433115012326"></a><a name="p1433115012326"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="p1043345063214"><a name="p1043345063214"></a><a name="p1043345063214"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row36412167122234"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="p63704378122234"><a name="p63704378122234"></a><a name="p63704378122234"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="28.999999999999996%" headers="mcps1.2.4.1.2 "><p id="p59781031122234"><a name="p59781031122234"></a><a name="p59781031122234"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p10425332122234"><a name="p10425332122234"></a><a name="p10425332122234"></a>云磁盘ID。</p>
</td>
</tr>
<tr id="row156174394818"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="p9561643144814"><a name="p9561643144814"></a><a name="p9561643144814"></a>delete_on_termination</p>
</td>
<td class="cellrowborder" valign="top" width="28.999999999999996%" headers="mcps1.2.4.1.2 "><p id="p45694310485"><a name="p45694310485"></a><a name="p45694310485"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p110774385110"><a name="p110774385110"></a><a name="p110774385110"></a>一个标志，指示在删除服务器时是否删除附加的卷。、</p>
<p id="p856184314483"><a name="p856184314483"></a><a name="p856184314483"></a>默认情况下，这是False</p>
<p id="p1169334275311"><a name="p1169334275311"></a><a name="p1169334275311"></a>微版本2.3后支持</p>
</td>
</tr>
</tbody>
</table>

**表 10**  security\_groups字段数据结构说明

<a name="table2053207517233"></a>
<table><thead align="left"><tr id="row2114422117233"><th class="cellrowborder" valign="top" width="21%" id="mcps1.2.4.1.1"><p id="p894305273218"><a name="p894305273218"></a><a name="p894305273218"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.999999999999996%" id="mcps1.2.4.1.2"><p id="p139591452193215"><a name="p139591452193215"></a><a name="p139591452193215"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="p695912521323"><a name="p695912521323"></a><a name="p695912521323"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5784450417233"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="p5489327917233"><a name="p5489327917233"></a><a name="p5489327917233"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="28.999999999999996%" headers="mcps1.2.4.1.2 "><p id="p1717057717233"><a name="p1717057717233"></a><a name="p1717057717233"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p52012230"><a name="p52012230"></a><a name="p52012230"></a>安全组名称或者uuid。</p>
</td>
</tr>
</tbody>
</table>

**表 11**  fault字段数据结构说明

<a name="table1075312230549"></a>
<table><thead align="left"><tr id="row14754182345416"><th class="cellrowborder" valign="top" width="21%" id="mcps1.2.4.1.1"><p id="p15754172315410"><a name="p15754172315410"></a><a name="p15754172315410"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.999999999999996%" id="mcps1.2.4.1.2"><p id="p075415233543"><a name="p075415233543"></a><a name="p075415233543"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="p175422315410"><a name="p175422315410"></a><a name="p175422315410"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row975452395413"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="p27541723165410"><a name="p27541723165410"></a><a name="p27541723165410"></a>code</p>
</td>
<td class="cellrowborder" valign="top" width="28.999999999999996%" headers="mcps1.2.4.1.2 "><p id="p97542231542"><a name="p97542231542"></a><a name="p97542231542"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p17559236540"><a name="p17559236540"></a><a name="p17559236540"></a>错误码。</p>
</td>
</tr>
<tr id="row11901115718561"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="p590117577560"><a name="p590117577560"></a><a name="p590117577560"></a>created</p>
</td>
<td class="cellrowborder" valign="top" width="28.999999999999996%" headers="mcps1.2.4.1.2 "><p id="p290105719562"><a name="p290105719562"></a><a name="p290105719562"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p1790110571561"><a name="p1790110571561"></a><a name="p1790110571561"></a>异常出现的时间。</p>
</td>
</tr>
<tr id="row7674955155611"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="p767412557568"><a name="p767412557568"></a><a name="p767412557568"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="28.999999999999996%" headers="mcps1.2.4.1.2 "><p id="p2674185516566"><a name="p2674185516566"></a><a name="p2674185516566"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p1267414555563"><a name="p1267414555563"></a><a name="p1267414555563"></a>异常描述信息。</p>
</td>
</tr>
<tr id="row2107195385616"><td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.1 "><p id="p12108145314564"><a name="p12108145314564"></a><a name="p12108145314564"></a>details</p>
</td>
<td class="cellrowborder" valign="top" width="28.999999999999996%" headers="mcps1.2.4.1.2 "><p id="p13108195335615"><a name="p13108195335615"></a><a name="p13108195335615"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p610865345615"><a name="p610865345615"></a><a name="p610865345615"></a>异常详情信息，可选参数，在非空条件下才返回。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section17256720205514"></a>

```
GET https://{endpoint}/v2.1/{project_id}/servers/{server_id}
```

## 响应示例<a name="section827141312330"></a>

```
{
    "server": {
        "addresses": {
            "68269e6e-4a27-441b-8029-35373ad50bd9": [
                {
                    "addr": "192.168.0.3", 
                    "version": 4,
                    "OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:1b:35:78",
                    "OS-EXT-IPS:type": "fixed"
                }
            ]
        }, 
        "created": "2012-08-20T21:11:09Z", 
        "flavor": {
            "id": "1", 
            "links": [
                {
                    "href": "http://openstack.example.com/openstack/flavors/1", 
                    "rel": "bookmark"
                }
            ]
        }, 
        "hostId": "65201c14a29663e06d0748e561207d998b343e1d164bfa0aafa9c45d", 
        "id": "893c7791-f1df-4c3d-8383-3caae9656c62", 
        "image": "", 
        "links": [
            {
                "href": "http://openstack.example.com/v2/openstack/servers/893c7791-f1df-4c3d-8383-3caae9656c62", 
                "rel": "self"
            }, 
            {
                "href": "http://openstack.example.com/openstack/servers/893c7791-f1df-4c3d-8383-3caae9656c62", 
                "rel": "bookmark"
            }
        ], 
        "metadata": {},
        "name": "new-server-test", 
        "progress": 0, 
        "status": "ACTIVE", 
        "tenant_id": "openstack", 
        "updated": "2012-08-20T21:11:09Z", 
        "user_id": "fake"
    }
}
```

## 返回值<a name="section7610951"></a>

请参考[通用请求返回值](通用请求返回值.md)。

