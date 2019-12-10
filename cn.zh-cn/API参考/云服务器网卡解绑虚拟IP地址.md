# 云服务器网卡解绑虚拟IP地址<a name="ZH-CN_TOPIC_0077846077"></a>

## 功能介绍<a name="section10723444"></a>

虚拟IP地址用于为网卡提供第二个IP地址，同时支持与多个弹性云服务器的网卡绑定，从而实现多个弹性云服务器之间的高可用性。

该接口用于解绑定弹性云服务器网卡的虚拟IP地址。解绑后，网卡不会被删除，如需删除云服务器网卡，请参见[批量删除云服务器网卡](批量删除云服务器网卡.md)。

## URI<a name="section29402138"></a>

PUT /v1/\{project\_id\}/cloudservers/nics/\{nic\_id\}

参数说明请参见[表1](#table55925239)。

**表 1**  参数说明

<a name="table55925239"></a>
<table><thead align="left"><tr id="row60011419"><th class="cellrowborder" valign="top" width="23.369999999999997%" id="mcps1.2.4.1.1"><p id="p29086798"><a name="p29086798"></a><a name="p29086798"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.48%" id="mcps1.2.4.1.2"><p id="p7220417"><a name="p7220417"></a><a name="p7220417"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="58.15%" id="mcps1.2.4.1.3"><p id="p47982876"><a name="p47982876"></a><a name="p47982876"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row61407752"><td class="cellrowborder" valign="top" width="23.369999999999997%" headers="mcps1.2.4.1.1 "><p id="p7972012"><a name="p7972012"></a><a name="p7972012"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.48%" headers="mcps1.2.4.1.2 "><p id="p41753265"><a name="p41753265"></a><a name="p41753265"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="58.15%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row37815352"><td class="cellrowborder" valign="top" width="23.369999999999997%" headers="mcps1.2.4.1.1 "><p id="p43144677"><a name="p43144677"></a><a name="p43144677"></a>nic_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.48%" headers="mcps1.2.4.1.2 "><p id="p5057967"><a name="p5057967"></a><a name="p5057967"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="58.15%" headers="mcps1.2.4.1.3 "><p id="p7042173"><a name="p7042173"></a><a name="p7042173"></a>云服务器网卡ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section63292653"></a>

请求参数如[表2](#table21989419)所示。

**表 2**  请求参数

<a name="table21989419"></a>
<table><thead align="left"><tr id="row20106686"><th class="cellrowborder" valign="top" width="25.192519251925194%" id="mcps1.2.5.1.1"><p id="p19325759"><a name="p19325759"></a><a name="p19325759"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.471447144714473%" id="mcps1.2.5.1.2"><p id="p21882681"><a name="p21882681"></a><a name="p21882681"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="24.62246224622462%" id="mcps1.2.5.1.3"><p id="p27666764"><a name="p27666764"></a><a name="p27666764"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="35.713571357135706%" id="mcps1.2.5.1.4"><p id="p26415391"><a name="p26415391"></a><a name="p26415391"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row52301286"><td class="cellrowborder" valign="top" width="25.192519251925194%" headers="mcps1.2.5.1.1 "><p id="p8545767"><a name="p8545767"></a><a name="p8545767"></a>nic</p>
</td>
<td class="cellrowborder" valign="top" width="14.471447144714473%" headers="mcps1.2.5.1.2 "><p id="p21118492"><a name="p21118492"></a><a name="p21118492"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="24.62246224622462%" headers="mcps1.2.5.1.3 "><p id="p32876269"><a name="p32876269"></a><a name="p32876269"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="35.713571357135706%" headers="mcps1.2.5.1.4 "><p id="p8936292"><a name="p8936292"></a><a name="p8936292"></a>需要解绑虚拟IP的网卡参数列表。更多信息请参见<a href="#table44975500">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  nic字段数据结构说明

<a name="table44975500"></a>
<table><thead align="left"><tr id="row35373287"><th class="cellrowborder" valign="top" width="18.990000000000002%" id="mcps1.2.5.1.1"><p id="p141945507518"><a name="p141945507518"></a><a name="p141945507518"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.099999999999998%" id="mcps1.2.5.1.2"><p id="p219415011510"><a name="p219415011510"></a><a name="p219415011510"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="26.69%" id="mcps1.2.5.1.3"><p id="p219414500510"><a name="p219414500510"></a><a name="p219414500510"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40.22%" id="mcps1.2.5.1.4"><p id="p31944501053"><a name="p31944501053"></a><a name="p31944501053"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row19920592"><td class="cellrowborder" valign="top" width="18.990000000000002%" headers="mcps1.2.5.1.1 "><p id="p4735204513"><a name="p4735204513"></a><a name="p4735204513"></a>subnet_id</p>
</td>
<td class="cellrowborder" valign="top" width="14.099999999999998%" headers="mcps1.2.5.1.2 "><p id="p20009535204513"><a name="p20009535204513"></a><a name="p20009535204513"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="p50225666204513"><a name="p50225666204513"></a><a name="p50225666204513"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40.22%" headers="mcps1.2.5.1.4 "><p id="p52170790174229"><a name="p52170790174229"></a><a name="p52170790174229"></a>云服务器添加网卡的信息。</p>
<p id="p60897809205048"><a name="p60897809205048"></a><a name="p60897809205048"></a>约束：解绑虚拟IP时，subnet_id为空字符串</p>
</td>
</tr>
<tr id="row65287294"><td class="cellrowborder" valign="top" width="18.990000000000002%" headers="mcps1.2.5.1.1 "><p id="p63725211204513"><a name="p63725211204513"></a><a name="p63725211204513"></a>ip_address</p>
</td>
<td class="cellrowborder" valign="top" width="14.099999999999998%" headers="mcps1.2.5.1.2 "><p id="p65363500204513"><a name="p65363500204513"></a><a name="p65363500204513"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="p7812801204513"><a name="p7812801204513"></a><a name="p7812801204513"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40.22%" headers="mcps1.2.5.1.4 "><p id="p58632794204513"><a name="p58632794204513"></a><a name="p58632794204513"></a>网卡即将配置的虚拟IP的地址。</p>
<p id="p5068839620513"><a name="p5068839620513"></a><a name="p5068839620513"></a>约束：解绑虚拟IP时，ip_address为空字符串</p>
</td>
</tr>
<tr id="row6769295"><td class="cellrowborder" valign="top" width="18.990000000000002%" headers="mcps1.2.5.1.1 "><p id="p64501959204513"><a name="p64501959204513"></a><a name="p64501959204513"></a>reverse_binding</p>
</td>
<td class="cellrowborder" valign="top" width="14.099999999999998%" headers="mcps1.2.5.1.2 "><p id="p58790058204513"><a name="p58790058204513"></a><a name="p58790058204513"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="p18090641204513"><a name="p18090641204513"></a><a name="p18090641204513"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="40.22%" headers="mcps1.2.5.1.4 "><p id="p63072380204513"><a name="p63072380204513"></a><a name="p63072380204513"></a>虚拟IP的allowed_address_pairs属性是否添加网卡的IP/Mac对。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section32762966"></a>

响应参数如[表4](#table54154414204821)所示。

**表 4**  响应参数

<a name="table54154414204821"></a>
<table><thead align="left"><tr id="row60076110204821"><th class="cellrowborder" valign="top" width="30.64%" id="mcps1.2.4.1.1"><p id="p21494305"><a name="p21494305"></a><a name="p21494305"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.76%" id="mcps1.2.4.1.2"><p id="p673716201611"><a name="p673716201611"></a><a name="p673716201611"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40.6%" id="mcps1.2.4.1.3"><p id="p28416672"><a name="p28416672"></a><a name="p28416672"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row9009218204821"><td class="cellrowborder" valign="top" width="30.64%" headers="mcps1.2.4.1.1 "><p id="p15842885204821"><a name="p15842885204821"></a><a name="p15842885204821"></a>port_id</p>
</td>
<td class="cellrowborder" valign="top" width="28.76%" headers="mcps1.2.4.1.2 "><p id="p28653632204821"><a name="p28653632204821"></a><a name="p28653632204821"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40.6%" headers="mcps1.2.4.1.3 "><p id="p64315455204821"><a name="p64315455204821"></a><a name="p64315455204821"></a>云服务器网卡ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section157005917910"></a>

```
PUT https://{endpoint}/v1/{project_id}/cloudservers/nics/{nic_id}
```

```
{
    "nic": { 
           "subnet_id": "",
           "ip_address": "",
           "reverse_binding": false
    }
}
```

## 响应示例<a name="section3608142813812"></a>

```
{
   "port_id": "d32019d3-bc6e-4319-9c1d-6722fc136a23"
}
```

## 返回值<a name="section26431238"></a>

请参考[通用请求返回值](通用请求返回值.md)。

## 错误码<a name="section85821649202813"></a>

请参考[错误码说明](错误码说明.md)。

