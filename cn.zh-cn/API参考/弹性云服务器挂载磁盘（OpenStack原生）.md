# 弹性云服务器挂载磁盘<a name="ZH-CN_TOPIC_0031167350"></a>

## 功能介绍<a name="section53922917165259"></a>

云服务器器挂载磁盘。

弹性云服务器挂载磁盘应用示例请参考[示例4：弹性云服务器挂载磁盘](示例4-弹性云服务器挂载磁盘.md)。

## 接口约束<a name="section64211377173223"></a>

1.  挂载bootable卷必须指定挂载盘符。
2.  由备份创建的磁盘不能挂载为系统盘。
3.  弹性云服务器状态（弹性云服务器的OS-EXT-STS:vm\_state属性）处于SUSPENDED和PAUSED状态下不支持挂卷。
4.  待挂载的云硬盘必须是available状态。
5.  待挂载的云硬盘与云服务器属于同一可用区。
6.  VBD类型的云硬盘不支持挂载到裸金属服务器上。

## URI<a name="section51121191165259"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/os-volume\_attachments

参数说明请参见[表1](#table60562285165259)。

**表 1**  参数说明

<a name="table60562285165259"></a>
<table><thead align="left"><tr id="row4861884165259"><th class="cellrowborder" valign="top" width="25.06%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.04%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="58.9%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row63809876165259"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.4.1.1 "><p id="p1217433165259"><a name="p1217433165259"></a><a name="p1217433165259"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="16.04%" headers="mcps1.2.4.1.2 "><p id="p31503226165259"><a name="p31503226165259"></a><a name="p31503226165259"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="58.9%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row59999756151519"><td class="cellrowborder" valign="top" width="25.06%" headers="mcps1.2.4.1.1 "><p id="p28142050151519"><a name="p28142050151519"></a><a name="p28142050151519"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="16.04%" headers="mcps1.2.4.1.2 "><p id="p64913614151519"><a name="p64913614151519"></a><a name="p64913614151519"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="58.9%" headers="mcps1.2.4.1.3 "><p id="p23511349151519"><a name="p23511349151519"></a><a name="p23511349151519"></a>云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section8194118165259"></a>

请求参数如[表2](#table38613152151549)所示。

**表 2**  请求参数

<a name="table38613152151549"></a>
<table><thead align="left"><tr id="row40874938151549"><th class="cellrowborder" valign="top" width="17.9%" id="mcps1.2.5.1.1"><p id="p22535719151549"><a name="p22535719151549"></a><a name="p22535719151549"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.719999999999999%" id="mcps1.2.5.1.2"><p id="p35271647131"><a name="p35271647131"></a><a name="p35271647131"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.79%" id="mcps1.2.5.1.3"><p id="p13453940151549"><a name="p13453940151549"></a><a name="p13453940151549"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.59%" id="mcps1.2.5.1.4"><p id="p23145935151549"><a name="p23145935151549"></a><a name="p23145935151549"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row62881453151549"><td class="cellrowborder" valign="top" width="17.9%" headers="mcps1.2.5.1.1 "><p id="p60232972151549"><a name="p60232972151549"></a><a name="p60232972151549"></a>volumeAttachment</p>
</td>
<td class="cellrowborder" valign="top" width="13.719999999999999%" headers="mcps1.2.5.1.2 "><p id="p1652794161320"><a name="p1652794161320"></a><a name="p1652794161320"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.79%" headers="mcps1.2.5.1.3 "><p id="p47032596151549"><a name="p47032596151549"></a><a name="p47032596151549"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48.59%" headers="mcps1.2.5.1.4 "><p id="p14307644151549"><a name="p14307644151549"></a><a name="p14307644151549"></a>要挂载的卷相关信息，详情请参见<a href="#table40707503151632">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  volumeAttachment数据结构说明

<a name="table40707503151632"></a>
<table><thead align="left"><tr id="row46910609151632"><th class="cellrowborder" valign="top" width="17.888211178882113%" id="mcps1.2.5.1.1"><p id="p9688145419315"><a name="p9688145419315"></a><a name="p9688145419315"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.908609139086092%" id="mcps1.2.5.1.2"><p id="p118264710132"><a name="p118264710132"></a><a name="p118264710132"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.608039196080394%" id="mcps1.2.5.1.3"><p id="p368816541035"><a name="p368816541035"></a><a name="p368816541035"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.595140485951404%" id="mcps1.2.5.1.4"><p id="p8703154232"><a name="p8703154232"></a><a name="p8703154232"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row56436699151632"><td class="cellrowborder" valign="top" width="17.888211178882113%" headers="mcps1.2.5.1.1 "><p id="p7969910151632"><a name="p7969910151632"></a><a name="p7969910151632"></a>volumeId</p>
</td>
<td class="cellrowborder" valign="top" width="13.908609139086092%" headers="mcps1.2.5.1.2 "><p id="p1582647151320"><a name="p1582647151320"></a><a name="p1582647151320"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.608039196080394%" headers="mcps1.2.5.1.3 "><p id="p41582949151632"><a name="p41582949151632"></a><a name="p41582949151632"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.595140485951404%" headers="mcps1.2.5.1.4 "><p id="p28198497151632"><a name="p28198497151632"></a><a name="p28198497151632"></a>待挂载磁盘的磁盘ID，UUID格式。</p>
</td>
</tr>
<tr id="row52459882151632"><td class="cellrowborder" valign="top" width="17.888211178882113%" headers="mcps1.2.5.1.1 "><p id="p21392044151632"><a name="p21392044151632"></a><a name="p21392044151632"></a>device</p>
</td>
<td class="cellrowborder" valign="top" width="13.908609139086092%" headers="mcps1.2.5.1.2 "><p id="p1827472138"><a name="p1827472138"></a><a name="p1827472138"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.608039196080394%" headers="mcps1.2.5.1.3 "><p id="p55033990151632"><a name="p55033990151632"></a><a name="p55033990151632"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.595140485951404%" headers="mcps1.2.5.1.4 "><p id="p7777719105553"><a name="p7777719105553"></a><a name="p7777719105553"></a>磁盘挂载点，如/dev/sda，/dev/sdb。</p>
<p id="p58233871152743"><a name="p58233871152743"></a><a name="p58233871152743"></a>新增加的磁盘挂载点不能和已有的磁盘挂载点相同。</p>
<p id="p22488653151632"><a name="p22488653151632"></a><a name="p22488653151632"></a>需要根据已有设备名称顺序指定，否则由系统自动生成。</p>
<div class="note" id="note794417411107"><a name="note794417411107"></a><a name="note794417411107"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1694404115106"><a name="p1694404115106"></a><a name="p1694404115106"></a>VBD磁盘挂载点只支持从/dev/vdb到/dev/vdx，建议按英文字母顺序进行挂载，否则可能出现云服务器中磁盘盘符错乱的情况。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section58140617165259"></a>

响应参数如[表4](#table548498215180)所示。

**表 4**  响应参数

<a name="table548498215180"></a>
<table><thead align="left"><tr id="row3759039515180"><th class="cellrowborder" valign="top" width="28.54%" id="mcps1.2.4.1.1"><p id="p62404314"><a name="p62404314"></a><a name="p62404314"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.459999999999997%" id="mcps1.2.4.1.2"><p id="p3528183"><a name="p3528183"></a><a name="p3528183"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="53%" id="mcps1.2.4.1.3"><p id="p17347392"><a name="p17347392"></a><a name="p17347392"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row4742233715180"><td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.2.4.1.1 "><p id="p1600407115180"><a name="p1600407115180"></a><a name="p1600407115180"></a>device</p>
</td>
<td class="cellrowborder" valign="top" width="18.459999999999997%" headers="mcps1.2.4.1.2 "><p id="p2126141115180"><a name="p2126141115180"></a><a name="p2126141115180"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="53%" headers="mcps1.2.4.1.3 "><p id="p4389880615180"><a name="p4389880615180"></a><a name="p4389880615180"></a>设备名称。</p>
</td>
</tr>
<tr id="row5954494215180"><td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.2.4.1.1 "><p id="p5841097215180"><a name="p5841097215180"></a><a name="p5841097215180"></a>serverId</p>
</td>
<td class="cellrowborder" valign="top" width="18.459999999999997%" headers="mcps1.2.4.1.2 "><p id="p3366825815180"><a name="p3366825815180"></a><a name="p3366825815180"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="53%" headers="mcps1.2.4.1.3 "><p id="p4217250415180"><a name="p4217250415180"></a><a name="p4217250415180"></a>挂载的云服务器ID，UUID格式。</p>
</td>
</tr>
<tr id="row4400822315180"><td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.2.4.1.1 "><p id="p789628615180"><a name="p789628615180"></a><a name="p789628615180"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="18.459999999999997%" headers="mcps1.2.4.1.2 "><p id="p3561941815180"><a name="p3561941815180"></a><a name="p3561941815180"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="53%" headers="mcps1.2.4.1.3 "><p id="p2593706215180"><a name="p2593706215180"></a><a name="p2593706215180"></a>卷的ID，UUID格式。</p>
</td>
</tr>
<tr id="row3210697315180"><td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.2.4.1.1 "><p id="p5052800715180"><a name="p5052800715180"></a><a name="p5052800715180"></a>volumeId</p>
</td>
<td class="cellrowborder" valign="top" width="18.459999999999997%" headers="mcps1.2.4.1.2 "><p id="p6623678615180"><a name="p6623678615180"></a><a name="p6623678615180"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="53%" headers="mcps1.2.4.1.3 "><p id="p4966276115180"><a name="p4966276115180"></a><a name="p4966276115180"></a>挂载ID，目前实现与卷UUID相同。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section8675155319416"></a>

```
POST https://{endpoint}/v2.1/{project_id}/servers/{server_id}/os-volume_attachments
```

```
{
    "volumeAttachment": {
        "volumeId": "54667652-3029-4af8-9222-2d53066fd61c",
        "device": "/dev/sdb"
    }
}
```

## 响应示例<a name="section104992312387"></a>

```
{
    "volumeAttachment": {
        "device": "/dev/vdb",
        "serverId": "ab258e25-e351-47c7-b6e3-0749c5d9ed6a",
        "id": "54667652-3029-4af8-9222-2d53066fd61c",
        "volumeId": "54667652-3029-4af8-9222-2d53066fd61c"
    }
}
```

## 返回值<a name="section38817202165259"></a>

请参考[通用请求返回值](通用请求返回值.md)。

