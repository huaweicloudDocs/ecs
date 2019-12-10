# 创建FPGA镜像<a name="ZH-CN_TOPIC_0129111232"></a>

## 功能介绍<a name="section6847204211311"></a>

本接口用于创建FPGA镜像。当前仅支持创建能够加载到Xilinx VU9P芯片的镜像文件。

>![](public_sys-resources/icon-note.gif) **说明：**   
>目前仅“华北-北京一、华东-上海二、华南-广州”区域支持，其他区域暂未支持。  

在创建FPGA镜像前，用户需要提供创建FPGA镜像所需的DCP（Design Checkpoint ）文件，并将该文件存放到OBS（Object Storage Service）桶中。

本接口在完成FPGA镜像的初始化操作后会首先为用户返回FPGA镜像ID，然后通过后端的AFS（Accelerated Engine Image Factory Service）构建集群完成DCP文件到FPGA镜像文件的生成，并将构建过程中产生的日志文件上传到用户OBS桶的指定目录。构建日志文件会按照“\{FPGA镜像ID\}\_log.tar”的格式命名，例如“4010a32c5c62bad9015c62dc2290002b\_log.tar”。

在创建过程中，FPGA镜像的状态会不断变化。当状态为active或error时，表示创建完成。

**表 1**  状态说明

<a name="table930017963120"></a>
<table><thead align="left"><tr id="row193013983117"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p627861516312"><a name="p627861516312"></a><a name="p627861516312"></a>状态</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p628121519317"><a name="p628121519317"></a><a name="p628121519317"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row830111963119"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1928401510314"><a name="p1928401510314"></a><a name="p1928401510314"></a>initialling</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p716919361990"><a name="p716919361990"></a><a name="p716919361990"></a>创建FPGA镜像任务初始化中</p>
</td>
</tr>
<tr id="row230114943115"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1289111516312"><a name="p1289111516312"></a><a name="p1289111516312"></a>scheduling</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p536318526156"><a name="p536318526156"></a><a name="p536318526156"></a>FPGA镜像等待调度创建。</p>
</td>
</tr>
<tr id="row93012920317"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p13294191514314"><a name="p13294191514314"></a><a name="p13294191514314"></a>creating</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5771354161019"><a name="p5771354161019"></a><a name="p5771354161019"></a>FPGA镜像正在创建中</p>
</td>
</tr>
<tr id="row153012095317"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p15299201543116"><a name="p15299201543116"></a><a name="p15299201543116"></a>active</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1539967101115"><a name="p1539967101115"></a><a name="p1539967101115"></a>FPGA镜像可以正常使用</p>
</td>
</tr>
<tr id="row1630159153116"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p9304201553113"><a name="p9304201553113"></a><a name="p9304201553113"></a>error</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p193061615123110"><a name="p193061615123110"></a><a name="p193061615123110"></a>FPGA镜像创建失败</p>
</td>
</tr>
</tbody>
</table>

创建配额：单个租户一次最多只能创建一个FPGA镜像。当租户尝试同时创建多个FPGA镜像时，将创建失败。

## URI<a name="section62251638211311"></a>

POST /v2/\{project\_id\}/cloudservers/fpga\_image

