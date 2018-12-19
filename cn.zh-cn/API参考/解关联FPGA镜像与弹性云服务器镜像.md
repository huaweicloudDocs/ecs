# 解关联FPGA镜像与弹性云服务器镜像<a name="ZH-CN_TOPIC_0081950549"></a>

## 功能介绍<a name="section43795230211632"></a>

本接口用于删除FPGA镜像与弹性云服务器镜像之间的关联映射关系。

## URI<a name="section28033540211632"></a>

DELETE /v1/\{project\_id\}/cloudservers/fpga\_image/\{fpga\_image\_id\}/association

参数说明请参见[表1](#table28107133211632)。

**表 1**  参数说明

<a name="table28107133211632"></a>
<table><thead align="left"><tr id="row19177941211632"><th class="cellrowborder" valign="top" width="30.490000000000002%" id="mcps1.2.4.1.1"><p id="p7707213"><a name="p7707213"></a><a name="p7707213"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.73%" id="mcps1.2.4.1.2"><p id="p20304554"><a name="p20304554"></a><a name="p20304554"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="48.78%" id="mcps1.2.4.1.3"><p id="p34056167"><a name="p34056167"></a><a name="p34056167"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row33377558211632"><td class="cellrowborder" valign="top" width="30.490000000000002%" headers="mcps1.2.4.1.1 "><p id="p53863828211632"><a name="p53863828211632"></a><a name="p53863828211632"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20.73%" headers="mcps1.2.4.1.2 "><p id="p47645557211632"><a name="p47645557211632"></a><a name="p47645557211632"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48.78%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row176964211632"><td class="cellrowborder" valign="top" width="30.490000000000002%" headers="mcps1.2.4.1.1 "><p id="p48913232211632"><a name="p48913232211632"></a><a name="p48913232211632"></a>fpga_image_id</p>
</td>
<td class="cellrowborder" valign="top" width="20.73%" headers="mcps1.2.4.1.2 "><p id="p66905560211632"><a name="p66905560211632"></a><a name="p66905560211632"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48.78%" headers="mcps1.2.4.1.3 "><p id="p5594788211632"><a name="p5594788211632"></a><a name="p5594788211632"></a>FPGA镜像ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section3313651211632"></a>

**请求参数**

请求参数如[表2](#table39016918211632)所示。

**表 2**  请求参数

<a name="table39016918211632"></a>
<table><thead align="left"><tr id="row31417811211632"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p13501148211632"><a name="p13501148211632"></a><a name="p13501148211632"></a>参数名称</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p32752343211632"><a name="p32752343211632"></a><a name="p32752343211632"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="16.73%" id="mcps1.2.5.1.3"><p id="p47957996211632"><a name="p47957996211632"></a><a name="p47957996211632"></a>必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.269999999999996%" id="mcps1.2.5.1.4"><p id="p51666370211632"><a name="p51666370211632"></a><a name="p51666370211632"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row22126978211632"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p24226259211632"><a name="p24226259211632"></a><a name="p24226259211632"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p42610398211632"><a name="p42610398211632"></a><a name="p42610398211632"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="16.73%" headers="mcps1.2.5.1.3 "><p id="p27767370211632"><a name="p27767370211632"></a><a name="p27767370211632"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.269999999999996%" headers="mcps1.2.5.1.4 "><p id="p57026368211632"><a name="p57026368211632"></a><a name="p57026368211632"></a>ECS镜像ID。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section727655211632"></a>

无

## 示例<a name="section47627159211632"></a>

-   请求示例

    ```
    {
      "image": {
        "id": "18efee75-e058-4c52-a49c-9e3ba4d1c8de"
      }
    }
    ```

-   响应示例

    无


## 返回值<a name="section3477250491225"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码说明](错误码说明.md)。

