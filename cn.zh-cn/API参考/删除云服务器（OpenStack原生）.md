# 删除云服务器<a name="ZH-CN_TOPIC_0025560296"></a>

## 功能介绍<a name="section4329148591032"></a>

删除一台云服务器。

## 扩展说明<a name="section14125473229"></a>

在Juno版本中当弹性云服务器被删除时，弹性云服务器挂载的所有的port都会被删除；而在Mitaka版本中当弹性云服务器被删除时，如果port是在创建弹性云服务器时指定的（即用户创建的port），则不会被删除。

注：此功能采用了配置开关方式，支持M版本原生处理方式，也支持J版本的兼容模式，版本缺省使用M版本原生处理方式，老版本升级采用支持J版本的兼容模式。

## URI<a name="section1832690791032"></a>

DELETE /v2/\{project\_id\}/servers/\{server\_id\}

DELETE /v2.1/\{project\_id\}/servers/\{server\_id\}

参数说明请参见[表1](#table2659898791032)。

**表 1**  参数说明

<a name="table2659898791032"></a>
<table><thead align="left"><tr id="row4869561291032"><th class="cellrowborder" valign="top" width="33.333333333333336%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.171717171717173%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="49.494949494949495%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6666852391032"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p3144131991032"><a name="p3144131991032"></a><a name="p3144131991032"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.2 "><p id="p6371887891032"><a name="p6371887891032"></a><a name="p6371887891032"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="49.494949494949495%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row5885541191134"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p255895491134"><a name="p255895491134"></a><a name="p255895491134"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="17.171717171717173%" headers="mcps1.2.4.1.2 "><p id="p594874291134"><a name="p594874291134"></a><a name="p594874291134"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="49.494949494949495%" headers="mcps1.2.4.1.3 "><p id="p1208612791134"><a name="p1208612791134"></a><a name="p1208612791134"></a>云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section1172872291032"></a>

不涉及

## 响应消息<a name="section6619360391225"></a>

不涉及

## 返回值<a name="section3477250491225"></a>

请参考[通用请求返回值](通用请求返回值.md)。

