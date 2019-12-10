# Windows云服务器获取密码（企业项目）<a name="ZH-CN_TOPIC_0125978579"></a>

## 功能介绍<a name="section57769674"></a>

当通过支持Cloudbase-init功能的镜像创建Windows云服务器时，获取云服务器初始安装时系统生成的管理员帐户（Administrator帐户或Cloudbase-init设置的帐户）随机密码。

## URI<a name="section50165025"></a>

GET /v1/\{project\_id\}/cloudservers/\{server\_id\}/os-server-password

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

## 请求消息<a name="section1172344041018"></a>

无

## 响应消息<a name="section36835188"></a>

响应参数如[表2](#table23477058)所示。

**表 2**  响应参数

<a name="table23477058"></a>
<table><thead align="left"><tr id="row2792905"><th class="cellrowborder" valign="top" width="22.052205220522055%" id="mcps1.2.4.1.1"><p id="p24898733"><a name="p24898733"></a><a name="p24898733"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="32.20322032203221%" id="mcps1.2.4.1.2"><p id="p17614915"><a name="p17614915"></a><a name="p17614915"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="45.744574457445744%" id="mcps1.2.4.1.3"><p id="p17521988"><a name="p17521988"></a><a name="p17521988"></a>说明</p>
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

## 请求示例<a name="section1134418254116"></a>

```
GET https://{endpoint}/v1/{project_id}/cloudservers/{server_id}/os-server-password
```

## 响应示例<a name="section7495161632511"></a>

```
{
    "password": "UHC9+YW1xDC1Yu8Mg9n+tnOp7euEO/cW//9KgdJKWhr5w=="
}
```

## 返回值<a name="section63081244"></a>

请参考[通用请求返回值](通用请求返回值.md)。

