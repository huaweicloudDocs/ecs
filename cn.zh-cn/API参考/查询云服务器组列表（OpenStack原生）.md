# 查询云服务器组列表<a name="ZH-CN_TOPIC_0065817721"></a>

## 功能介绍<a name="zh-cn_topic_0057973158_section14574577"></a>

查询云服务器组列表。

## URI<a name="zh-cn_topic_0057973158_section64062336"></a>

GET /v2.1/\{project\_id\}/os-server-groups

参数说明请参见[表1](#zh-cn_topic_0057973158_zh-cn_topic_0020212650_table62669527)。

**表 1**  参数说明

<a name="zh-cn_topic_0057973158_zh-cn_topic_0020212650_table62669527"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973158_zh-cn_topic_0020212650_row33894570"><th class="cellrowborder" valign="top" width="20.74%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.05%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.209999999999994%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973158_zh-cn_topic_0020212650_row8419032"><td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973158_zh-cn_topic_0020212650_p10852974"><a name="zh-cn_topic_0057973158_zh-cn_topic_0020212650_p10852974"></a><a name="zh-cn_topic_0057973158_zh-cn_topic_0020212650_p10852974"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.05%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973158_zh-cn_topic_0020212650_p6675738"><a name="zh-cn_topic_0057973158_zh-cn_topic_0020212650_p6675738"></a><a name="zh-cn_topic_0057973158_zh-cn_topic_0020212650_p6675738"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="60.209999999999994%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

可以将如下作为URI参数，过滤查询结果。

使用方式：/v2/\{project\_id\}/os-server-groups?

-   支持租户查询自己的server\_group列表，目前最多返回1000条查询结果。

## 请求消息<a name="section3227155991615"></a>

无

## 响应消息<a name="zh-cn_topic_0057973158_section10175274"></a>

响应参数如[表2](#zh-cn_topic_0057973158_table37835893)所示。

**表 2**  响应参数

<a name="zh-cn_topic_0057973158_table37835893"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973158_row61250015"><th class="cellrowborder" valign="top" width="17.42%" id="mcps1.2.5.1.1"><p id="p64251742182612"><a name="p64251742182612"></a><a name="p64251742182612"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.810000000000002%" id="mcps1.2.5.1.2"><p id="p4425114212266"><a name="p4425114212266"></a><a name="p4425114212266"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="27.380000000000003%" id="mcps1.2.5.1.3"><p id="p164258426261"><a name="p164258426261"></a><a name="p164258426261"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="36.39000000000001%" id="mcps1.2.5.1.4"><p id="p1942534214263"><a name="p1942534214263"></a><a name="p1942534214263"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973158_row43900666"><td class="cellrowborder" valign="top" width="17.42%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973158_p66293025"><a name="zh-cn_topic_0057973158_p66293025"></a><a name="zh-cn_topic_0057973158_p66293025"></a>server_groups</p>
</td>
<td class="cellrowborder" valign="top" width="18.810000000000002%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057973158_p15994374"><a name="zh-cn_topic_0057973158_p15994374"></a><a name="zh-cn_topic_0057973158_p15994374"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="27.380000000000003%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973158_p1025965"><a name="zh-cn_topic_0057973158_p1025965"></a><a name="zh-cn_topic_0057973158_p1025965"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="36.39000000000001%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973158_p20475923"><a name="zh-cn_topic_0057973158_p20475923"></a><a name="zh-cn_topic_0057973158_p20475923"></a><span id="text1756312347541"><a name="text1756312347541"></a><a name="text1756312347541"></a>云服务器</span>组信息</p>
</td>
</tr>
</tbody>
</table>

**表 3**  server\_groups参数信息

<a name="zh-cn_topic_0057973158_table47937085"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973158_row65811616"><th class="cellrowborder" valign="top" width="17.481748174817483%" id="mcps1.2.5.1.1"><p id="p6654124612269"><a name="p6654124612269"></a><a name="p6654124612269"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.271827182718273%" id="mcps1.2.5.1.2"><p id="p193178411326"><a name="p193178411326"></a><a name="p193178411326"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18.72187218721872%" id="mcps1.2.5.1.3"><p id="p1865454611261"><a name="p1865454611261"></a><a name="p1865454611261"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="45.52455245524553%" id="mcps1.2.5.1.4"><p id="p6654446102616"><a name="p6654446102616"></a><a name="p6654446102616"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973158_row33147825"><td class="cellrowborder" valign="top" width="17.481748174817483%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973158_p619317"><a name="zh-cn_topic_0057973158_p619317"></a><a name="zh-cn_topic_0057973158_p619317"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.2.5.1.2 "><p id="p731784113211"><a name="p731784113211"></a><a name="p731784113211"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18.72187218721872%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973158_p50164680"><a name="zh-cn_topic_0057973158_p50164680"></a><a name="zh-cn_topic_0057973158_p50164680"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.52455245524553%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973158_p28602690"><a name="zh-cn_topic_0057973158_p28602690"></a><a name="zh-cn_topic_0057973158_p28602690"></a><span id="text17659035105418"><a name="text17659035105418"></a><a name="text17659035105418"></a>云服务器</span>组UUID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row56097620"><td class="cellrowborder" valign="top" width="17.481748174817483%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973158_p47613365"><a name="zh-cn_topic_0057973158_p47613365"></a><a name="zh-cn_topic_0057973158_p47613365"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.2.5.1.2 "><p id="p73176418323"><a name="p73176418323"></a><a name="p73176418323"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18.72187218721872%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973158_p31477322"><a name="zh-cn_topic_0057973158_p31477322"></a><a name="zh-cn_topic_0057973158_p31477322"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.52455245524553%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973158_p28736562"><a name="zh-cn_topic_0057973158_p28736562"></a><a name="zh-cn_topic_0057973158_p28736562"></a><span id="text179641361541"><a name="text179641361541"></a><a name="text179641361541"></a>云服务器</span>组名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row29632828"><td class="cellrowborder" valign="top" width="17.481748174817483%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973158_p51448853"><a name="zh-cn_topic_0057973158_p51448853"></a><a name="zh-cn_topic_0057973158_p51448853"></a>members</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.2.5.1.2 "><p id="p163171544326"><a name="p163171544326"></a><a name="p163171544326"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18.72187218721872%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973158_p6607563"><a name="zh-cn_topic_0057973158_p6607563"></a><a name="zh-cn_topic_0057973158_p6607563"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="45.52455245524553%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973158_p67004395"><a name="zh-cn_topic_0057973158_p67004395"></a><a name="zh-cn_topic_0057973158_p67004395"></a><span id="text3988193715542"><a name="text3988193715542"></a><a name="text3988193715542"></a>云服务器</span>组中包含的<span id="text385203885412"><a name="text385203885412"></a><a name="text385203885412"></a>云服务器</span>列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row66168651"><td class="cellrowborder" valign="top" width="17.481748174817483%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973158_p58060511"><a name="zh-cn_topic_0057973158_p58060511"></a><a name="zh-cn_topic_0057973158_p58060511"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.2.5.1.2 "><p id="p173171444324"><a name="p173171444324"></a><a name="p173171444324"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18.72187218721872%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973158_p5280980"><a name="zh-cn_topic_0057973158_p5280980"></a><a name="zh-cn_topic_0057973158_p5280980"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="45.52455245524553%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973158_p20340992"><a name="zh-cn_topic_0057973158_p20340992"></a><a name="zh-cn_topic_0057973158_p20340992"></a><span id="text2066033910549"><a name="text2066033910549"></a><a name="text2066033910549"></a>云服务器</span>组元数据。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row32671040185312"><td class="cellrowborder" valign="top" width="17.481748174817483%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973158_p64633146"><a name="zh-cn_topic_0057973158_p64633146"></a><a name="zh-cn_topic_0057973158_p64633146"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.2.5.1.2 "><p id="p12317204163220"><a name="p12317204163220"></a><a name="p12317204163220"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18.72187218721872%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973158_p793464"><a name="zh-cn_topic_0057973158_p793464"></a><a name="zh-cn_topic_0057973158_p793464"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.52455245524553%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973158_p38538274"><a name="zh-cn_topic_0057973158_p38538274"></a><a name="zh-cn_topic_0057973158_p38538274"></a><span id="text164069404549"><a name="text164069404549"></a><a name="text164069404549"></a>云服务器</span>组所属租户ID，UUID格式。</p>
<p id="zh-cn_topic_0057973158_p457295075618"><a name="zh-cn_topic_0057973158_p457295075618"></a><a name="zh-cn_topic_0057973158_p457295075618"></a>2.13版本新增。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row146121548185317"><td class="cellrowborder" valign="top" width="17.481748174817483%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973158_p11612848145317"><a name="zh-cn_topic_0057973158_p11612848145317"></a><a name="zh-cn_topic_0057973158_p11612848145317"></a>policies</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.2.5.1.2 "><p id="p131734123219"><a name="p131734123219"></a><a name="p131734123219"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18.72187218721872%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973158_p961210488537"><a name="zh-cn_topic_0057973158_p961210488537"></a><a name="zh-cn_topic_0057973158_p961210488537"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="45.52455245524553%" headers="mcps1.2.5.1.4 "><div class="p" id="p11241458144516"><a name="p11241458144516"></a><a name="p11241458144516"></a>与<span id="text512594195414"><a name="text512594195414"></a><a name="text512594195414"></a>云服务器</span>组关联的策略名称列表。包括：<a name="zh-cn_topic_0057973153_ul1237514118527"></a><a name="zh-cn_topic_0057973153_ul1237514118527"></a><ul id="zh-cn_topic_0057973153_ul1237514118527"><li>anti-affinity：此组中的<span id="text108531141105410"><a name="text108531141105410"></a><a name="text108531141105410"></a>云服务器</span>必须安排到不同的主机。</li><li>affinity：此组中的<span id="text45441542205412"><a name="text45441542205412"></a><a name="text45441542205412"></a>云服务器</span>必须安排在同一主机上。</li><li>soft-anti-affinity：如果可能，应将此组中的<span id="text19269184312543"><a name="text19269184312543"></a><a name="text19269184312543"></a>云服务器</span>尽量安排到不同的主机上，但如果无法实现，则仍应安排它们，而不是导致生成失败。</li><li>soft-affinity：如果可能，应将此组中的<span id="text146184418540"><a name="text146184418540"></a><a name="text146184418540"></a>云服务器</span>尽量安排在同一主机上， 但如果无法实现，则仍应安排它们，而不是导致生成失败。<div class="note" id="zh-cn_topic_0057973153_note172209325315"><a name="zh-cn_topic_0057973153_note172209325315"></a><a name="zh-cn_topic_0057973153_note172209325315"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0057973153_p17221036536"><a name="zh-cn_topic_0057973153_p17221036536"></a><a name="zh-cn_topic_0057973153_p17221036536"></a>当前仅支持反亲和性anti-affinity策略。</p>
</div></div>
</li></ul>
</div>
</td>
</tr>
<tr id="zh-cn_topic_0057973158_row1110365011537"><td class="cellrowborder" valign="top" width="17.481748174817483%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057973158_p110325019536"><a name="zh-cn_topic_0057973158_p110325019536"></a><a name="zh-cn_topic_0057973158_p110325019536"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.2.5.1.2 "><p id="p12317134183217"><a name="p12317134183217"></a><a name="p12317134183217"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18.72187218721872%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057973158_p1310325019539"><a name="zh-cn_topic_0057973158_p1310325019539"></a><a name="zh-cn_topic_0057973158_p1310325019539"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.52455245524553%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057973158_p16833172165712"><a name="zh-cn_topic_0057973158_p16833172165712"></a><a name="zh-cn_topic_0057973158_p16833172165712"></a><span id="text14924044115417"><a name="text14924044115417"></a><a name="text14924044115417"></a>云服务器</span>组所属用户ID，UUID格式。</p>
<p id="zh-cn_topic_0057973158_p1783472155719"><a name="zh-cn_topic_0057973158_p1783472155719"></a><a name="zh-cn_topic_0057973158_p1783472155719"></a>2.13版本新增。</p>
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

