# 切换弹性云服务器操作系统（安装Cloud-init）<a name="ecs_02_0202"></a>

## 功能介绍<a name="section61372619"></a>

切换弹性云服务器操作系统。支持弹性云服务器数据盘不变的情况下，使用新镜像重装系统盘。

调用该接口后，系统将卸载系统盘，然后使用新镜像重新创建系统盘，并挂载至弹性云服务器，实现切换操作系统功能。

## 接口约束<a name="section2842257210401"></a>

-   该接口仅支持安装了Cloud-init或Cloudbase-init的镜像。如果镜像未安装Cloud-init或者Cloudbase-init，请使用  [切换弹性云服务器操作系统（未安装Cloud-init）](切换弹性云服务器操作系统（未安装Cloud-init）.md)接口。
-   不包含系统盘的弹性云服务器不能切换操作系统。
-   执行切换操作系统任务时，请勿并行执行其他任务，否则可能会引起切换操作系统失败。

## URI<a name="section15482662"></a>

POST /v2/\{project\_id\}/cloudservers/\{server\_id\}/changeos

参数说明请参见[表1](#table55945983)。

**表 1**  参数说明

<a name="table55945983"></a>
<table><thead align="left"><tr id="row11302482"><th class="cellrowborder" valign="top" width="28.322832283228323%" id="mcps1.2.4.1.1"><p id="p43085863"><a name="p43085863"></a><a name="p43085863"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="27.502750275027505%" id="mcps1.2.4.1.2"><p id="p294000"><a name="p294000"></a><a name="p294000"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="44.174417441744176%" id="mcps1.2.4.1.3"><p id="p23814038"><a name="p23814038"></a><a name="p23814038"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row49888896"><td class="cellrowborder" valign="top" width="28.322832283228323%" headers="mcps1.2.4.1.1 "><p id="p14468758"><a name="p14468758"></a><a name="p14468758"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="27.502750275027505%" headers="mcps1.2.4.1.2 "><p id="p31118786"><a name="p31118786"></a><a name="p31118786"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="44.174417441744176%" headers="mcps1.2.4.1.3 "><p id="p14668137174919"><a name="p14668137174919"></a><a name="p14668137174919"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row613736410235"><td class="cellrowborder" valign="top" width="28.322832283228323%" headers="mcps1.2.4.1.1 "><p id="p2736446410235"><a name="p2736446410235"></a><a name="p2736446410235"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="27.502750275027505%" headers="mcps1.2.4.1.2 "><p id="p192907210235"><a name="p192907210235"></a><a name="p192907210235"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="44.174417441744176%" headers="mcps1.2.4.1.3 "><p id="p2203711610235"><a name="p2203711610235"></a><a name="p2203711610235"></a><span id="text21613364484"><a name="text21613364484"></a><a name="text21613364484"></a>弹性云服务器</span>ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section5126234"></a>

请求参数如[表2](#table2840889)所示。

**表 2**  请求参数

<a name="table2840889"></a>
<table><thead align="left"><tr id="row19854472"><th class="cellrowborder" valign="top" width="22%" id="mcps1.2.5.1.1"><p id="p5212090120624"><a name="p5212090120624"></a><a name="p5212090120624"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.5.1.2"><p id="p5568008920626"><a name="p5568008920626"></a><a name="p5568008920626"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16%" id="mcps1.2.5.1.3"><p id="p4189246820628"><a name="p4189246820628"></a><a name="p4189246820628"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48%" id="mcps1.2.5.1.4"><p id="p2137802720629"><a name="p2137802720629"></a><a name="p2137802720629"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6277626"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p38725660"><a name="p38725660"></a><a name="p38725660"></a>os-change</p>
</td>
<td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.5.1.2 "><p id="p49770771"><a name="p49770771"></a><a name="p49770771"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.5.1.3 "><p id="p4900679"><a name="p4900679"></a><a name="p4900679"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48%" headers="mcps1.2.5.1.4 "><p id="p61410719"><a name="p61410719"></a><a name="p61410719"></a>切换<span id="text192332371481"><a name="text192332371481"></a><a name="text192332371481"></a>弹性云服务器</span>操作系统，详情参见<a href="#table32200631">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  os-change字段数据结构说明

<a name="table32200631"></a>
<table><thead align="left"><tr id="row47660253"><th class="cellrowborder" valign="top" width="21.990000000000002%" id="mcps1.2.5.1.1"><p id="p121269618348"><a name="p121269618348"></a><a name="p121269618348"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.01%" id="mcps1.2.5.1.2"><p id="p1312613618346"><a name="p1312613618346"></a><a name="p1312613618346"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="15.879999999999999%" id="mcps1.2.5.1.3"><p id="p51418673415"><a name="p51418673415"></a><a name="p51418673415"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.120000000000005%" id="mcps1.2.5.1.4"><p id="p7141166143418"><a name="p7141166143418"></a><a name="p7141166143418"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row65851064"><td class="cellrowborder" valign="top" width="21.990000000000002%" headers="mcps1.2.5.1.1 "><p id="p32335967"><a name="p32335967"></a><a name="p32335967"></a>adminpass</p>
</td>
<td class="cellrowborder" valign="top" width="14.01%" headers="mcps1.2.5.1.2 "><p id="p1967662"><a name="p1967662"></a><a name="p1967662"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.879999999999999%" headers="mcps1.2.5.1.3 "><p id="p25162958"><a name="p25162958"></a><a name="p25162958"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.120000000000005%" headers="mcps1.2.5.1.4 "><p id="p47739706113712"><a name="p47739706113712"></a><a name="p47739706113712"></a><span id="text51831520162420"><a name="text51831520162420"></a><a name="text51831520162420"></a>云服务器</span>管理员帐户的初始登录密码。</p>
<p id="p8742832102714"><a name="p8742832102714"></a><a name="p8742832102714"></a>其中，Windows管理员帐户的用户名为Administrator，Linux管理员账户的用户名为root。</p>
<p id="p11576631102714"><a name="p11576631102714"></a><a name="p11576631102714"></a>建议密码复杂度如下：</p>
<a name="ul37080817102714"></a><a name="ul37080817102714"></a><ul id="ul37080817102714"><li>长度为8-26位。</li><li>密码至少必须包含大写字母、小写字母、数字和特殊字符（!@$%^-_=+[{}]:,./?~#*）中的三种。</li></ul>
<div class="note" id="note15723730113732"><a name="note15723730113732"></a><a name="note15723730113732"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul1384211203571"></a><a name="ul1384211203571"></a><ul id="ul1384211203571"><li>Windows<span id="text1944152117246"><a name="text1944152117246"></a><a name="text1944152117246"></a>云服务器</span>的密码，不能包含用户名或用户名的逆序，不能包含用户名中超过两个连续字符的部分。</li><li>对于Linux弹性云服务器也可使用user_data字段实现密码注入，此时adminpass字段无效。</li><li>adminpass和keyname不能同时有值。</li><li>adminpass和keyname如果同时为空，此时，metadata中的user_data属性必须有值。</li><li>对于已安装Cloud-init的<span id="text1579052111243"><a name="text1579052111243"></a><a name="text1579052111243"></a>云服务器</span>，使用adminpass字段切换操作系统时，系统如果提示您使用keypair方式切换操作系统，表示当前区域暂不支持使用密码方式。</li></ul>
</div></div>
</td>
</tr>
<tr id="row45934497"><td class="cellrowborder" valign="top" width="21.990000000000002%" headers="mcps1.2.5.1.1 "><p id="p29706771"><a name="p29706771"></a><a name="p29706771"></a>keyname</p>
</td>
<td class="cellrowborder" valign="top" width="14.01%" headers="mcps1.2.5.1.2 "><p id="p57438237"><a name="p57438237"></a><a name="p57438237"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.879999999999999%" headers="mcps1.2.5.1.3 "><p id="p21985640"><a name="p21985640"></a><a name="p21985640"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.120000000000005%" headers="mcps1.2.5.1.4 "><p id="p36006428"><a name="p36006428"></a><a name="p36006428"></a>密钥名称。</p>
<p id="p12355338417"><a name="p12355338417"></a><a name="p12355338417"></a><span>密钥可以通过密钥创建接口</span><span>进行</span><span>创建 </span><a href="创建和导入SSH密钥.md">创建和导入SSH密钥</a><span>（请参见），或使用SSH密钥查询接口</span><span>查</span><span>询已有的密钥（请参见</span><a href="查询SSH密钥列表.md">查询SSH密钥列表</a><span> ）。</span></p>
</td>
</tr>
<tr id="row2345411710289"><td class="cellrowborder" valign="top" width="21.990000000000002%" headers="mcps1.2.5.1.1 "><p id="p2073531110289"><a name="p2073531110289"></a><a name="p2073531110289"></a>userid</p>
</td>
<td class="cellrowborder" valign="top" width="14.01%" headers="mcps1.2.5.1.2 "><p id="p183865010289"><a name="p183865010289"></a><a name="p183865010289"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.879999999999999%" headers="mcps1.2.5.1.3 "><p id="p1471297410289"><a name="p1471297410289"></a><a name="p1471297410289"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.120000000000005%" headers="mcps1.2.5.1.4 "><p id="p5090020910289"><a name="p5090020910289"></a><a name="p5090020910289"></a>用户ID。当传入keyname参数时，此参数为必选。</p>
<div class="p" id="p650419516719"><a name="p650419516719"></a><a name="p650419516719"></a>查看用户ID方法：<a name="ecs_02_0201_ol118119201404"></a><a name="ecs_02_0201_ol118119201404"></a><ol id="ecs_02_0201_ol118119201404"><li>登录管理控制台。</li><li><span>单击用户名，在下拉列表中单击“我的凭证”。</span>在该页面查看用户ID。</li></ol>
</div>
</td>
</tr>
<tr id="row13463057104537"><td class="cellrowborder" valign="top" width="21.990000000000002%" headers="mcps1.2.5.1.1 "><p id="p16765867104537"><a name="p16765867104537"></a><a name="p16765867104537"></a>imageid</p>
</td>
<td class="cellrowborder" valign="top" width="14.01%" headers="mcps1.2.5.1.2 "><p id="p15858014104537"><a name="p15858014104537"></a><a name="p15858014104537"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="15.879999999999999%" headers="mcps1.2.5.1.3 "><p id="p9430737104537"><a name="p9430737104537"></a><a name="p9430737104537"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.120000000000005%" headers="mcps1.2.5.1.4 "><p id="p25692204104537"><a name="p25692204104537"></a><a name="p25692204104537"></a>切换系统所使用的新镜像的ID，格式为UUID。</p>
<p id="p528161524217"><a name="p528161524217"></a><a name="p528161524217"></a>镜像的ID可以从控制台或者参考<a href="https://support.huaweicloud.com/api-ims/ims_03_0702.html" target="_blank" rel="noopener noreferrer">《镜像服务API参考》</a>的“查询镜像列表”的章节获取。</p>
</td>
</tr>
<tr id="row6144862102847"><td class="cellrowborder" valign="top" width="21.990000000000002%" headers="mcps1.2.5.1.1 "><p id="p27971812102847"><a name="p27971812102847"></a><a name="p27971812102847"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="14.01%" headers="mcps1.2.5.1.2 "><p id="p51124270102847"><a name="p51124270102847"></a><a name="p51124270102847"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.879999999999999%" headers="mcps1.2.5.1.3 "><p id="p47425188102847"><a name="p47425188102847"></a><a name="p47425188102847"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48.120000000000005%" headers="mcps1.2.5.1.4 "><p id="p16235056102847"><a name="p16235056102847"></a><a name="p16235056102847"></a>切换<span id="text1473216229249"><a name="text1473216229249"></a><a name="text1473216229249"></a>云服务器</span>的元数据。</p>
<p id="p45467933113554"><a name="p45467933113554"></a><a name="p45467933113554"></a>更多信息，请参见<a href="#table9120223">表4</a>。</p>
</td>
</tr>
<tr id="row8901153165514"><td class="cellrowborder" valign="top" width="21.990000000000002%" headers="mcps1.2.5.1.1 "><p id="p184731425012"><a name="p184731425012"></a><a name="p184731425012"></a>mode</p>
</td>
<td class="cellrowborder" valign="top" width="14.01%" headers="mcps1.2.5.1.2 "><p id="p440141715114"><a name="p440141715114"></a><a name="p440141715114"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.879999999999999%" headers="mcps1.2.5.1.3 "><p id="p154051718113"><a name="p154051718113"></a><a name="p154051718113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.120000000000005%" headers="mcps1.2.5.1.4 "><p id="p15551537416"><a name="p15551537416"></a><a name="p15551537416"></a>取值为withStopServer ，支持开机状态下切换<span id="text1524133812487"><a name="text1524133812487"></a><a name="text1524133812487"></a>弹性云服务器</span>操作系统。</p>
<p id="p15289182385312"><a name="p15289182385312"></a><a name="p15289182385312"></a>mode取值为withStopServer时，对开机状态的<span id="text3545839114819"><a name="text3545839114819"></a><a name="text3545839114819"></a>弹性云服务器</span>执行切换操作系统操作，系统自动对云服务器先执行关机，再切换操作系统。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  metadata字段数据结构说明

<a name="table9120223"></a>
<table><thead align="left"><tr id="row45607220"><th class="cellrowborder" valign="top" width="22%" id="mcps1.2.5.1.1"><p id="p5260151013341"><a name="p5260151013341"></a><a name="p5260151013341"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.09%" id="mcps1.2.5.1.2"><p id="p1226017106348"><a name="p1226017106348"></a><a name="p1226017106348"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="15.909999999999998%" id="mcps1.2.5.1.3"><p id="p226013107341"><a name="p226013107341"></a><a name="p226013107341"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48%" id="mcps1.2.5.1.4"><p id="p526021019349"><a name="p526021019349"></a><a name="p526021019349"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row11285618104313"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p1737951110318"><a name="p1737951110318"></a><a name="p1737951110318"></a>user_data</p>
</td>
<td class="cellrowborder" valign="top" width="14.09%" headers="mcps1.2.5.1.2 "><p id="p39934810104313"><a name="p39934810104313"></a><a name="p39934810104313"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="15.909999999999998%" headers="mcps1.2.5.1.3 "><p id="p13494158104313"><a name="p13494158104313"></a><a name="p13494158104313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48%" headers="mcps1.2.5.1.4 "><p id="p124835165514"><a name="p124835165514"></a><a name="p124835165514"></a>创建<span id="text86731033192216"><a name="text86731033192216"></a><a name="text86731033192216"></a>云服务器</span>过程中待注入实例自定义数据。支持注入文本、文本文件。</p>
<div class="note" id="note1076765671813"><a name="note1076765671813"></a><a name="note1076765671813"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul749201611912"></a><a name="ul749201611912"></a><ul id="ul749201611912"><li>user_data的值为base64编码之后的内容。</li><li>注入内容（编码之前的内容）最大长度为32K。</li></ul>
</div></div>
<p id="p10685165919553"><a name="p10685165919553"></a><a name="p10685165919553"></a>了解更多实例自定义数据注入请参考<a href="https://support.huaweicloud.com/usermanual-ecs/zh-cn_topic_0032380449.html" target="_blank" rel="noopener noreferrer">用户数据注入</a>。</p>
<p id="p1633783620117"><a name="p1633783620117"></a><a name="p1633783620117"></a>示例：</p>
<p id="p12545313524"><a name="p12545313524"></a><a name="p12545313524"></a>base64编码前：</p>
<a name="ul13541314520"></a><a name="ul13541314520"></a><ul id="ul13541314520"><li>Linux服务器：<pre class="screen" id="screen16541531125220"><a name="screen16541531125220"></a><a name="screen16541531125220"></a>#! /bin/bash
echo user_test &gt;&gt; /home/user.txt</pre>
</li><li>Windows服务器：<pre class="screen" id="screen35418316520"><a name="screen35418316520"></a><a name="screen35418316520"></a>rem cmd
echo 111 &gt; c:\aaa.txt</pre>
</li></ul>
<p id="p16762152318318"><a name="p16762152318318"></a><a name="p16762152318318"></a>base64编码后：</p>
<a name="ul2069415489311"></a><a name="ul2069415489311"></a><ul id="ul2069415489311"><li>Linux服务器：<pre class="screen" id="screen1769415480317"><a name="screen1769415480317"></a><a name="screen1769415480317"></a>IyEgL2Jpbi9iYXNoDQplY2hvIHVzZXJfdGVzdCAmZ3Q7Jmd0OyAvaG9tZS91c2VyLnR4dA==</pre>
</li><li>Windows服务器：<pre class="screen" id="screen1969444873114"><a name="screen1969444873114"></a><a name="screen1969444873114"></a>cmVtIGNtZA0KZWNobyAxMTEgJmd0OyBjOlxhYWEudHh0</pre>
</li></ul>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section46136113"></a>

请参考[响应（任务类）](响应（任务类）.md)。

## 请求示例<a name="section6230163813416"></a>

-   请求URL示例

    ```
    POST https://{endpoint}/v2/{project_id}/cloudservers/{server_id}/changeos
    ```


-   请求示例1（使用密码方式远程登录重装后的系统）

    ```
    {
        "os-change": {
            "adminpass": "1qazXSW@", 
            "userid": "7e25b1da389f4697a79df3a0e5bd494e", 
            "imageid": "e215580f-73ad-429d-b6f2-5433947433b0",
            "mode": "withStopServer"
        }
    }
    ```


-   请求示例2（使用密钥方式远程登录重装后的系统）

    ```
    {
        "os-change": {
            "keyname": "KeyPair-350b", 
            "userid": "7e25b1da389f4697a79df3a0e5bd494e", 
            "imageid": "e215580f-73ad-429d-b6f2-5433947433b0"
        }
    }
    ```


## 响应示例<a name="section449243013451"></a>

请参考[响应（任务类）](响应（任务类）.md)。

## 返回值<a name="section27037160"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码](错误码.md)。

