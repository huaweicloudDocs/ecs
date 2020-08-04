# 删除云服务器<a name="ZH-CN_TOPIC_0025560296"></a>

## 功能介绍<a name="section4329148591032"></a>

删除一台云服务器。

## 接口约束<a name="section14125473229"></a>

当弹性云服务器被删除时，通过Openstack Nova API指定 port\_id 参数挂载的网卡会保留，通过指定 net\_id 挂载的网卡会被删除。

## URI<a name="section1832690791032"></a>

DELETE /v2.1/\{project\_id\}/servers/\{server\_id\}

参数说明请参见[表1](#table2659898791032)。

**表 1**  参数说明

<a name="table2659898791032"></a>
<table><thead align="left"><tr id="row4869561291032"><th class="cellrowborder" valign="top" width="21.626262626262626%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.686868686868685%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="58.686868686868685%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6666852391032"><td class="cellrowborder" valign="top" width="21.626262626262626%" headers="mcps1.2.4.1.1 "><p id="p3144131991032"><a name="p3144131991032"></a><a name="p3144131991032"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.686868686868685%" headers="mcps1.2.4.1.2 "><p id="p6371887891032"><a name="p6371887891032"></a><a name="p6371887891032"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="58.686868686868685%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row5885541191134"><td class="cellrowborder" valign="top" width="21.626262626262626%" headers="mcps1.2.4.1.1 "><p id="p255895491134"><a name="p255895491134"></a><a name="p255895491134"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.686868686868685%" headers="mcps1.2.4.1.2 "><p id="p594874291134"><a name="p594874291134"></a><a name="p594874291134"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="58.686868686868685%" headers="mcps1.2.4.1.3 "><p id="p1208612791134"><a name="p1208612791134"></a><a name="p1208612791134"></a><span id="text1724179113718"><a name="text1724179113718"></a><a name="text1724179113718"></a>云服务器</span>ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section1172872291032"></a>

无

## 响应消息<a name="section6619360391225"></a>

无

## 请求示例<a name="section1399410202536"></a>

```
DELETE https://{endpoint}/v2.1/{project_id}/servers/{server_id}
```

## 响应示例<a name="section975263145318"></a>

无

## 返回值<a name="section3477250491225"></a>

请参考[通用请求返回值](通用请求返回值.md)。

