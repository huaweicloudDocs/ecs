# 查询云服务器详情<a name="ecs_03_0206"></a>

## 功能介绍<a name="section11242227"></a>

根据云服务器ID，查询云服务器的详细信息。

## 调试<a name="section926243314015"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=ECS&api=NovaShowServer)中直接运行调试该接口。

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
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="p11568292"><a name="p11568292"></a><a name="p11568292"></a><span id="text105835204314"><a name="text105835204314"></a><a name="text105835204314"></a>云服务器</span>ID。</p>
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
<td class="cellrowborder" valign="top" width="49.5%" headers="mcps1.2.4.1.3 "><p id="p36377578"><a name="p36377578"></a><a name="p36377578"></a><span id="text8178537438"><a name="text8178537438"></a><a name="text8178537438"></a>云服务器</span>信息，详情请参见<a href="#table26210179">表3</a>。</p>
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
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p37524445"><a name="p37524445"></a><a name="p37524445"></a><span id="text272945317433"><a name="text272945317433"></a><a name="text272945317433"></a>云服务器</span>名称。</p>
</td>
</tr>
<tr id="row2175687"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p42012952"><a name="p42012952"></a><a name="p42012952"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p30874046"><a name="p30874046"></a><a name="p30874046"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p17769829"><a name="p17769829"></a><a name="p17769829"></a><span id="text3402115419432"><a name="text3402115419432"></a><a name="text3402115419432"></a>云服务器</span>唯一标识。</p>
</td>
</tr>
<tr id="row25710733"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p2194613"><a name="p2194613"></a><a name="p2194613"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p37560342"><a name="p37560342"></a><a name="p37560342"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p22488863"><a name="p22488863"></a><a name="p22488863"></a><span id="text612115510435"><a name="text612115510435"></a><a name="text612115510435"></a>云服务器</span>当前状态信息。</p>
<p id="p17952198145121"><a name="p17952198145121"></a><a name="p17952198145121"></a>取值范围：</p>
<p id="p53652898145152"><a name="p53652898145152"></a><a name="p53652898145152"></a>ACTIVE、BUILD、DELETED、ERROR、HARD_REBOOT、MIGRATING、PAUSED、REBOOT、REBUILD、RESIZE、REVERT_RESIZE、SHUTOFF、SHELVED、SHELVED_OFFLOADED、SOFT_DELETED、SUSPENDED、VERIFY_RESIZE</p>
<p id="p5103192105518"><a name="p5103192105518"></a><a name="p5103192105518"></a><span id="text0714155504312"><a name="text0714155504312"></a><a name="text0714155504312"></a>云服务器</span>状态说明请参考<a href="云服务器状态.md">云服务器状态</a>。</p>
</td>
</tr>
<tr id="row1073183"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p19818984"><a name="p19818984"></a><a name="p19818984"></a>created</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p42487544"><a name="p42487544"></a><a name="p42487544"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p18939022"><a name="p18939022"></a><a name="p18939022"></a><span id="text10667358124319"><a name="text10667358124319"></a><a name="text10667358124319"></a>云服务器</span>创建时间。时间格式例如：2019-05-22T07:48:19Z</p>
</td>
</tr>
<tr id="row36233478"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p49230602"><a name="p49230602"></a><a name="p49230602"></a>updated</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p7022941"><a name="p7022941"></a><a name="p7022941"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p31987323"><a name="p31987323"></a><a name="p31987323"></a><span id="text13449175984311"><a name="text13449175984311"></a><a name="text13449175984311"></a>云服务器</span>上一次更新时间。时间格式例如：2019-05-22T07:48:19Z</p>
</td>
</tr>
<tr id="row19450451"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p31982717"><a name="p31982717"></a><a name="p31982717"></a>flavor</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p56299846"><a name="p56299846"></a><a name="p56299846"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p39071968"><a name="p39071968"></a><a name="p39071968"></a><span id="text8282100154416"><a name="text8282100154416"></a><a name="text8282100154416"></a>云服务器</span>规格信息，详情请参见<a href="#table29241163">表4</a>。</p>
</td>
</tr>
<tr id="row16103393"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p29306417"><a name="p29306417"></a><a name="p29306417"></a>image</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p12507614"><a name="p12507614"></a><a name="p12507614"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p58354673"><a name="p58354673"></a><a name="p58354673"></a><span id="text18651612447"><a name="text18651612447"></a><a name="text18651612447"></a>云服务器</span>镜像信息，对镜像创的<span id="text4394646125614"><a name="text4394646125614"></a><a name="text4394646125614"></a>弹性云服务器</span>该属性通常返回镜像id和链接。</p>
<p id="p5571104842212"><a name="p5571104842212"></a><a name="p5571104842212"></a>详情请参见<a href="#table1080891111402">表5</a>。</p>
</td>
</tr>
<tr id="row55430014"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p60646173"><a name="p60646173"></a><a name="p60646173"></a>tenant_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p11089280"><a name="p11089280"></a><a name="p11089280"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p25816468"><a name="p25816468"></a><a name="p25816468"></a><span id="text948655446"><a name="text948655446"></a><a name="text948655446"></a>云服务器</span>所属租户ID。即项目id，和project_id表示的是一个概念。</p>
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
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p27177474"><a name="p27177474"></a><a name="p27177474"></a><span id="text877693317442"><a name="text877693317442"></a><a name="text877693317442"></a>云服务器</span>所属用户ID。</p>
</td>
</tr>
<tr id="row43270676"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p15263883"><a name="p15263883"></a><a name="p15263883"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p19916823"><a name="p19916823"></a><a name="p19916823"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p23849822"><a name="p23849822"></a><a name="p23849822"></a><span id="text2473143464420"><a name="text2473143464420"></a><a name="text2473143464420"></a>云服务器</span>元数据。</p>
</td>
</tr>
<tr id="row13321813"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p5325067"><a name="p5325067"></a><a name="p5325067"></a>hostId</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p41156139"><a name="p41156139"></a><a name="p41156139"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p45312999"><a name="p45312999"></a><a name="p45312999"></a><span id="text1012920353449"><a name="text1012920353449"></a><a name="text1012920353449"></a>云服务器</span>对应的主机ID。</p>
</td>
</tr>
<tr id="row5163807"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p15615252"><a name="p15615252"></a><a name="p15615252"></a>addresses</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p43546944"><a name="p43546944"></a><a name="p43546944"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p19934154819297"><a name="p19934154819297"></a><a name="p19934154819297"></a><span id="text11801113517441"><a name="text11801113517441"></a><a name="text11801113517441"></a>云服务器</span>对应的网络地址信息。</p>
<a name="ul8213145222916"></a><a name="ul8213145222916"></a><ul id="ul8213145222916"><li>key为网络名称，如“demo_net”。</li><li>value为网络详细信息。</li></ul>
<p id="p3229562"><a name="p3229562"></a><a name="p3229562"></a>详情请参见<a href="#table1972725101724">表7</a>。</p>
</td>
</tr>
<tr id="row2817586217053"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p2741526417147"><a name="p2741526417147"></a><a name="p2741526417147"></a>security_groups</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p604393417147"><a name="p604393417147"></a><a name="p604393417147"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p4395185217147"><a name="p4395185217147"></a><a name="p4395185217147"></a><span id="text212933913442"><a name="text212933913442"></a><a name="text212933913442"></a>云服务器</span>所属安全组列表，详情请参见<a href="#table2053207517233">表9</a>。</p>
</td>
</tr>
<tr id="row29066061"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p5540732"><a name="p5540732"></a><a name="p5540732"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p46852469"><a name="p46852469"></a><a name="p46852469"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p64147070"><a name="p64147070"></a><a name="p64147070"></a><span id="text18980739194416"><a name="text18980739194416"></a><a name="text18980739194416"></a>云服务器</span>相关标记快捷链接信息，详情请参见<a href="#table35230296">表6</a>。</p>
</td>
</tr>
<tr id="row5544204718389"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p749372082418"><a name="p749372082418"></a><a name="p749372082418"></a>tags</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p14493420142420"><a name="p14493420142420"></a><a name="p14493420142420"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p1620274611333"><a name="p1620274611333"></a><a name="p1620274611333"></a><span id="text106411040104412"><a name="text106411040104412"></a><a name="text106411040104412"></a>云服务器</span>的标签列表。</p>
<p id="p1149310203247"><a name="p1149310203247"></a><a name="p1149310203247"></a>微版本2.26及以上版本支持，如果不使用微版本查询，响应中无tags字段。</p>
<div class="p" id="p7300949059"><a name="p7300949059"></a><a name="p7300949059"></a>系统近期对标签功能进行了升级，升级后，返回的tag值遵循如下规则：<a name="ecs_03_0205_ul871515496611"></a><a name="ecs_03_0205_ul871515496611"></a><ul id="ecs_03_0205_ul871515496611"><li>key与value使用“=”连接，如“key=value”。</li><li>如果value为空字符串，则仅返回key。</li></ul>
</div>
</td>
</tr>
<tr id="row6518153677"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972661_p47044325"><a name="zh-cn_topic_0057972661_p47044325"></a><a name="zh-cn_topic_0057972661_p47044325"></a>os:scheduler_hints</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p4679135396"><a name="p4679135396"></a><a name="p4679135396"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972661_p10232270"><a name="zh-cn_topic_0057972661_p10232270"></a><a name="zh-cn_topic_0057972661_p10232270"></a><span id="text1560265485318"><a name="text1560265485318"></a><a name="text1560265485318"></a>弹性云服务器</span>调度信息，参见<a href="#zh-cn_topic_0057972661_table12534817105641">表11</a>。裸金属服务器场景不支持。仅在DEH专属主机的场景下存在该字段。</p>
</td>
</tr>
<tr id="row65689897121119"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p19281432121119"><a name="p19281432121119"></a><a name="p19281432121119"></a>OS-DCF:diskConfig</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p18292184121119"><a name="p18292184121119"></a><a name="p18292184121119"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p5271953121119"><a name="p5271953121119"></a><a name="p5271953121119"></a>扩展属性，磁盘配置方式。对镜像启动<span id="text5890448125610"><a name="text5890448125610"></a><a name="text5890448125610"></a>弹性云服务器</span>生效。</p>
<p id="p978417418171"><a name="p978417418171"></a><a name="p978417418171"></a>取值范围：</p>
<p id="p12130413131719"><a name="p12130413131719"></a><a name="p12130413131719"></a>AUTO: API使用单个分区构建目标磁盘大小的<span id="text1448235017568"><a name="text1448235017568"></a><a name="text1448235017568"></a>弹性云服务器</span>。 API会自动调整文件系统以适应整个分区。</p>
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
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p63293526121127"><a name="p63293526121127"></a><a name="p63293526121127"></a>扩展属性，<span id="text96208448446"><a name="text96208448446"></a><a name="text96208448446"></a>云服务器</span>宿主名称。</p>
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
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p44801116121128"><a name="p44801116121128"></a><a name="p44801116121128"></a>扩展属性，<span id="text245744564415"><a name="text245744564415"></a><a name="text245744564415"></a>云服务器</span>ID。</p>
</td>
</tr>
<tr id="row66679123121128"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p32299911121128"><a name="p32299911121128"></a><a name="p32299911121128"></a>OS-EXT-STS:power_state</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p66155999121128"><a name="p66155999121128"></a><a name="p66155999121128"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p57035716121128"><a name="p57035716121128"></a><a name="p57035716121128"></a>扩展属性，<span id="text76749462448"><a name="text76749462448"></a><a name="text76749462448"></a>云服务器</span>电源状态。</p>
<p id="p2689123602310"><a name="p2689123602310"></a><a name="p2689123602310"></a>取值范围：0 , 1 , 2 , 3 , 4</p>
<a name="ul934453312193"></a><a name="ul934453312193"></a><ul id="ul934453312193"><li>0 : pending</li><li>1 : running</li><li>2 : paused</li><li>3 : shutdown</li><li>4 : crashed</li></ul>
</td>
</tr>
<tr id="row19260742121226"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p16616235121226"><a name="p16616235121226"></a><a name="p16616235121226"></a>OS-EXT-STS:task_state</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p3737772121226"><a name="p3737772121226"></a><a name="p3737772121226"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p34324147121226"><a name="p34324147121226"></a><a name="p34324147121226"></a>扩展属性，<span id="text24411647184418"><a name="text24411647184418"></a><a name="text24411647184418"></a>云服务器</span>任务状态。</p>
<p id="p13922047162612"><a name="p13922047162612"></a><a name="p13922047162612"></a>取值范围请参考<a href="云服务器状态.md">云服务器状态</a>表3。</p>
</td>
</tr>
<tr id="row11298969121227"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p42801278121227"><a name="p42801278121227"></a><a name="p42801278121227"></a>OS-EXT-STS:vm_state</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p44351508121227"><a name="p44351508121227"></a><a name="p44351508121227"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p9331154012376"><a name="p9331154012376"></a><a name="p9331154012376"></a>扩展属性，<span id="text183246517443"><a name="text183246517443"></a><a name="text183246517443"></a>云服务器</span>状态。</p>
<p id="p35702402121227"><a name="p35702402121227"></a><a name="p35702402121227"></a>取值范围：</p>
<p id="p15276846381"><a name="p15276846381"></a><a name="p15276846381"></a>ACTIVE,BUILDING,STOPPED,RESIZED,PAUSED,SUSPENDED,RESCUED,ERROR,DELETED,SOFT_DELETED,SHELVED,SHELVED_OFFLOADED</p>
<p id="p69818711559"><a name="p69818711559"></a><a name="p69818711559"></a><span id="text10226175216445"><a name="text10226175216445"></a><a name="text10226175216445"></a>云服务器</span>状态说明请参考<a href="云服务器状态.md">云服务器状态</a>。</p>
</td>
</tr>
<tr id="row59870257121227"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p17652642121227"><a name="p17652642121227"></a><a name="p17652642121227"></a>OS-SRV-USG:launched_at</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p20577863121227"><a name="p20577863121227"></a><a name="p20577863121227"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p56194184121227"><a name="p56194184121227"></a><a name="p56194184121227"></a>扩展属性，<span id="text20874115415443"><a name="text20874115415443"></a><a name="text20874115415443"></a>云服务器</span>启动时间。时间格式例如：2019-05-22T07:48:19.000000</p>
</td>
</tr>
<tr id="row58808453121228"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p65864237121228"><a name="p65864237121228"></a><a name="p65864237121228"></a>OS-SRV-USG:terminated_at</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p33402957121228"><a name="p33402957121228"></a><a name="p33402957121228"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p21285006121228"><a name="p21285006121228"></a><a name="p21285006121228"></a>扩展属性，<span id="text25623556445"><a name="text25623556445"></a><a name="text25623556445"></a>云服务器</span>删除时间。时间格式例如：2019-05-22T07:48:19.000000</p>
</td>
</tr>
<tr id="row22845263122110"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p29403502122828"><a name="p29403502122828"></a><a name="p29403502122828"></a>os-extended-volumes:volumes_attached</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p32873451122828"><a name="p32873451122828"></a><a name="p32873451122828"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p6881526122828"><a name="p6881526122828"></a><a name="p6881526122828"></a><span id="text34187563443"><a name="text34187563443"></a><a name="text34187563443"></a>云服务器</span>挂载的云磁盘信息，详情请参见<a href="#table10024873122234">表8</a>。</p>
</td>
</tr>
<tr id="row161046711504"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p43095310"><a name="zh-cn_topic_0057972887_p43095310"></a><a name="zh-cn_topic_0057972887_p43095310"></a>fault</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p1059226"><a name="zh-cn_topic_0057972887_p1059226"></a><a name="zh-cn_topic_0057972887_p1059226"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p37371779"><a name="zh-cn_topic_0057972887_p37371779"></a><a name="zh-cn_topic_0057972887_p37371779"></a><span id="text13981057124411"><a name="text13981057124411"></a><a name="text13981057124411"></a>云服务器</span>故障信息。</p>
<p id="p14777766535"><a name="p14777766535"></a><a name="p14777766535"></a>可选参数，在<span id="text1675425724416"><a name="text1675425724416"></a><a name="text1675425724416"></a>云服务器</span>状态为ERROR且存在异常的情况下返回。</p>
<p id="p1688015424530"><a name="p1688015424530"></a><a name="p1688015424530"></a>详情参见 <a href="#table1075312230549">表11 fault字段数据结构说明</a>。</p>
</td>
</tr>
<tr id="row107959146481"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p57463526"><a name="zh-cn_topic_0057972887_p57463526"></a><a name="zh-cn_topic_0057972887_p57463526"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p24034004"><a name="zh-cn_topic_0057972887_p24034004"></a><a name="zh-cn_topic_0057972887_p24034004"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p48379233"><a name="zh-cn_topic_0057972887_p48379233"></a><a name="zh-cn_topic_0057972887_p48379233"></a><span id="text5394125874414"><a name="text5394125874414"></a><a name="text5394125874414"></a>云服务器</span>的描述信息。</p>
<p id="p28201545155518"><a name="p28201545155518"></a><a name="p28201545155518"></a>微版本2.19及以上版本支持。</p>
</td>
</tr>
<tr id="row456252015488"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p58332432"><a name="zh-cn_topic_0057972887_p58332432"></a><a name="zh-cn_topic_0057972887_p58332432"></a>host_status</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p27306569"><a name="zh-cn_topic_0057972887_p27306569"></a><a name="zh-cn_topic_0057972887_p27306569"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p44841923"><a name="zh-cn_topic_0057972887_p44841923"></a><a name="zh-cn_topic_0057972887_p44841923"></a>nova-compute状态。</p>
<a name="zh-cn_topic_0057972887_ul924126"></a><a name="zh-cn_topic_0057972887_ul924126"></a><ul id="zh-cn_topic_0057972887_ul924126"><li>UP：服务正常</li><li>UNKNOWN：状态未知</li><li>DOWN：服务异常</li><li>MAINTENANCE：维护状态</li><li>空字符串：<span id="text19130125920447"><a name="text19130125920447"></a><a name="text19130125920447"></a>云服务器</span>无主机信息</li></ul>
<p id="p9178121814561"><a name="p9178121814561"></a><a name="p9178121814561"></a>微版本2.16及以上版本支持。</p>
</td>
</tr>
<tr id="row1043718233485"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p7131169"><a name="zh-cn_topic_0057972887_p7131169"></a><a name="zh-cn_topic_0057972887_p7131169"></a>OS-EXT-SRV-ATTR:hostname</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p40753854"><a name="zh-cn_topic_0057972887_p40753854"></a><a name="zh-cn_topic_0057972887_p40753854"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p24324288"><a name="zh-cn_topic_0057972887_p24324288"></a><a name="zh-cn_topic_0057972887_p24324288"></a><span id="text10786165911446"><a name="text10786165911446"></a><a name="text10786165911446"></a>云服务器</span>的主机名。</p>
<p id="p3479627194317"><a name="p3479627194317"></a><a name="p3479627194317"></a>微版本2.3及以上版本支持。</p>
</td>
</tr>
<tr id="row1843752316486"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p6779396"><a name="zh-cn_topic_0057972887_p6779396"></a><a name="zh-cn_topic_0057972887_p6779396"></a>OS-EXT-SRV-ATTR:reservation_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p12260243"><a name="zh-cn_topic_0057972887_p12260243"></a><a name="zh-cn_topic_0057972887_p12260243"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p43041107"><a name="zh-cn_topic_0057972887_p43041107"></a><a name="zh-cn_topic_0057972887_p43041107"></a>批量创建场景，<span id="text20434101457"><a name="text20434101457"></a><a name="text20434101457"></a>云服务器</span>的预留ID。</p>
<p id="p18137583436"><a name="p18137583436"></a><a name="p18137583436"></a>微版本2.3及以上版本支持。</p>
</td>
</tr>
<tr id="row12424182718489"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p54550808"><a name="zh-cn_topic_0057972887_p54550808"></a><a name="zh-cn_topic_0057972887_p54550808"></a>OS-EXT-SRV-ATTR:launch_index</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p56539341"><a name="zh-cn_topic_0057972887_p56539341"></a><a name="zh-cn_topic_0057972887_p56539341"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p43927036"><a name="zh-cn_topic_0057972887_p43927036"></a><a name="zh-cn_topic_0057972887_p43927036"></a>批量创建场景，<span id="text186713134512"><a name="text186713134512"></a><a name="text186713134512"></a>云服务器</span>的启动顺序。</p>
<p id="p12601191124414"><a name="p12601191124414"></a><a name="p12601191124414"></a>微版本2.3及以上版本支持。</p>
</td>
</tr>
<tr id="row14424927204815"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p22853796"><a name="zh-cn_topic_0057972887_p22853796"></a><a name="zh-cn_topic_0057972887_p22853796"></a>OS-EXT-SRV-ATTR:kernel_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p39218184"><a name="zh-cn_topic_0057972887_p39218184"></a><a name="zh-cn_topic_0057972887_p39218184"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p15126299"><a name="zh-cn_topic_0057972887_p15126299"></a><a name="zh-cn_topic_0057972887_p15126299"></a>若使用AMI格式的镜像，则表示kernel image的UUID；否则，留空。</p>
<p id="p196273244466"><a name="p196273244466"></a><a name="p196273244466"></a>微版本2.3及以上版本支持。</p>
</td>
</tr>
<tr id="row1842472711482"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p40968939"><a name="zh-cn_topic_0057972887_p40968939"></a><a name="zh-cn_topic_0057972887_p40968939"></a>OS-EXT-SRV-ATTR:ramdisk_id</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p30149753"><a name="zh-cn_topic_0057972887_p30149753"></a><a name="zh-cn_topic_0057972887_p30149753"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p11808112215493"><a name="p11808112215493"></a><a name="p11808112215493"></a>若使用AMI格式镜像，则表示ramdisk image的UUID；否则，留空。</p>
<p id="zh-cn_topic_0057972887_p42710723"><a name="zh-cn_topic_0057972887_p42710723"></a><a name="zh-cn_topic_0057972887_p42710723"></a>微版本2.3及以上版本支持。</p>
</td>
</tr>
<tr id="row5425122710481"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p7284856"><a name="zh-cn_topic_0057972887_p7284856"></a><a name="zh-cn_topic_0057972887_p7284856"></a>OS-EXT-SRV-ATTR:root_device_name</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p53202458"><a name="zh-cn_topic_0057972887_p53202458"></a><a name="zh-cn_topic_0057972887_p53202458"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p28127439"><a name="zh-cn_topic_0057972887_p28127439"></a><a name="zh-cn_topic_0057972887_p28127439"></a><span id="text138101114457"><a name="text138101114457"></a><a name="text138101114457"></a>云服务器</span>系统盘的设备名称。</p>
<p id="p11804132124618"><a name="p11804132124618"></a><a name="p11804132124618"></a>微版本2.3及以上版本支持。</p>
</td>
</tr>
<tr id="row11445163194818"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p61864358"><a name="zh-cn_topic_0057972887_p61864358"></a><a name="zh-cn_topic_0057972887_p61864358"></a>OS-EXT-SRV-ATTR:user_data</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p44957139"><a name="zh-cn_topic_0057972887_p44957139"></a><a name="zh-cn_topic_0057972887_p44957139"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p20334069"><a name="zh-cn_topic_0057972887_p20334069"></a><a name="zh-cn_topic_0057972887_p20334069"></a>创建<span id="text1352212204510"><a name="text1352212204510"></a><a name="text1352212204510"></a>云服务器</span>时指定的user_data。</p>
<p id="p1815314834617"><a name="p1815314834617"></a><a name="p1815314834617"></a>微版本2.3及以上版本支持。</p>
</td>
</tr>
<tr id="row8537324827"><td class="cellrowborder" valign="top" width="24.752475247524753%" headers="mcps1.2.4.1.1 "><p id="p1253710242210"><a name="p1253710242210"></a><a name="p1253710242210"></a>locked</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.2.4.1.2 "><p id="p1653720241521"><a name="p1653720241521"></a><a name="p1653720241521"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="51.48514851485149%" headers="mcps1.2.4.1.3 "><p id="p18537624422"><a name="p18537624422"></a><a name="p18537624422"></a>当<span id="text23645315457"><a name="text23645315457"></a><a name="text23645315457"></a>云服务器</span>被锁时为True，否则为False。</p>
<p id="p13993454402"><a name="p13993454402"></a><a name="p13993454402"></a>微版本2.9及以上版本支持。</p>
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
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p2351288"><a name="p2351288"></a><a name="p2351288"></a><span id="text317811584519"><a name="text317811584519"></a><a name="text317811584519"></a>云服务器</span>类型ID。</p>
<p id="p5578010620"><a name="p5578010620"></a><a name="p5578010620"></a>微版本2.47及以上版本不支持。</p>
</td>
</tr>
<tr id="row21161599"><td class="cellrowborder" valign="top" width="20.677932206779325%" headers="mcps1.2.4.1.1 "><p id="p36367968"><a name="p36367968"></a><a name="p36367968"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p38229923"><a name="p38229923"></a><a name="p38229923"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p19435912"><a name="p19435912"></a><a name="p19435912"></a><span id="text1781915511454"><a name="text1781915511454"></a><a name="text1781915511454"></a>云服务器</span>类型相关标记快捷链接信息。</p>
<p id="p580410263265"><a name="p580410263265"></a><a name="p580410263265"></a>详情请参见<a href="#table35230296">表6</a>。</p>
<p id="p1923951718615"><a name="p1923951718615"></a><a name="p1923951718615"></a>微版本2.47及以上版本不支持。</p>
</td>
</tr>
<tr id="row11601145721619"><td class="cellrowborder" valign="top" width="20.677932206779325%" headers="mcps1.2.4.1.1 "><p id="p18647653114019"><a name="p18647653114019"></a><a name="p18647653114019"></a>vcpus</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p5647153194013"><a name="p5647153194013"></a><a name="p5647153194013"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p594712133917"><a name="p594712133917"></a><a name="p594712133917"></a>该<span id="text84581064456"><a name="text84581064456"></a><a name="text84581064456"></a>云服务器</span>规格对应的CPU核数。</p>
<p id="p7411737161018"><a name="p7411737161018"></a><a name="p7411737161018"></a>在微版本2.47及以上版本支持。</p>
</td>
</tr>
<tr id="row146331125171"><td class="cellrowborder" valign="top" width="20.677932206779325%" headers="mcps1.2.4.1.1 "><p id="p460015587400"><a name="p460015587400"></a><a name="p460015587400"></a>ram</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p1760065884017"><a name="p1760065884017"></a><a name="p1760065884017"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p1760065884013"><a name="p1760065884013"></a><a name="p1760065884013"></a>该<span id="text14831575455"><a name="text14831575455"></a><a name="text14831575455"></a>云服务器</span>规格对应的内存大小，单位为MB。</p>
<p id="p0979145841010"><a name="p0979145841010"></a><a name="p0979145841010"></a>在微版本2.47及以上版本支持。</p>
</td>
</tr>
<tr id="row663372141712"><td class="cellrowborder" valign="top" width="20.677932206779325%" headers="mcps1.2.4.1.1 "><p id="p338192124118"><a name="p338192124118"></a><a name="p338192124118"></a>disk</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p143817234115"><a name="p143817234115"></a><a name="p143817234115"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p1381422419"><a name="p1381422419"></a><a name="p1381422419"></a>该<span id="text1967413774516"><a name="text1967413774516"></a><a name="text1967413774516"></a>云服务器</span>规格对应要求系统盘大小，0为不限制。</p>
<p id="p155897161110"><a name="p155897161110"></a><a name="p155897161110"></a>在微版本2.47及以上版本支持。</p>
</td>
</tr>
<tr id="row14477413101710"><td class="cellrowborder" valign="top" width="20.677932206779325%" headers="mcps1.2.4.1.1 "><p id="p175990512419"><a name="p175990512419"></a><a name="p175990512419"></a>ephemeral</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p55996517419"><a name="p55996517419"></a><a name="p55996517419"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p1059914514118"><a name="p1059914514118"></a><a name="p1059914514118"></a>未使用。</p>
<p id="p138227319114"><a name="p138227319114"></a><a name="p138227319114"></a>在微版本2.47及以上版本支持。</p>
</td>
</tr>
<tr id="row184771134175"><td class="cellrowborder" valign="top" width="20.677932206779325%" headers="mcps1.2.4.1.1 "><p id="p66306183429"><a name="p66306183429"></a><a name="p66306183429"></a>swap</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p863019183421"><a name="p863019183421"></a><a name="p863019183421"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p15630121813429"><a name="p15630121813429"></a><a name="p15630121813429"></a>未使用。</p>
<p id="p568210631113"><a name="p568210631113"></a><a name="p568210631113"></a>在微版本2.47及以上版本支持。</p>
</td>
</tr>
<tr id="row154771813181718"><td class="cellrowborder" valign="top" width="20.677932206779325%" headers="mcps1.2.4.1.1 "><p id="p1936516339428"><a name="p1936516339428"></a><a name="p1936516339428"></a>original_name</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p163651333144219"><a name="p163651333144219"></a><a name="p163651333144219"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p2365113374215"><a name="p2365113374215"></a><a name="p2365113374215"></a><span id="text1537920819450"><a name="text1537920819450"></a><a name="text1537920819450"></a>云服务器</span>规格名称。</p>
<p id="p47911894115"><a name="p47911894115"></a><a name="p47911894115"></a>在微版本2.47及以上版本支持。</p>
</td>
</tr>
<tr id="row62747810179"><td class="cellrowborder" valign="top" width="20.677932206779325%" headers="mcps1.2.4.1.1 "><p id="p136311336194210"><a name="p136311336194210"></a><a name="p136311336194210"></a>extra_specs</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p563116366423"><a name="p563116366423"></a><a name="p563116366423"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="49.43505649435057%" headers="mcps1.2.4.1.3 "><p id="p10674132212106"><a name="p10674132212106"></a><a name="p10674132212106"></a>flavor扩展字段请参考：<a href="数据结构(查询规格详情).md">os_extra_specs（flavor）字段数据结构说明</a></p>
<p id="p68221938111119"><a name="p68221938111119"></a><a name="p68221938111119"></a>在微版本2.47及以上版本支持。</p>
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
<td class="cellrowborder" valign="top" width="49.5%" headers="mcps1.2.4.1.3 "><p id="p1399417684820"><a name="p1399417684820"></a><a name="p1399417684820"></a>镜像相关标记快捷链接信息，详情请参见<a href="#table35230296">表6</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  links字段数据结构说明

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

