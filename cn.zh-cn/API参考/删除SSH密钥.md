# 删除SSH密钥<a name="ecs_03_1204"></a>

## 功能介绍<a name="section33132068"></a>

根据SSH密钥的名称，删除指定SSH密钥。

## URI<a name="section29753161"></a>

DELETE /v2.1/\{project\_id\}/os-keypairs/\{keypair\_name\}

参数说明请参见[表1](#table48776445)。

**表 1**  参数说明

<a name="table48776445"></a>
<table><thead align="left"><tr id="row64721603"><th class="cellrowborder" valign="top" width="25.44%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.93%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="53.63%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row8464456"><td class="cellrowborder" valign="top" width="25.44%" headers="mcps1.2.4.1.1 "><p id="p14532322"><a name="p14532322"></a><a name="p14532322"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20.93%" headers="mcps1.2.4.1.2 "><p id="p36267453"><a name="p36267453"></a><a name="p36267453"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="53.63%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row65190153"><td class="cellrowborder" valign="top" width="25.44%" headers="mcps1.2.4.1.1 "><p id="p45911036"><a name="p45911036"></a><a name="p45911036"></a>keypair_name</p>
</td>
<td class="cellrowborder" valign="top" width="20.93%" headers="mcps1.2.4.1.2 "><p id="p27806444"><a name="p27806444"></a><a name="p27806444"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="53.63%" headers="mcps1.2.4.1.3 "><p id="p37729472"><a name="p37729472"></a><a name="p37729472"></a>密钥名称。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section66451858"></a>

无

## 响应消息<a name="section61195818"></a>

无

## 请求示例<a name="section118665219435"></a>

```
DELETE https://{endpoint}/v2.1/{project_id}/os-keypairs/{keypair_name}
```

## 响应示例<a name="section19716123044320"></a>

无

## 返回值<a name="section13891457"></a>

请参考[通用请求返回值](通用请求返回值.md)。

