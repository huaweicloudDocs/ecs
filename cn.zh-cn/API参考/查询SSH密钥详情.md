# 查询SSH密钥详情<a name="ZH-CN_TOPIC_0020212677"></a>

## 功能介绍<a name="section62942996"></a>

根据SSH密钥名称查询指定SSH密钥。

## URI<a name="section29616056"></a>

GET /v2.1/\{project\_id\}/os-keypairs/\{keypair\_name\}

参数说明请参见[表1](#table51931981)。

**表 1**  参数说明

<a name="table51931981"></a>
<table><thead align="left"><tr id="row62634432"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="21%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="46%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row22724462"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p28742116"><a name="p28742116"></a><a name="p28742116"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.2 "><p id="p46410096"><a name="p46410096"></a><a name="p46410096"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="46%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row10092597"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p12194051"><a name="p12194051"></a><a name="p12194051"></a>keypair_name</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.4.1.2 "><p id="p48194049"><a name="p48194049"></a><a name="p48194049"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="46%" headers="mcps1.2.4.1.3 "><p id="p11403863"><a name="p11403863"></a><a name="p11403863"></a>密钥名称信息。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section65217919"></a>

无

## 响应消息<a name="section50090360"></a>

响应参数如[表2](#table49096623)所示。

**表 2**  响应参数

<a name="table49096623"></a>
<table><thead align="left"><tr id="row20553506"><th class="cellrowborder" valign="top" width="23.057694230576942%" id="mcps1.2.4.1.1"><p id="p52863116"><a name="p52863116"></a><a name="p52863116"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.76692330766923%" id="mcps1.2.4.1.2"><p id="p16299242"><a name="p16299242"></a><a name="p16299242"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="46.17538246175382%" id="mcps1.2.4.1.3"><p id="p45170224"><a name="p45170224"></a><a name="p45170224"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row31470474"><td class="cellrowborder" valign="top" width="23.057694230576942%" headers="mcps1.2.4.1.1 "><p id="p66080459"><a name="p66080459"></a><a name="p66080459"></a>keypair</p>
</td>
<td class="cellrowborder" valign="top" width="30.76692330766923%" headers="mcps1.2.4.1.2 "><p id="p30630481"><a name="p30630481"></a><a name="p30630481"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="46.17538246175382%" headers="mcps1.2.4.1.3 "><p id="p49478440"><a name="p49478440"></a><a name="p49478440"></a>SSH密钥信息，详情请参见<a href="#table32323009">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  keypair字段数据结构说明

<a name="table32323009"></a>
<table><thead align="left"><tr id="row56122340"><th class="cellrowborder" valign="top" width="23%" id="mcps1.2.4.1.1"><p id="p3579112043319"><a name="p3579112043319"></a><a name="p3579112043319"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="27%" id="mcps1.2.4.1.2"><p id="p1457914201333"><a name="p1457914201333"></a><a name="p1457914201333"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="p8579112033320"><a name="p8579112033320"></a><a name="p8579112033320"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1091845"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.1 "><p id="p21330650"><a name="p21330650"></a><a name="p21330650"></a>public_key</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.4.1.2 "><p id="p28418246"><a name="p28418246"></a><a name="p28418246"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p47371280"><a name="p47371280"></a><a name="p47371280"></a>密钥对应publicKey信息。</p>
</td>
</tr>
<tr id="row23688339"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.1 "><p id="p39707298"><a name="p39707298"></a><a name="p39707298"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.4.1.2 "><p id="p2977371"><a name="p2977371"></a><a name="p2977371"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p23019892"><a name="p23019892"></a><a name="p23019892"></a>密钥名称。</p>
</td>
</tr>
<tr id="row19588278171758"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.1 "><p id="p3411854217180"><a name="p3411854217180"></a><a name="p3411854217180"></a>fingerprint</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.4.1.2 "><p id="p1213855517180"><a name="p1213855517180"></a><a name="p1213855517180"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p5774567417180"><a name="p5774567417180"></a><a name="p5774567417180"></a>密钥对应指纹信息。</p>
</td>
</tr>
<tr id="row5852437"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.1 "><p id="p4285383"><a name="p4285383"></a><a name="p4285383"></a>created_at</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.4.1.2 "><p id="p64894876"><a name="p64894876"></a><a name="p64894876"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p63724816"><a name="p63724816"></a><a name="p63724816"></a>密钥创建时间。</p>
</td>
</tr>
<tr id="row36652435"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.1 "><p id="p16057296"><a name="p16057296"></a><a name="p16057296"></a>deleted</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.4.1.2 "><p id="p58113810"><a name="p58113810"></a><a name="p58113810"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p19274797"><a name="p19274797"></a><a name="p19274797"></a>密钥删除标记。</p>
<a name="ul1594190135612"></a><a name="ul1594190135612"></a><ul id="ul1594190135612"><li>true，表示密钥已被删除。</li><li>false，表示密钥未被删除。</li></ul>
</td>
</tr>
<tr id="row39255446"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.1 "><p id="p25574597"><a name="p25574597"></a><a name="p25574597"></a>deleted_at</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.4.1.2 "><p id="p22776773"><a name="p22776773"></a><a name="p22776773"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p28378258"><a name="p28378258"></a><a name="p28378258"></a>密钥删除时间。</p>
</td>
</tr>
<tr id="row54077734"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.1 "><p id="p18220335"><a name="p18220335"></a><a name="p18220335"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.4.1.2 "><p id="p22737212"><a name="p22737212"></a><a name="p22737212"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p66647176"><a name="p66647176"></a><a name="p66647176"></a>密钥ID。</p>
</td>
</tr>
<tr id="row62953674"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.1 "><p id="p66082838"><a name="p66082838"></a><a name="p66082838"></a>updated_at</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.4.1.2 "><p id="p46241663"><a name="p46241663"></a><a name="p46241663"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p21523158"><a name="p21523158"></a><a name="p21523158"></a>密钥更新时间。</p>
</td>
</tr>
<tr id="row59490699"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.1 "><p id="p54017281"><a name="p54017281"></a><a name="p54017281"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.4.1.2 "><p id="p5473047"><a name="p5473047"></a><a name="p5473047"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p30428869"><a name="p30428869"></a><a name="p30428869"></a>密钥所属用户信息。</p>
</td>
</tr>
<tr id="row462920453538"><td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.1 "><p id="p199751011803"><a name="p199751011803"></a><a name="p199751011803"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="27%" headers="mcps1.2.4.1.2 "><p id="p139751111204"><a name="p139751111204"></a><a name="p139751111204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p1097512112013"><a name="p1097512112013"></a><a name="p1097512112013"></a>密钥类型，默认“ssh”</p>
<p id="p144811212011"><a name="p144811212011"></a><a name="p144811212011"></a>微版本2.2以上支持</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section4978145455016"></a>

```
GET https://{endpoint}/v2.1/{project_id}/os-keypairs/{keypair_name}
```

## 响应示例<a name="section13613112651113"></a>

```
{
    "keypair": {
        "created_at": "2014-05-07T12:06:13.681238",
        "deleted": false,
        "deleted_at": null,
        "fingerprint": "9d:00:f4:d7:26:6e:52:06:4c:c1:d3:1d:fd:06:66:01",
        "id": 1,
        "name": "keypair-3582d8b7-e588-4aad-b7f7-f4e76f0e4314",
        "public_key": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDYJrTVpcMwFqQy/oMvtUSRofZdSRHEwrsX8AYkRvn2ZnCXM+b6+GZ2NQuuWj+ocznlnwiGFQDsL/yeE+/kurqcPJFKKp60mToXIMyzioFxW88fJtwEWawHKAclbHWpR1t4fQ4DS+/sIbX/Yd9btlVQ2tpQjodGDbM9Tr9/+/3i6rcR+EoLqmbgCgAiGiVV6VbM2Zx79yUwd+GnQejHX8BlYZoOjCnt3NREsITcmWE9FVFy6TnLmahs3FkEO/QGgWGkaohAJlsgaVvSWGgDn2AujKYwyDokK3dXyeX3m2Vmc3ejiqPa/C4nRrCOlko5nSgV/9IXRx1ERImsqZnE9usB Generated-by-Nova\n",
        "updated_at": null,
        "user_id": "fake"
    }
}
```

## 返回值<a name="section48160062"></a>

请参考[通用请求返回值](通用请求返回值.md)。

