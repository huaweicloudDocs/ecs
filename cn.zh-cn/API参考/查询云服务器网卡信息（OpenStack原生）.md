# 查询云服务器网卡信息<a name="ecs_03_0801"></a>

## 功能介绍<a name="section36073588"></a>

查询云服务器网卡信息。

## URI<a name="section56226836"></a>

GET /v2.1/\{project\_id\}/servers/\{server\_id\}/os-interface

参数说明请参见[表1](#table38523909)。

**表 1**  参数说明

<a name="table38523909"></a>
<table><thead align="left"><tr id="row15247616"><th class="cellrowborder" valign="top" width="21.12%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25.06%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="53.82%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row23712525"><td class="cellrowborder" valign="top" width="21.12%" headers="mcps1.2.4.1.1 "><p id="p41666396"><a name="p41666396"></a><a name="p41666396"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.4.1.2 "><p id="p19534911"><a name="p19534911"></a><a name="p19534911"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="53.82%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row45459464114812"><td class="cellrowborder" valign="top" width="21.12%" headers="mcps1.2.4.1.1 "><p id="p6481999114812"><a name="p6481999114812"></a><a name="p6481999114812"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.4.1.2 "><p id="p55279920114812"><a name="p55279920114812"></a><a name="p55279920114812"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="53.82%" headers="mcps1.2.4.1.3 "><p id="p48488537114812"><a name="p48488537114812"></a><a name="p48488537114812"></a><span id="text129311722194914"><a name="text129311722194914"></a><a name="text129311722194914"></a>云服务器</span>ID</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section36279478"></a>

无

## 响应消息<a name="section58079852"></a>

响应参数如[表2](#table25276401)所示。

**表 2**  响应参数

<a name="table25276401"></a>
<table><thead align="left"><tr id="row30840926"><th class="cellrowborder" valign="top" width="32.46%" id="mcps1.2.4.1.1"><p id="p137113478283"><a name="p137113478283"></a><a name="p137113478283"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.2%" id="mcps1.2.4.1.2"><p id="p748676"><a name="p748676"></a><a name="p748676"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="37.34%" id="mcps1.2.4.1.3"><p id="p60642794"><a name="p60642794"></a><a name="p60642794"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row13119252"><td class="cellrowborder" valign="top" width="32.46%" headers="mcps1.2.4.1.1 "><p id="p56026474"><a name="p56026474"></a><a name="p56026474"></a>interfaceAttachments</p>
</td>
<td class="cellrowborder" valign="top" width="30.2%" headers="mcps1.2.4.1.2 "><p id="p34453949"><a name="p34453949"></a><a name="p34453949"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="37.34%" headers="mcps1.2.4.1.3 "><p id="p18214233"><a name="p18214233"></a><a name="p18214233"></a><span id="text0692122316499"><a name="text0692122316499"></a><a name="text0692122316499"></a>云服务器</span>网卡信息列表，详情请参见<a href="#table49805933">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  interfaceAttachments字段数据结构说明

<a name="table49805933"></a>
<table><thead align="left"><tr id="row9026257"><th class="cellrowborder" valign="top" width="25.81741825817418%" id="mcps1.2.4.1.1"><p id="p0275155662814"><a name="p0275155662814"></a><a name="p0275155662814"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.947005299470053%" id="mcps1.2.4.1.2"><p id="p15275145672813"><a name="p15275145672813"></a><a name="p15275145672813"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.235576442355764%" id="mcps1.2.4.1.3"><p id="p182751256102814"><a name="p182751256102814"></a><a name="p182751256102814"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row10727144"><td class="cellrowborder" valign="top" width="25.81741825817418%" headers="mcps1.2.4.1.1 "><p id="p63592346"><a name="p63592346"></a><a name="p63592346"></a>port_state</p>
</td>
<td class="cellrowborder" valign="top" width="29.947005299470053%" headers="mcps1.2.4.1.2 "><p id="p13579756"><a name="p13579756"></a><a name="p13579756"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.235576442355764%" headers="mcps1.2.4.1.3 "><p id="p34639550"><a name="p34639550"></a><a name="p34639550"></a>网卡端口状态。</p>
</td>
</tr>
<tr id="row43320496"><td class="cellrowborder" valign="top" width="25.81741825817418%" headers="mcps1.2.4.1.1 "><p id="p19299281"><a name="p19299281"></a><a name="p19299281"></a>fixed_ips</p>
</td>
<td class="cellrowborder" valign="top" width="29.947005299470053%" headers="mcps1.2.4.1.2 "><p id="p55265559"><a name="p55265559"></a><a name="p55265559"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="44.235576442355764%" headers="mcps1.2.4.1.3 "><p id="p23274750"><a name="p23274750"></a><a name="p23274750"></a>网卡私网IP信息列表，详情请参见<a href="#table19750463">表4</a>。</p>
</td>
</tr>
<tr id="row8146160"><td class="cellrowborder" valign="top" width="25.81741825817418%" headers="mcps1.2.4.1.1 "><p id="p55859239"><a name="p55859239"></a><a name="p55859239"></a>net_id</p>
</td>
<td class="cellrowborder" valign="top" width="29.947005299470053%" headers="mcps1.2.4.1.2 "><p id="p10966323"><a name="p10966323"></a><a name="p10966323"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.235576442355764%" headers="mcps1.2.4.1.3 "><p id="p8495130"><a name="p8495130"></a><a name="p8495130"></a>网卡端口所属网络ID（network_id）。</p>
</td>
</tr>
<tr id="row9347313"><td class="cellrowborder" valign="top" width="25.81741825817418%" headers="mcps1.2.4.1.1 "><p id="p18934887"><a name="p18934887"></a><a name="p18934887"></a>port_id</p>
</td>
<td class="cellrowborder" valign="top" width="29.947005299470053%" headers="mcps1.2.4.1.2 "><p id="p13287175"><a name="p13287175"></a><a name="p13287175"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.235576442355764%" headers="mcps1.2.4.1.3 "><p id="p22674843"><a name="p22674843"></a><a name="p22674843"></a>网卡端口ID。</p>
</td>
</tr>
<tr id="row2747002"><td class="cellrowborder" valign="top" width="25.81741825817418%" headers="mcps1.2.4.1.1 "><p id="p21180630"><a name="p21180630"></a><a name="p21180630"></a>mac_addr</p>
</td>
<td class="cellrowborder" valign="top" width="29.947005299470053%" headers="mcps1.2.4.1.2 "><p id="p50770908"><a name="p50770908"></a><a name="p50770908"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.235576442355764%" headers="mcps1.2.4.1.3 "><p id="p35008393"><a name="p35008393"></a><a name="p35008393"></a>网卡Mac地址信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  fixed\_ips字段数据结构说明

<a name="table19750463"></a>
<table><thead align="left"><tr id="row60761195"><th class="cellrowborder" valign="top" width="25.937406259374065%" id="mcps1.2.4.1.1"><p id="p1495811588288"><a name="p1495811588288"></a><a name="p1495811588288"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.887011298870114%" id="mcps1.2.4.1.2"><p id="p5958105810282"><a name="p5958105810282"></a><a name="p5958105810282"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.17558244175583%" id="mcps1.2.4.1.3"><p id="p1495816587288"><a name="p1495816587288"></a><a name="p1495816587288"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row61624137"><td class="cellrowborder" valign="top" width="25.937406259374065%" headers="mcps1.2.4.1.1 "><p id="p25499238"><a name="p25499238"></a><a name="p25499238"></a>subnet_id</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p65213800"><a name="p65213800"></a><a name="p65213800"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.17558244175583%" headers="mcps1.2.4.1.3 "><p id="p27784979"><a name="p27784979"></a><a name="p27784979"></a>网卡私网IP对应子网信息。</p>
</td>
</tr>
<tr id="row48738220"><td class="cellrowborder" valign="top" width="25.937406259374065%" headers="mcps1.2.4.1.1 "><p id="p55481787"><a name="p55481787"></a><a name="p55481787"></a>ip_address</p>
</td>
<td class="cellrowborder" valign="top" width="29.887011298870114%" headers="mcps1.2.4.1.2 "><p id="p17532027"><a name="p17532027"></a><a name="p17532027"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.17558244175583%" headers="mcps1.2.4.1.3 "><p id="p30163672"><a name="p30163672"></a><a name="p30163672"></a>网卡私网IP信息。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section10941134193415"></a>

```
GET https://{endpoint}/v2.1/{project_id}/servers/{server_id}/os-interface
```

## 响应示例<a name="section1829831018292"></a>

```
{
    "interfaceAttachments": [
        {
            "port_state": "ACTIVE",
            "fixed_ips": [
                {
                    "subnet_id": "f8a6e8f8-c2ec-497c-9f23-da9616de54ef",
                    "ip_address": "192.168.1.3"
                }
            ],
            "net_id": "3cb9bc59-5699-4588-a4b1-b87f96708bc6",
            "port_id": "ce531f90-199f-48c0-816c-13e38010b442",
            "mac_addr": "fa:16:3e:4c:2c:30"
        }
    ]
}
```

## 返回值<a name="section52956621"></a>

请参考[通用请求返回值](通用请求返回值.md)。

