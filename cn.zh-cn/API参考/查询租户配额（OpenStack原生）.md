# 查询租户配额<a name="ZH-CN_TOPIC_0067298110"></a>

## 功能介绍<a name="zh-cn_topic_0057973199_section15804956"></a>

查询配额，包括云服务器、CPU、内存等计算资源的规格。

提供user\_id参数，对应user执行相应操作，获取指定user的quota配置。

## URI<a name="zh-cn_topic_0057973199_section8026877"></a>

GET /v2.1/\{project\_id\}/os-quota-sets/\{project\_id\}?user\_id=\{user\_id\}

参数说明请参见[表1](#zh-cn_topic_0057973199_table12637461156)。

**表 1**  参数说明

<a name="zh-cn_topic_0057973199_table12637461156"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973199_row15273164612514"><th class="cellrowborder" valign="top" width="20.69%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.24%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="62.07%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973199_row828511468510"><td class="cellrowborder" valign="top" width="20.69%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p6287184613518"><a name="zh-cn_topic_0057973199_p6287184613518"></a><a name="zh-cn_topic_0057973199_p6287184613518"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p22901046657"><a name="zh-cn_topic_0057973199_p22901046657"></a><a name="zh-cn_topic_0057973199_p22901046657"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="62.07%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p1129212464514"><a name="zh-cn_topic_0057973199_p1129212464514"></a><a name="zh-cn_topic_0057973199_p1129212464514"></a>项目ID，如果指定的租户不存在，返回系统默认quota。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row132920461656"><td class="cellrowborder" valign="top" width="20.69%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p102952462511"><a name="zh-cn_topic_0057973199_p102952462511"></a><a name="zh-cn_topic_0057973199_p102952462511"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p1629820467514"><a name="zh-cn_topic_0057973199_p1629820467514"></a><a name="zh-cn_topic_0057973199_p1629820467514"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="62.07%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p1529916466519"><a name="zh-cn_topic_0057973199_p1529916466519"></a><a name="zh-cn_topic_0057973199_p1529916466519"></a>用户ID，如果指定的用户不存在，返回系统默认quota。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057973199_section13122166"></a>

无

## 响应消息<a name="zh-cn_topic_0057973199_section50990633"></a>

响应参数如[表2](#zh-cn_topic_0057973199_zh-cn_topic_0057973197_table62068690)所示。

**表 2**  响应参数

<a name="zh-cn_topic_0057973199_zh-cn_topic_0057973197_table62068690"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973199_zh-cn_topic_0057973197_row56098908"><th class="cellrowborder" valign="top" width="30.643064306430645%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0057973197_p47717737"><a name="zh-cn_topic_0057973197_p47717737"></a><a name="zh-cn_topic_0057973197_p47717737"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.643064306430645%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0057973197_p39931478"><a name="zh-cn_topic_0057973197_p39931478"></a><a name="zh-cn_topic_0057973197_p39931478"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="38.71387138713872%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0057973197_p64532721"><a name="zh-cn_topic_0057973197_p64532721"></a><a name="zh-cn_topic_0057973197_p64532721"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973199_zh-cn_topic_0057973197_row59767919"><td class="cellrowborder" valign="top" width="30.643064306430645%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_zh-cn_topic_0057973197_p9363310"><a name="zh-cn_topic_0057973199_zh-cn_topic_0057973197_p9363310"></a><a name="zh-cn_topic_0057973199_zh-cn_topic_0057973197_p9363310"></a>quota_set</p>
</td>
<td class="cellrowborder" valign="top" width="30.643064306430645%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_zh-cn_topic_0057973197_p20230678"><a name="zh-cn_topic_0057973199_zh-cn_topic_0057973197_p20230678"></a><a name="zh-cn_topic_0057973199_zh-cn_topic_0057973197_p20230678"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="38.71387138713872%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_zh-cn_topic_0057973197_p59256190"><a name="zh-cn_topic_0057973199_zh-cn_topic_0057973197_p59256190"></a><a name="zh-cn_topic_0057973199_zh-cn_topic_0057973197_p59256190"></a>quota_set对象，详情请参见<a href="#zh-cn_topic_0057973199_table30231561">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  quota\_set参数信息

<a name="zh-cn_topic_0057973199_table30231561"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973199_row25113310"><th class="cellrowborder" valign="top" width="30.769999999999996%" id="mcps1.2.4.1.1"><p id="p9963183415323"><a name="p9963183415323"></a><a name="p9963183415323"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.54%" id="mcps1.2.4.1.2"><p id="p0963133410326"><a name="p0963133410326"></a><a name="p0963133410326"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.69%" id="mcps1.2.4.1.3"><p id="p996317342321"><a name="p996317342321"></a><a name="p996317342321"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973199_row30393275"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p45936220"><a name="zh-cn_topic_0057973199_p45936220"></a><a name="zh-cn_topic_0057973199_p45936220"></a>cores</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p29846341"><a name="zh-cn_topic_0057973199_p29846341"></a><a name="zh-cn_topic_0057973199_p29846341"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p47666411392"><a name="zh-cn_topic_0057973199_p47666411392"></a><a name="zh-cn_topic_0057973199_p47666411392"></a>vcpu数量配额</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row50766756"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p18466542"><a name="zh-cn_topic_0057973199_p18466542"></a><a name="zh-cn_topic_0057973199_p18466542"></a>fixed_ips</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p1691612101512"><a name="zh-cn_topic_0057973199_p1691612101512"></a><a name="zh-cn_topic_0057973199_p1691612101512"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p7766144103912"><a name="zh-cn_topic_0057973199_p7766144103912"></a><a name="zh-cn_topic_0057973199_p7766144103912"></a>固定IP数量配额，目前不支持此参数</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row37686197"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p32683139"><a name="zh-cn_topic_0057973199_p32683139"></a><a name="zh-cn_topic_0057973199_p32683139"></a>floating_ips</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p158282315153"><a name="zh-cn_topic_0057973199_p158282315153"></a><a name="zh-cn_topic_0057973199_p158282315153"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p16766740399"><a name="zh-cn_topic_0057973199_p16766740399"></a><a name="zh-cn_topic_0057973199_p16766740399"></a>浮动IP数量配额，目前不支持此参数</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row60322465"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p54281500"><a name="zh-cn_topic_0057973199_p54281500"></a><a name="zh-cn_topic_0057973199_p54281500"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p34725355"><a name="zh-cn_topic_0057973199_p34725355"></a><a name="zh-cn_topic_0057973199_p34725355"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p107671041392"><a name="zh-cn_topic_0057973199_p107671041392"></a><a name="zh-cn_topic_0057973199_p107671041392"></a>project的UUID</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row53277152"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p20482050"><a name="zh-cn_topic_0057973199_p20482050"></a><a name="zh-cn_topic_0057973199_p20482050"></a>injected_file_content_bytes</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p193011246151"><a name="zh-cn_topic_0057973199_p193011246151"></a><a name="zh-cn_topic_0057973199_p193011246151"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p19767154163911"><a name="zh-cn_topic_0057973199_p19767154163911"></a><a name="zh-cn_topic_0057973199_p19767154163911"></a>注入文件的文件大小配额，单位字节</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row28988915"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p66400774"><a name="zh-cn_topic_0057973199_p66400774"></a><a name="zh-cn_topic_0057973199_p66400774"></a>injected_file_path_bytes</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p72501227151510"><a name="zh-cn_topic_0057973199_p72501227151510"></a><a name="zh-cn_topic_0057973199_p72501227151510"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p1176715413396"><a name="zh-cn_topic_0057973199_p1176715413396"></a><a name="zh-cn_topic_0057973199_p1176715413396"></a>注入文件的路径大小配额，单位字节</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row13369507"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p9188289"><a name="zh-cn_topic_0057973199_p9188289"></a><a name="zh-cn_topic_0057973199_p9188289"></a>injected_files</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p1460345412151"><a name="zh-cn_topic_0057973199_p1460345412151"></a><a name="zh-cn_topic_0057973199_p1460345412151"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p9767246391"><a name="zh-cn_topic_0057973199_p9767246391"></a><a name="zh-cn_topic_0057973199_p9767246391"></a>注入文件数量配额</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row59944257"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p23646677"><a name="zh-cn_topic_0057973199_p23646677"></a><a name="zh-cn_topic_0057973199_p23646677"></a>instances</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p97481655101511"><a name="zh-cn_topic_0057973199_p97481655101511"></a><a name="zh-cn_topic_0057973199_p97481655101511"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p1876714183917"><a name="zh-cn_topic_0057973199_p1876714183917"></a><a name="zh-cn_topic_0057973199_p1876714183917"></a><span id="text1079810298532"><a name="text1079810298532"></a><a name="text1079810298532"></a>云服务器</span>数量配额</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row5482215"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p41406250"><a name="zh-cn_topic_0057973199_p41406250"></a><a name="zh-cn_topic_0057973199_p41406250"></a>key_pairs</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p152511579158"><a name="zh-cn_topic_0057973199_p152511579158"></a><a name="zh-cn_topic_0057973199_p152511579158"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p1876716493911"><a name="zh-cn_topic_0057973199_p1876716493911"></a><a name="zh-cn_topic_0057973199_p1876716493911"></a>密钥对数量配额，目前不支持此参数</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row43614388"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p43104560"><a name="zh-cn_topic_0057973199_p43104560"></a><a name="zh-cn_topic_0057973199_p43104560"></a>metadata_items</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p5274115911512"><a name="zh-cn_topic_0057973199_p5274115911512"></a><a name="zh-cn_topic_0057973199_p5274115911512"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p187671742393"><a name="zh-cn_topic_0057973199_p187671742393"></a><a name="zh-cn_topic_0057973199_p187671742393"></a>元数据数量配额</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row20242451"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p29025826"><a name="zh-cn_topic_0057973199_p29025826"></a><a name="zh-cn_topic_0057973199_p29025826"></a>ram</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p23505391618"><a name="zh-cn_topic_0057973199_p23505391618"></a><a name="zh-cn_topic_0057973199_p23505391618"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p17670483911"><a name="zh-cn_topic_0057973199_p17670483911"></a><a name="zh-cn_topic_0057973199_p17670483911"></a>内存配额，单位MB</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row46426356"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p2438464"><a name="zh-cn_topic_0057973199_p2438464"></a><a name="zh-cn_topic_0057973199_p2438464"></a>security_group_rules</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p19881144163"><a name="zh-cn_topic_0057973199_p19881144163"></a><a name="zh-cn_topic_0057973199_p19881144163"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p97671453913"><a name="zh-cn_topic_0057973199_p97671453913"></a><a name="zh-cn_topic_0057973199_p97671453913"></a>每个安全组规则的配额，目前不支持此参数</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row50813968"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p22290707"><a name="zh-cn_topic_0057973199_p22290707"></a><a name="zh-cn_topic_0057973199_p22290707"></a>security_groups</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p181921769166"><a name="zh-cn_topic_0057973199_p181921769166"></a><a name="zh-cn_topic_0057973199_p181921769166"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p10769114153919"><a name="zh-cn_topic_0057973199_p10769114153919"></a><a name="zh-cn_topic_0057973199_p10769114153919"></a>安全组数量配额，目前不支持此参数</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row47118120"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p58471341"><a name="zh-cn_topic_0057973199_p58471341"></a><a name="zh-cn_topic_0057973199_p58471341"></a>server_groups</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p819119817166"><a name="zh-cn_topic_0057973199_p819119817166"></a><a name="zh-cn_topic_0057973199_p819119817166"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p7769944391"><a name="zh-cn_topic_0057973199_p7769944391"></a><a name="zh-cn_topic_0057973199_p7769944391"></a><span id="text529933165318"><a name="text529933165318"></a><a name="text529933165318"></a>云服务器</span>组数量配额。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973199_row18294597"><td class="cellrowborder" valign="top" width="30.769999999999996%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973199_p5467365"><a name="zh-cn_topic_0057973199_p5467365"></a><a name="zh-cn_topic_0057973199_p5467365"></a>server_group_members</p>
</td>
<td class="cellrowborder" valign="top" width="21.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973199_p172754921610"><a name="zh-cn_topic_0057973199_p172754921610"></a><a name="zh-cn_topic_0057973199_p172754921610"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.69%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973199_p5769134203914"><a name="zh-cn_topic_0057973199_p5769134203914"></a><a name="zh-cn_topic_0057973199_p5769134203914"></a><span id="text123511326537"><a name="text123511326537"></a><a name="text123511326537"></a>云服务器</span>组中云服务器个数配额。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0057973199_section56262520"></a>

```
GET https://{endpoint}/v2.1/d9ebe43510414ef590a4aa158605329e/os-quota-sets/d9ebe43510414ef590a4aa158605329e
```

## 响应示例<a name="section1965011613499"></a>

```
{
    "quota_set": {
        "cores": 20,
        "fixed_ips": 40,
        "floating_ips": 10,
        "id": "d9ebe43510414ef590a4aa158605329e",
        "injected_file_content_bytes": 10240,
        "injected_file_path_bytes": 255,
        "injected_files": 5,
        "instances": 20,
        "key_pairs": 100,
        "metadata_items": 128,
        "ram": 51200,
        "security_group_rules": 20,
        "security_groups": 50,
        "server_group_members": 10,
        "server_groups": 10
    }
}
```

## 返回值<a name="zh-cn_topic_0057973199_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

