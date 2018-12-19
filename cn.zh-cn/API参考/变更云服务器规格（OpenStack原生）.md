# 变更云服务器规格<a name="ZH-CN_TOPIC_0028714261"></a>

## 功能介绍<a name="section5763990416457"></a>

变更单台云服务器规格。

对于运行中的弹性云服务器，系统会自动关机，并将弹性云服务器中的数据拷贝到目标节点（目标节点可与源节点相同）后重新启动弹性云服务器。

该接口不单独使用，需配合“确认变更云服务器规格（POST /v2/\{project\_id\}/servers/\{server\_id\}/action）”或“回退变更云服务器规格（POST /v2/\{project\_id\}/servers/\{server\_id\}/action）”两个接口一起使用。

## URI<a name="section934152916457"></a>

POST /v2/\{project\_id\}/servers/\{server\_id\}/action

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/action

参数说明请参见[表1](#table3588765216457)。

**表 1**  参数说明

<a name="table3588765216457"></a>
<table><thead align="left"><tr id="row3213599316457"><th class="cellrowborder" valign="top" width="20.549999999999997%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.86%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.589999999999996%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5283576216457"><td class="cellrowborder" valign="top" width="20.549999999999997%" headers="mcps1.2.4.1.1 "><p id="p5183832116457"><a name="p5183832116457"></a><a name="p5183832116457"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.86%" headers="mcps1.2.4.1.2 "><p id="p3815449716457"><a name="p3815449716457"></a><a name="p3815449716457"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="60.589999999999996%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row3155913116457"><td class="cellrowborder" valign="top" width="20.549999999999997%" headers="mcps1.2.4.1.1 "><p id="p615277916457"><a name="p615277916457"></a><a name="p615277916457"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.86%" headers="mcps1.2.4.1.2 "><p id="p2861306316457"><a name="p2861306316457"></a><a name="p2861306316457"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="60.589999999999996%" headers="mcps1.2.4.1.3 "><p id="p3595679216457"><a name="p3595679216457"></a><a name="p3595679216457"></a>云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section5517568016457"></a>

**请求参数**

请求参数如[表2](#table2242889516457)所示。

**表 2**  请求参数

<a name="table2242889516457"></a>
<table><thead align="left"><tr id="row3650219016457"><th class="cellrowborder" valign="top" width="21.557844215578445%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0057973030_p1494644"><a name="zh-cn_topic_0057973030_p1494644"></a><a name="zh-cn_topic_0057973030_p1494644"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.58834116588341%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0057973030_p53957349"><a name="zh-cn_topic_0057973030_p53957349"></a><a name="zh-cn_topic_0057973030_p53957349"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="17.44825517448255%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0057973030_p8469150"><a name="zh-cn_topic_0057973030_p8469150"></a><a name="zh-cn_topic_0057973030_p8469150"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="44.40555944405559%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0057973030_p14912584"><a name="zh-cn_topic_0057973030_p14912584"></a><a name="zh-cn_topic_0057973030_p14912584"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1418337416457"><td class="cellrowborder" valign="top" width="21.557844215578445%" headers="mcps1.2.5.1.1 "><p id="p800266116457"><a name="p800266116457"></a><a name="p800266116457"></a>flavorRef</p>
</td>
<td class="cellrowborder" valign="top" width="16.58834116588341%" headers="mcps1.2.5.1.2 "><p id="p4423583316457"><a name="p4423583316457"></a><a name="p4423583316457"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.44825517448255%" headers="mcps1.2.5.1.3 "><p id="p2633272116457"><a name="p2633272116457"></a><a name="p2633272116457"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.40555944405559%" headers="mcps1.2.5.1.4 "><p id="p341898416457"><a name="p341898416457"></a><a name="p341898416457"></a>新规格ID或URI。</p>
</td>
</tr>
<tr id="row6013179512935"><td class="cellrowborder" valign="top" width="21.557844215578445%" headers="mcps1.2.5.1.1 "><p id="p2840141712945"><a name="p2840141712945"></a><a name="p2840141712945"></a>dedicated_host_id</p>
</td>
<td class="cellrowborder" valign="top" width="16.58834116588341%" headers="mcps1.2.5.1.2 "><p id="p5880503012935"><a name="p5880503012935"></a><a name="p5880503012935"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.44825517448255%" headers="mcps1.2.5.1.3 "><p id="p6558702312935"><a name="p6558702312935"></a><a name="p6558702312935"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.40555944405559%" headers="mcps1.2.5.1.4 "><p id="p1094865212935"><a name="p1094865212935"></a><a name="p1094865212935"></a>新专属主机ID（仅适用于专属主机上的弹性云服务器）。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section1759889416457"></a>

不涉及

## 示例<a name="section1264820314241"></a>

-   请求样例

    ```
    {
        "resize" : {
            "flavorRef" : "4",
            "dedicated_host_id": "459a2b9d-804a-4745-ab19-a113bb1b4ddc"
        }
    }
    ```


## 返回值<a name="section1180080516457"></a>

请参考[通用请求返回值](通用请求返回值.md)。

