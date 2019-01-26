# 查询浮动IP（废弃，不推荐使用）<a name="ZH-CN_TOPIC_0065820818"></a>

## 功能介绍<a name="zh-cn_topic_0057972673_section10293088"></a>

根据浮动IP的ID查询浮动IP详情。

## 接口约束<a name="zh-cn_topic_0057972673_section28433766"></a>

-   该API准备废弃，建议直接使用对应的网络服务接口["查询浮动IP"](https://support.huaweicloud.com/api-vpc/zh-cn_topic_0060333021.html)。

## URI<a name="zh-cn_topic_0057972673_section25528928"></a>

GET /v2/\{project\_id\}/os-floating-ips/\{floating\_ip\_id\}

GET /v2.1/\{project\_id\}/os-floating-ips/\{floating\_ip\_id\}

参数说明请参见[表1](#zh-cn_topic_0057972673_table32475667)。

**表 1**  参数说明

<a name="zh-cn_topic_0057972673_table32475667"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972673_row44937496"><th class="cellrowborder" valign="top" width="22.24%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21.87%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.88999999999999%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972673_row1664874"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972673_p637140"><a name="zh-cn_topic_0057972673_p637140"></a><a name="zh-cn_topic_0057972673_p637140"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972673_p51608407"><a name="zh-cn_topic_0057972673_p51608407"></a><a name="zh-cn_topic_0057972673_p51608407"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972673_row102094505165"><td class="cellrowborder" valign="top" width="22.24%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972673_p620919503165"><a name="zh-cn_topic_0057972673_p620919503165"></a><a name="zh-cn_topic_0057972673_p620919503165"></a>floating_ip_id</p>
</td>
<td class="cellrowborder" valign="top" width="21.87%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972673_p32091350111612"><a name="zh-cn_topic_0057972673_p32091350111612"></a><a name="zh-cn_topic_0057972673_p32091350111612"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="55.88999999999999%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972673_p2209205020164"><a name="zh-cn_topic_0057972673_p2209205020164"></a><a name="zh-cn_topic_0057972673_p2209205020164"></a>浮动IP的ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0057972673_section54577306"></a>

**请求参数**

请求参数如[表2](#zh-cn_topic_0057972673_table54995351)所示。

**表 2**  请求参数

<a name="zh-cn_topic_0057972673_table54995351"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972673_row16221316"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0057972670_p57733603"><a name="zh-cn_topic_0057972670_p57733603"></a><a name="zh-cn_topic_0057972670_p57733603"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0057972670_p45910260"><a name="zh-cn_topic_0057972670_p45910260"></a><a name="zh-cn_topic_0057972670_p45910260"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="16.54%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0057972670_p27743545"><a name="zh-cn_topic_0057972670_p27743545"></a><a name="zh-cn_topic_0057972670_p27743545"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.46%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0057972670_p32634650"><a name="zh-cn_topic_0057972670_p32634650"></a><a name="zh-cn_topic_0057972670_p32634650"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972673_row62034116"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972673_p58707504"><a name="zh-cn_topic_0057972673_p58707504"></a><a name="zh-cn_topic_0057972673_p58707504"></a>tenant_id</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972673_p57687380"><a name="zh-cn_topic_0057972673_p57687380"></a><a name="zh-cn_topic_0057972673_p57687380"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="16.54%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972673_p42166233"><a name="zh-cn_topic_0057972673_p42166233"></a><a name="zh-cn_topic_0057972673_p42166233"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.46%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972673_p60021735"><a name="zh-cn_topic_0057972673_p60021735"></a><a name="zh-cn_topic_0057972673_p60021735"></a>租户ID，在URI中指定。</p>
<p id="p10217519037"><a name="p10217519037"></a><a name="p10217519037"></a>UUID格式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972673_row3324704"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972673_p865613"><a name="zh-cn_topic_0057972673_p865613"></a><a name="zh-cn_topic_0057972673_p865613"></a>floating_ip_id</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972673_p3005847"><a name="zh-cn_topic_0057972673_p3005847"></a><a name="zh-cn_topic_0057972673_p3005847"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="16.54%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972673_p42147045"><a name="zh-cn_topic_0057972673_p42147045"></a><a name="zh-cn_topic_0057972673_p42147045"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.46%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972673_p58467488"><a name="zh-cn_topic_0057972673_p58467488"></a><a name="zh-cn_topic_0057972673_p58467488"></a>浮动IP的ID，在URI中指定。</p>
<p id="p13147112412315"><a name="p13147112412315"></a><a name="p13147112412315"></a>UUID格式。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0057972673_section21433709"></a>

**响应参数**

响应参数如[表3](#zh-cn_topic_0057972673_table38246063)所示。

**表 3**  响应参数

<a name="zh-cn_topic_0057972673_table38246063"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972673_row31787174"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p1810134211253"><a name="p1810134211253"></a><a name="p1810134211253"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p88251842102518"><a name="p88251842102518"></a><a name="p88251842102518"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="16.73%" id="mcps1.2.5.1.3"><p id="p6825114216253"><a name="p6825114216253"></a><a name="p6825114216253"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.269999999999996%" id="mcps1.2.5.1.4"><p id="p16825942112519"><a name="p16825942112519"></a><a name="p16825942112519"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972673_row12502218"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972673_p6046746"><a name="zh-cn_topic_0057972673_p6046746"></a><a name="zh-cn_topic_0057972673_p6046746"></a>floating_ip</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972673_p20024398"><a name="zh-cn_topic_0057972673_p20024398"></a><a name="zh-cn_topic_0057972673_p20024398"></a>Dict</p>
</td>
<td class="cellrowborder" valign="top" width="16.73%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972673_p11363535"><a name="zh-cn_topic_0057972673_p11363535"></a><a name="zh-cn_topic_0057972673_p11363535"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.269999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972673_p48031108"><a name="zh-cn_topic_0057972673_p48031108"></a><a name="zh-cn_topic_0057972673_p48031108"></a>floating_ip对象，参见<a href="#zh-cn_topic_0057972673_table65314517">表4</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  floating\_ip对象表

<a name="zh-cn_topic_0057972673_table65314517"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972673_row49408564"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p83352466258"><a name="p83352466258"></a><a name="p83352466258"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p103351946192513"><a name="p103351946192513"></a><a name="p103351946192513"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="16.73%" id="mcps1.2.5.1.3"><p id="p633574622516"><a name="p633574622516"></a><a name="p633574622516"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.269999999999996%" id="mcps1.2.5.1.4"><p id="p15335144615253"><a name="p15335144615253"></a><a name="p15335144615253"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972673_row23930149"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972673_p59293887"><a name="zh-cn_topic_0057972673_p59293887"></a><a name="zh-cn_topic_0057972673_p59293887"></a>fixed_ip</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972673_p38075525"><a name="zh-cn_topic_0057972673_p38075525"></a><a name="zh-cn_topic_0057972673_p38075525"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="16.73%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972673_p64218721"><a name="zh-cn_topic_0057972673_p64218721"></a><a name="zh-cn_topic_0057972673_p64218721"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.269999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972673_p34333880"><a name="zh-cn_topic_0057972673_p34333880"></a><a name="zh-cn_topic_0057972673_p34333880"></a>私有IP地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972673_row40569470"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972673_p64901660"><a name="zh-cn_topic_0057972673_p64901660"></a><a name="zh-cn_topic_0057972673_p64901660"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972673_p22543082"><a name="zh-cn_topic_0057972673_p22543082"></a><a name="zh-cn_topic_0057972673_p22543082"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="16.73%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972673_p14050320"><a name="zh-cn_topic_0057972673_p14050320"></a><a name="zh-cn_topic_0057972673_p14050320"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.269999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972673_p64334135"><a name="zh-cn_topic_0057972673_p64334135"></a><a name="zh-cn_topic_0057972673_p64334135"></a>浮动IP的ID，UUID格式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972673_row42136306"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972673_p57597629"><a name="zh-cn_topic_0057972673_p57597629"></a><a name="zh-cn_topic_0057972673_p57597629"></a>instance_id</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972673_p34896348"><a name="zh-cn_topic_0057972673_p34896348"></a><a name="zh-cn_topic_0057972673_p34896348"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="16.73%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972673_p8031928"><a name="zh-cn_topic_0057972673_p8031928"></a><a name="zh-cn_topic_0057972673_p8031928"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.269999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972673_p46606392"><a name="zh-cn_topic_0057972673_p46606392"></a><a name="zh-cn_topic_0057972673_p46606392"></a>被绑定主机的ID，UUID格式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972673_row16804345"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972673_p18974699"><a name="zh-cn_topic_0057972673_p18974699"></a><a name="zh-cn_topic_0057972673_p18974699"></a>ip</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972673_p60555637"><a name="zh-cn_topic_0057972673_p60555637"></a><a name="zh-cn_topic_0057972673_p60555637"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="16.73%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972673_p6059584"><a name="zh-cn_topic_0057972673_p6059584"></a><a name="zh-cn_topic_0057972673_p6059584"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.269999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972673_p21064308"><a name="zh-cn_topic_0057972673_p21064308"></a><a name="zh-cn_topic_0057972673_p21064308"></a>浮动IP的IP地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972673_row55361044"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972673_p55059575"><a name="zh-cn_topic_0057972673_p55059575"></a><a name="zh-cn_topic_0057972673_p55059575"></a>pool</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972673_p30640599"><a name="zh-cn_topic_0057972673_p30640599"></a><a name="zh-cn_topic_0057972673_p30640599"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="16.73%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972673_p65969435"><a name="zh-cn_topic_0057972673_p65969435"></a><a name="zh-cn_topic_0057972673_p65969435"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.269999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972673_p41924012"><a name="zh-cn_topic_0057972673_p41924012"></a><a name="zh-cn_topic_0057972673_p41924012"></a>网络资源池名称，用于分配浮动IP地址。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="zh-cn_topic_0057972673_section58685656"></a>

-   请求示例

    ```
    GET /v2/e73621affb8f44e1bc01898747ca09d4/os-floating-ips/05f71f43-f3c9-47ef-ac8d-9f02aef66418
    GET /v2.1/e73621affb8f44e1bc01898747ca09d4/os-floating-ips/05f71f43-f3c9-47ef-ac8d-9f02aef66418
    ```

-   响应示例

    ```
    {
      "floating_ip":{
          "id": "05f71f43-f3c9-47ef-ac8d-9f02aef66418",
          "pool": "external",
          "ip": "10.154.51.235",
          "fixed_ip": "192.168.1.2",
          "instance_id": "8b380f68-5057-4aa2-a33a-170b37218fa8"
        }
    }
    ```


## 返回值<a name="zh-cn_topic_0057972673_zh-cn_topic_0020212692_section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

