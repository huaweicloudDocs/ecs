# 重装弹性云服务器操作系统（未安装Cloud-init）<a name="ecs_02_0203"></a>

## 功能介绍<a name="section61372619"></a>

重装弹性云服务器的操作系统。

本接口为异步接口，当前重装弹性云服务器操作系统请求下发成功后会返回job\_id，此时重装弹性云服务器操作系统并没有立即完成，需要通过调用[查询任务的执行状态](查询任务的执行状态.md)查询job状态，当Job状态为 SUCCESS 时代表云服务器操作系统重装成功。

调用该接口后，系统将卸载系统盘，然后使用原镜像重新创建系统盘，并挂载至弹性云服务器，实现重装操作系统功能。

该接口支持未安装Cloud-init或Cloudbase-init的镜像，如果镜像安装了Cloud-init或者Cloudbase-init，请使用  [重装弹性云服务器操作系统（安装Cloud-init）](重装弹性云服务器操作系统（安装Cloud-init）.md)接口。

## 接口约束<a name="section2842257210401"></a>

-   不包含系统盘的弹性云服务器不能执行重装操作。
-   执行重装操作系统任务时，请勿并行执行其他任务，否则可能会引起重装操作系统失败。

## 调试<a name="section926243314015"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=ECS&api=ReinstallServerWithoutCloudInit)中调试该接口。

## URI<a name="section15482662"></a>

POST /v1/\{project\_id\}/cloudservers/\{server\_id\}/reinstallos

