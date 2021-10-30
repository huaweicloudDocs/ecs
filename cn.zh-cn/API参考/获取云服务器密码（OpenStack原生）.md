# 获取云服务器密码<a name="ecs_03_1205"></a>

## 功能介绍<a name="section57769674"></a>

当通过支持Cloudbase-init功能的镜像创建Windows云服务器时，获取云服务器初始安装时系统生成的管理员帐户（Administrator帐户或Cloudbase-init设置的帐户）随机密码。

当云服务器启动后，需要等待5\~10分钟，保证密码注入完成，才可使用此接口查询到密码。

Linux云服务器未使用此通道获取密码。

## URI<a name="section50165025"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/os-server-password

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
<td class="cellrowborder" valign="top" width="59.27%" headers="mcps1.2.4.1.3 "><p id="p1719074216521"><a name="p1719074216521"></a><a name="p1719074216521"></a><span id="text13948846135314"><a name="text13948846135314"></a><a name="text13948846135314"></a>云服务器</span>ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section48832041"></a>

无

## 响应消息<a name="section36835188"></a>

响应参数如[表2](#table23477058)所示。

**表 2**  响应参数

<a name="table23477058"></a>
<table><thead align="left"><tr id="row2792905"><th class="cellrowborder" valign="top" width="22.052205220522055%" id="mcps1.2.4.1.1"><p id="p24898733"><a name="p24898733"></a><a name="p24898733"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="32.20322032203221%" id="mcps1.2.4.1.2"><p id="p17614915"><a name="p17614915"></a><a name="p17614915"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="45.744574457445744%" id="mcps1.2.4.1.3"><p id="p17521988"><a name="p17521988"></a><a name="p17521988"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row9994955"><td class="cellrowborder" valign="top" width="22.052205220522055%" headers="mcps1.2.4.1.1 "><p id="p4284989"><a name="p4284989"></a><a name="p4284989"></a>password</p>
</td>
<td class="cellrowborder" valign="top" width="32.20322032203221%" headers="mcps1.2.4.1.2 "><p id="p62312200"><a name="p62312200"></a><a name="p62312200"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.744574457445744%" headers="mcps1.2.4.1.3 "><p id="p60002101"><a name="p60002101"></a><a name="p60002101"></a>加密后的密码。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section10960125004315"></a>

```
GET https://{endpoint}/v2.1/{project_id}/servers/{server_id}/os-server-password
```

## 响应示例<a name="section15240205325510"></a>

```
{
    "password": "UHC9+YW1xDC1Yu8Mg9n+tnOp7euEO/cW//9KgdJKWhr5w=="
}
```

## 返回值<a name="section63081244"></a>

请参考[通用请求返回值](通用请求返回值.md)。

