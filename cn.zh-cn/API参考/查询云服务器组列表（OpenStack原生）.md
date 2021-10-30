# 查询云服务器组列表<a name="ecs_03_1402"></a>

## 功能介绍<a name="zh-cn_topic_0057973158_section14574577"></a>

查询云服务器组列表。

## URI<a name="zh-cn_topic_0057973158_section64062336"></a>

GET /v2.1/\{project\_id\}/os-server-groups

参数说明请参见[表1](#table12344152719154)。

**表 1**  参数说明

<a name="table12344152719154"></a>
<table><thead align="left"><tr id="row8345627191518"><th class="cellrowborder" valign="top" width="22.422242224222423%" id="mcps1.2.4.1.1"><p id="p86851935171514"><a name="p86851935171514"></a><a name="p86851935171514"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.301930193019302%" id="mcps1.2.4.1.2"><p id="p13685193551513"><a name="p13685193551513"></a><a name="p13685193551513"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="58.275827582758275%" id="mcps1.2.4.1.3"><p id="p5685163571516"><a name="p5685163571516"></a><a name="p5685163571516"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1434592713158"><td class="cellrowborder" valign="top" width="22.422242224222423%" headers="mcps1.2.4.1.1 "><p id="p26851935151517"><a name="p26851935151517"></a><a name="p26851935151517"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.301930193019302%" headers="mcps1.2.4.1.2 "><p id="p10685183518157"><a name="p10685183518157"></a><a name="p10685183518157"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="58.275827582758275%" headers="mcps1.2.4.1.3 "><p id="p166851235111514"><a name="p166851235111514"></a><a name="p166851235111514"></a>项目ID。</p>
<p id="p166861835101514"><a name="p166861835101514"></a><a name="p166861835101514"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

可以将如下作为URI参数，过滤查询结果。

使用方式：/v2/\{project\_id\}/os-server-groups?

## 请求消息<a name="section3227155991615"></a>

无

## 响应消息<a name="zh-cn_topic_0057973158_section10175274"></a>

响应参数如[表2](#table151218547156)所示。

**表 2**  响应参数

<a name="table151218547156"></a>
<table><thead align="left"><tr id="row18513175441514"><th class="cellrowborder" valign="top" width="22.650000000000002%" id="mcps1.2.4.1.1"><p id="p56771746163"><a name="p56771746163"></a><a name="p56771746163"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="26.340000000000003%" id="mcps1.2.4.1.2"><p id="p13677440167"><a name="p13677440167"></a><a name="p13677440167"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="51.01%" id="mcps1.2.4.1.3"><p id="p176771346162"><a name="p176771346162"></a><a name="p176771346162"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row4513354141513"><td class="cellrowborder" valign="top" width="22.650000000000002%" headers="mcps1.2.4.1.1 "><p id="p9677247166"><a name="p9677247166"></a><a name="p9677247166"></a>server_groups</p>
</td>
<td class="cellrowborder" valign="top" width="26.340000000000003%" headers="mcps1.2.4.1.2 "><p id="p66773471614"><a name="p66773471614"></a><a name="p66773471614"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="51.01%" headers="mcps1.2.4.1.3 "><p id="p116779419169"><a name="p116779419169"></a><a name="p116779419169"></a><span id="text1167724191615"><a name="text1167724191615"></a><a name="text1167724191615"></a>云服务器</span>组信息，参考<a href="#zh-cn_topic_0057973158_table47937085">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  server\_groups参数信息

<a name="zh-cn_topic_0057973158_table47937085"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973158_row65811616"><th class="cellrowborder" valign="top" width="21.39%" id="mcps1.2.4.1.1"><p id="p6654124612269"><a name="p6654124612269"></a><a name="p6654124612269"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.91%" id="mcps1.2.4.1.2"><p id="p1865454611261"><a name="p1865454611261"></a><a name="p1865454611261"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.7%" id="mcps1.2.4.1.3"><p id="p6654446102616"><a name="p6654446102616"></a><a name="p6654446102616"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973158_row33147825"><td class="cellrowborder" valign="top" width="21.39%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973158_p619317"><a name="zh-cn_topic_0057973158_p619317"></a><a name="zh-cn_topic_0057973158_p619317"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="22.91%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973158_p50164680"><a name="zh-cn_topic_0057973158_p50164680"></a><a name="zh-cn_topic_0057973158_p50164680"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.7%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973158_p28602690"><a name="zh-cn_topic_0057973158_p28602690"></a><a name="zh-cn_topic_0057973158_p28602690"></a><span id="text17659035105418"><a name="text17659035105418"></a><a name="text17659035105418"></a>云服务器</span>组UUID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row56097620"><td class="cellrowborder" valign="top" width="21.39%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973158_p47613365"><a name="zh-cn_topic_0057973158_p47613365"></a><a name="zh-cn_topic_0057973158_p47613365"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="22.91%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973158_p31477322"><a name="zh-cn_topic_0057973158_p31477322"></a><a name="zh-cn_topic_0057973158_p31477322"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.7%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973158_p28736562"><a name="zh-cn_topic_0057973158_p28736562"></a><a name="zh-cn_topic_0057973158_p28736562"></a><span id="text179641361541"><a name="text179641361541"></a><a name="text179641361541"></a>云服务器</span>组名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row29632828"><td class="cellrowborder" valign="top" width="21.39%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973158_p51448853"><a name="zh-cn_topic_0057973158_p51448853"></a><a name="zh-cn_topic_0057973158_p51448853"></a>members</p>
</td>
<td class="cellrowborder" valign="top" width="22.91%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973158_p6607563"><a name="zh-cn_topic_0057973158_p6607563"></a><a name="zh-cn_topic_0057973158_p6607563"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="55.7%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973158_p67004395"><a name="zh-cn_topic_0057973158_p67004395"></a><a name="zh-cn_topic_0057973158_p67004395"></a><span id="text3988193715542"><a name="text3988193715542"></a><a name="text3988193715542"></a>云服务器</span>组中包含的<span id="text385203885412"><a name="text385203885412"></a><a name="text385203885412"></a>云服务器</span>列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row66168651"><td class="cellrowborder" valign="top" width="21.39%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973158_p58060511"><a name="zh-cn_topic_0057973158_p58060511"></a><a name="zh-cn_topic_0057973158_p58060511"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="22.91%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973158_p5280980"><a name="zh-cn_topic_0057973158_p5280980"></a><a name="zh-cn_topic_0057973158_p5280980"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="55.7%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973158_p20340992"><a name="zh-cn_topic_0057973158_p20340992"></a><a name="zh-cn_topic_0057973158_p20340992"></a><span id="text2066033910549"><a name="text2066033910549"></a><a name="text2066033910549"></a>云服务器</span>组元数据。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row32671040185312"><td class="cellrowborder" valign="top" width="21.39%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973158_p64633146"><a name="zh-cn_topic_0057973158_p64633146"></a><a name="zh-cn_topic_0057973158_p64633146"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="22.91%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973158_p793464"><a name="zh-cn_topic_0057973158_p793464"></a><a name="zh-cn_topic_0057973158_p793464"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.7%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973158_p38538274"><a name="zh-cn_topic_0057973158_p38538274"></a><a name="zh-cn_topic_0057973158_p38538274"></a><span id="text164069404549"><a name="text164069404549"></a><a name="text164069404549"></a>云服务器</span>组所属租户ID，UUID格式。</p>
<p id="zh-cn_topic_0057973158_p457295075618"><a name="zh-cn_topic_0057973158_p457295075618"></a><a name="zh-cn_topic_0057973158_p457295075618"></a>微版本2.13及以上版本支持。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row146121548185317"><td class="cellrowborder" valign="top" width="21.39%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973158_p11612848145317"><a name="zh-cn_topic_0057973158_p11612848145317"></a><a name="zh-cn_topic_0057973158_p11612848145317"></a>policies</p>
</td>
<td class="cellrowborder" valign="top" width="22.91%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973158_p961210488537"><a name="zh-cn_topic_0057973158_p961210488537"></a><a name="zh-cn_topic_0057973158_p961210488537"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="55.7%" headers="mcps1.2.4.1.3 "><div class="p" id="p11241458144516"><a name="p11241458144516"></a><a name="p11241458144516"></a>与<span id="text512594195414"><a name="text512594195414"></a><a name="text512594195414"></a>云服务器</span>组关联的策略名称列表。包括：<a name="zh-cn_topic_0057973153_ul1237514118527"></a><a name="zh-cn_topic_0057973153_ul1237514118527"></a><ul id="zh-cn_topic_0057973153_ul1237514118527"><li>anti-affinity：此组中的<span id="text108531141105410"><a name="text108531141105410"></a><a name="text108531141105410"></a>云服务器</span>必须安排到不同的主机。</li><li>affinity：此组中的<span id="text45441542205412"><a name="text45441542205412"></a><a name="text45441542205412"></a>云服务器</span>必须安排在同一主机上。</li><li>soft-anti-affinity：如果可能，应将此组中的<span id="text19269184312543"><a name="text19269184312543"></a><a name="text19269184312543"></a>云服务器</span>尽量安排到不同的主机上，但如果无法实现，则仍应安排它们，而不是导致生成失败。</li><li>soft-affinity：如果可能，应将此组中的<span id="text146184418540"><a name="text146184418540"></a><a name="text146184418540"></a>云服务器</span>尽量安排在同一主机上， 但如果无法实现，则仍应安排它们，而不是导致生成失败。</li></ul>
</div>
<div class="note" id="note5401171874620"><a name="note5401171874620"></a><a name="note5401171874620"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p540151814611"><a name="p540151814611"></a><a name="p540151814611"></a>当前仅支持反亲和性anti-affinity策略。不建议使用其他策略。如果使用其他策略云服务器组可能会创建失败。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row1110365011537"><td class="cellrowborder" valign="top" width="21.39%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973158_p110325019536"><a name="zh-cn_topic_0057973158_p110325019536"></a><a name="zh-cn_topic_0057973158_p110325019536"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="22.91%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973158_p1310325019539"><a name="zh-cn_topic_0057973158_p1310325019539"></a><a name="zh-cn_topic_0057973158_p1310325019539"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.7%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973158_p16833172165712"><a name="zh-cn_topic_0057973158_p16833172165712"></a><a name="zh-cn_topic_0057973158_p16833172165712"></a><span id="text14924044115417"><a name="text14924044115417"></a><a name="text14924044115417"></a>云服务器</span>组所属用户ID，UUID格式。</p>
<p id="zh-cn_topic_0057973158_p1783472155719"><a name="zh-cn_topic_0057973158_p1783472155719"></a><a name="zh-cn_topic_0057973158_p1783472155719"></a>微版本2.13及以上版本支持。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0057973158_section24468610"></a>

```
GET https://{endpoint}/v2.1/9c53a566cb3443ab910cf0daebca90c4/os-server-groups
```

## 响应示例<a name="section451882185114"></a>

```
{
    "server_groups": [
        {
            "id": "616fb98f-46ca-475e-917e-2563e5a8cd19",
            "name": "test",
            "policies": ["anti-affinity"],
            "members": [],
            "metadata": {},
            "project_id": "9c53a566cb3443ab910cf0daebca90c4"
        }
    ]
}
```

## 返回值<a name="zh-cn_topic_0057973158_section1220312142315"></a>

请参考[通用请求返回值](通用请求返回值.md)。

