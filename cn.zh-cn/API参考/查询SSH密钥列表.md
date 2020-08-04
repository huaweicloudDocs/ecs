# 查询SSH密钥列表<a name="ZH-CN_TOPIC_0020212676"></a>

## 功能介绍<a name="section66325402"></a>

查询SSH密钥信息列表。

## URI<a name="section60057706"></a>

GET /v2.1/\{project\_id\}/os-keypairs

参数说明请参见[表1](#table38623499)。

**表 1**  参数说明

<a name="table38623499"></a>
<table><thead align="left"><tr id="row59671974"><th class="cellrowborder" valign="top" width="23.93%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.8%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="56.269999999999996%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row53887795"><td class="cellrowborder" valign="top" width="23.93%" headers="mcps1.2.4.1.1 "><p id="p2835298"><a name="p2835298"></a><a name="p2835298"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.8%" headers="mcps1.2.4.1.2 "><p id="p28332581"><a name="p28332581"></a><a name="p28332581"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="56.269999999999996%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section3648444"></a>

无

## 响应消息<a name="section32836002"></a>

响应参数如[表2](#table46959463)所示。

**表 2**  响应参数

<a name="table46959463"></a>
<table><thead align="left"><tr id="row9766180"><th class="cellrowborder" valign="top" width="24.122412241224122%" id="mcps1.2.4.1.1"><p id="p52863116"><a name="p52863116"></a><a name="p52863116"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="31.453145314531454%" id="mcps1.2.4.1.2"><p id="p16299242"><a name="p16299242"></a><a name="p16299242"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.42444244424442%" id="mcps1.2.4.1.3"><p id="p45170224"><a name="p45170224"></a><a name="p45170224"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row34909498"><td class="cellrowborder" valign="top" width="24.122412241224122%" headers="mcps1.2.4.1.1 "><p id="p9097072"><a name="p9097072"></a><a name="p9097072"></a>keypairs</p>
</td>
<td class="cellrowborder" valign="top" width="31.453145314531454%" headers="mcps1.2.4.1.2 "><p id="p26115459"><a name="p26115459"></a><a name="p26115459"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="44.42444244424442%" headers="mcps1.2.4.1.3 "><p id="p46361647"><a name="p46361647"></a><a name="p46361647"></a>密钥信息列表，详情请参见<a href="#table41882197">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  keypairs字段数据结构说明

<a name="table41882197"></a>
<table><thead align="left"><tr id="row19241577"><th class="cellrowborder" valign="top" width="23.932393239323932%" id="mcps1.2.4.1.1"><p id="p564410811336"><a name="p564410811336"></a><a name="p564410811336"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="31.83318331833183%" id="mcps1.2.4.1.2"><p id="p2064412853319"><a name="p2064412853319"></a><a name="p2064412853319"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.23442344234424%" id="mcps1.2.4.1.3"><p id="p166444810334"><a name="p166444810334"></a><a name="p166444810334"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row34772456"><td class="cellrowborder" valign="top" width="23.932393239323932%" headers="mcps1.2.4.1.1 "><p id="p65105571"><a name="p65105571"></a><a name="p65105571"></a>keypair</p>
</td>
<td class="cellrowborder" valign="top" width="31.83318331833183%" headers="mcps1.2.4.1.2 "><p id="p9736186"><a name="p9736186"></a><a name="p9736186"></a>Obejct</p>
</td>
<td class="cellrowborder" valign="top" width="44.23442344234424%" headers="mcps1.2.4.1.3 "><p id="p51249570"><a name="p51249570"></a><a name="p51249570"></a>密钥信息详情，详情请参见<a href="#table48408329">表4</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  keypair字段数据结构说明

<a name="table48408329"></a>
<table><thead align="left"><tr id="row27259828"><th class="cellrowborder" valign="top" width="23.93%" id="mcps1.2.4.1.1"><p id="p956121163317"><a name="p956121163317"></a><a name="p956121163317"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="32.019999999999996%" id="mcps1.2.4.1.2"><p id="p656110113337"><a name="p656110113337"></a><a name="p656110113337"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.05%" id="mcps1.2.4.1.3"><p id="p1256131103312"><a name="p1256131103312"></a><a name="p1256131103312"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row37982174"><td class="cellrowborder" valign="top" width="23.93%" headers="mcps1.2.4.1.1 "><p id="p56657239"><a name="p56657239"></a><a name="p56657239"></a>fingerprint</p>
</td>
<td class="cellrowborder" valign="top" width="32.019999999999996%" headers="mcps1.2.4.1.2 "><p id="p12150471"><a name="p12150471"></a><a name="p12150471"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.05%" headers="mcps1.2.4.1.3 "><p id="p66432381"><a name="p66432381"></a><a name="p66432381"></a>密钥对应指纹信息。</p>
</td>
</tr>
<tr id="row61020521"><td class="cellrowborder" valign="top" width="23.93%" headers="mcps1.2.4.1.1 "><p id="p43715136"><a name="p43715136"></a><a name="p43715136"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="32.019999999999996%" headers="mcps1.2.4.1.2 "><p id="p58836357"><a name="p58836357"></a><a name="p58836357"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.05%" headers="mcps1.2.4.1.3 "><p id="p9140568"><a name="p9140568"></a><a name="p9140568"></a>密钥名称。</p>
</td>
</tr>
<tr id="row199744112018"><td class="cellrowborder" valign="top" width="23.93%" headers="mcps1.2.4.1.1 "><p id="p199751011803"><a name="p199751011803"></a><a name="p199751011803"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="32.019999999999996%" headers="mcps1.2.4.1.2 "><p id="p139751111204"><a name="p139751111204"></a><a name="p139751111204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.05%" headers="mcps1.2.4.1.3 "><p id="p1097512112013"><a name="p1097512112013"></a><a name="p1097512112013"></a>密钥类型，默认“ssh”</p>
<p id="p144811212011"><a name="p144811212011"></a><a name="p144811212011"></a>微版本2.2以上支持</p>
</td>
</tr>
<tr id="row15156252"><td class="cellrowborder" valign="top" width="23.93%" headers="mcps1.2.4.1.1 "><p id="p19696890"><a name="p19696890"></a><a name="p19696890"></a>public_key</p>
</td>
<td class="cellrowborder" valign="top" width="32.019999999999996%" headers="mcps1.2.4.1.2 "><p id="p46735588"><a name="p46735588"></a><a name="p46735588"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.05%" headers="mcps1.2.4.1.3 "><p id="p46049856"><a name="p46049856"></a><a name="p46049856"></a>密钥对应publicKey信息。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section13755153085015"></a>

```
GET https://{endpoint}/v2.1/{project_id}/os-keypairs
```

## 响应示例<a name="section4713102134415"></a>

```
{
    "keypairs": [
        {
            "keypair": {
                "fingerprint": "15:b0:f8:b3:f9:48:63:71:cf:7b:5b:38:6d:44:2d:4a",
                "name": "keypair-601a2305-4f25-41ed-89c6-2a966fc8027a",
                "type": "ssh",
                "public_key": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQC+Eo/RZRngaGTkFs7I62ZjsIlO79KklKbMXi8F+KITD4bVQHHn+kV+4gRgkgCRbdoDqoGfpaDFs877DYX9n4z6FrAIZ4PES8TNKhatifpn9NdQYWA+IkU8CuvlEKGuFpKRi/k7JLos/gHi2hy7QUwgtRvcefvD/vgQZOVw/mGR9Q== Generated-by-Nova\n"
            }
        }
    ]
}
```

## 返回值<a name="section27088563"></a>

请参考[通用请求返回值](通用请求返回值.md)。

