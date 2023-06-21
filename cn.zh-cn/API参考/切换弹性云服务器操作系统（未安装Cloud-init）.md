# 切换弹性云服务器操作系统（未安装Cloud-init）<a name="ecs_02_0204"></a>

## 功能介绍<a name="section61372619"></a>

切换弹性云服务器操作系统。

调用该接口后，系统将卸载系统盘，然后使用新镜像重新创建系统盘，并挂载至弹性云服务器，实现切换操作系统功能。

该接口支持未安装Cloud-init或Cloudbase-init的镜像使用，如果镜像安装了Cloud-init或者Cloudbase-init，请使用  [切换弹性云服务器操作系统（安装Cloud-init）](切换弹性云服务器操作系统（安装Cloud-init）.md)接口。

## 接口约束<a name="section2842257210401"></a>

-   不包含系统盘的弹性云服务器不能切换操作系统。
-   执行切换操作系统任务时，请勿并行执行其他任务，否则可能会引起切换操作系统失败。

## 调试<a name="section926243314015"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=ECS&api=ChangeServerOsWithoutCloudInit)中调试该接口。

## URI<a name="section15482662"></a>

POST /v1/\{project\_id\}/cloudservers/\{server\_id\}/changeos

参数说明请参见[表1](#table55945983)。

**表 1**  参数说明

<a name="table55945983"></a>
<table><thead align="left"><tr id="row11302482"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p43085863"><a name="p43085863"></a><a name="p43085863"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p294000"><a name="p294000"></a><a name="p294000"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p23814038"><a name="p23814038"></a><a name="p23814038"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row49888896"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p14468758"><a name="p14468758"></a><a name="p14468758"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p31118786"><a name="p31118786"></a><a name="p31118786"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p126791020134915"><a name="p126791020134915"></a><a name="p126791020134915"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row613736410235"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p2736446410235"><a name="p2736446410235"></a><a name="p2736446410235"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p192907210235"><a name="p192907210235"></a><a name="p192907210235"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p2203711610235"><a name="p2203711610235"></a><a name="p2203711610235"></a>弹性云服务器ID。</p>
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
<tbody><tr id="row6277626"><td class="cellrowborder" valign="top" width="21.800000000000004%" headers="mcps1.2.5.1.1 "><p id="p38725660"><a name="p38725660"></a><a name="p38725660"></a>os-change</p>
</td>
<td class="cellrowborder" valign="top" width="13.720000000000002%" headers="mcps1.2.5.1.2 "><p id="p49770771"><a name="p49770771"></a><a name="p49770771"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21.620000000000005%" headers="mcps1.2.5.1.3 "><p id="p4900679"><a name="p4900679"></a><a name="p4900679"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="42.86000000000001%" headers="mcps1.2.5.1.4 "><p id="p61410719"><a name="p61410719"></a><a name="p61410719"></a>切换弹性云服务器操作系统，详情参见 <a href="#table32200631">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  os-change字段数据结构说明

<a name="table32200631"></a>
<table><thead align="left"><tr id="row47660253"><th class="cellrowborder" valign="top" width="21.74217421742174%" id="mcps1.2.5.1.1"><p id="p59121236153913"><a name="p59121236153913"></a><a name="p59121236153913"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.601360136013602%" id="mcps1.2.5.1.2"><p id="p109126367395"><a name="p109126367395"></a><a name="p109126367395"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.61216121612161%" id="mcps1.2.5.1.3"><p id="p4927183633919"><a name="p4927183633919"></a><a name="p4927183633919"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.04430443044304%" id="mcps1.2.5.1.4"><p id="p8927183603911"><a name="p8927183603911"></a><a name="p8927183603911"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row65851064"><td class="cellrowborder" valign="top" width="21.74217421742174%" headers="mcps1.2.5.1.1 "><p id="p32335967"><a name="p32335967"></a><a name="p32335967"></a>adminpass</p>
</td>
<td class="cellrowborder" valign="top" width="13.601360136013602%" headers="mcps1.2.5.1.2 "><p id="p1967662"><a name="p1967662"></a><a name="p1967662"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p25162958"><a name="p25162958"></a><a name="p25162958"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p47739706113712"><a name="p47739706113712"></a><a name="p47739706113712"></a>云服务器管理员帐户的初始登录密码。</p>
<p id="p8742832102714"><a name="p8742832102714"></a><a name="p8742832102714"></a>其中，Windows管理员帐户的用户名为Administrator，Linux管理员账户的用户名为root。</p>
<p id="p11576631102714"><a name="p11576631102714"></a><a name="p11576631102714"></a>建议密码复杂度如下：</p>
<a name="ul37080817102714"></a><a name="ul37080817102714"></a><ul id="ul37080817102714"><li>长度为8-26位。</li><li>密码至少必须包含大写字母、小写字母、数字和特殊字符（!@$%^-_=+[{}]:,./?~#*）中的三种。</li></ul>
<div class="note" id="note15723730113732"><a name="note15723730113732"></a><a name="note15723730113732"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul11278217125417"></a><a name="ul11278217125417"></a><ul id="ul11278217125417"><li>Windows云服务器仅支持密码方式，且密码不能包含用户名或用户名的逆序，不能包含用户名中超过两个连续字符的部分。</li><li>adminpass和keyname不能同时为空。</li><li>adminpass和keyname不能同时有值。</li></ul>
</div></div>
</td>
</tr>
<tr id="row45934497"><td class="cellrowborder" valign="top" width="21.74217421742174%" headers="mcps1.2.5.1.1 "><p id="p29706771"><a name="p29706771"></a><a name="p29706771"></a>keyname</p>
</td>
<td class="cellrowborder" valign="top" width="13.601360136013602%" headers="mcps1.2.5.1.2 "><p id="p57438237"><a name="p57438237"></a><a name="p57438237"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p21985640"><a name="p21985640"></a><a name="p21985640"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p36006428"><a name="p36006428"></a><a name="p36006428"></a>密钥名称。</p>
<p id="p12355338417"><a name="p12355338417"></a><a name="p12355338417"></a>密钥可以通过密钥创建接口进行创建 <a href="创建和导入SSH密钥.md">创建和导入SSH密钥</a>（请参见），或使用SSH密钥查询接口查询已有的密钥（请参见<a href="查询SSH密钥列表.md">查询SSH密钥列表</a> ）。</p>
</td>
</tr>
<tr id="row2345411710289"><td class="cellrowborder" valign="top" width="21.74217421742174%" headers="mcps1.2.5.1.1 "><p id="p2073531110289"><a name="p2073531110289"></a><a name="p2073531110289"></a>userid</p>
</td>
<td class="cellrowborder" valign="top" width="13.601360136013602%" headers="mcps1.2.5.1.2 "><p id="p183865010289"><a name="p183865010289"></a><a name="p183865010289"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p1471297410289"><a name="p1471297410289"></a><a name="p1471297410289"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p5090020910289"><a name="p5090020910289"></a><a name="p5090020910289"></a>用户ID。当传入keyname参数时，优先使用本参数设置的userid，若userid为空，默认使用当前token中的userid。</p>
<div class="p" id="p650419516719"><a name="p650419516719"></a><a name="p650419516719"></a>查看用户ID方法：<a name="ecs_02_0201_ol118119201404"></a><a name="ecs_02_0201_ol118119201404"></a><ol id="ecs_02_0201_ol118119201404"><li>登录管理控制台。</li><li>单击用户名，在下拉列表中单击“我的凭证”。在该页面查看用户ID。</li></ol>
</div>
</td>
</tr>
<tr id="row13463057104537"><td class="cellrowborder" valign="top" width="21.74217421742174%" headers="mcps1.2.5.1.1 "><p id="p16765867104537"><a name="p16765867104537"></a><a name="p16765867104537"></a>imageid</p>
</td>
<td class="cellrowborder" valign="top" width="13.601360136013602%" headers="mcps1.2.5.1.2 "><p id="p15858014104537"><a name="p15858014104537"></a><a name="p15858014104537"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p9430737104537"><a name="p9430737104537"></a><a name="p9430737104537"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p25692204104537"><a name="p25692204104537"></a><a name="p25692204104537"></a>切换系统所使用的新镜像的ID，格式为UUID。</p>
<p id="p528161524217"><a name="p528161524217"></a><a name="p528161524217"></a>镜像的ID可以从控制台或者参考<a href="https://support.huaweicloud.com/api-ims/ims_03_0702.html" target="_blank" rel="noopener noreferrer">《镜像服务API参考》</a>的“查询镜像列表”的章节获取。</p>
</td>
</tr>
<tr id="row6144862102847"><td class="cellrowborder" valign="top" width="21.74217421742174%" headers="mcps1.2.5.1.1 "><p id="p27971812102847"><a name="p27971812102847"></a><a name="p27971812102847"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="13.601360136013602%" headers="mcps1.2.5.1.2 "><p id="p51124270102847"><a name="p51124270102847"></a><a name="p51124270102847"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p47425188102847"><a name="p47425188102847"></a><a name="p47425188102847"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p16235056102847"><a name="p16235056102847"></a><a name="p16235056102847"></a>切换云服务器的元数据。</p>
<p id="p45467933113554"><a name="p45467933113554"></a><a name="p45467933113554"></a>更多信息，请参见<a href="#table9120223">表4</a>。</p>
</td>
</tr>
<tr id="row341611732318"><td class="cellrowborder" valign="top" width="21.74217421742174%" headers="mcps1.2.5.1.1 "><p id="p184731425012"><a name="p184731425012"></a><a name="p184731425012"></a>mode</p>
</td>
<td class="cellrowborder" valign="top" width="13.601360136013602%" headers="mcps1.2.5.1.2 "><p id="p440141715114"><a name="p440141715114"></a><a name="p440141715114"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p154051718113"><a name="p154051718113"></a><a name="p154051718113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p15551537416"><a name="p15551537416"></a><a name="p15551537416"></a>取值为withStopServer ，支持开机状态下切换<span id="text540118559481"><a name="text540118559481"></a><a name="text540118559481"></a>弹性云服务器</span>操作系统。</p>
<p id="p15289182385312"><a name="p15289182385312"></a><a name="p15289182385312"></a>mode取值为withStopServer时，对开机状态的</p>
<p id="p122661523155311"><a name="p122661523155311"></a><a name="p122661523155311"></a><span id="text11777105644816"><a name="text11777105644816"></a><a name="text11777105644816"></a>弹性云服务器</span>执行切换操作系统操作，系统自动对云服务器先执行关机，再切换操作系统。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  metadata字段数据结构说明

<a name="table9120223"></a>
<table><thead align="left"><tr id="row45607220"><th class="cellrowborder" valign="top" width="21.62%" id="mcps1.2.5.1.1"><p id="p17545124116392"><a name="p17545124116392"></a><a name="p17545124116392"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.719999999999999%" id="mcps1.2.5.1.2"><p id="p115457418391"><a name="p115457418391"></a><a name="p115457418391"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.42%" id="mcps1.2.5.1.3"><p id="p154524113397"><a name="p154524113397"></a><a name="p154524113397"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.24%" id="mcps1.2.5.1.4"><p id="p12545104110392"><a name="p12545104110392"></a><a name="p12545104110392"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row8797171742418"><td class="cellrowborder" valign="top" width="21.62%" headers="mcps1.2.5.1.1 "><p id="p1562408795622"><a name="p1562408795622"></a><a name="p1562408795622"></a>__system__encrypted</p>
</td>
<td class="cellrowborder" valign="top" width="13.719999999999999%" headers="mcps1.2.5.1.2 "><p id="p5759155095622"><a name="p5759155095622"></a><a name="p5759155095622"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.42%" headers="mcps1.2.5.1.3 "><p id="p3440400295622"><a name="p3440400295622"></a><a name="p3440400295622"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.24%" headers="mcps1.2.5.1.4 "><p id="p729227516614"><a name="p729227516614"></a><a name="p729227516614"></a>metadata中的表示加密功能的字段，0代表不加密，1代表加密。</p>
<p id="p3526077895622"><a name="p3526077895622"></a><a name="p3526077895622"></a>该字段不存在时，系统盘默认为不加密。</p>
</td>
</tr>
<tr id="row469292072413"><td class="cellrowborder" valign="top" width="21.62%" headers="mcps1.2.5.1.1 "><p id="p241272995622"><a name="p241272995622"></a><a name="p241272995622"></a>__system__cmkid</p>
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

## 请求示例<a name="section7786195110396"></a>

```
POST https://{endpoint}/v1/{project_id}/cloudservers/{server_id}/changeos
```

```
{
    "os-change": {
        "keyname": "KeyPair-350b", 
        "userid": "7e25b1da389f4697a79df3a0e5bd494e", 
        "imageid": "e215580f-73ad-429d-b6f2-5433947433b0",
        "metadata": {
              "__system__encrypted": "1",
              "__system__cmkid": "83cdb52d-9ebf-4469-9cfa-e7b5b80da846"
        },
       "mode": "withStopServer"
    }
}
```

## 响应示例<a name="section188567402462"></a>

请参考[响应（任务类）](响应（任务类）.md)。

```
{      
    "job_id": "70a599e0-31e7-49b7-b260-868f441e862b" 
} 
```

## 返回值<a name="section27037160"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码](错误码.md)。

