# 分配浮动IP（废弃，不推荐使用）<a name="ZH-CN_TOPIC_0065817718"></a>

## 功能介绍<a name="zh-cn_topic_0057972997_section32822464"></a>

将浮动IP绑定到一台云服务器上。

## 接口约束<a name="zh-cn_topic_0057972997_section41373960"></a>

-   该API准备废弃，从微版本2.44开始，调用该接口将报404错误。建议直接使用对应的网络服务接口["更新浮动IP"](https://support.huaweicloud.com/api-vpc/vpc_floatingiP_0004.html)。

## URI<a name="zh-cn_topic_0057972997_section26966728"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/action

参数说明请参见[表1](#zh-cn_topic_0057972997_table32475667)。

**表 1**  参数说明

<a name="zh-cn_topic_0057972997_table32475667"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972997_row44937496"><th class="cellrowborder" valign="top" width="22.24%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.87%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.88999999999999%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972997_row1664874"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972997_p637140"><a name="zh-cn_topic_0057972997_p637140"></a><a name="zh-cn_topic_0057972997_p637140"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972997_p51608407"><a name="zh-cn_topic_0057972997_p51608407"></a><a name="zh-cn_topic_0057972997_p51608407"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972997_row41565035"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972997_p11324657"><a name="zh-cn_topic_0057972997_p11324657"></a><a name="zh-cn_topic_0057972997_p11324657"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972997_p44882061"><a name="zh-cn_topic_0057972997_p44882061"></a><a name="zh-cn_topic_0057972997_p44882061"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972997_p11568292"><a name="zh-cn_topic_0057972997_p11568292"></a><a name="zh-cn_topic_0057972997_p11568292"></a>云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057972997_section62956448"></a>

请求参数如[表2](#zh-cn_topic_0057972997_table49322741)所示。

**表 2**  请求参数

<a name="zh-cn_topic_0057972997_table49322741"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972997_row35749488"><th class="cellrowborder" valign="top" width="22.37%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0057972997_p10027379"><a name="zh-cn_topic_0057972997_p10027379"></a><a name="zh-cn_topic_0057972997_p10027379"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.15%" id="mcps1.2.5.1.2"><p id="p1579692179"><a name="p1579692179"></a><a name="p1579692179"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="26.8%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0057972997_p6911408"><a name="zh-cn_topic_0057972997_p6911408"></a><a name="zh-cn_topic_0057972997_p6911408"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="37.68%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0057972997_p47267058"><a name="zh-cn_topic_0057972997_p47267058"></a><a name="zh-cn_topic_0057972997_p47267058"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972997_row3426504"><td class="cellrowborder" valign="top" width="22.37%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972997_p9111414"><a name="zh-cn_topic_0057972997_p9111414"></a><a name="zh-cn_topic_0057972997_p9111414"></a>addFloatingIp</p>
</td>
<td class="cellrowborder" valign="top" width="13.15%" headers="mcps1.2.5.1.2 "><p id="p2057918910178"><a name="p2057918910178"></a><a name="p2057918910178"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="26.8%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972997_p66935973"><a name="zh-cn_topic_0057972997_p66935973"></a><a name="zh-cn_topic_0057972997_p66935973"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="37.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972997_p6518693"><a name="zh-cn_topic_0057972997_p6518693"></a><a name="zh-cn_topic_0057972997_p6518693"></a>云服务器绑定浮动IP。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  addFloatingIp参数信息

<a name="zh-cn_topic_0057972997_table58252101"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972997_row45148248"><th class="cellrowborder" valign="top" width="21.59%" id="mcps1.2.5.1.1"><p id="p863285611197"><a name="p863285611197"></a><a name="p863285611197"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.930000000000001%" id="mcps1.2.5.1.2"><p id="p8861511151711"><a name="p8861511151711"></a><a name="p8861511151711"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="26.8%" id="mcps1.2.5.1.3"><p id="p86328569191"><a name="p86328569191"></a><a name="p86328569191"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="37.68%" id="mcps1.2.5.1.4"><p id="p863217564195"><a name="p863217564195"></a><a name="p863217564195"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972997_row23607505"><td class="cellrowborder" valign="top" width="21.59%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972997_p33159773"><a name="zh-cn_topic_0057972997_p33159773"></a><a name="zh-cn_topic_0057972997_p33159773"></a>address</p>
</td>
<td class="cellrowborder" valign="top" width="13.930000000000001%" headers="mcps1.2.5.1.2 "><p id="p88619112175"><a name="p88619112175"></a><a name="p88619112175"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="26.8%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972997_p1587126"><a name="zh-cn_topic_0057972997_p1587126"></a><a name="zh-cn_topic_0057972997_p1587126"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972997_p11263469"><a name="zh-cn_topic_0057972997_p11263469"></a><a name="zh-cn_topic_0057972997_p11263469"></a>浮动IP的IP地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972997_row34262360"><td class="cellrowborder" valign="top" width="21.59%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972997_p23787767"><a name="zh-cn_topic_0057972997_p23787767"></a><a name="zh-cn_topic_0057972997_p23787767"></a>fixed_address</p>
</td>
<td class="cellrowborder" valign="top" width="13.930000000000001%" headers="mcps1.2.5.1.2 "><p id="p3861211201716"><a name="p3861211201716"></a><a name="p3861211201716"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="26.8%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972997_p47760999"><a name="zh-cn_topic_0057972997_p47760999"></a><a name="zh-cn_topic_0057972997_p47760999"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="37.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972997_p28633049"><a name="zh-cn_topic_0057972997_p28633049"></a><a name="zh-cn_topic_0057972997_p28633049"></a>固定IP的IP地址，即你想要关联浮动IP的那个固定IP地址。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0057972997_section29737121"></a>

无

## 请求示例<a name="zh-cn_topic_0057972997_section66307504"></a>

```
POST https://{endpoint}/v2.1/9c53a566cb3443ab910cf0daebca90c4/servers/47e9be4e-a7b9-471f-92d9-ffc83814e07a/action
```

```
{
   "addFloatingIp" : {
       "address" : "10.144.2.1",
       "fixed_address" : "192.168.1.3"
    }
}
```

## 响应示例<a name="section462213664713"></a>

无

## 返回值<a name="zh-cn_topic_0057972997_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

