# 删除云服务器指定元数据<a name="ZH-CN_TOPIC_0025560299"></a>

## 功能介绍<a name="section5520708185439"></a>

删除云服务器指定元数据。

## 接口约束<a name="section4794112412015"></a>

云服务器状态（云服务器的OS-EXT-STS:vm\_state属性）必须是active，stopped，paused或者suspended。

## URI<a name="section65173692185439"></a>

DELETE /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata/\{key\}

参数说明请参见[表1](#table14014174185439)。

**表 1**  参数说明

<a name="table14014174185439"></a>
<table><thead align="left"><tr id="row32160776185439"><th class="cellrowborder" valign="top" width="19.99%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.67%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="61.339999999999996%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row26570121185439"><td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.1 "><p id="p4696221185439"><a name="p4696221185439"></a><a name="p4696221185439"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.67%" headers="mcps1.2.4.1.2 "><p id="p44849621185439"><a name="p44849621185439"></a><a name="p44849621185439"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="61.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row13357420185439"><td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.1 "><p id="p8209263185439"><a name="p8209263185439"></a><a name="p8209263185439"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.67%" headers="mcps1.2.4.1.2 "><p id="p60970546185439"><a name="p60970546185439"></a><a name="p60970546185439"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="61.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p39667165185439"><a name="p39667165185439"></a><a name="p39667165185439"></a><span id="text1957342419520"><a name="text1957342419520"></a><a name="text1957342419520"></a>云服务器</span>ID。</p>
</td>
</tr>
<tr id="row32078344185622"><td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.1 "><p id="p48209085185622"><a name="p48209085185622"></a><a name="p48209085185622"></a>key</p>
</td>
<td class="cellrowborder" valign="top" width="18.67%" headers="mcps1.2.4.1.2 "><p id="p12621798185622"><a name="p12621798185622"></a><a name="p12621798185622"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="61.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p15732716185622"><a name="p15732716185622"></a><a name="p15732716185622"></a>待删除的<span id="text94181625185212"><a name="text94181625185212"></a><a name="text94181625185212"></a>云服务器</span>metadata键值</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section21460169185439"></a>

无

## 响应消息<a name="section31286738185439"></a>

无

## 请求示例<a name="section43661451124217"></a>

```
DELETE https://{endpoint}/v2.1/{project_id}/servers/{server_id}/metadata/{key}
```

## 响应示例<a name="section105131358154219"></a>

无

## 返回值<a name="section4253667185439"></a>

请参考[通用请求返回值](通用请求返回值.md)。

