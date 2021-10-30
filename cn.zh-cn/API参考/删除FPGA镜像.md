# 删除FPGA镜像<a name="ecs_02_1202"></a>

## 功能介绍<a name="section19527005211725"></a>

本接口用于删除FPGA镜像。

>![](public_sys-resources/icon-note.gif) **说明：** 
>目前仅“华北-北京一、华东-上海二、华南-广州”区域支持，其他区域暂未支持。

## URI<a name="section38661040211725"></a>

DELETE /v1/\{project\_id\}/cloudservers/fpga\_image/\{fpga\_image\_id\}

参数说明请参见[表1](#table44329634211725)。

**表 1**  参数说明

<a name="table44329634211725"></a>
<table><thead align="left"><tr id="row41557603211725"><th class="cellrowborder" valign="top" width="23.580000000000002%" id="mcps1.2.4.1.1"><p id="p7707213"><a name="p7707213"></a><a name="p7707213"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.57%" id="mcps1.2.4.1.2"><p id="p20304554"><a name="p20304554"></a><a name="p20304554"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="57.85%" id="mcps1.2.4.1.3"><p id="p34056167"><a name="p34056167"></a><a name="p34056167"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row55081924211725"><td class="cellrowborder" valign="top" width="23.580000000000002%" headers="mcps1.2.4.1.1 "><p id="p50162201211725"><a name="p50162201211725"></a><a name="p50162201211725"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.57%" headers="mcps1.2.4.1.2 "><p id="p27862189211725"><a name="p27862189211725"></a><a name="p27862189211725"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="57.85%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row30180665211725"><td class="cellrowborder" valign="top" width="23.580000000000002%" headers="mcps1.2.4.1.1 "><p id="p44186266211725"><a name="p44186266211725"></a><a name="p44186266211725"></a>fpga_image_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.57%" headers="mcps1.2.4.1.2 "><p id="p17752625211725"><a name="p17752625211725"></a><a name="p17752625211725"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="57.85%" headers="mcps1.2.4.1.3 "><p id="p33122615211725"><a name="p33122615211725"></a><a name="p33122615211725"></a>FPGA镜像的ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section49362668211725"></a>

无

## 响应消息<a name="section34595306211725"></a>

无

## 请求示例<a name="section20514490211725"></a>

```
DELETE https://{endpoint}/v1/{project_id}/cloudservers/fpga_image/{fpga_image_id}
```

## 响应示例<a name="section142498762720"></a>

无

## 返回值<a name="section3477250491225"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码](错误码.md)。

