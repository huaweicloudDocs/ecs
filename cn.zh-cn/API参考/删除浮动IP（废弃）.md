# 删除浮动IP（废弃）<a name="ZH-CN_TOPIC_0065820819"></a>

## 功能介绍<a name="zh-cn_topic_0057972674_section41330139"></a>

删除浮动IP地址。

当前API已废弃，请使用["删除浮动IP"](https://support.huaweicloud.com/api-eip/eip_openstackapi_0010.html)。

## URI<a name="zh-cn_topic_0057972674_section36426933"></a>

DELETE /v2.1/\{project\_id\}/os-floating-ips/\{floating\_ip\_id\}

参数说明请参见[表1](#zh-cn_topic_0057972674_table32475667)。

**表 1**  参数说明

<a name="zh-cn_topic_0057972674_table32475667"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972674_row44937496"><th class="cellrowborder" valign="top" width="22.24%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.87%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.88999999999999%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972674_row1664874"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972674_p637140"><a name="zh-cn_topic_0057972674_p637140"></a><a name="zh-cn_topic_0057972674_p637140"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972674_p51608407"><a name="zh-cn_topic_0057972674_p51608407"></a><a name="zh-cn_topic_0057972674_p51608407"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972674_row102094505165"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972674_p620919503165"><a name="zh-cn_topic_0057972674_p620919503165"></a><a name="zh-cn_topic_0057972674_p620919503165"></a>floating_ip_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972674_p32091350111612"><a name="zh-cn_topic_0057972674_p32091350111612"></a><a name="zh-cn_topic_0057972674_p32091350111612"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972674_p2209205020164"><a name="zh-cn_topic_0057972674_p2209205020164"></a><a name="zh-cn_topic_0057972674_p2209205020164"></a>浮动IP的ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057972674_section64900454"></a>

无

## 响应消息<a name="zh-cn_topic_0057972674_section47233174"></a>

无

## 请求示例<a name="zh-cn_topic_0057972674_section22445387"></a>

```
DELETE https://{endpoint}/v2.1/e73621affb8f44e1bc01898747ca09d4/os-floating-ips/05f71f43-f3c9-47ef-ac8d-9f02aef66418
```

## 响应示例<a name="section38161942204920"></a>

无

## 返回值<a name="zh-cn_topic_0092803065_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

