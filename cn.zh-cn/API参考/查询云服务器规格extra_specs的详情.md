# 查询云服务器规格extra\_specs的详情<a name="ZH-CN_TOPIC_0065817706"></a>

## 功能介绍<a name="zh-cn_topic_0057973064_section33891944"></a>

查询指定的规格的详细信息。

## URI<a name="zh-cn_topic_0057973064_section36592045"></a>

GET /v2.1/\{project\_id\}/flavors/\{flavor\_id\}/os-extra\_specs

参数说明请参见[表1](#zh-cn_topic_0057973064_table47154420)。

**表 1**  参数说明

<a name="zh-cn_topic_0057973064_table47154420"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973064_row324668"><th class="cellrowborder" valign="top" width="30.7%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.5%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="44.800000000000004%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973064_row17004965"><td class="cellrowborder" valign="top" width="30.7%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973064_p35224963"><a name="zh-cn_topic_0057973064_p35224963"></a><a name="zh-cn_topic_0057973064_p35224963"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.5%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973064_p34649765"><a name="zh-cn_topic_0057973064_p34649765"></a><a name="zh-cn_topic_0057973064_p34649765"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="44.800000000000004%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973064_row26746391"><td class="cellrowborder" valign="top" width="30.7%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973064_p18974100"><a name="zh-cn_topic_0057973064_p18974100"></a><a name="zh-cn_topic_0057973064_p18974100"></a>flavors_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.5%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973064_p60507121"><a name="zh-cn_topic_0057973064_p60507121"></a><a name="zh-cn_topic_0057973064_p60507121"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="44.800000000000004%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973064_p2129750"><a name="zh-cn_topic_0057973064_p2129750"></a><a name="zh-cn_topic_0057973064_p2129750"></a>规格ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057973064_section33381957"></a>

无

## 响应消息<a name="zh-cn_topic_0057973064_section32002165"></a>

响应参数如[表2](#zh-cn_topic_0057973064_table28168569)所示。

**表 2**  响应参数

<a name="zh-cn_topic_0057973064_table28168569"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973064_row26406300"><th class="cellrowborder" valign="top" width="28.910000000000004%" id="mcps1.2.4.1.1"><p id="p110452114597"><a name="p110452114597"></a><a name="p110452114597"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.830000000000002%" id="mcps1.2.4.1.2"><p id="p71044217595"><a name="p71044217595"></a><a name="p71044217595"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.26%" id="mcps1.2.4.1.3"><p id="p15104102175910"><a name="p15104102175910"></a><a name="p15104102175910"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973064_row46433444"><td class="cellrowborder" valign="top" width="28.910000000000004%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973064_p3012613"><a name="zh-cn_topic_0057973064_p3012613"></a><a name="zh-cn_topic_0057973064_p3012613"></a>extra_specs</p>
</td>
<td class="cellrowborder" valign="top" width="22.830000000000002%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973064_p42695066"><a name="zh-cn_topic_0057973064_p42695066"></a><a name="zh-cn_topic_0057973064_p42695066"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48.26%" headers="mcps1.2.4.1.3 "><p id="p1679511281174"><a name="p1679511281174"></a><a name="p1679511281174"></a>描述<span id="text27145231511"><a name="text27145231511"></a><a name="text27145231511"></a>弹性云服务器</span>规格的键值对。</p>
<p id="p194000157416"><a name="p194000157416"></a><a name="p194000157416"></a>返回字段详细说明请参见<a href="查询规格详情和规格扩展信息列表.md#table59078165">表6</a>章节os_extra_specs数据结构说明。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0057973064_section19584029"></a>

```
GET https://{endpoint}/v2.1/743b4c0428d94531b9f2add666642e6b/flavors/c3.2xlarge.2/os-extra_specs
```

## 响应示例<a name="section1679819123313"></a>

```
{
    "extra_specs": {
        "ecs:performancetype": "computingv3",
        "resource_type": "IOoptimizedC3_2"
    }
}
```

## 返回值<a name="zh-cn_topic_0057973064_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

