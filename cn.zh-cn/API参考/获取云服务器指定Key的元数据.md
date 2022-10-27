# 获取云服务器指定Key的元数据<a name="ecs_03_1005"></a>

## 功能介绍<a name="zh-cn_topic_0057973169_section56350203"></a>

获取云服务器指定key的元数据信息。

## 调试<a name="section926243314015"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=ECS&api=NovaShowServerMetadataItem)中调试该接口。

## URI<a name="zh-cn_topic_0057973169_section37389779"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata/\{key\}

参数说明请参见[表1](#zh-cn_topic_0057973169_table32475667)。

**表 1**  参数说明

<a name="zh-cn_topic_0057973169_table32475667"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973169_row44937496"><th class="cellrowborder" valign="top" width="22.24%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.87%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.88999999999999%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973169_row1664874"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973169_p637140"><a name="zh-cn_topic_0057973169_p637140"></a><a name="zh-cn_topic_0057973169_p637140"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973169_p51608407"><a name="zh-cn_topic_0057973169_p51608407"></a><a name="zh-cn_topic_0057973169_p51608407"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973169_row41565035"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973169_p11324657"><a name="zh-cn_topic_0057973169_p11324657"></a><a name="zh-cn_topic_0057973169_p11324657"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973169_p44882061"><a name="zh-cn_topic_0057973169_p44882061"></a><a name="zh-cn_topic_0057973169_p44882061"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973169_p11568292"><a name="zh-cn_topic_0057973169_p11568292"></a><a name="zh-cn_topic_0057973169_p11568292"></a><span id="text5243113213529"><a name="text5243113213529"></a><a name="text5243113213529"></a>云服务器</span>ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973169_row1922793418562"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973169_p1922793475613"><a name="zh-cn_topic_0057973169_p1922793475613"></a><a name="zh-cn_topic_0057973169_p1922793475613"></a>key</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973169_p122714346560"><a name="zh-cn_topic_0057973169_p122714346560"></a><a name="zh-cn_topic_0057973169_p122714346560"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973169_p2022718345561"><a name="zh-cn_topic_0057973169_p2022718345561"></a><a name="zh-cn_topic_0057973169_p2022718345561"></a><span id="text1396473235212"><a name="text1396473235212"></a><a name="text1396473235212"></a>云服务器</span>metadata键值。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057973169_section10950734"></a>

无

## 响应消息<a name="zh-cn_topic_0057973169_section31447750"></a>

响应参数如[表2](#zh-cn_topic_0057973169_table40140147)所示。

**表 2**  响应参数

<a name="zh-cn_topic_0057973169_table40140147"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973169_row18362576"><th class="cellrowborder" valign="top" width="29.752975297529748%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0057973169_p10973688"><a name="zh-cn_topic_0057973169_p10973688"></a><a name="zh-cn_topic_0057973169_p10973688"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.752975297529748%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0057973169_p16453549"><a name="zh-cn_topic_0057973169_p16453549"></a><a name="zh-cn_topic_0057973169_p16453549"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40.49404940494049%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0057973169_p40683740"><a name="zh-cn_topic_0057973169_p40683740"></a><a name="zh-cn_topic_0057973169_p40683740"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973169_row7048614"><td class="cellrowborder" valign="top" width="29.752975297529748%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973165_p48441714"><a name="zh-cn_topic_0057973165_p48441714"></a><a name="zh-cn_topic_0057973165_p48441714"></a>meta</p>
</td>
<td class="cellrowborder" valign="top" width="29.752975297529748%" headers="mcps1.2.4.1.2 "><p id="p91831743181514"><a name="p91831743181514"></a><a name="p91831743181514"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="40.49404940494049%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973165_p13467047"><a name="zh-cn_topic_0057973165_p13467047"></a><a name="zh-cn_topic_0057973165_p13467047"></a>用户自定义键值对</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0057973169_section14594295"></a>

```
GET https://{endpoint}/v2.1/9c53a566cb3443ab910cf0daebca90c4/servers/998af54b-5762-4041-abc1-f98a2c27b3a2/metadata/key1
```

## 响应示例<a name="section148361253124314"></a>

```
{
	"meta": {
		"key1": "value1"
	}
}
```

## 返回值<a name="zh-cn_topic_0057973169_ecs_03_0202_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

