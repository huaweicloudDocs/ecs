# 注册FPGA镜像<a name="ZH-CN_TOPIC_0065962597"></a>

## 功能介绍<a name="section6847204211311"></a>

本接口用于注册FPGA镜像。

FPGA镜像是指用户开发的FPGA逻辑文件，通常也称为AEI（Accelerated Engine Image）。在注册FPGA镜像时，该逻辑文件需要存放在用户的OBS（Object Storage Service）桶中。

>![](public_sys-resources/icon-note.gif) **说明：**   
>目前仅“华北-北京一、华东-上海二、华南-广州”区域支持，其他区域暂未支持。  

## URI<a name="section62251638211311"></a>

POST /v1/\{project\_id\}/cloudservers/fpga\_image

参数说明请参见[表1](#table10080802211311)。

**表 1**  参数说明

<a name="table10080802211311"></a>
<table><thead align="left"><tr id="row23258692211311"><th class="cellrowborder" valign="top" width="21.86%" id="mcps1.2.4.1.1"><p id="p7707213"><a name="p7707213"></a><a name="p7707213"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.66%" id="mcps1.2.4.1.2"><p id="p20304554"><a name="p20304554"></a><a name="p20304554"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.480000000000004%" id="mcps1.2.4.1.3"><p id="p34056167"><a name="p34056167"></a><a name="p34056167"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row37402583211311"><td class="cellrowborder" valign="top" width="21.86%" headers="mcps1.2.4.1.1 "><p id="p54826436211311"><a name="p54826436211311"></a><a name="p54826436211311"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="17.66%" headers="mcps1.2.4.1.2 "><p id="p54905009211311"><a name="p54905009211311"></a><a name="p54905009211311"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="60.480000000000004%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section20272402211311"></a>

请求参数如[表2](#table5698154011375)所示。

**表 2**  请求参数

<a name="table5698154011375"></a>
<table><thead align="left"><tr id="row18698940103719"><th class="cellrowborder" valign="top" width="18.35%" id="mcps1.2.5.1.1"><p id="p1569884093712"><a name="p1569884093712"></a><a name="p1569884093712"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.02%" id="mcps1.2.5.1.2"><p id="p9699184073710"><a name="p9699184073710"></a><a name="p9699184073710"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="15.1%" id="mcps1.2.5.1.3"><p id="p1769974053715"><a name="p1769974053715"></a><a name="p1769974053715"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="51.53%" id="mcps1.2.5.1.4"><p id="p469974003711"><a name="p469974003711"></a><a name="p469974003711"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row769974019371"><td class="cellrowborder" valign="top" width="18.35%" headers="mcps1.2.5.1.1 "><p id="p1378615433718"><a name="p1378615433718"></a><a name="p1378615433718"></a>fpga_image</p>
</td>
<td class="cellrowborder" valign="top" width="15.02%" headers="mcps1.2.5.1.2 "><p id="p769911401374"><a name="p769911401374"></a><a name="p769911401374"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="15.1%" headers="mcps1.2.5.1.3 "><p id="p18699104011370"><a name="p18699104011370"></a><a name="p18699104011370"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.53%" headers="mcps1.2.5.1.4 "><p id="p19699134073719"><a name="p19699134073719"></a><a name="p19699134073719"></a>FPGA镜像信息详情。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  fpga\_image字段结构说明

<a name="table36632723211311"></a>
<table><thead align="left"><tr id="row6485675211311"><th class="cellrowborder" valign="top" width="18.42%" id="mcps1.2.5.1.1"><p id="p22916806211311"><a name="p22916806211311"></a><a name="p22916806211311"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.85%" id="mcps1.2.5.1.2"><p id="p58378163211311"><a name="p58378163211311"></a><a name="p58378163211311"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="15.409999999999998%" id="mcps1.2.5.1.3"><p id="p36640154211311"><a name="p36640154211311"></a><a name="p36640154211311"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="51.32%" id="mcps1.2.5.1.4"><p id="p58095138211311"><a name="p58095138211311"></a><a name="p58095138211311"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row55081076211311"><td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.1 "><p id="p30311735211311"><a name="p30311735211311"></a><a name="p30311735211311"></a>location</p>
</td>
<td class="cellrowborder" valign="top" width="14.85%" headers="mcps1.2.5.1.2 "><p id="p25396884211311"><a name="p25396884211311"></a><a name="p25396884211311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="15.409999999999998%" headers="mcps1.2.5.1.3 "><p id="p65343538211311"><a name="p65343538211311"></a><a name="p65343538211311"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.5.1.4 "><p id="p161527536573"><a name="p161527536573"></a><a name="p161527536573"></a>FPGA逻辑文件在OBS桶中的路径，格式为“桶名:文件名”，例如“obs-fpga:fpga.bin”。</p>
<p id="p1315225312576"><a name="p1315225312576"></a><a name="p1315225312576"></a>桶名的命名规则满足OBS的约束：</p>
<a name="ul43426540194839"></a><a name="ul43426540194839"></a><ul id="ul43426540194839"><li>由英文小写字母、数字以及特殊字符<span class="parmvalue" id="parmvalue53874239194845"><a name="parmvalue53874239194845"></a><a name="parmvalue53874239194845"></a>“.”</span>、<span class="parmvalue" id="parmvalue15106108194845"><a name="parmvalue15106108194845"></a><a name="parmvalue15106108194845"></a>“-”</span>组成。</li><li>只能以数字或字母开头和结尾。</li><li>长度3～63个字符。</li><li>不能是ip地址。</li><li>不能包含<span class="parmvalue" id="parmvalue54201329194939"><a name="parmvalue54201329194939"></a><a name="parmvalue54201329194939"></a>“..”</span>、<span class="parmvalue" id="parmvalue41175582194957"><a name="parmvalue41175582194957"></a><a name="parmvalue41175582194957"></a>“.-”</span>&nbsp;、<span class="parmvalue" id="parmvalue66080536195013"><a name="parmvalue66080536195013"></a><a name="parmvalue66080536195013"></a>“-.”</span>字符串。</li></ul>
<p id="p13624699194711"><a name="p13624699194711"></a><a name="p13624699194711"></a>文件名的命名规则如下：</p>
<a name="ul40992670194757"></a><a name="ul40992670194757"></a><ul id="ul40992670194757"><li>由英文大、小写字母，数字，中划线，下划线，斜杠，英文句号组成。</li><li>必须以<span class="parmvalue" id="parmvalue56750524194757"><a name="parmvalue56750524194757"></a><a name="parmvalue56750524194757"></a>“.bin”</span>或“xclbin”结尾。</li><li>长度4～64个字符。</li></ul>
</td>
</tr>
<tr id="row43174483211311"><td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.1 "><p id="p11983269211311"><a name="p11983269211311"></a><a name="p11983269211311"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="14.85%" headers="mcps1.2.5.1.2 "><p id="p1310425211311"><a name="p1310425211311"></a><a name="p1310425211311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="15.409999999999998%" headers="mcps1.2.5.1.3 "><p id="p7009559211311"><a name="p7009559211311"></a><a name="p7009559211311"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.5.1.4 "><p id="p5607686211311"><a name="p5607686211311"></a><a name="p5607686211311"></a>FPGA镜像的名称。</p>
<p id="p52669702211311"><a name="p52669702211311"></a><a name="p52669702211311"></a>取值范围：</p>
<a name="ul64450334162249"></a><a name="ul64450334162249"></a><ul id="ul64450334162249"><li>只能由英文字母、数字、下划线、中划线组成。</li><li>长度1~64个字符。</li></ul>
</td>
</tr>
<tr id="row49437453114111"><td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.1 "><p id="p32309183114120"><a name="p32309183114120"></a><a name="p32309183114120"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="14.85%" headers="mcps1.2.5.1.2 "><p id="p45454409114125"><a name="p45454409114125"></a><a name="p45454409114125"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="15.409999999999998%" headers="mcps1.2.5.1.3 "><p id="p36703951114111"><a name="p36703951114111"></a><a name="p36703951114111"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.5.1.4 "><p id="p37045433589"><a name="p37045433589"></a><a name="p37045433589"></a>FPGA镜像的元数据信息，要求是合法的JSON（JavaScript Object Notation）对象类型。</p>
<p id="p770494355817"><a name="p770494355817"></a><a name="p770494355817"></a>metadata在进行JSON序列化后的字符个数不能超过1024。</p>
</td>
</tr>
<tr id="row21013490211311"><td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.1 "><p id="p63941444211311"><a name="p63941444211311"></a><a name="p63941444211311"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="14.85%" headers="mcps1.2.5.1.2 "><p id="p9176036211311"><a name="p9176036211311"></a><a name="p9176036211311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="15.409999999999998%" headers="mcps1.2.5.1.3 "><p id="p53464121211311"><a name="p53464121211311"></a><a name="p53464121211311"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="51.32%" headers="mcps1.2.5.1.4 "><p id="p28403755211311"><a name="p28403755211311"></a><a name="p28403755211311"></a>FPGA镜像的描述信息，由中文汉字、中文句号、中文逗号、英文大小写字母、数字、中划线、下划线、英文句号、英文逗号、空格组成，长度0到255个字符。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section55994659211311"></a>

响应参数如[表4](#table551653634018)所示。

**表 4**  响应参数

<a name="table551653634018"></a>
<table><thead align="left"><tr id="row17516036104012"><th class="cellrowborder" valign="top" width="23.792379237923793%" id="mcps1.2.4.1.1"><p id="p75161336124015"><a name="p75161336124015"></a><a name="p75161336124015"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.583058305830583%" id="mcps1.2.4.1.2"><p id="p14517136124013"><a name="p14517136124013"></a><a name="p14517136124013"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="45.62456245624562%" id="mcps1.2.4.1.3"><p id="p751711364402"><a name="p751711364402"></a><a name="p751711364402"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1551763664016"><td class="cellrowborder" valign="top" width="23.792379237923793%" headers="mcps1.2.4.1.1 "><p id="p8517103634019"><a name="p8517103634019"></a><a name="p8517103634019"></a>fpga_image</p>
</td>
<td class="cellrowborder" valign="top" width="30.583058305830583%" headers="mcps1.2.4.1.2 "><p id="p6517173604019"><a name="p6517173604019"></a><a name="p6517173604019"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="45.62456245624562%" headers="mcps1.2.4.1.3 "><p id="p1451793612400"><a name="p1451793612400"></a><a name="p1451793612400"></a>FPGA镜像信息详情。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  fpga\_image字段结构说明

<a name="table8648200211311"></a>
<table><thead align="left"><tr id="row47349056211311"><th class="cellrowborder" valign="top" width="23.87%" id="mcps1.2.4.1.1"><p id="p15806308"><a name="p15806308"></a><a name="p15806308"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.64%" id="mcps1.2.4.1.2"><p id="p21995508"><a name="p21995508"></a><a name="p21995508"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="45.49%" id="mcps1.2.4.1.3"><p id="p36805753"><a name="p36805753"></a><a name="p36805753"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row64340933211311"><td class="cellrowborder" valign="top" width="23.87%" headers="mcps1.2.4.1.1 "><p id="p32671333211311"><a name="p32671333211311"></a><a name="p32671333211311"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="30.64%" headers="mcps1.2.4.1.2 "><p id="p30640904211311"><a name="p30640904211311"></a><a name="p30640904211311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.49%" headers="mcps1.2.4.1.3 "><p id="p51329136211311"><a name="p51329136211311"></a><a name="p51329136211311"></a>FPGA镜像的ID。</p>
</td>
</tr>
<tr id="row1620851211311"><td class="cellrowborder" valign="top" width="23.87%" headers="mcps1.2.4.1.1 "><p id="p26004605211311"><a name="p26004605211311"></a><a name="p26004605211311"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="30.64%" headers="mcps1.2.4.1.2 "><p id="p64423181211311"><a name="p64423181211311"></a><a name="p64423181211311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45.49%" headers="mcps1.2.4.1.3 "><p id="p63235550211311"><a name="p63235550211311"></a><a name="p63235550211311"></a>FPGA镜像状态。取值如下：</p>
<a name="ul10437195973916"></a><a name="ul10437195973916"></a><ul id="ul10437195973916"><li>saving：表示FPGA镜像正在上传文件到后端存储。</li><li>deleting：表示FPGA镜像正在删除中。</li><li>error：表示FPGA镜像创建失败。</li><li>active：表示FPGA镜像可以正常使用。</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section11362753211311"></a>

```
POST https://{endpoint}/v1/{project_id}/cloudservers/fpga_image
```

```
{ 
  "fpga_image": { 
    "location": "obs-fpga:fpga.bin", 
    "name": "fpga-image-test", 
    "description": "fpga description", 
    "metadata": { 
      "shell_type": "OCL", 
      "shell_version": "1.0" 
    } 
  } 
}
```

## 响应示例<a name="section7937164492610"></a>

```
{
  "fpga_image": {
    "status": "saving",
    "id": "4010a32c5c62bad9015c62dc2290002b"
  }
}
```

## 返回值<a name="section3477250491225"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码说明](错误码说明.md)。

