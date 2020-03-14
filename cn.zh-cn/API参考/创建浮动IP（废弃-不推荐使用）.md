# 创建浮动IP（废弃，不推荐使用）<a name="ZH-CN_TOPIC_0065820816"></a>

## 功能介绍<a name="zh-cn_topic_0057972670_section30936422"></a>

创建浮动IP。

## 接口约束<a name="zh-cn_topic_0057972670_section22822288"></a>

-   用户需要去获取可用于分配浮动IP的网络资源池。获取方式如下：使用GET /v2.0/networks?router:external=True或neutron net-external-list方式获取。
-   该API准备废弃，建议直接使用对应的网络服务接口["创建浮动IP"](https://support.huaweicloud.com/api-vpc/vpc_floatingiP_0003.html)。

## URI<a name="zh-cn_topic_0057972670_section9992350"></a>

POST /v2.1/\{project\_id\}/os-floating-ips

参数说明请参见[表1](#zh-cn_topic_0057972670_table32475667)。

**表 1**  参数说明

<a name="zh-cn_topic_0057972670_table32475667"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972670_row44937496"><th class="cellrowborder" valign="top" width="22.24%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.87%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.88999999999999%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972670_row1664874"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972670_p637140"><a name="zh-cn_topic_0057972670_p637140"></a><a name="zh-cn_topic_0057972670_p637140"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972670_p51608407"><a name="zh-cn_topic_0057972670_p51608407"></a><a name="zh-cn_topic_0057972670_p51608407"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057972670_section4074007"></a>

请求参数如[表2](#zh-cn_topic_0057972670_table62287048)所示。

**表 2**  请求参数

<a name="zh-cn_topic_0057972670_table62287048"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972670_row38823967"><th class="cellrowborder" valign="top" width="16.73%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0057972670_p57733603"><a name="zh-cn_topic_0057972670_p57733603"></a><a name="zh-cn_topic_0057972670_p57733603"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.98%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0057972670_p45910260"><a name="zh-cn_topic_0057972670_p45910260"></a><a name="zh-cn_topic_0057972670_p45910260"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="20.119999999999997%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0057972670_p27743545"><a name="zh-cn_topic_0057972670_p27743545"></a><a name="zh-cn_topic_0057972670_p27743545"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="41.17%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0057972670_p32634650"><a name="zh-cn_topic_0057972670_p32634650"></a><a name="zh-cn_topic_0057972670_p32634650"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972670_row25276401"><td class="cellrowborder" valign="top" width="16.73%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972670_p34122633"><a name="zh-cn_topic_0057972670_p34122633"></a><a name="zh-cn_topic_0057972670_p34122633"></a>tenant_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.98%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972670_p12469873"><a name="zh-cn_topic_0057972670_p12469873"></a><a name="zh-cn_topic_0057972670_p12469873"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20.119999999999997%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972670_p3426769"><a name="zh-cn_topic_0057972670_p3426769"></a><a name="zh-cn_topic_0057972670_p3426769"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="41.17%" headers="mcps1.2.5.1.4 "><p id="p993215234119"><a name="p993215234119"></a><a name="p993215234119"></a>租户ID，在URI中指定。</p>
<p id="zh-cn_topic_0057972670_p9132882"><a name="zh-cn_topic_0057972670_p9132882"></a><a name="zh-cn_topic_0057972670_p9132882"></a>UUID格式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972670_row15087078"><td class="cellrowborder" valign="top" width="16.73%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972670_p14093819"><a name="zh-cn_topic_0057972670_p14093819"></a><a name="zh-cn_topic_0057972670_p14093819"></a>pool</p>
</td>
<td class="cellrowborder" valign="top" width="21.98%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972670_p748676"><a name="zh-cn_topic_0057972670_p748676"></a><a name="zh-cn_topic_0057972670_p748676"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="20.119999999999997%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972670_p60642794"><a name="zh-cn_topic_0057972670_p60642794"></a><a name="zh-cn_topic_0057972670_p60642794"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="41.17%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972670_p13119252"><a name="zh-cn_topic_0057972670_p13119252"></a><a name="zh-cn_topic_0057972670_p13119252"></a>用于分配浮动IP的资源池的名字，如果不指定，则使用默认资源池。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0057972670_section36666067"></a>

响应参数如[表3](#zh-cn_topic_0057972670_table56026474)所示。

**表 3**  响应参数

<a name="zh-cn_topic_0057972670_table56026474"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972670_row18214233"><th class="cellrowborder" valign="top" width="17.691769176917692%" id="mcps1.2.5.1.1"><p id="p1857817110255"><a name="p1857817110255"></a><a name="p1857817110255"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.591359135913592%" id="mcps1.2.5.1.2"><p id="p7269121916223"><a name="p7269121916223"></a><a name="p7269121916223"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="23.112311231123112%" id="mcps1.2.5.1.3"><p id="p1557841182517"><a name="p1557841182517"></a><a name="p1557841182517"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="45.604560456045604%" id="mcps1.2.5.1.4"><p id="p8578111172512"><a name="p8578111172512"></a><a name="p8578111172512"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972670_row11710498"><td class="cellrowborder" valign="top" width="17.691769176917692%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972670_p9026257"><a name="zh-cn_topic_0057972670_p9026257"></a><a name="zh-cn_topic_0057972670_p9026257"></a>floating_ip</p>
</td>
<td class="cellrowborder" valign="top" width="13.591359135913592%" headers="mcps1.2.5.1.2 "><p id="p4269111962214"><a name="p4269111962214"></a><a name="p4269111962214"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="23.112311231123112%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972670_p60038205"><a name="zh-cn_topic_0057972670_p60038205"></a><a name="zh-cn_topic_0057972670_p60038205"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="45.604560456045604%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972670_p48740201"><a name="zh-cn_topic_0057972670_p48740201"></a><a name="zh-cn_topic_0057972670_p48740201"></a>floating_ip对象，参见<a href="#zh-cn_topic_0057972670_table55642234">表4</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  floating\_ip对象

<a name="zh-cn_topic_0057972670_table55642234"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972670_row53704644"><th class="cellrowborder" valign="top" width="17.948205179482056%" id="mcps1.2.5.1.1"><p id="p1385210153257"><a name="p1385210153257"></a><a name="p1385210153257"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.538646135386465%" id="mcps1.2.5.1.2"><p id="p1192152214222"><a name="p1192152214222"></a><a name="p1192152214222"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="23.237676232376767%" id="mcps1.2.5.1.3"><p id="p8852171516252"><a name="p8852171516252"></a><a name="p8852171516252"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="45.275472452754734%" id="mcps1.2.5.1.4"><p id="p485291517253"><a name="p485291517253"></a><a name="p485291517253"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972670_row19737894"><td class="cellrowborder" valign="top" width="17.948205179482056%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972670_p55265559"><a name="zh-cn_topic_0057972670_p55265559"></a><a name="zh-cn_topic_0057972670_p55265559"></a>fixed_ip</p>
</td>
<td class="cellrowborder" valign="top" width="13.538646135386465%" headers="mcps1.2.5.1.2 "><p id="p019232262212"><a name="p019232262212"></a><a name="p019232262212"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="23.237676232376767%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972670_p47325326"><a name="zh-cn_topic_0057972670_p47325326"></a><a name="zh-cn_topic_0057972670_p47325326"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.275472452754734%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972670_p55859239"><a name="zh-cn_topic_0057972670_p55859239"></a><a name="zh-cn_topic_0057972670_p55859239"></a>私有IP地址</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972670_row32971110"><td class="cellrowborder" valign="top" width="17.948205179482056%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972670_p53414263"><a name="zh-cn_topic_0057972670_p53414263"></a><a name="zh-cn_topic_0057972670_p53414263"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="13.538646135386465%" headers="mcps1.2.5.1.2 "><p id="p10192172215221"><a name="p10192172215221"></a><a name="p10192172215221"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="23.237676232376767%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972670_p31588048"><a name="zh-cn_topic_0057972670_p31588048"></a><a name="zh-cn_topic_0057972670_p31588048"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.275472452754734%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972670_p17016957"><a name="zh-cn_topic_0057972670_p17016957"></a><a name="zh-cn_topic_0057972670_p17016957"></a>浮动IP的ID，UUID格式</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972670_row18934887"><td class="cellrowborder" valign="top" width="17.948205179482056%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972670_p57330849"><a name="zh-cn_topic_0057972670_p57330849"></a><a name="zh-cn_topic_0057972670_p57330849"></a>instance_id</p>
</td>
<td class="cellrowborder" valign="top" width="13.538646135386465%" headers="mcps1.2.5.1.2 "><p id="p131921922152211"><a name="p131921922152211"></a><a name="p131921922152211"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="23.237676232376767%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972670_p13287175"><a name="zh-cn_topic_0057972670_p13287175"></a><a name="zh-cn_topic_0057972670_p13287175"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.275472452754734%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972670_p2747002"><a name="zh-cn_topic_0057972670_p2747002"></a><a name="zh-cn_topic_0057972670_p2747002"></a>被绑定主机的ID，UUID格式</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972670_row24723024"><td class="cellrowborder" valign="top" width="17.948205179482056%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972670_p56407950"><a name="zh-cn_topic_0057972670_p56407950"></a><a name="zh-cn_topic_0057972670_p56407950"></a>ip</p>
</td>
<td class="cellrowborder" valign="top" width="13.538646135386465%" headers="mcps1.2.5.1.2 "><p id="p7192152219224"><a name="p7192152219224"></a><a name="p7192152219224"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="23.237676232376767%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972670_p5641212"><a name="zh-cn_topic_0057972670_p5641212"></a><a name="zh-cn_topic_0057972670_p5641212"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.275472452754734%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972670_p35008393"><a name="zh-cn_topic_0057972670_p35008393"></a><a name="zh-cn_topic_0057972670_p35008393"></a>浮动IP的ip地址</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972670_row46640084"><td class="cellrowborder" valign="top" width="17.948205179482056%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972670_p19750463"><a name="zh-cn_topic_0057972670_p19750463"></a><a name="zh-cn_topic_0057972670_p19750463"></a>pool</p>
</td>
<td class="cellrowborder" valign="top" width="13.538646135386465%" headers="mcps1.2.5.1.2 "><p id="p81922022112215"><a name="p81922022112215"></a><a name="p81922022112215"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="23.237676232376767%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972670_p56283646"><a name="zh-cn_topic_0057972670_p56283646"></a><a name="zh-cn_topic_0057972670_p56283646"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.275472452754734%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972670_p44033946"><a name="zh-cn_topic_0057972670_p44033946"></a><a name="zh-cn_topic_0057972670_p44033946"></a>网络资源池名称，用于分配浮动IP</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0057972670_section61559149"></a>

```
POST https://{endpoint}/v2.1/e73621affb8f44e1bc01898747ca09d4/os-floating-ips
```

```
{
    "pool": "external"
}
```

## 响应示例<a name="section668881316481"></a>

```
{
  "floating_ip": {
    "id": "7aa2aa63-3097-4cfe-a2e4-596c301d3b1b",
    "pool": "external",
    "ip": "10.154.53.184",
    "fixed_ip": null,
    "instance_id": null
  }
}
```

## 返回值<a name="zh-cn_topic_0057972670_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

