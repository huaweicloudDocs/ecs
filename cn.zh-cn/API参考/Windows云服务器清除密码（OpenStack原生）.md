# Windows云服务器清除密码<a name="ZH-CN_TOPIC_0031176554"></a>

## 功能介绍<a name="section57769674"></a>

清除Windows云服务器初始安装时系统生成的密码记录。清除密码后，不影响云服务器密码登录功能，但不能再使用获取密码功能来查询该云服务器密码。

## URI<a name="section50165025"></a>

DELETE /v2.1/\{project\_id\}/servers/\{server\_id\}/os-server-password

参数说明请参见[表1](#table46110007)。

**表 1**  参数说明

<a name="table46110007"></a>
<table><thead align="left"><tr id="row14148614"><th class="cellrowborder" valign="top" width="20.74%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.99%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.27%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17201924"><td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.1 "><p id="p51178607"><a name="p51178607"></a><a name="p51178607"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.2 "><p id="p51826478"><a name="p51826478"></a><a name="p51826478"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="59.27%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row615338831654"><td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.1 "><p id="p519996316521"><a name="p519996316521"></a><a name="p519996316521"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.2 "><p id="p5588153816521"><a name="p5588153816521"></a><a name="p5588153816521"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="59.27%" headers="mcps1.2.4.1.3 "><p id="p1719074216521"><a name="p1719074216521"></a><a name="p1719074216521"></a><span id="text183704525531"><a name="text183704525531"></a><a name="text183704525531"></a>云服务器</span>ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section48832041"></a>

无

## 响应消息<a name="section1927776"></a>

无

## 请求示例<a name="section118665219435"></a>

```
DELETE https://{endpoint}/v2.1/{project_id}/servers/{server_id}/os-server-password
```

## 响应示例<a name="section19716123044320"></a>

无

## 返回值<a name="section17349988"></a>

请参考[通用请求返回值](通用请求返回值.md)。