参数说明请参见[表1](#table55945983)。

**表 1**  参数说明

<a name="table55945983"></a>
<table><thead align="left"><tr id="row11302482"><th class="cellrowborder" valign="top" width="24.462446244624463%" id="mcps1.2.4.1.1"><p id="p43085863"><a name="p43085863"></a><a name="p43085863"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.272427242724273%" id="mcps1.2.4.1.2"><p id="p294000"><a name="p294000"></a><a name="p294000"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="51.26512651265126%" id="mcps1.2.4.1.3"><p id="p23814038"><a name="p23814038"></a><a name="p23814038"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row49888896"><td class="cellrowborder" valign="top" width="24.462446244624463%" headers="mcps1.2.4.1.1 "><p id="p14468758"><a name="p14468758"></a><a name="p14468758"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.272427242724273%" headers="mcps1.2.4.1.2 "><p id="p31118786"><a name="p31118786"></a><a name="p31118786"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.26512651265126%" headers="mcps1.2.4.1.3 "><p id="p145635146499"><a name="p145635146499"></a><a name="p145635146499"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row613736410235"><td class="cellrowborder" valign="top" width="24.462446244624463%" headers="mcps1.2.4.1.1 "><p id="p2736446410235"><a name="p2736446410235"></a><a name="p2736446410235"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.272427242724273%" headers="mcps1.2.4.1.2 "><p id="p192907210235"><a name="p192907210235"></a><a name="p192907210235"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="51.26512651265126%" headers="mcps1.2.4.1.3 "><p id="p2203711610235"><a name="p2203711610235"></a><a name="p2203711610235"></a>弹性云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section5126234"></a>

请求参数如[表2](#table2840889)所示。

**表 2**  请求参数

<a name="table2840889"></a>
<table><thead align="left"><tr id="row19854472"><th class="cellrowborder" valign="top" width="21.800000000000004%" id="mcps1.2.5.1.1"><p id="p5212090120624"><a name="p5212090120624"></a><a name="p5212090120624"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.720000000000002%" id="mcps1.2.5.1.2"><p id="p5568008920626"><a name="p5568008920626"></a><a name="p5568008920626"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.620000000000005%" id="mcps1.2.5.1.3"><p id="p4189246820628"><a name="p4189246820628"></a><a name="p4189246820628"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="42.86000000000001%" id="mcps1.2.5.1.4"><p id="p2137802720629"><a name="p2137802720629"></a><a name="p2137802720629"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6277626"><td class="cellrowborder" valign="top" width="21.800000000000004%" headers="mcps1.2.5.1.1 "><p id="p38725660"><a name="p38725660"></a><a name="p38725660"></a>os-reinstall</p>
</td>
<td class="cellrowborder" valign="top" width="13.720000000000002%" headers="mcps1.2.5.1.2 "><p id="p49770771"><a name="p49770771"></a><a name="p49770771"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21.620000000000005%" headers="mcps1.2.5.1.3 "><p id="p4900679"><a name="p4900679"></a><a name="p4900679"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="42.86000000000001%" headers="mcps1.2.5.1.4 "><p id="p61410719"><a name="p61410719"></a><a name="p61410719"></a>重装弹性云服务器，详情参见<a href="#table32200631">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  os-reinstall字段数据结构说明

<a name="table32200631"></a>
<table><thead align="left"><tr id="row47660253"><th class="cellrowborder" valign="top" width="21.62216221622162%" id="mcps1.2.5.1.1"><p id="p12719134223610"><a name="p12719134223610"></a><a name="p12719134223610"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.72137213721372%" id="mcps1.2.5.1.2"><p id="p171964243615"><a name="p171964243615"></a><a name="p171964243615"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.61216121612161%" id="mcps1.2.5.1.3"><p id="p11719144217362"><a name="p11719144217362"></a><a name="p11719144217362"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.04430443044304%" id="mcps1.2.5.1.4"><p id="p97194429363"><a name="p97194429363"></a><a name="p97194429363"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row65851064"><td class="cellrowborder" valign="top" width="21.62216221622162%" headers="mcps1.2.5.1.1 "><p id="p32335967"><a name="p32335967"></a><a name="p32335967"></a>adminpass</p>
</td>
<td class="cellrowborder" valign="top" width="13.72137213721372%" headers="mcps1.2.5.1.2 "><p id="p1967662"><a name="p1967662"></a><a name="p1967662"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p25162958"><a name="p25162958"></a><a name="p25162958"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p16847167112050"><a name="p16847167112050"></a><a name="p16847167112050"></a>云服务器管理员账户的初始登录密码。</p>
<p id="p8742832102714"><a name="p8742832102714"></a><a name="p8742832102714"></a>其中，Windows管理员账户的用户名为Administrator，Linux管理员账户的用户名为root。</p>
<p id="p11576631102714"><a name="p11576631102714"></a><a name="p11576631102714"></a>建议密码复杂度如下：</p>
<a name="ul37080817102714"></a><a name="ul37080817102714"></a><ul id="ul37080817102714"><li>长度为8-26位。</li><li>密码至少必须包含大写字母、小写字母、数字和特殊字符（!@$%^-_=+[{}]:,./?~#*）中的三种。</li></ul>
<div class="note" id="note65349643112129"><a name="note65349643112129"></a><a name="note65349643112129"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul8134516175112"></a><a name="ul8134516175112"></a><ul id="ul8134516175112"><li>对于Windows弹性云服务器，仅支持密码方式，且密码不能包含用户名或用户名的逆序，不能包含用户名中超过两个连续字符的部分。</li><li>adminpass和keyname不能同时为空。</li><li>adminpass和keyname不能同时有值。</li></ul>
</div></div>
</td>
</tr>
<tr id="row45934497"><td class="cellrowborder" valign="top" width="21.62216221622162%" headers="mcps1.2.5.1.1 "><p id="p29706771"><a name="p29706771"></a><a name="p29706771"></a>keyname</p>
</td>
<td class="cellrowborder" valign="top" width="13.72137213721372%" headers="mcps1.2.5.1.2 "><p id="p57438237"><a name="p57438237"></a><a name="p57438237"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p21985640"><a name="p21985640"></a><a name="p21985640"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p36006428"><a name="p36006428"></a><a name="p36006428"></a>密钥名称。</p>
</td>
</tr>
<tr id="row2345411710289"><td class="cellrowborder" valign="top" width="21.62216221622162%" headers="mcps1.2.5.1.1 "><p id="p2073531110289"><a name="p2073531110289"></a><a name="p2073531110289"></a>userid</p>
</td>
<td class="cellrowborder" valign="top" width="13.72137213721372%" headers="mcps1.2.5.1.2 "><p id="p183865010289"><a name="p183865010289"></a><a name="p183865010289"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p1471297410289"><a name="p1471297410289"></a><a name="p1471297410289"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p5090020910289"><a name="p5090020910289"></a><a name="p5090020910289"></a>用户ID。</p>
</td>
</tr>
<tr id="row6144862102847"><td class="cellrowborder" valign="top" width="21.62216221622162%" headers="mcps1.2.5.1.1 "><p id="p27971812102847"><a name="p27971812102847"></a><a name="p27971812102847"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="13.72137213721372%" headers="mcps1.2.5.1.2 "><p id="p51124270102847"><a name="p51124270102847"></a><a name="p51124270102847"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p47425188102847"><a name="p47425188102847"></a><a name="p47425188102847"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p16235056102847"><a name="p16235056102847"></a><a name="p16235056102847"></a>重装云服务器的元数据。</p>
<p id="p3830913711291"><a name="p3830913711291"></a><a name="p3830913711291"></a>更多信息，请参见<a href="#table9120223">表4</a>。</p>
</td>
</tr>
<tr id="row11625112219"><td class="cellrowborder" valign="top" width="21.62216221622162%" headers="mcps1.2.5.1.1 "><p id="p184731425012"><a name="p184731425012"></a><a name="p184731425012"></a>mode</p>
</td>
<td class="cellrowborder" valign="top" width="13.72137213721372%" headers="mcps1.2.5.1.2 "><p id="p440141715114"><a name="p440141715114"></a><a name="p440141715114"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p154051718113"><a name="p154051718113"></a><a name="p154051718113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p15551537416"><a name="p15551537416"></a><a name="p15551537416"></a>取值为withStopServer ，支持开机状态下重装<span id="text12241204994818"><a name="text12241204994818"></a><a name="text12241204994818"></a>弹性云服务器</span>。</p>
<p id="p15289182385312"><a name="p15289182385312"></a><a name="p15289182385312"></a>mode取值为withStopServer时，对开机状态的</p>
<p id="p122661523155311"><a name="p122661523155311"></a><a name="p122661523155311"></a><span id="text109125011482"><a name="text109125011482"></a><a name="text109125011482"></a>弹性云服务器</span>执行重装操作，系统自动对云服务器先执行关机，再重装操作系统。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  metadata字段数据结构说明

<a name="table9120223"></a>
<table><thead align="left"><tr id="row45607220"><th class="cellrowborder" valign="top" width="21.62%" id="mcps1.2.5.1.1"><p id="p281394610369"><a name="p281394610369"></a><a name="p281394610369"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.719999999999999%" id="mcps1.2.5.1.2"><p id="p188291346183618"><a name="p188291346183618"></a><a name="p188291346183618"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.42%" id="mcps1.2.5.1.3"><p id="p682911463367"><a name="p682911463367"></a><a name="p682911463367"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.24%" id="mcps1.2.5.1.4"><p id="p98291846203618"><a name="p98291846203618"></a><a name="p98291846203618"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1666125613534"><td class="cellrowborder" valign="top" width="21.62%" headers="mcps1.2.5.1.1 "><p id="p1562408795622"><a name="p1562408795622"></a><a name="p1562408795622"></a>__system__encrypted</p>
</td>
<td class="cellrowborder" valign="top" width="13.719999999999999%" headers="mcps1.2.5.1.2 "><p id="p5759155095622"><a name="p5759155095622"></a><a name="p5759155095622"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.42%" headers="mcps1.2.5.1.3 "><p id="p3440400295622"><a name="p3440400295622"></a><a name="p3440400295622"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.24%" headers="mcps1.2.5.1.4 "><p id="p729227516614"><a name="p729227516614"></a><a name="p729227516614"></a>metadata中的表示加密功能的字段，0代表不加密，1代表加密。</p>
<p id="p3526077895622"><a name="p3526077895622"></a><a name="p3526077895622"></a>该字段不存在时，系统盘默认为不加密。</p>
</td>
</tr>
<tr id="row146669561533"><td class="cellrowborder" valign="top" width="21.62%" headers="mcps1.2.5.1.1 "><p id="p241272995622"><a name="p241272995622"></a><a name="p241272995622"></a>__system__cmkid</p>
</td>
<td class="cellrowborder" valign="top" width="13.719999999999999%" headers="mcps1.2.5.1.2 "><p id="p683657101711"><a name="p683657101711"></a><a name="p683657101711"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.42%" headers="mcps1.2.5.1.3 "><p id="p5933737595622"><a name="p5933737595622"></a><a name="p5933737595622"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.24%" headers="mcps1.2.5.1.4 "><p id="p20670814113715"><a name="p20670814113715"></a><a name="p20670814113715"></a>用户主密钥ID，是metadata中的表示加密功能的字段，与__system__encrypted配合使用。</p>
<div class="note" id="note153392271895"><a name="note153392271895"></a><a name="note153392271895"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1859814343917"><a name="p1859814343917"></a><a name="p1859814343917"></a>请参考<a href="https://support.huaweicloud.com/api-dew/ListKeys.html" target="_blank" rel="noopener noreferrer">查询密钥列表</a>，通过HTTPS请求获取密钥ID。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section46136113"></a>

请参考[响应（任务类）](响应（任务类）.md)。

## 请求示例<a name="section15863105410364"></a>

重装云服务器操作系统，重装后采用密钥方式登录鉴权。

```
POST https://{endpoint}/v1/{project_id}/cloudservers/{server_id}/reinstallos

{
    "os-reinstall": {
        "keyname": "KeyPair-350b", 
        "userid": "7e25b1da389f4697a79df3a0e5bd494e",
        "metadata": {
              "__system__encrypted": "1",
              "__system__cmkid": "83cdb52d-9ebf-4469-9cfa-e7b5b80da846"
        }
    }
}
```

## 响应示例<a name="section1760151015465"></a>

请参考[响应（任务类）](响应（任务类）.md)。

```
{      
    "job_id": "ff80808288d41e1b018990260955686a" 
}
```

## 返回值<a name="section27037160"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码](错误码.md)。

