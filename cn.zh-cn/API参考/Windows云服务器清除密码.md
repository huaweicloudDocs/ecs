# Windows云服务器清除密码<a name="ZH-CN_TOPIC_0125983478"></a>

## 功能介绍<a name="section57769674"></a>

清除Windows云服务器初始安装时系统生成的密码记录。清除密码后，不影响云服务器密码登录功能，但不能再使用获取密码功能来查询该云服务器密码。

## URI<a name="section50165025"></a>

DELETE /v1/\{project\_id\}/cloudservers/\{server\_id\}/os-server-password

参数说明请参见[表1](#table35528365105553)。

**表 1**  参数说明

<a name="table35528365105553"></a>
<table><thead align="left"><tr id="row17119455105553"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p37105578"><a name="p37105578"></a><a name="p37105578"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p52761866"><a name="p52761866"></a><a name="p52761866"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p45852771"><a name="p45852771"></a><a name="p45852771"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row39853249105553"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p6887725105553"><a name="p6887725105553"></a><a name="p6887725105553"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p21034813105553"><a name="p21034813105553"></a><a name="p21034813105553"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row670727210579"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p41505172105731"><a name="p41505172105731"></a><a name="p41505172105731"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p6475762105731"><a name="p6475762105731"></a><a name="p6475762105731"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p54774717105731"><a name="p54774717105731"></a><a name="p54774717105731"></a>云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section48832041"></a>

无

## 响应消息<a name="section1927776"></a>

无

## 请求示例<a name="section270013359259"></a>

```
DELETE https://{endpoint}/v1/{project_id}/cloudservers/{server_id}/os-server-password
```

## 响应示例<a name="section53023424257"></a>

无

## 返回值<a name="section17349988"></a>

请参考[通用请求返回值](通用请求返回值.md)。

