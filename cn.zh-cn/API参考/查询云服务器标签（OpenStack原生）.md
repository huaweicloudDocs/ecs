# 查询云服务器标签<a name="ZH-CN_TOPIC_0065820822"></a>

查看弹性云服务器的所有Tag。

需在客户端通过以下HTTP header指定微版本号：X-OpenStack-Nova-API-Version: 2.26。

## URI<a name="zh-cn_topic_0057972837_section48648066"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/tags

参数说明请参见[表1](#zh-cn_topic_0057972837_table32475667)。

**表 1**  参数说明

<a name="zh-cn_topic_0057972837_table32475667"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972837_row44937496"><th class="cellrowborder" valign="top" width="22.24%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.87%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.88999999999999%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972837_row1664874"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972837_p637140"><a name="zh-cn_topic_0057972837_p637140"></a><a name="zh-cn_topic_0057972837_p637140"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972837_p51608407"><a name="zh-cn_topic_0057972837_p51608407"></a><a name="zh-cn_topic_0057972837_p51608407"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972837_row41565035"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972837_p11324657"><a name="zh-cn_topic_0057972837_p11324657"></a><a name="zh-cn_topic_0057972837_p11324657"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972837_p44882061"><a name="zh-cn_topic_0057972837_p44882061"></a><a name="zh-cn_topic_0057972837_p44882061"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972837_p11568292"><a name="zh-cn_topic_0057972837_p11568292"></a><a name="zh-cn_topic_0057972837_p11568292"></a><span id="text1677015675519"><a name="text1677015675519"></a><a name="text1677015675519"></a>云服务器</span>ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057972837_section35179415"></a>

无

## 响应消息<a name="zh-cn_topic_0057972837_section1485113257556"></a>

响应参数如[表2](#zh-cn_topic_0057972838_table28387752)所示。

**表 2**  响应参数

<a name="zh-cn_topic_0057972838_table28387752"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972838_row66802302"><th class="cellrowborder" valign="top" width="17%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0057972838_p42277343"><a name="zh-cn_topic_0057972838_p42277343"></a><a name="zh-cn_topic_0057972838_p42277343"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0057972838_p1912753"><a name="zh-cn_topic_0057972838_p1912753"></a><a name="zh-cn_topic_0057972838_p1912753"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="65%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0057972838_p217030"><a name="zh-cn_topic_0057972838_p217030"></a><a name="zh-cn_topic_0057972838_p217030"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972838_row17579482"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972838_p14651901"><a name="zh-cn_topic_0057972838_p14651901"></a><a name="zh-cn_topic_0057972838_p14651901"></a>tags</p>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972838_p45953370"><a name="zh-cn_topic_0057972838_p45953370"></a><a name="zh-cn_topic_0057972838_p45953370"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972838_p47045852"><a name="zh-cn_topic_0057972838_p47045852"></a><a name="zh-cn_topic_0057972838_p47045852"></a><span id="text07151057145520"><a name="text07151057145520"></a><a name="text07151057145520"></a>云服务器</span>tag列表。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section14532216125819"></a>

```
GET https://{endpoint}/v2.1/{project_id}/servers/{server_id}/tags
```

## 响应示例<a name="section1956815525910"></a>

响应示例

```
{ 
    "tags": ["baz=xyy", "foo", "qux"]
}
```

## 返回值<a name="zh-cn_topic_0057972837_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

