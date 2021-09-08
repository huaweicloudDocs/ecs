# 重装弹性云服务器操作系统（安装Cloud-init）<a name="ZH-CN_TOPIC_0067876349"></a>

## 功能介绍<a name="section61372619"></a>

重装弹性云服务器的操作系统。支持弹性云服务器数据盘不变的情况下，使用原镜像重装系统盘。

调用该接口后，系统将卸载系统盘，然后使用原镜像重新创建系统盘，并挂载至弹性云服务器，实现重装操作系统功能。

## 接口约束<a name="section2842257210401"></a>

-   该接口仅支持安装Cloud-init或Cloudbase-init的镜像。如果镜像未安装Cloud-init或者Cloudbase-init，请使用  [重装弹性云服务器操作系统（未安装Cloud-init）](重装弹性云服务器操作系统（未安装Cloud-init）.md)接口。
-   不包含系统盘的弹性云服务器不能执行重装操作。
-   执行重装操作系统任务时，请勿并行执行其他任务，否则可能会引起重装操作系统失败。

## URI<a name="section15482662"></a>

POST /v2/\{project\_id\}/cloudservers/\{server\_id\}/reinstallos

参数说明请参见[表1](#table55945983)。

**表 1**  参数说明

<a name="table55945983"></a>
<table><thead align="left"><tr id="row11302482"><th class="cellrowborder" valign="top" width="31.979999999999997%" id="mcps1.2.4.1.1"><p id="p43085863"><a name="p43085863"></a><a name="p43085863"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25.290000000000003%" id="mcps1.2.4.1.2"><p id="p294000"><a name="p294000"></a><a name="p294000"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="42.730000000000004%" id="mcps1.2.4.1.3"><p id="p23814038"><a name="p23814038"></a><a name="p23814038"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row49888896"><td class="cellrowborder" valign="top" width="31.979999999999997%" headers="mcps1.2.4.1.1 "><p id="p14468758"><a name="p14468758"></a><a name="p14468758"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.290000000000003%" headers="mcps1.2.4.1.2 "><p id="p31118786"><a name="p31118786"></a><a name="p31118786"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="42.730000000000004%" headers="mcps1.2.4.1.3 "><p id="p7411459134810"><a name="p7411459134810"></a><a name="p7411459134810"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row613736410235"><td class="cellrowborder" valign="top" width="31.979999999999997%" headers="mcps1.2.4.1.1 "><p id="p2736446410235"><a name="p2736446410235"></a><a name="p2736446410235"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.290000000000003%" headers="mcps1.2.4.1.2 "><p id="p192907210235"><a name="p192907210235"></a><a name="p192907210235"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="42.730000000000004%" headers="mcps1.2.4.1.3 "><p id="p2203711610235"><a name="p2203711610235"></a><a name="p2203711610235"></a><span id="text0617103984716"><a name="text0617103984716"></a><a name="text0617103984716"></a>弹性云服务器</span>ID。</p>
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
<td class="cellrowborder" valign="top" width="42.86000000000001%" headers="mcps1.2.5.1.4 "><p id="p61410719"><a name="p61410719"></a><a name="p61410719"></a>重装<span id="text567344024713"><a name="text567344024713"></a><a name="text567344024713"></a>弹性云服务器</span>，详情参见<a href="#table32200631">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  os-reinstall字段数据结构说明

<a name="table32200631"></a>
<table><thead align="left"><tr id="row47660253"><th class="cellrowborder" valign="top" width="21.67216721672167%" id="mcps1.2.5.1.1"><p id="p17130113293015"><a name="p17130113293015"></a><a name="p17130113293015"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.67136713671367%" id="mcps1.2.5.1.2"><p id="p101301832193010"><a name="p101301832193010"></a><a name="p101301832193010"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.61216121612161%" id="mcps1.2.5.1.3"><p id="p813003213017"><a name="p813003213017"></a><a name="p813003213017"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.04430443044304%" id="mcps1.2.5.1.4"><p id="p19146143273020"><a name="p19146143273020"></a><a name="p19146143273020"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row65851064"><td class="cellrowborder" valign="top" width="21.67216721672167%" headers="mcps1.2.5.1.1 "><p id="p32335967"><a name="p32335967"></a><a name="p32335967"></a>adminpass</p>
</td>
<td class="cellrowborder" valign="top" width="13.67136713671367%" headers="mcps1.2.5.1.2 "><p id="p1967662"><a name="p1967662"></a><a name="p1967662"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p25162958"><a name="p25162958"></a><a name="p25162958"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p16847167112050"><a name="p16847167112050"></a><a name="p16847167112050"></a><span id="text26955862318"><a name="text26955862318"></a><a name="text26955862318"></a>云服务器</span>管理员帐户的初始登录密码。</p>
<p id="p8742832102714"><a name="p8742832102714"></a><a name="p8742832102714"></a>其中，Windows管理员帐户的用户名为Administrator，Linux管理员账户的用户名为root。</p>
<p id="p11576631102714"><a name="p11576631102714"></a><a name="p11576631102714"></a>建议密码复杂度如下：</p>
<a name="ul37080817102714"></a><a name="ul37080817102714"></a><ul id="ul37080817102714"><li>长度为8-26位。</li><li>密码至少必须包含大写字母、小写字母、数字和特殊字符（!@$%^-_=+[{}]:,./?~#*）中的三种。</li></ul>
<div class="note" id="note65349643112129"><a name="note65349643112129"></a><a name="note65349643112129"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul58921915515"></a><a name="ul58921915515"></a><ul id="ul58921915515"><li>对于Windows<span id="text1891219483"><a name="text1891219483"></a><a name="text1891219483"></a>弹性云服务器</span>，密码不能包含用户名或用户名的逆序，不能包含用户名中超过两个连续字符的部分。</li><li>对于Linux弹性云服务器也可使用user_data字段实现密码注入，此时adminpass字段无效。</li><li>adminpass和keyname不能同时有值。</li><li>adminpass和keyname如果同时为空，此时，metadata中的user_data属性必须有值。</li></ul>
</div></div>
</td>
</tr>
<tr id="row45934497"><td class="cellrowborder" valign="top" width="21.67216721672167%" headers="mcps1.2.5.1.1 "><p id="p29706771"><a name="p29706771"></a><a name="p29706771"></a>keyname</p>
</td>
<td class="cellrowborder" valign="top" width="13.67136713671367%" headers="mcps1.2.5.1.2 "><p id="p57438237"><a name="p57438237"></a><a name="p57438237"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p21985640"><a name="p21985640"></a><a name="p21985640"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p36006428"><a name="p36006428"></a><a name="p36006428"></a>密钥名称。</p>
<p id="p12355338417"><a name="p12355338417"></a><a name="p12355338417"></a>密钥可以通过密钥创建接口进行创建 <a href="创建和导入SSH密钥.md">创建和导入SSH密钥</a>（请参见），或使用SSH密钥查询接口查询已有的密钥（请参见<a href="查询SSH密钥列表.md">查询SSH密钥列表</a> ）。</p>
</td>
</tr>
<tr id="row2345411710289"><td class="cellrowborder" valign="top" width="21.67216721672167%" headers="mcps1.2.5.1.1 "><p id="p2073531110289"><a name="p2073531110289"></a><a name="p2073531110289"></a>userid</p>
</td>
<td class="cellrowborder" valign="top" width="13.67136713671367%" headers="mcps1.2.5.1.2 "><p id="p183865010289"><a name="p183865010289"></a><a name="p183865010289"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p1471297410289"><a name="p1471297410289"></a><a name="p1471297410289"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p5090020910289"><a name="p5090020910289"></a><a name="p5090020910289"></a>用户ID。</p>
<div class="p" id="p650419516719"><a name="p650419516719"></a><a name="p650419516719"></a>查看用户ID方法：<a name="ol118119201404"></a><a name="ol118119201404"></a><ol id="ol118119201404"><li>登录管理控制台。</li><li>单击用户名，在下拉列表中单击“我的凭证”。在该页面查看用户ID。</li></ol>
</div>
</td>
</tr>
<tr id="row6144862102847"><td class="cellrowborder" valign="top" width="21.67216721672167%" headers="mcps1.2.5.1.1 "><p id="p27971812102847"><a name="p27971812102847"></a><a name="p27971812102847"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="13.67136713671367%" headers="mcps1.2.5.1.2 "><p id="p51124270102847"><a name="p51124270102847"></a><a name="p51124270102847"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p47425188102847"><a name="p47425188102847"></a><a name="p47425188102847"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p16235056102847"><a name="p16235056102847"></a><a name="p16235056102847"></a>重装<span id="text1199150192410"><a name="text1199150192410"></a><a name="text1199150192410"></a>云服务器</span>的元数据。</p>
<p id="p3830913711291"><a name="p3830913711291"></a><a name="p3830913711291"></a>更多信息，请参见<a href="#table9120223">表4</a>。</p>
</td>
</tr>
<tr id="row7138191515212"><td class="cellrowborder" valign="top" width="21.67216721672167%" headers="mcps1.2.5.1.1 "><p id="p184731425012"><a name="p184731425012"></a><a name="p184731425012"></a>mode</p>
</td>
<td class="cellrowborder" valign="top" width="13.67136713671367%" headers="mcps1.2.5.1.2 "><p id="p440141715114"><a name="p440141715114"></a><a name="p440141715114"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.61216121612161%" headers="mcps1.2.5.1.3 "><p id="p154051718113"><a name="p154051718113"></a><a name="p154051718113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.04430443044304%" headers="mcps1.2.5.1.4 "><p id="p15551537416"><a name="p15551537416"></a><a name="p15551537416"></a>取值为withStopServer ，支持开机状态下重装<span id="text7363162174816"><a name="text7363162174816"></a><a name="text7363162174816"></a>弹性云服务器</span>。</p>
<p id="p15289182385312"><a name="p15289182385312"></a><a name="p15289182385312"></a>mode取值为withStopServer时，对开机状态的</p>
<p id="p122661523155311"><a name="p122661523155311"></a><a name="p122661523155311"></a><span id="text15507203184811"><a name="text15507203184811"></a><a name="text15507203184811"></a>弹性云服务器</span>执行重装操作，系统自动对云服务器先执行关机，再重装操作系统。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  metadata字段数据结构说明

<a name="table9120223"></a>
<table><thead align="left"><tr id="row45607220"><th class="cellrowborder" valign="top" width="21.65%" id="mcps1.2.5.1.1"><p id="p1139016367303"><a name="p1139016367303"></a><a name="p1139016367303"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.73%" id="mcps1.2.5.1.2"><p id="p18390836193011"><a name="p18390836193011"></a><a name="p18390836193011"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.38%" id="mcps1.2.5.1.3"><p id="p6390153618307"><a name="p6390153618307"></a><a name="p6390153618307"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.24%" id="mcps1.2.5.1.4"><p id="p83901436133015"><a name="p83901436133015"></a><a name="p83901436133015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row11285618104313"><td class="cellrowborder" valign="top" width="21.65%" headers="mcps1.2.5.1.1 "><p id="p1737951110318"><a name="p1737951110318"></a><a name="p1737951110318"></a>user_data</p>
</td>
<td class="cellrowborder" valign="top" width="13.73%" headers="mcps1.2.5.1.2 "><p id="p39934810104313"><a name="p39934810104313"></a><a name="p39934810104313"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.38%" headers="mcps1.2.5.1.3 "><p id="p13494158104313"><a name="p13494158104313"></a><a name="p13494158104313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.24%" headers="mcps1.2.5.1.4 "><p id="p4078366294136"><a name="p4078366294136"></a><a name="p4078366294136"></a>创建<span id="text86731033192216"><a name="text86731033192216"></a><a name="text86731033192216"></a>云服务器</span>过程中待注入用户数据。支持注入文本、文本文件。</p>
<div class="note" id="note1076765671813"><a name="note1076765671813"></a><a name="note1076765671813"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul749201611912"></a><a name="ul749201611912"></a><ul id="ul749201611912"><li>user_data的值为base64编码之后的内容。</li><li>注入内容（编码之前的内容）最大长度为32K。</li></ul>
</div></div>
<p id="p10685165919553"><a name="p10685165919553"></a><a name="p10685165919553"></a>了解更多用户数据注入请参考<a href="https://support.huaweicloud.com/usermanual-ecs/zh-cn_topic_0032380449.html" target="_blank" rel="noopener noreferrer">用户数据注入</a>。</p>
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

## 响应参数<a name="section46136113"></a>

请参考[响应（任务类）](响应（任务类）.md)。

## 请求示例<a name="section4722162513312"></a>

-   请求URL示例

    ```
    POST https://{endpoint}/v2/{project_id}/cloudservers/{server_id}/reinstallos
    ```

-   请求示例1（使用密码方式远程登录重装后的系统）

    ```
    {
        "os-reinstall": {
            "adminpass": "!QAZxsw2", 
            "userid": "7e25b1da389f4697a79df3a0e5bd494e",
            "mode": "withStopServer"
        }
    }
    ```


-   请求示例2（使用密钥方式远程登录重装后的系统）

    ```
    {
        "os-reinstall": {
            "keyname": "KeyPair-350b", 
            "userid": "7e25b1da389f4697a79df3a0e5bd494e"
        }
    }
    ```


## 响应示例<a name="section079845214419"></a>

请参考[响应（任务类）](响应（任务类）.md)。

## 返回值<a name="section27037160"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码](错误码.md)。

