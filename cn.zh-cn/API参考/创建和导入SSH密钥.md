# 创建和导入SSH密钥<a name="ZH-CN_TOPIC_0020212678"></a>

## 功能介绍<a name="section52930837"></a>

创建SSH密钥，或把公钥导入系统，生成密钥对。

创建SSH密钥成功后，请把响应数据中的私钥内容保存到本地文件，用户使用该私钥登录云服务器。为保证云服务器安全，私钥数据只能读取一次，请妥善保管。

密钥对创建后默认是属于创建用户的，如果是子帐号创建的密钥，包括主帐号在内的其他用户无法查看不属于本用户的密钥对。

## URI<a name="section6615485"></a>

POST /v2.1/\{project\_id\}/os-keypairs

参数说明请参见[表1](#table909717)。

**表 1**  参数说明

<a name="table909717"></a>
<table><thead align="left"><tr id="row9180116"><th class="cellrowborder" valign="top" width="33.333333333333336%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.202020202020204%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="46.46464646464647%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row67029240"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.2.4.1.1 "><p id="p60659387"><a name="p60659387"></a><a name="p60659387"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20.202020202020204%" headers="mcps1.2.4.1.2 "><p id="p14463294"><a name="p14463294"></a><a name="p14463294"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="46.46464646464647%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section59539371"></a>

请求参数如[表2](#table8287277)所示。

>![](public_sys-resources/icon-note.gif) **说明：** 
>创建SSH密钥时，只需要提交SSH密钥的name属性。导入SSH密钥时，才需要提交public\_key属性。

**表 2**  请求参数

<a name="table8287277"></a>
<table><thead align="left"><tr id="row6478825"><th class="cellrowborder" valign="top" width="18.05%" id="mcps1.2.5.1.1"><p id="p55022811"><a name="p55022811"></a><a name="p55022811"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.66%" id="mcps1.2.5.1.2"><p id="p27662693"><a name="p27662693"></a><a name="p27662693"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="23.119999999999997%" id="mcps1.2.5.1.3"><p id="p26085680"><a name="p26085680"></a><a name="p26085680"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.17%" id="mcps1.2.5.1.4"><p id="p32565348"><a name="p32565348"></a><a name="p32565348"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row20547495"><td class="cellrowborder" valign="top" width="18.05%" headers="mcps1.2.5.1.1 "><p id="p53734436"><a name="p53734436"></a><a name="p53734436"></a>keypair</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.2 "><p id="p57522049"><a name="p57522049"></a><a name="p57522049"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="23.119999999999997%" headers="mcps1.2.5.1.3 "><p id="p28774374"><a name="p28774374"></a><a name="p28774374"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="44.17%" headers="mcps1.2.5.1.4 "><p id="p38553569"><a name="p38553569"></a><a name="p38553569"></a>创建或导入的SSH密钥信息，详情请参见<a href="#table54046809">表3</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  keypair字段数据结构说明

<a name="table54046809"></a>
<table><thead align="left"><tr id="row66830726"><th class="cellrowborder" valign="top" width="18.181818181818183%" id="mcps1.2.5.1.1"><p id="p47584422136"><a name="p47584422136"></a><a name="p47584422136"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.181818181818183%" id="mcps1.2.5.1.2"><p id="p47581425137"><a name="p47581425137"></a><a name="p47581425137"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.191919191919194%" id="mcps1.2.5.1.3"><p id="p187581542191314"><a name="p187581542191314"></a><a name="p187581542191314"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.44444444444445%" id="mcps1.2.5.1.4"><p id="p197587425136"><a name="p197587425136"></a><a name="p197587425136"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row4961980"><td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.5.1.1 "><p id="p66376082"><a name="p66376082"></a><a name="p66376082"></a>public_key</p>
</td>
<td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.5.1.2 "><p id="p7753598"><a name="p7753598"></a><a name="p7753598"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.2.5.1.3 "><p id="p24061669"><a name="p24061669"></a><a name="p24061669"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.2.5.1.4 "><p id="p189241054111414"><a name="p189241054111414"></a><a name="p189241054111414"></a>导入的公钥信息。</p>
<p id="p52054505113323"><a name="p52054505113323"></a><a name="p52054505113323"></a>建议导入的公钥长度不大于1024字节。</p>
<div class="note" id="note6540161717279"><a name="note6540161717279"></a><a name="note6540161717279"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p354119176278"><a name="p354119176278"></a><a name="p354119176278"></a>长度超过1024字节会导致<span id="text1287464145312"><a name="text1287464145312"></a><a name="text1287464145312"></a>云服务器</span>注入该密钥失败。</p>
</div></div>
</td>
</tr>
<tr id="row82031036195016"><td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.5.1.1 "><p id="p920333685015"><a name="p920333685015"></a><a name="p920333685015"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.5.1.2 "><p id="p9203836135020"><a name="p9203836135020"></a><a name="p9203836135020"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.2.5.1.3 "><p id="p1420310367501"><a name="p1420310367501"></a><a name="p1420310367501"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.2.5.1.4 "><p id="p142031336145018"><a name="p142031336145018"></a><a name="p142031336145018"></a>密钥类型，值为<span class="parmvalue" id="parmvalue15700202243020"><a name="parmvalue15700202243020"></a><a name="parmvalue15700202243020"></a>“ssh”</span>或<span class="parmvalue" id="parmvalue9128122803013"><a name="parmvalue9128122803013"></a><a name="parmvalue9128122803013"></a>“x509”</span>。</p>
<p id="p11201175716463"><a name="p11201175716463"></a><a name="p11201175716463"></a>微版本2.2及以上版本支持。</p>
</td>
</tr>
<tr id="row28567114"><td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.5.1.1 "><p id="p32234903"><a name="p32234903"></a><a name="p32234903"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.5.1.2 "><p id="p60890369"><a name="p60890369"></a><a name="p60890369"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.2.5.1.3 "><p id="p33172847"><a name="p33172847"></a><a name="p33172847"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.2.5.1.4 "><p id="p23814811"><a name="p23814811"></a><a name="p23814811"></a>密钥名称。</p>
<p id="p3185261315290"><a name="p3185261315290"></a><a name="p3185261315290"></a>新创建的密钥名称不能和已有密钥名称相同。</p>
</td>
</tr>
<tr id="row22241550192311"><td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.5.1.1 "><p id="p14224450172312"><a name="p14224450172312"></a><a name="p14224450172312"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.5.1.2 "><p id="p167344512420"><a name="p167344512420"></a><a name="p167344512420"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.2.5.1.3 "><p id="p1022419500232"><a name="p1022419500232"></a><a name="p1022419500232"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.2.5.1.4 "><p id="p1622411505237"><a name="p1622411505237"></a><a name="p1622411505237"></a>密钥的用户ID。</p>
<p id="p141914504713"><a name="p141914504713"></a><a name="p141914504713"></a>微版本2.10及以上版本支持。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section66092295"></a>

响应参数如[表4](#table51598880)所示。

**表 4**  响应参数

<a name="table51598880"></a>
<table><thead align="left"><tr id="row44903457"><th class="cellrowborder" valign="top" width="25.687431256874316%" id="mcps1.2.4.1.1"><p id="p52863116"><a name="p52863116"></a><a name="p52863116"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="27.567243275672432%" id="mcps1.2.4.1.2"><p id="p16299242"><a name="p16299242"></a><a name="p16299242"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="46.745325467453256%" id="mcps1.2.4.1.3"><p id="p45170224"><a name="p45170224"></a><a name="p45170224"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row23474126"><td class="cellrowborder" valign="top" width="25.687431256874316%" headers="mcps1.2.4.1.1 "><p id="p22356031"><a name="p22356031"></a><a name="p22356031"></a>keypair</p>
</td>
<td class="cellrowborder" valign="top" width="27.567243275672432%" headers="mcps1.2.4.1.2 "><p id="p45057304"><a name="p45057304"></a><a name="p45057304"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="46.745325467453256%" headers="mcps1.2.4.1.3 "><p id="p30540622"><a name="p30540622"></a><a name="p30540622"></a>SSH密钥信息，详情请参见<a href="#table51079899">表5</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  keypair字段数据结构说明

<a name="table51079899"></a>
<table><thead align="left"><tr id="row66208776"><th class="cellrowborder" valign="top" width="25.619999999999997%" id="mcps1.2.4.1.1"><p id="p1117813381339"><a name="p1117813381339"></a><a name="p1117813381339"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.11%" id="mcps1.2.4.1.2"><p id="p1517883853320"><a name="p1517883853320"></a><a name="p1517883853320"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="56.269999999999996%" id="mcps1.2.4.1.3"><p id="p13178153853317"><a name="p13178153853317"></a><a name="p13178153853317"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row27729526"><td class="cellrowborder" valign="top" width="25.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p31499108"><a name="p31499108"></a><a name="p31499108"></a>fingerprint</p>
</td>
<td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.2 "><p id="p37455857"><a name="p37455857"></a><a name="p37455857"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.269999999999996%" headers="mcps1.2.4.1.3 "><p id="p59121255"><a name="p59121255"></a><a name="p59121255"></a>密钥对应指纹信息。</p>
</td>
</tr>
<tr id="row62329248"><td class="cellrowborder" valign="top" width="25.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p15504345"><a name="p15504345"></a><a name="p15504345"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.2 "><p id="p54079315"><a name="p54079315"></a><a name="p54079315"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.269999999999996%" headers="mcps1.2.4.1.3 "><p id="p30917775"><a name="p30917775"></a><a name="p30917775"></a>密钥名称。</p>
</td>
</tr>
<tr id="row9824527"><td class="cellrowborder" valign="top" width="25.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p57589242"><a name="p57589242"></a><a name="p57589242"></a>public_key</p>
</td>
<td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.2 "><p id="p20116657"><a name="p20116657"></a><a name="p20116657"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.269999999999996%" headers="mcps1.2.4.1.3 "><p id="p35311297"><a name="p35311297"></a><a name="p35311297"></a>密钥对应publicKey信息。</p>
</td>
</tr>
<tr id="row16629746121557"><td class="cellrowborder" valign="top" width="25.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p4832208121557"><a name="p4832208121557"></a><a name="p4832208121557"></a>private_key</p>
</td>
<td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.2 "><p id="p55864542121557"><a name="p55864542121557"></a><a name="p55864542121557"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.269999999999996%" headers="mcps1.2.4.1.3 "><p id="p28734020121557"><a name="p28734020121557"></a><a name="p28734020121557"></a>密钥对应privateKey信息。</p>
<a name="ul53408548183356"></a><a name="ul53408548183356"></a><ul id="ul53408548183356"><li>创建SSH密钥时，响应中包括private_key的信息。</li><li>导入SSH密钥时，响应中不包括private_key的信息。</li></ul>
</td>
</tr>
<tr id="row49366219"><td class="cellrowborder" valign="top" width="25.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p39240784"><a name="p39240784"></a><a name="p39240784"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.2 "><p id="p29185940"><a name="p29185940"></a><a name="p29185940"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.269999999999996%" headers="mcps1.2.4.1.3 "><p id="p3041091"><a name="p3041091"></a><a name="p3041091"></a>密钥所属用户ID。</p>
</td>
</tr>
<tr id="row97681950172617"><td class="cellrowborder" valign="top" width="25.619999999999997%" headers="mcps1.2.4.1.1 "><p id="p1076825012260"><a name="p1076825012260"></a><a name="p1076825012260"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="18.11%" headers="mcps1.2.4.1.2 "><p id="p1768150152614"><a name="p1768150152614"></a><a name="p1768150152614"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.269999999999996%" headers="mcps1.2.4.1.3 "><p id="p121861283275"><a name="p121861283275"></a><a name="p121861283275"></a>密钥类型，值为<span class="parmvalue" id="parmvalue13791663419"><a name="parmvalue13791663419"></a><a name="parmvalue13791663419"></a>“ssh”</span>或<span class="parmvalue" id="parmvalue552697346"><a name="parmvalue552697346"></a><a name="parmvalue552697346"></a>“x509”</span>。</p>
<p id="p2812534719"><a name="p2812534719"></a><a name="p2812534719"></a>微版本2.2及以上版本支持。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例（导入SSH密钥）<a name="section1176153117145"></a>

```
POST https://{endpoint}/v2.1/{project_id}/os-keypairs
```

```
{
    "keypair": {
        "public_key": "ssh-rsaAAAAB3NzaC1yc2EAAAADAQABAAABAQDWNgTxQYeBzK9LYy4IakX7IsIl5j5zqR6BU2GJaEg3RK6dlS7rKFQhvy/V/1emK+GT/7P8up9VsMZ9Dx6PBOLow5p+2/wGsMlwDJpWiQ8zNnEMg+u/Ar/ZhYHAMyKEAOOJxIcnPoUgxfNdj/eiXV98AabsBdUA7QD30Og8F4Bmn2lii/WD9KbQQVjb7kbB3gNIJpGTUcoX73arorqkq/ppaLRmmwMJ7bTIGl8/0MWU2Dy+eTByOaDMb2htbB+j8ZXyEu7Oooy0NaSd+PNHv3PZ9OIVO7gd1lyoTRvCMK/F346+zmZtk5EASSOx5RifnSwk3NtugVjXs9GMJfFLBRibGenerated-by-Nova\\n\n",
        "type": "ssh",
        "name": "demo1",
        "user_id": "fake"
    }
}
```

## 请求示例（创建SSH密钥）<a name="section17825152411017"></a>

```
POST https://{endpoint}/v2.1/{project_id}/os-keypairs
```

```
{
    "keypair": {
        "name": "demo"
    }
}
```

## 响应示例（导入SSH密钥）<a name="section8681151155119"></a>

```
{
    "keypair": {
        "public_key": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDWNgTxQYeBzK9LYy4IakX7IsIl5j5zqR6BU2GJaEg3RK6dlS7rKFQhvy/V/1emK+GT/7P8up9VsMZ9Dx6PBOLow5p+2/wGsMlwDJpWiQ8zNnEMg+u/Ar/ZhYHAMyKEAOOJxIcnPoUgxfNdj/eiXV98AabsBdUA7QD30Og8F4Bmn2lii/WD9KbQQVjb7kbB3gNIJpGTUcoX73arorqkq/ppaLRmmwMJ7bTIGl8/0MWU2Dy+eTByOaDMb2htbB+j8ZXyEu7Oooy0NaSd+PNHv3PZ9OIVO7gd1lyoTRvCMK/F346+zmZtk5EASSOx5RifnSwk3NtugVjXs9GMJfFLBRib Generated-by-Nova\\n\n",
        "user_id": "6fc0d2cbbfab40b199874b97097e913d",
        "name": "demo1",
        "fingerprint": "fc:47:b5:c3:7d:25:32:d5:d2:0c:19:f9:62:ac:8c:5a"
    }
}
```

## 响应示例（创建SSH密钥）<a name="section97601124125214"></a>

```
{
    "keypair": {
        "public_key": "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDWNgTxQYeBzK9LYy4IakX7IsIl5j5zqR6BU2GJaEg3RK6dlS7rKFQhvy/V/1emK+GT/7P8up9VsMZ9Dx6PBOLow5p+2/wGsMlwDJpWiQ8zNnEMg+u/Ar/ZhYHAMyKEAOOJxIcnPoUgxfNdj/eiXV98AabsBdUA7QD30Og8F4Bmn2lii/WD9KbQQVjb7kbB3gNIJpGTUcoX73arorqkq/ppaLRmmwMJ7bTIGl8/0MWU2Dy+eTByOaDMb2htbB+j8ZXyEu7Oooy0NaSd+PNHv3PZ9OIVO7gd1lyoTRvCMK/F346+zmZtk5EASSOx5RifnSwk3NtugVjXs9GMJfFLBRib Generated-by-Nova\n",
        "private_key": "-----BEGIN RSA PRIVATE KEY-----\nMIIEpQIBAAKCAQEA1jYE8UGHgcyvS2MuCGpF+yLCJeY+c6kegVNhiWhIN0SunZUu\n6yhUIb8v1f9Xpivhk/+z/LqfVbDGfQ8ejwTi6MOaftv8BrDJcAyaVokPMzZxDIPr\nvwK/2YWBwDMihADjicSHJz6FIMXzXY/3ol1ffAGm7AXVAO0A99DoPBeAZp9pYov1\ng/Sm0EFY2+5Gwd4DSCaRk1HKF+92q6K6pKv6aWi0ZpsDCe20yBpfP9DFlNg8vnkw\ncjmgzG9obWwfo/GV8hLuzqKMtDWknfjzR79z2fTiFTu4HdZcqE0bwjCvxd+Ovs5m\nbZORAEkjseUYn50sJNzbboFY17PRjCXxSwUYmwIDAQABAoIBADNKQ+ywUA3YQLDA\nUqlZKOB09h+0/YccG13D5TrNaV0yaMz6h31u7pYV/RI0TXxQTXbuZt5AoR4Xca9I\nC30bImmxTDDL45CGi/T0T5AgyS7t/iuM+smFkwI2YVbv53fL7q9yCxpucdnjC95/\nNj/+M3qxupIQ42uRVAYCU1jwF6J6YLy/9UamrmVd4bWFRtT19O7uszUhHLqJOZXq\n3ItqnMyD5bSMkzMN+RxmZVXAPkBOonGVeBBInCjvHv23REkngX38zcUSc543H3Di\n4673helqSdMnI0/TgyfLQcNuOsfQcD02ABWlGBe0nCTqP8pTRo86nzK1+AoCUp72\nIsTeviECgYEA8yHKeo/eZw25eDb3YTJovbgzA61n6AYQlDQv7rBGQDwKKQHdEqhR\nP0PbScaoT7wSeLtYV0vxxA6qjEEuHhZIk/t2wEILu+AH4AK88SUbUn6ZoYu+XmTA\nx26e2QRo8Ngi/KtIfeOGXx1PM/H2/OjEN3XjkfwJsj5bB+HjpF/wsnUCgYEA4Yxg\nWJYNrvSkmvXmDgxHwdxfUpVAcp40bvomNgYpKn9R2TyjMCSDIw8vVC6cGCFB9/Pc\nG0pr8RN2SvbTaPo/96DkKdHz7NAWkzUSChD4Oy7ZNXw6GK3x1tGwMWeTs1hQDHhO\nrjS+E3bV2jC4EIvLLBxCNCbhtmQwlGUj7ZhgHM8CgYEA14UGpWpOrW8/D086LpCu\nxC46GnJmfwiRPa6dJqpfO6V9JCigvV8y1i/ifR16KWP/w8HeZ1PMtgyCJd3JcaYz\nI+pus7JYEGxgzrPepKxN8eyDZu4nDCmnsaFfceQ02fnd2bhDhERh4oJqqRM966ax\n+K+p0MhoF/aqXuxgDF93T9kCgYEAw7TsfLFnGiJJGfS4NARP11UCmUPMcif4UztX\nIJVj7u4e9SJ6bvGfoDIy3Ra8duuUtDOzDzMaSkqa4B0f//z0uEew8uCsiRVeIUlx\nZ66l1aSm8JPkTTnRmJbGDXhUXtAIVWmmy94T+AurL/IKJMFH//RdNadvPrXcuUax\nUB5hd10CgYEA3JBuX4BriSk6Bii0kYniqFM/1tEgVelAP6DT6uePvzTFdSJ0dMQo\nzwgWNmm43CyoKW/rw8yIbtIQZKBfHudSNx72nSmnBKaf3QPB40xsCip90ZUTfZdn\nLJzX1t4clg1wNsN4mJDwiYM9k3rB/8EY1fh9gUYI84X6xFAHllkv0To=\n-----END RSA PRIVATE KEY-----\n",
        "user_id": "6fc0d2cbbfab40b199874b97097e913d",
        "type": "ssh",
        "name": "demo",
        "fingerprint": "fc:47:b5:c3:7d:25:32:d5:d2:0c:19:f9:62:ac:8c:5a"
   }
}
```

## 返回值<a name="section57959746"></a>

请参考[通用请求返回值](通用请求返回值.md)。

