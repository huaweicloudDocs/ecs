# 修改云服务器指定Key的元数据<a name="ZH-CN_TOPIC_0025567413"></a>

## 功能介绍<a name="section19950704192629"></a>

设置云服务器指定key的元数据。

-   如果元数据中没有待更新字段，则自动添加该字段。
-   如果元数据中已存在待更新字段，则直接更新字段值。

## 接口约束<a name="section178513519245"></a>

云服务器状态（云服务器的OS-EXT-STS:vm\_state属性）必须是active，stopped，paused或者suspended。

## URI<a name="section48549151192629"></a>

PUT /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata/\{key\}

参数说明请参见[表1](#table258804192629)。

**表 1**  参数说明

<a name="table258804192629"></a>
<table><thead align="left"><tr id="row33277594192629"><th class="cellrowborder" valign="top" width="19.99%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.67%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="61.339999999999996%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row56232837192629"><td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.1 "><p id="p58565959192629"><a name="p58565959192629"></a><a name="p58565959192629"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.67%" headers="mcps1.2.4.1.2 "><p id="p46222262192629"><a name="p46222262192629"></a><a name="p46222262192629"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="61.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row7379590192629"><td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.1 "><p id="p60875907192629"><a name="p60875907192629"></a><a name="p60875907192629"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.67%" headers="mcps1.2.4.1.2 "><p id="p32001416192629"><a name="p32001416192629"></a><a name="p32001416192629"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="61.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p41977918192629"><a name="p41977918192629"></a><a name="p41977918192629"></a><span id="text1435123855218"><a name="text1435123855218"></a><a name="text1435123855218"></a>云服务器</span>ID。</p>
</td>
</tr>
<tr id="row1185148119279"><td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.1 "><p id="p2044590819279"><a name="p2044590819279"></a><a name="p2044590819279"></a>key</p>
</td>
<td class="cellrowborder" valign="top" width="18.67%" headers="mcps1.2.4.1.2 "><p id="p4550582719279"><a name="p4550582719279"></a><a name="p4550582719279"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="61.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p6209335919279"><a name="p6209335919279"></a><a name="p6209335919279"></a>待修改的<span id="text2603338175211"><a name="text2603338175211"></a><a name="text2603338175211"></a>云服务器</span>metadata键值。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section42256947192629"></a>

请求参数如[表2](#table21113531192629)所示。

**表 2**  请求参数

<a name="table21113531192629"></a>
<table><thead align="left"><tr id="row12974012192629"><th class="cellrowborder" valign="top" width="15.229999999999999%" id="mcps1.2.5.1.1"><p id="p44262053192629"><a name="p44262053192629"></a><a name="p44262053192629"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.29%" id="mcps1.2.5.1.2"><p id="p28456575192629"><a name="p28456575192629"></a><a name="p28456575192629"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="24.060000000000002%" id="mcps1.2.5.1.3"><p id="p23281266192629"><a name="p23281266192629"></a><a name="p23281266192629"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.419999999999995%" id="mcps1.2.5.1.4"><p id="p6734373192629"><a name="p6734373192629"></a><a name="p6734373192629"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row8613312192629"><td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.1 "><p id="p26589676192629"><a name="p26589676192629"></a><a name="p26589676192629"></a>meta</p>
</td>
<td class="cellrowborder" valign="top" width="17.29%" headers="mcps1.2.5.1.2 "><p id="p6280144192629"><a name="p6280144192629"></a><a name="p6280144192629"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="24.060000000000002%" headers="mcps1.2.5.1.3 "><p id="p38929685192629"><a name="p38929685192629"></a><a name="p38929685192629"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="43.419999999999995%" headers="mcps1.2.5.1.4 "><p id="p59800316192629"><a name="p59800316192629"></a><a name="p59800316192629"></a>用户自定义metadata键值对。</p>
<p id="p19894192011457"><a name="p19894192011457"></a><a name="p19894192011457"></a>键。</p>
<p id="p131921502154"><a name="p131921502154"></a><a name="p131921502154"></a>最大长度255个Unicode字符，不能为空。可以为大写字母（A-Z）、小写字母（a-z）、数字（0-9）、中划线（-）、下划线（_）、冒号（:）和小数点（.）。</p>
<p id="p999582373317"><a name="p999582373317"></a><a name="p999582373317"></a>值。</p>
<p id="p186075811515"><a name="p186075811515"></a><a name="p186075811515"></a>最大长度为255个Unicode字符。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section12391939192629"></a>

响应参数如[表3](#table34681280192629)所示。

**表 3**  响应参数

<a name="table34681280192629"></a>
<table><thead align="left"><tr id="row7754416192629"><th class="cellrowborder" valign="top" width="21.93%" id="mcps1.2.4.1.1"><p id="p24127969192629"><a name="p24127969192629"></a><a name="p24127969192629"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="27.189999999999998%" id="mcps1.2.4.1.2"><p id="p8208474192629"><a name="p8208474192629"></a><a name="p8208474192629"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.88%" id="mcps1.2.4.1.3"><p id="p60906692192629"><a name="p60906692192629"></a><a name="p60906692192629"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row34495047192629"><td class="cellrowborder" valign="top" width="21.93%" headers="mcps1.2.4.1.1 "><p id="p42635402192629"><a name="p42635402192629"></a><a name="p42635402192629"></a>meta</p>
</td>
<td class="cellrowborder" valign="top" width="27.189999999999998%" headers="mcps1.2.4.1.2 "><p id="p30915509192629"><a name="p30915509192629"></a><a name="p30915509192629"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.3 "><p id="p55937021192629"><a name="p55937021192629"></a><a name="p55937021192629"></a>用户自定义metadata键值对。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section1854919457276"></a>

```
PUT https://{endpoint}/v2.1/{project_id}/servers/{server_id}/metadata/{key}
```

```
{
    "meta":{
        "key":"value"
    }
} 
```

## 响应示例<a name="section06122457441"></a>

```
{
    "meta":{
        "key":"value"
    }
} 
```

## 返回值<a name="section38207615192629"></a>

请参考[通用请求返回值](通用请求返回值.md)。

