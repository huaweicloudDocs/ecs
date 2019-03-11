# 查询浮动IP资源池列表（废弃，不推荐使用）<a name="ZH-CN_TOPIC_0065820820"></a>

## 功能介绍<a name="zh-cn_topic_0057972835_section7554882"></a>

查询浮动IP资源池列表。

## 接口约束<a name="zh-cn_topic_0057972835_section7965739"></a>

-   该API准备废弃，建议直接使用对应的网络服务接口["查询网络"](https://support.huaweicloud.com/api-vpc/zh-cn_topic_0060495801.html)。

接口参数为：router:external=True

```
GET /networks?router:external=True 返回结果中的name字段
```

## URI<a name="zh-cn_topic_0057972835_section885082"></a>

GET /v2/\{project\_id\}/os-floating-ip-pools

GET /v2.1/\{project\_id\}/os-floating-ip-pools

参数说明请参见[表1](#zh-cn_topic_0057972835_table32475667)。

**表 1**  参数说明

<a name="zh-cn_topic_0057972835_table32475667"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972835_row44937496"><th class="cellrowborder" valign="top" width="22.24%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.87%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.88999999999999%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972835_row1664874"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972835_p637140"><a name="zh-cn_topic_0057972835_p637140"></a><a name="zh-cn_topic_0057972835_p637140"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972835_p51608407"><a name="zh-cn_topic_0057972835_p51608407"></a><a name="zh-cn_topic_0057972835_p51608407"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057972835_section4582792"></a>

**请求参数**

请求参数如[表2](#zh-cn_topic_0057972835_table51488960)所示。

**表 2**  请求参数

<a name="zh-cn_topic_0057972835_table51488960"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972835_row34407239"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0057972670_p57733603"><a name="zh-cn_topic_0057972670_p57733603"></a><a name="zh-cn_topic_0057972670_p57733603"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0057972670_p45910260"><a name="zh-cn_topic_0057972670_p45910260"></a><a name="zh-cn_topic_0057972670_p45910260"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="16.73%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0057972670_p27743545"><a name="zh-cn_topic_0057972670_p27743545"></a><a name="zh-cn_topic_0057972670_p27743545"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.269999999999996%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0057972670_p32634650"><a name="zh-cn_topic_0057972670_p32634650"></a><a name="zh-cn_topic_0057972670_p32634650"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972835_row51383952"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972835_p1350554"><a name="zh-cn_topic_0057972835_p1350554"></a><a name="zh-cn_topic_0057972835_p1350554"></a>tenant_id</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972835_p42286032"><a name="zh-cn_topic_0057972835_p42286032"></a><a name="zh-cn_topic_0057972835_p42286032"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="16.73%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972835_p2616604"><a name="zh-cn_topic_0057972835_p2616604"></a><a name="zh-cn_topic_0057972835_p2616604"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.269999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972835_p10618339"><a name="zh-cn_topic_0057972835_p10618339"></a><a name="zh-cn_topic_0057972835_p10618339"></a>租户ID，在URI中指定。</p>
<p id="p4231132048"><a name="p4231132048"></a><a name="p4231132048"></a>UUID格式。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0057972835_section41245128"></a>

**响应参数**

响应参数如[表3](#zh-cn_topic_0057972835_table54779151)所示。

**表 3**  响应参数

<a name="zh-cn_topic_0057972835_table54779151"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972835_row21723514"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p2181159142617"><a name="p2181159142617"></a><a name="p2181159142617"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p1418119982619"><a name="p1418119982619"></a><a name="p1418119982619"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="16.919999999999998%" id="mcps1.2.5.1.3"><p id="p018139112615"><a name="p018139112615"></a><a name="p018139112615"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.08%" id="mcps1.2.5.1.4"><p id="p1218116952619"><a name="p1218116952619"></a><a name="p1218116952619"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972835_row56262227"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972835_p60946511"><a name="zh-cn_topic_0057972835_p60946511"></a><a name="zh-cn_topic_0057972835_p60946511"></a>floating_ip_pools</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972835_p37720384"><a name="zh-cn_topic_0057972835_p37720384"></a><a name="zh-cn_topic_0057972835_p37720384"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="16.919999999999998%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972835_p35452302"><a name="zh-cn_topic_0057972835_p35452302"></a><a name="zh-cn_topic_0057972835_p35452302"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.08%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972835_p53064224"><a name="zh-cn_topic_0057972835_p53064224"></a><a name="zh-cn_topic_0057972835_p53064224"></a>floating_ip_pools对象。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972835_row7815975"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972835_p29114202"><a name="zh-cn_topic_0057972835_p29114202"></a><a name="zh-cn_topic_0057972835_p29114202"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972835_p9440199"><a name="zh-cn_topic_0057972835_p9440199"></a><a name="zh-cn_topic_0057972835_p9440199"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="16.919999999999998%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972835_p26458644"><a name="zh-cn_topic_0057972835_p26458644"></a><a name="zh-cn_topic_0057972835_p26458644"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.08%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972835_p62775401"><a name="zh-cn_topic_0057972835_p62775401"></a><a name="zh-cn_topic_0057972835_p62775401"></a>floating ip pool的名字。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="zh-cn_topic_0057972835_section35661838"></a>

-   请求示例

    ```
    GET /v2/e73621affb8f44e1bc01898747ca09d4/os-floating-ip-pools
    GET /v2.1/e73621affb8f44e1bc01898747ca09d4/os-floating-ip-pools
    ```

-   响应示例

    ```
    {
        "floating_ip_pools": [
            {
                "name": "pool1"
            },
            {
                "name": "pool2"
            }
        ]
    }
    ```


## 返回值<a name="zh-cn_topic_0057972835_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

