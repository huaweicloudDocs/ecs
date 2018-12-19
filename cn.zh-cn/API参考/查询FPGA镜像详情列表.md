# 查询FPGA镜像详情列表<a name="ZH-CN_TOPIC_0065962600"></a>

## 功能介绍<a name="section48834480211756"></a>

本接口用于查询租户拥有的FPGA镜像详情列表。

## URI<a name="section30048492211756"></a>

GET /v1/\{project\_id\}/cloudservers/fpga\_image/detail\{?fpga\_image\_id,page,size\}

参数说明请参见[表1](#table972014396283)。

**表 1**  参数说明

<a name="table972014396283"></a>
<table><thead align="left"><tr id="row18736639162810"><th class="cellrowborder" valign="top" width="25.630000000000003%" id="mcps1.2.4.1.1"><p id="p1873611398284"><a name="p1873611398284"></a><a name="p1873611398284"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.080000000000002%" id="mcps1.2.4.1.2"><p id="p13736113918287"><a name="p13736113918287"></a><a name="p13736113918287"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="56.290000000000006%" id="mcps1.2.4.1.3"><p id="p1736123982813"><a name="p1736123982813"></a><a name="p1736123982813"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row873613910283"><td class="cellrowborder" valign="top" width="25.630000000000003%" headers="mcps1.2.4.1.1 "><p id="p127363398282"><a name="p127363398282"></a><a name="p127363398282"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.080000000000002%" headers="mcps1.2.4.1.2 "><p id="p1573653913281"><a name="p1573653913281"></a><a name="p1573653913281"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="56.290000000000006%" headers="mcps1.2.4.1.3 "><p id="p573610392287"><a name="p573610392287"></a><a name="p573610392287"></a>项目ID。</p>
<p id="p7736143910281"><a name="p7736143910281"></a><a name="p7736143910281"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row104351048202211"><td class="cellrowborder" valign="top" width="25.630000000000003%" headers="mcps1.2.4.1.1 "><p id="p20435134810224"><a name="p20435134810224"></a><a name="p20435134810224"></a>fpga_image_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.080000000000002%" headers="mcps1.2.4.1.2 "><p id="p114361048162214"><a name="p114361048162214"></a><a name="p114361048162214"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="56.290000000000006%" headers="mcps1.2.4.1.3 "><p id="p134361248182213"><a name="p134361248182213"></a><a name="p134361248182213"></a>FPGA镜像的ID。</p>
</td>
</tr>
<tr id="row1273633912816"><td class="cellrowborder" valign="top" width="25.630000000000003%" headers="mcps1.2.4.1.1 "><p id="p075111399287"><a name="p075111399287"></a><a name="p075111399287"></a>page</p>
</td>
<td class="cellrowborder" valign="top" width="18.080000000000002%" headers="mcps1.2.4.1.2 "><p id="p575113399286"><a name="p575113399286"></a><a name="p575113399286"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="56.290000000000006%" headers="mcps1.2.4.1.3 "><p id="p11751839102813"><a name="p11751839102813"></a><a name="p11751839102813"></a>分页查询的页数。</p>
<p id="p375133982819"><a name="p375133982819"></a><a name="p375133982819"></a>该参数值需满足如下要求：</p>
<a name="ul5751239142816"></a><a name="ul5751239142816"></a><ul id="ul5751239142816"><li>十进制整数</li><li>取值范围[1, 65535)</li><li>不能包含<span class="parmvalue" id="parmvalue18751183912818"><a name="parmvalue18751183912818"></a><a name="parmvalue18751183912818"></a>“+”</span></li></ul>
</td>
</tr>
<tr id="row4751539122812"><td class="cellrowborder" valign="top" width="25.630000000000003%" headers="mcps1.2.4.1.1 "><p id="p375115393284"><a name="p375115393284"></a><a name="p375115393284"></a>size</p>
</td>
<td class="cellrowborder" valign="top" width="18.080000000000002%" headers="mcps1.2.4.1.2 "><p id="p2751639162811"><a name="p2751639162811"></a><a name="p2751639162811"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="56.290000000000006%" headers="mcps1.2.4.1.3 "><p id="p10751193912280"><a name="p10751193912280"></a><a name="p10751193912280"></a>分页查询时，每页最多展示的记录数。</p>
<a name="ul137519397282"></a><a name="ul137519397282"></a><ul id="ul137519397282"><li>十进制整数。</li><li>取值范围[1, 100]。</li><li>不能包含<span class="parmvalue" id="parmvalue37671391288"><a name="parmvalue37671391288"></a><a name="parmvalue37671391288"></a>“+”</span></li></ul>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   page和size的参数值均存在时，分页查询功能才会生效。如果只存在一个，系统会显示参数非法的错误。  
>-   当指定fpga\_image\_id参数时，page和size参数指定的分页查询功能将不生效。  

## 请求消息<a name="section8276847211756"></a>

不涉及

## 响应消息<a name="section1847981211756"></a>

**响应参数**

响应参数如[表2](#table41296006211756)所示。

**表 2**  响应参数

<a name="table41296006211756"></a>
<table><thead align="left"><tr id="row1990984211756"><th class="cellrowborder" valign="top" width="26%" id="mcps1.2.4.1.1"><p id="p15806308"><a name="p15806308"></a><a name="p15806308"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.75%" id="mcps1.2.4.1.2"><p id="p21995508"><a name="p21995508"></a><a name="p21995508"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.24999999999999%" id="mcps1.2.4.1.3"><p id="p36805753"><a name="p36805753"></a><a name="p36805753"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row12291995211756"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p47611720211756"><a name="p47611720211756"></a><a name="p47611720211756"></a>count</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p65870980211756"><a name="p65870980211756"></a><a name="p65870980211756"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p63884995211756"><a name="p63884995211756"></a><a name="p63884995211756"></a>查询的FPGA镜像数量。</p>
</td>
</tr>
<tr id="row13988964122742"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p59364323122742"><a name="p59364323122742"></a><a name="p59364323122742"></a>fpgaimages</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p43780854122742"><a name="p43780854122742"></a><a name="p43780854122742"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p56588294122742"><a name="p56588294122742"></a><a name="p56588294122742"></a>查询的FPGA镜像详情列表。</p>
</td>
</tr>
<tr id="row43619055211756"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p17102613211756"><a name="p17102613211756"></a><a name="p17102613211756"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p50695788211756"><a name="p50695788211756"></a><a name="p50695788211756"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p49395919211756"><a name="p49395919211756"></a><a name="p49395919211756"></a>FPGA镜像的ID。</p>
</td>
</tr>
<tr id="row41382846211756"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p14594565211756"><a name="p14594565211756"></a><a name="p14594565211756"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p60068226211756"><a name="p60068226211756"></a><a name="p60068226211756"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p24580412211756"><a name="p24580412211756"></a><a name="p24580412211756"></a>FPGA镜像的名称。</p>
</td>
</tr>
<tr id="row2706776211756"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p12159451211756"><a name="p12159451211756"></a><a name="p12159451211756"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p31907576211756"><a name="p31907576211756"></a><a name="p31907576211756"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p30372637211756"><a name="p30372637211756"></a><a name="p30372637211756"></a>FPGA镜像的描述信息。</p>
</td>
</tr>
<tr id="row16501990211756"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p16482479211756"><a name="p16482479211756"></a><a name="p16482479211756"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p29509334211756"><a name="p29509334211756"></a><a name="p29509334211756"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p58488155211756"><a name="p58488155211756"></a><a name="p58488155211756"></a>FPGA镜像的状态。</p>
<p id="p209718246611"><a name="p209718246611"></a><a name="p209718246611"></a>取整范围：</p>
<p id="p14667531069"><a name="p14667531069"></a><a name="p14667531069"></a>active，saving，deleting，error</p>
</td>
</tr>
<tr id="row23208874211756"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p50294579211756"><a name="p50294579211756"></a><a name="p50294579211756"></a>size</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p55007805211756"><a name="p55007805211756"></a><a name="p55007805211756"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p40832246211756"><a name="p40832246211756"></a><a name="p40832246211756"></a>FPGA镜像的文件大小，单位为MB。</p>
</td>
</tr>
<tr id="row6209341211756"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p63772911211756"><a name="p63772911211756"></a><a name="p63772911211756"></a>createdAt</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p23403431211756"><a name="p23403431211756"></a><a name="p23403431211756"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p7571123314012"><a name="p7571123314012"></a><a name="p7571123314012"></a>FPGA镜像的创建时间。</p>
<p id="p48706887211756"><a name="p48706887211756"></a><a name="p48706887211756"></a>使用UTC（Coordinated Universal Time）时间。</p>
</td>
</tr>
<tr id="row3069902211756"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p56866436211756"><a name="p56866436211756"></a><a name="p56866436211756"></a>protected</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p14992676211756"><a name="p14992676211756"></a><a name="p14992676211756"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p10022464211756"><a name="p10022464211756"></a><a name="p10022464211756"></a>该FPGA镜像是否受保护。</p>
<p id="p11704713203339"><a name="p11704713203339"></a><a name="p11704713203339"></a>受保护是指，该FPGA镜像与创建弹性云服务器使用的镜像关联，此时，不可以执行删除FPGA镜像的操作。</p>
</td>
</tr>
<tr id="row57042024211756"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p31688172211756"><a name="p31688172211756"></a><a name="p31688172211756"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p34157725211756"><a name="p34157725211756"></a><a name="p34157725211756"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p12786151213735"><a name="p12786151213735"></a><a name="p12786151213735"></a>FPGA镜像的附加信息。</p>
</td>
</tr>
<tr id="row9124165114747"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p859913114747"><a name="p859913114747"></a><a name="p859913114747"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p17931171520319"><a name="p17931171520319"></a><a name="p17931171520319"></a>Dict</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p29151897114957"><a name="p29151897114957"></a><a name="p29151897114957"></a>FPGA镜像的元数据信息。</p>
</td>
</tr>
<tr id="row1599674922420"><td class="cellrowborder" valign="top" width="26%" headers="mcps1.2.4.1.1 "><p id="p179961449132417"><a name="p179961449132417"></a><a name="p179961449132417"></a>log_directory</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.2.4.1.2 "><p id="p0996649122411"><a name="p0996649122411"></a><a name="p0996649122411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.24999999999999%" headers="mcps1.2.4.1.3 "><p id="p59961849152415"><a name="p59961849152415"></a><a name="p59961849152415"></a>FPGA镜像的构建日志文件在OBS中的目录路径，格式为“桶名:目录路径”，例如“obs-fpga:vu9p/log”。</p>
</td>
</tr>
</tbody>
</table>

## 示例<a name="section31303547211756"></a>

-   请求示例

    无

-   响应示例

    ```
    { 
      "count": 2, 
      "fpgaimages": [ 
        { 
          "id": "4010a32c5c7d7711015c81ac714c009d", 
          "name": "FPGA001", 
          "description": "fpga test", 
          "status": "active", 
          "size": 40, 
          "createdAt": "2017-06-07 08:29:41", 
          "protected": false, 
          "message": null, 
          "metadata": { 
            "shell_type": "OCL", 
            "shell_version": "1.0" 
          },
          "log_directory": "obs-fpga:vu9p/log"
        }, 
        { 
          "id": "4010a32c5c7d7711015c813e69bd002c", 
          "name": "FPGA002", 
          "description": "fpga test", 
          "status": "active", 
          "size": 43, 
          "createdAt": "2017-06-07 16:29:30", 
          "protected": true, 
          "messgae": null, 
          "metadata": { 
            "shell_type": "OCL", 
            "shell_version": "1.0" 
          },
          "log_directory": "obs-fpga:vu9p/log"
        } 
      ] 
    }
    ```


## 返回值<a name="section3477250491225"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码说明](错误码说明.md)。