**表 7**  弹性云服务器所属网络信息的数据结构说明

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

**表 8**  os-extended-volumes:volumes\_attached字段数据结构说明

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
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p110774385110"><a name="p110774385110"></a><a name="p110774385110"></a>一个标志，指示在删除服务器时是否删除附加的卷。</p>
<p id="p856184314483"><a name="p856184314483"></a><a name="p856184314483"></a>默认情况下，这是False</p>
<p id="p1169334275311"><a name="p1169334275311"></a><a name="p1169334275311"></a>微版本2.3及以上版本支持。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  security\_groups字段数据结构说明

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

**表 10**  fault字段数据结构说明

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

**表 11**  os:scheduler\_hints参数

<a name="zh-cn_topic_0057972661_table12534817105641"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972661_row26068168105641"><th class="cellrowborder" valign="top" width="25.740000000000002%" id="mcps1.2.5.1.1"><p id="p1858783513243"><a name="p1858783513243"></a><a name="p1858783513243"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12.46%" id="mcps1.2.5.1.2"><p id="p165381328142"><a name="p165381328142"></a><a name="p165381328142"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.01%" id="mcps1.2.5.1.3"><p id="p360443592415"><a name="p360443592415"></a><a name="p360443592415"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="41.79%" id="mcps1.2.5.1.4"><p id="p160413532410"><a name="p160413532410"></a><a name="p160413532410"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972661_row63947270105641"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p12417014105656"><a name="zh-cn_topic_0057972661_p12417014105656"></a><a name="zh-cn_topic_0057972661_p12417014105656"></a>tenancy</p>
</td>
<td class="cellrowborder" valign="top" width="12.46%" headers="mcps1.2.5.1.2 "><p id="p1854062161414"><a name="p1854062161414"></a><a name="p1854062161414"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.01%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p66254100105656"><a name="zh-cn_topic_0057972661_p66254100105656"></a><a name="zh-cn_topic_0057972661_p66254100105656"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="41.79%" headers="mcps1.2.5.1.4 "><p id="p2075515233412"><a name="p2075515233412"></a><a name="p2075515233412"></a>在指定的专属主机或者共享主机上创建<span id="text47531458105820"><a name="text47531458105820"></a><a name="text47531458105820"></a>弹性云服务器</span>。</p>
<p id="p475545223418"><a name="p475545223418"></a><a name="p475545223418"></a>参数值为shared或者dedicated。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row31685405105641"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p19286814105656"><a name="zh-cn_topic_0057972661_p19286814105656"></a><a name="zh-cn_topic_0057972661_p19286814105656"></a>dedicated_host_id</p>
</td>
<td class="cellrowborder" valign="top" width="12.46%" headers="mcps1.2.5.1.2 "><p id="p2540112161416"><a name="p2540112161416"></a><a name="p2540112161416"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.01%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p18728119105656"><a name="zh-cn_topic_0057972661_p18728119105656"></a><a name="zh-cn_topic_0057972661_p18728119105656"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="41.79%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p65968369105656"><a name="zh-cn_topic_0057972661_p65968369105656"></a><a name="zh-cn_topic_0057972661_p65968369105656"></a>专属主机ID。</p>
<p id="zh-cn_topic_0057972661_p56844412105656"><a name="zh-cn_topic_0057972661_p56844412105656"></a><a name="zh-cn_topic_0057972661_p56844412105656"></a>此属性仅在tenancy值为dedicated时有效。</p>
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