参数说明请参见[表2](#table10080802211311)。

**表 2**  参数说明

<a name="table10080802211311"></a>
<table><thead align="left"><tr id="row23258692211311"><th class="cellrowborder" valign="top" width="21.86%" id="mcps1.2.4.1.1"><p id="p7707213"><a name="p7707213"></a><a name="p7707213"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.009999999999998%" id="mcps1.2.4.1.2"><p id="p20304554"><a name="p20304554"></a><a name="p20304554"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="56.13%" id="mcps1.2.4.1.3"><p id="p34056167"><a name="p34056167"></a><a name="p34056167"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row37402583211311"><td class="cellrowborder" valign="top" width="21.86%" headers="mcps1.2.4.1.1 "><p id="p54826436211311"><a name="p54826436211311"></a><a name="p54826436211311"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="22.009999999999998%" headers="mcps1.2.4.1.2 "><p id="p54905009211311"><a name="p54905009211311"></a><a name="p54905009211311"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="56.13%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section862212944020"></a>

请求参数如[表3](#table5698154011375)所示。

**表 3**  请求参数

<a name="table5698154011375"></a>
<table><thead align="left"><tr id="row18698940103719"><th class="cellrowborder" valign="top" width="22%" id="mcps1.2.5.1.1"><p id="p1569884093712"><a name="p1569884093712"></a><a name="p1569884093712"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16%" id="mcps1.2.5.1.2"><p id="p9699184073710"><a name="p9699184073710"></a><a name="p9699184073710"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.5.1.3"><p id="p1769974053715"><a name="p1769974053715"></a><a name="p1769974053715"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="48%" id="mcps1.2.5.1.4"><p id="p469974003711"><a name="p469974003711"></a><a name="p469974003711"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row769974019371"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p1378615433718"><a name="p1378615433718"></a><a name="p1378615433718"></a>fpga_image</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.5.1.2 "><p id="p769911401374"><a name="p769911401374"></a><a name="p769911401374"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.3 "><p id="p18699104011370"><a name="p18699104011370"></a><a name="p18699104011370"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="48%" headers="mcps1.2.5.1.4 "><p id="p19699134073719"><a name="p19699134073719"></a><a name="p19699134073719"></a>FPGA镜像信息详情。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  fpga\_image字段结构说明

<a name="table196831029174016"></a>
<table><thead align="left"><tr id="row0668132944014"><th class="cellrowborder" valign="top" width="22.052205220522055%" id="mcps1.2.5.1.1"><p id="p14668132912409"><a name="p14668132912409"></a><a name="p14668132912409"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.891589158915892%" id="mcps1.2.5.1.2"><p id="p11158193613577"><a name="p11158193613577"></a><a name="p11158193613577"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="14.321432143214322%" id="mcps1.2.5.1.3"><p id="p12707104595516"><a name="p12707104595516"></a><a name="p12707104595516"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="47.73477347734774%" id="mcps1.2.5.1.4"><p id="p136682029184014"><a name="p136682029184014"></a><a name="p136682029184014"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17683329174017"><td class="cellrowborder" valign="top" width="22.052205220522055%" headers="mcps1.2.5.1.1 "><p id="p1668192984019"><a name="p1668192984019"></a><a name="p1668192984019"></a>dcp_location</p>
</td>
<td class="cellrowborder" valign="top" width="15.891589158915892%" headers="mcps1.2.5.1.2 "><p id="p1115833611574"><a name="p1115833611574"></a><a name="p1115833611574"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="14.321432143214322%" headers="mcps1.2.5.1.3 "><p id="p12707174595512"><a name="p12707174595512"></a><a name="p12707174595512"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.73477347734774%" headers="mcps1.2.5.1.4 "><p id="p2066852924018"><a name="p2066852924018"></a><a name="p2066852924018"></a>DCP文件在OBS桶中的路径，格式为“桶名:文件名”，例如“obs-fpga:fpga-test-dcp.tar”。</p>
<p id="p196687291402"><a name="p196687291402"></a><a name="p196687291402"></a>桶名的命名规则满足OBS的约束：</p>
<a name="ul566862964019"></a><a name="ul566862964019"></a><ul id="ul566862964019"><li>由英文小写字母、数字以及特殊字符<span class="parmvalue" id="parmvalue186681629124018"><a name="parmvalue186681629124018"></a><a name="parmvalue186681629124018"></a>“.”</span>、<span class="parmvalue" id="parmvalue136681529194013"><a name="parmvalue136681529194013"></a><a name="parmvalue136681529194013"></a>“-”</span>组成。</li><li>只能以数字或字母开头和结尾。</li><li>长度3～63个字符。</li><li>不能是ip地址。</li><li>不能包含<span class="parmvalue" id="parmvalue26681729124016"><a name="parmvalue26681729124016"></a><a name="parmvalue26681729124016"></a>“..”</span>、<span class="parmvalue" id="parmvalue4668162918409"><a name="parmvalue4668162918409"></a><a name="parmvalue4668162918409"></a>“.-”</span>&nbsp;、<span class="parmvalue" id="parmvalue7668129124018"><a name="parmvalue7668129124018"></a><a name="parmvalue7668129124018"></a>“-.”</span>字符串。</li></ul>
<p id="p1466822934018"><a name="p1466822934018"></a><a name="p1466822934018"></a>文件名的命名规则如下：</p>
<a name="ul76833297407"></a><a name="ul76833297407"></a><ul id="ul76833297407"><li>由英文大、小写字母，数字，中划线，下划线，斜杠，英文句号组成。</li><li>不能以<span class="parmvalue" id="parmvalue8668122914405"><a name="parmvalue8668122914405"></a><a name="parmvalue8668122914405"></a>“/”</span>开头。</li><li>必须以<span class="parmvalue" id="parmvalue86686295405"><a name="parmvalue86686295405"></a><a name="parmvalue86686295405"></a>“.tar”</span>结尾。</li><li>长度4～128个字符。</li></ul>
<p id="p146831629144018"><a name="p146831629144018"></a><a name="p146831629144018"></a>如果文件名中包含目录结构，例如“vu9p/fpga-test-dcp.tar”，则每一级目录名需要满足以下规则：</p>
<a name="ul26831429204019"></a><a name="ul26831429204019"></a><ul id="ul26831429204019"><li>不能为空。</li><li>不能以<span class="parmvalue" id="parmvalue186831429194018"><a name="parmvalue186831429194018"></a><a name="parmvalue186831429194018"></a>“.”</span>开头或结尾。</li></ul>
</td>
</tr>
<tr id="row1568362915405"><td class="cellrowborder" valign="top" width="22.052205220522055%" headers="mcps1.2.5.1.1 "><p id="p76832290404"><a name="p76832290404"></a><a name="p76832290404"></a>log_directory</p>
</td>
<td class="cellrowborder" valign="top" width="15.891589158915892%" headers="mcps1.2.5.1.2 "><p id="p111581436145712"><a name="p111581436145712"></a><a name="p111581436145712"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="14.321432143214322%" headers="mcps1.2.5.1.3 "><p id="p11707154525515"><a name="p11707154525515"></a><a name="p11707154525515"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="47.73477347734774%" headers="mcps1.2.5.1.4 "><p id="p166831229154012"><a name="p166831229154012"></a><a name="p166831229154012"></a>构建日志文件在上传到OBS桶（DCP文件所在的OBS桶）中时的目录路径，例如“vu9p/log”。当该字段不存在或为空时，默认与用户的DCP文件位于同一级目录下。</p>
<p id="p15683129124010"><a name="p15683129124010"></a><a name="p15683129124010"></a>命名规则如下：</p>
<a name="ul0683229164014"></a><a name="ul0683229164014"></a><ul id="ul0683229164014"><li>由英文大、小写字母，数字，中划线，下划线，斜杠，英文句号组成。</li><li>不能以<span class="parmvalue" id="parmvalue1668362934012"><a name="parmvalue1668362934012"></a><a name="parmvalue1668362934012"></a>“/”</span>开头或结尾。</li><li>如果包含多级目录，则每一级目录名都不能为空，且不能以<span class="parmvalue" id="parmvalue468312984020"><a name="parmvalue468312984020"></a><a name="parmvalue468312984020"></a>“.”</span>开头或结尾。</li><li>长度0～64个字符。</li></ul>
</td>
</tr>
<tr id="row206831229204010"><td class="cellrowborder" valign="top" width="22.052205220522055%" headers="mcps1.2.5.1.1 "><p id="p1768318299401"><a name="p1768318299401"></a><a name="p1768318299401"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="15.891589158915892%" headers="mcps1.2.5.1.2 "><p id="p1215812361577"><a name="p1215812361577"></a><a name="p1215812361577"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="14.321432143214322%" headers="mcps1.2.5.1.3 "><p id="p1570814459558"><a name="p1570814459558"></a><a name="p1570814459558"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.73477347734774%" headers="mcps1.2.5.1.4 "><p id="p968382994011"><a name="p968382994011"></a><a name="p968382994011"></a>FPGA镜像的名称。</p>
<p id="p11683132913403"><a name="p11683132913403"></a><a name="p11683132913403"></a>取值范围：</p>
<a name="ul768315290401"></a><a name="ul768315290401"></a><ul id="ul768315290401"><li>只能由英文字母、数字、下划线、中划线组成。</li><li>长度1~64个字符。</li></ul>
</td>
</tr>
<tr id="row3683152954013"><td class="cellrowborder" valign="top" width="22.052205220522055%" headers="mcps1.2.5.1.1 "><p id="p14683172994020"><a name="p14683172994020"></a><a name="p14683172994020"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="15.891589158915892%" headers="mcps1.2.5.1.2 "><p id="p1415853620571"><a name="p1415853620571"></a><a name="p1415853620571"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="14.321432143214322%" headers="mcps1.2.5.1.3 "><p id="p170894516558"><a name="p170894516558"></a><a name="p170894516558"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="47.73477347734774%" headers="mcps1.2.5.1.4 "><p id="p156833295408"><a name="p156833295408"></a><a name="p156833295408"></a>FPGA镜像的描述信息，由中文汉字、中文句号、中文逗号、英文大小写字母、数字、中划线、下划线、英文句号、英文逗号、空格组成，长度0到255个字符。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section55994659211311"></a>

响应参数如[表5](#table551653634018)所示。

**表 5**  响应参数

<a name="table551653634018"></a>
<table><thead align="left"><tr id="row17516036104012"><th class="cellrowborder" valign="top" width="24.062406240624064%" id="mcps1.2.4.1.1"><p id="p75161336124015"><a name="p75161336124015"></a><a name="p75161336124015"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.122012201220123%" id="mcps1.2.4.1.2"><p id="p14517136124013"><a name="p14517136124013"></a><a name="p14517136124013"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.81558155815583%" id="mcps1.2.4.1.3"><p id="p751711364402"><a name="p751711364402"></a><a name="p751711364402"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1551763664016"><td class="cellrowborder" valign="top" width="24.062406240624064%" headers="mcps1.2.4.1.1 "><p id="p8517103634019"><a name="p8517103634019"></a><a name="p8517103634019"></a>fpga_image</p>
</td>
<td class="cellrowborder" valign="top" width="20.122012201220123%" headers="mcps1.2.4.1.2 "><p id="p6517173604019"><a name="p6517173604019"></a><a name="p6517173604019"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="55.81558155815583%" headers="mcps1.2.4.1.3 "><p id="p1451793612400"><a name="p1451793612400"></a><a name="p1451793612400"></a>FPGA镜像信息详情。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  fpga\_image字段结构说明

<a name="table8648200211311"></a>
<table><thead align="left"><tr id="row47349056211311"><th class="cellrowborder" valign="top" width="23.880000000000003%" id="mcps1.2.4.1.1"><p id="p15806308"><a name="p15806308"></a><a name="p15806308"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.69%" id="mcps1.2.4.1.2"><p id="p21995508"><a name="p21995508"></a><a name="p21995508"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.43%" id="mcps1.2.4.1.3"><p id="p36805753"><a name="p36805753"></a><a name="p36805753"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row64340933211311"><td class="cellrowborder" valign="top" width="23.880000000000003%" headers="mcps1.2.4.1.1 "><p id="p32671333211311"><a name="p32671333211311"></a><a name="p32671333211311"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20.69%" headers="mcps1.2.4.1.2 "><p id="p30640904211311"><a name="p30640904211311"></a><a name="p30640904211311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.43%" headers="mcps1.2.4.1.3 "><p id="p51329136211311"><a name="p51329136211311"></a><a name="p51329136211311"></a>FPGA镜像的ID。</p>
</td>
</tr>
<tr id="row1620851211311"><td class="cellrowborder" valign="top" width="23.880000000000003%" headers="mcps1.2.4.1.1 "><p id="p26004605211311"><a name="p26004605211311"></a><a name="p26004605211311"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="20.69%" headers="mcps1.2.4.1.2 "><p id="p64423181211311"><a name="p64423181211311"></a><a name="p64423181211311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.43%" headers="mcps1.2.4.1.3 "><p id="p63235550211311"><a name="p63235550211311"></a><a name="p63235550211311"></a>FPGA镜像状态。取值如下：</p>
<a name="ul10437195973916"></a><a name="ul10437195973916"></a><ul id="ul10437195973916"><li>initialling：表示创建FPGA镜像任务初始化中。</li><li>scheduling：表示等待调度创建。</li><li>creating：表示FPGA镜像正在创建中。</li><li>deleting：表示FPGA镜像正在删除中。</li><li>error：表示FPGA镜像创建失败。</li><li>active：表示FPGA镜像可以正常使用。</li></ul>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section11362753211311"></a>

```
POST https://{endpoint}/v2/{project_id}/cloudservers/fpga_image
```

```
{
  "fpga_image": {
    "dcp_location": "obs-fpga:vu9p/fpga-vu9p-dcp.tar",
    "log_directory": "vu9p/log",
    "name": "fpga-image-test",
    "description": "fpga description"
  }
}
```

## 响应示例<a name="section1852219202304"></a>

```
{
  "fpga_image": {
    "status": "initialling",
    "id": "4010a32c5c62bad9015c62dc2290002b"
  }
}
```

## 返回值<a name="section3477250491225"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码说明](错误码说明.md)。

