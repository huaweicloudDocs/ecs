# 查询云服务器规格extra\_specs的详情<a name="ZH-CN_TOPIC_0065817706"></a>

## 功能介绍<a name="zh-cn_topic_0057973064_section33891944"></a>

查询指定的规格的详细信息。

## URI<a name="zh-cn_topic_0057973064_section36592045"></a>

GET /v2/\{project\_id\}/flavors/\{flavors\_id\}/os-extra\_specs

GET /v2.1/\{project\_id\}/flavors/\{flavors\_id\}/os-extra\_specs

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

不涉及

## 响应消息<a name="zh-cn_topic_0057973064_section32002165"></a>

**响应参数**

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
<td class="cellrowborder" valign="top" width="22.830000000000002%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973064_p42695066"><a name="zh-cn_topic_0057973064_p42695066"></a><a name="zh-cn_topic_0057973064_p42695066"></a>Dict</p>
</td>
<td class="cellrowborder" valign="top" width="48.26%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973064_p9931138"><a name="zh-cn_topic_0057973064_p9931138"></a><a name="zh-cn_topic_0057973064_p9931138"></a>描述弹性云服务器规格的键值对。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  os\_extra\_specs数据结构说明

<a name="table59078165"></a>
<table><thead align="left"><tr id="row48163256"><th class="cellrowborder" valign="top" width="24.12%" id="mcps1.2.4.1.1"><p id="p1840210342212"><a name="p1840210342212"></a><a name="p1840210342212"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12.76%" id="mcps1.2.4.1.2"><p id="p24022343215"><a name="p24022343215"></a><a name="p24022343215"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="63.12%" id="mcps1.2.4.1.3"><p id="p134021734323"><a name="p134021734323"></a><a name="p134021734323"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row169423685915"><td class="cellrowborder" valign="top" width="24.12%" headers="mcps1.2.4.1.1 "><p id="p395203616590"><a name="p395203616590"></a><a name="p395203616590"></a>cond:operation:status</p>
</td>
<td class="cellrowborder" valign="top" width="12.76%" headers="mcps1.2.4.1.2 "><p id="p29512361595"><a name="p29512361595"></a><a name="p29512361595"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63.12%" headers="mcps1.2.4.1.3 "><p id="p108052518111"><a name="p108052518111"></a><a name="p108052518111"></a>此参数是Region级配置，某个AZ没有在cond:operation:az参数中配置时默认使用此参数的取值。不配置或无此参数时等同于<span class="parmvalue" id="parmvalue1182675317816"><a name="parmvalue1182675317816"></a><a name="parmvalue1182675317816"></a>“normal”</span>。取值范围：</p>
<a name="ul14280914915"></a><a name="ul14280914915"></a><ul id="ul14280914915"><li>normal：正常商用</li><li>abandon：下线（即不显示）</li><li>sellout：售罄</li><li>obt：公测</li><li>promotion：推荐(等同normal，也是商用)</li></ul>
</td>
</tr>
<tr id="row1347820527114"><td class="cellrowborder" valign="top" width="24.12%" headers="mcps1.2.4.1.1 "><p id="p54798521311"><a name="p54798521311"></a><a name="p54798521311"></a>cond:operation:az</p>
</td>
<td class="cellrowborder" valign="top" width="12.76%" headers="mcps1.2.4.1.2 "><p id="p12479205214119"><a name="p12479205214119"></a><a name="p12479205214119"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63.12%" headers="mcps1.2.4.1.3 "><p id="p118175714108"><a name="p118175714108"></a><a name="p118175714108"></a>此参数是AZ级配置，某个AZ没有在此参数中配置时默认使用cond:operation:status参数的取值。此参数的配置格式<span class="parmvalue" id="parmvalue35503781214"><a name="parmvalue35503781214"></a><a name="parmvalue35503781214"></a>“az(xx)”</span>。()内为某个AZ的flavor状态，()内必须要填有状态，不填为无效配置。状态的取值范围与cond:operation:az参数相同。</p>
<p id="p994816551996"><a name="p994816551996"></a><a name="p994816551996"></a>例如：flavor在某个region的az0售罄，az1不显示，其他az正常显示，可配置为：</p>
<a name="ul18538152311016"></a><a name="ul18538152311016"></a><ul id="ul18538152311016"><li><span class="parmname" id="parmname185211228121019"><a name="parmname185211228121019"></a><a name="parmname185211228121019"></a>“cond:operation:status”</span>设置为<span class="parmvalue" id="parmvalue1259753121017"><a name="parmvalue1259753121017"></a><a name="parmvalue1259753121017"></a>“normal”</span></li><li><span class="parmname" id="parmname1091653419106"><a name="parmname1091653419106"></a><a name="parmname1091653419106"></a>“cond:operation:az”</span>设置为<span class="parmvalue" id="parmvalue14516104011015"><a name="parmvalue14516104011015"></a><a name="parmvalue14516104011015"></a>“az0(sellout), az1(abandon)”</span></li></ul>
<div class="note" id="note16390259827"><a name="note16390259827"></a><a name="note16390259827"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p33931591628"><a name="p33931591628"></a><a name="p33931591628"></a>如果flavor在某个AZ下的状态与cond:operation:status配置状态不同，必须配置该参数。</p>
</div></div>
</td>
</tr>
<tr id="row182067539163"><td class="cellrowborder" valign="top" width="24.12%" headers="mcps1.2.4.1.1 "><p id="p1597119116171"><a name="p1597119116171"></a><a name="p1597119116171"></a>cond:operation:roles</p>
</td>
<td class="cellrowborder" valign="top" width="12.76%" headers="mcps1.2.4.1.2 "><p id="p109711411121715"><a name="p109711411121715"></a><a name="p109711411121715"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="63.12%" headers="mcps1.2.4.1.3 "><p id="p11971111116171"><a name="p11971111116171"></a><a name="p11971111116171"></a>此参数用来配置flavor的公测标签，如果某个region下有公测AZ，必须配置该属性。</p>
<p id="p5971111171712"><a name="p5971111171712"></a><a name="p5971111171712"></a>例如：flavor仅在az1开始公测，其他az不可见，可配置为：</p>
<a name="ul16771174711176"></a><a name="ul16771174711176"></a><ul id="ul16771174711176"><li><span class="parmname" id="parmname8360125316177"><a name="parmname8360125316177"></a><a name="parmname8360125316177"></a>“cond:operation:status”</span>配置为<span class="parmvalue" id="parmvalue365619131818"><a name="parmvalue365619131818"></a><a name="parmvalue365619131818"></a>“abandon”</span></li><li><span class="parmname" id="parmname1950555161716"><a name="parmname1950555161716"></a><a name="parmname1950555161716"></a>“cond:operation:az”</span>配置为<span class="parmvalue" id="parmvalue128791949184"><a name="parmvalue128791949184"></a><a name="parmvalue128791949184"></a>“az1(obt)”</span></li><li><span class="parmname" id="parmname196331858191719"><a name="parmname196331858191719"></a><a name="parmname196331858191719"></a>“cond:operation:roles”</span>配置为<span class="parmvalue" id="parmvalue099158171816"><a name="parmvalue099158171816"></a><a name="parmvalue099158171816"></a>“op_gated_ecs_c3ne”</span></li></ul>
</td>
</tr>
</tbody>
</table>

## 示例<a name="zh-cn_topic_0057973064_section19584029"></a>

-   请求示例

    ```
    GET v2/775ad4f543e247938551b93417b27f0b/flavors/c2.medium/os-extra_specs
    GET v2.1/775ad4f543e247938551b93417b27f0b/flavors/c2.medium/os-extra_specs
    ```

-   响应示例

    ```
    {
        "extra_specs": {
            "key1": "value1",
            "key2": "value2"
        }
    }
    ```


## 返回值<a name="zh-cn_topic_0057973064_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

