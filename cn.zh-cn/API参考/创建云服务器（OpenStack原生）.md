# 创建云服务器<a name="ZH-CN_TOPIC_0068473331"></a>

## 功能介绍<a name="zh-cn_topic_0057972661_section31291646"></a>

创建一台按需弹性云服务器。

弹性云服务器创建完成后，如需开启自动恢复功能，可以调用配置云服务器自动恢复的接口，具体使用请参见[管理云服务器自动恢复动作](管理云服务器自动恢复动作.md)。

该接口在云服务器创建失败后不支持自动回滚。若需要自动回滚能力，可以调用POST /v1/\{project\_id\}/cloudservers接口，具体使用请参见[创建云服务器（按需）](创建云服务器（按需）.md)。

## URI<a name="zh-cn_topic_0057972661_section13189358"></a>

POST /v2.1/\{project\_id\}/servers

参数说明请参见[表1](#zh-cn_topic_0057972661_table47145209)。

**表 1**  参数说明

<a name="zh-cn_topic_0057972661_table47145209"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972661_row4152081"><th class="cellrowborder" valign="top" width="28.000000000000004%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="49%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972661_row11861416151631"><td class="cellrowborder" valign="top" width="28.000000000000004%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972661_p50425983151639"><a name="zh-cn_topic_0057972661_p50425983151639"></a><a name="zh-cn_topic_0057972661_p50425983151639"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972661_p57972822151639"><a name="zh-cn_topic_0057972661_p57972822151639"></a><a name="zh-cn_topic_0057972661_p57972822151639"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="49%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：**   
>创建弹性云服务器接口别名：/v2/\{project\_id\}/os-volumes\_boot，该调用方式仅在OpenStack Client中使用，用户不推荐使用。  

## 接口约束<a name="zh-cn_topic_0057972661_section51595365"></a>

1.  该接口为原生接口，不支持整机镜像创建弹性云服务器功能。如需使用整机镜像创建弹性云服务器，请使用ECS接口[创建云服务器（按需）](创建云服务器（按需）.md)。
2.  网络的三个参数（port、uuid和fixed\_ip）中，port优先级最高；指定fixed\_ip时必须指明uuid。
3.  注入文件失败，将导致创建弹性云服务器失败。
4.  使用镜像创建弹性云服务器时，存在下面约束：
    1.  不支持指定Host创建弹性云服务器。
    2.  租户如果对弹性云服务器中的卷进行了备份，则需要租户自行删除该卷所对应的快照等数据后，才能删除卷。
    3.  调整镜像创建的弹性云服务器规格时，不支持resource\_type不同的flavor之间的规格调整。

5.  公有云平台提供的原生接口/v2/\{project\_id\}/servers 和 /v2.1/\{project\_id\}/servers 是基于社区版OpenStack原生接口加固而成的，兼容社区版OpenStack原生接口。

    较之社区版的OpenStack原生接口，在使用指定镜像的方式创建弹性云服务器时存在如下差异：

    -   社区OpenStack原生接口：默认使用服务器本地磁盘创建弹性云服务器。
    -   公有云平台提供的原生接口：为了保障可靠性，使用共享存储作为系统盘创建弹性云服务器。

    该差异的具体表现为，当您使用提供的原生接口创建云服务器时：

    1.  可以查询到云服务器挂载的系统盘信息。
    2.  云服务器的系统盘会占用云硬盘的配额。
    3.  不支持使用image过滤查询指定镜像方式创建的弹性云服务器。

6.  公有云场景下，后端卷弹性云服务器必须与卷创建在相同的被级联OpenStack。
7.  用户创建弹性云服务器时在block\_device\_mapping\_v2设置的device\_name字段不会生效，系统会默认生成一个device\_name。
8.  请勿使用“provider:network\_type”为“geneve”的网络来创建弹性云服务器。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >“provider:network\_type”为“geneve”时，表示裸金属服务器使用的内部高速网络。  

9.  创建云服务器时，除非全局配置项allow\_duplicate\_networks开启，否则多个端口不能属于同一个网络。
10. 如果使用密钥方式远程登录云服务器，请使用key\_name参数。如果使用密码方式远程登录云服务器，可使用adminPass参数；对于Linux弹性云服务器，还可使用user\_data进行注入，对于Windows弹性云服务器，还可通过元数据admin\_pass进行注入。

## 请求消息<a name="zh-cn_topic_0057972661_section18475057"></a>

请求参数如[表2](#zh-cn_topic_0057972661_table40519951)所示。

**表 2**  请求参数

<a name="zh-cn_topic_0057972661_table40519951"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972661_row35619075"><th class="cellrowborder" valign="top" width="20.05%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0057972661_p66572856"><a name="zh-cn_topic_0057972661_p66572856"></a><a name="zh-cn_topic_0057972661_p66572856"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.719999999999999%" id="mcps1.2.5.1.2"><p id="p1467903512918"><a name="p1467903512918"></a><a name="p1467903512918"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.32%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0057972661_p23692278"><a name="zh-cn_topic_0057972661_p23692278"></a><a name="zh-cn_topic_0057972661_p23692278"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.91%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0057972661_p20908074"><a name="zh-cn_topic_0057972661_p20908074"></a><a name="zh-cn_topic_0057972661_p20908074"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972661_row15832433"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p7358688"><a name="zh-cn_topic_0057972661_p7358688"></a><a name="zh-cn_topic_0057972661_p7358688"></a>server</p>
</td>
<td class="cellrowborder" valign="top" width="13.719999999999999%" headers="mcps1.2.5.1.2 "><p id="p467915358917"><a name="p467915358917"></a><a name="p467915358917"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.32%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p59182880"><a name="zh-cn_topic_0057972661_p59182880"></a><a name="zh-cn_topic_0057972661_p59182880"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48.91%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p6993202"><a name="zh-cn_topic_0057972661_p6993202"></a><a name="zh-cn_topic_0057972661_p6993202"></a>弹性云服务器信息，参见<a href="#zh-cn_topic_0057972661_table64008488102639">表3</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row29578451"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p47044325"><a name="zh-cn_topic_0057972661_p47044325"></a><a name="zh-cn_topic_0057972661_p47044325"></a>os:scheduler_hints</p>
</td>
<td class="cellrowborder" valign="top" width="13.719999999999999%" headers="mcps1.2.5.1.2 "><p id="p4679135396"><a name="p4679135396"></a><a name="p4679135396"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.32%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p52493967"><a name="zh-cn_topic_0057972661_p52493967"></a><a name="zh-cn_topic_0057972661_p52493967"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48.91%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p10232270"><a name="zh-cn_topic_0057972661_p10232270"></a><a name="zh-cn_topic_0057972661_p10232270"></a>弹性云服务器调度信息，参见<a href="#zh-cn_topic_0057972661_table12534817105641">表8</a>。裸金属服务器场景不支持。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  server参数信息

<a name="zh-cn_topic_0057972661_table64008488102639"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972661_row56993194102639"><th class="cellrowborder" valign="top" width="19.939999999999998%" id="mcps1.2.5.1.1"><p id="p15357151212247"><a name="p15357151212247"></a><a name="p15357151212247"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.79%" id="mcps1.2.5.1.2"><p id="p67554367107"><a name="p67554367107"></a><a name="p67554367107"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.57%" id="mcps1.2.5.1.3"><p id="p19357112132415"><a name="p19357112132415"></a><a name="p19357112132415"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.699999999999996%" id="mcps1.2.5.1.4"><p id="p3372912142414"><a name="p3372912142414"></a><a name="p3372912142414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972661_row64892893102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p53667478102658"><a name="zh-cn_topic_0057972661_p53667478102658"></a><a name="zh-cn_topic_0057972661_p53667478102658"></a>imageRef</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p2075533681020"><a name="p2075533681020"></a><a name="p2075533681020"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p52098484102658"><a name="zh-cn_topic_0057972661_p52098484102658"></a><a name="zh-cn_topic_0057972661_p52098484102658"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p32710312102658"><a name="zh-cn_topic_0057972661_p32710312102658"></a><a name="zh-cn_topic_0057972661_p32710312102658"></a>镜像ID或者镜像资源的URL。</p>
<a name="zh-cn_topic_0057972661_ul25957356102658"></a><a name="zh-cn_topic_0057972661_ul25957356102658"></a><ul id="zh-cn_topic_0057972661_ul25957356102658"><li>镜像ID示例：3b8d6fef-af77-42ab-b8b7-5a7f0f0af8f2</li><li>镜像URL示例：http://glance.openstack.example.com/images/3b8d6fef-af77-42ab-b8b7-5a7f0f0af8f2</li><li>指定卷作为系统卷创弹性云服务器时，不需填写该参数；非卷创建弹性云服务器时需填写有效的UUID参数，否则API将返回400错误。</li></ul>
<div class="note" id="note12001550131917"><a name="note12001550131917"></a><a name="note12001550131917"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul185629592115"></a><a name="ul185629592115"></a><ul id="ul185629592115"><li>对于部分规格的弹性云服务器，不能支持公有云平台提供的所有公共镜像。具体规格的镜像支持列表，请登录管理控制台，以“创建弹性云服务器”页面系统自动过滤的镜像信息为准，并在镜像服务页面查询镜像ID。</li><li>如果创建失败，请尝试修改参数配置。</li></ul>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row993360102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p20533591102658"><a name="zh-cn_topic_0057972661_p20533591102658"></a><a name="zh-cn_topic_0057972661_p20533591102658"></a>flavorRef</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p2756536151015"><a name="p2756536151015"></a><a name="p2756536151015"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p52608144102658"><a name="zh-cn_topic_0057972661_p52608144102658"></a><a name="zh-cn_topic_0057972661_p52608144102658"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p21145347102658"><a name="zh-cn_topic_0057972661_p21145347102658"></a><a name="zh-cn_topic_0057972661_p21145347102658"></a>规格ID或URL。</p>
<p id="p27315444412"><a name="p27315444412"></a><a name="p27315444412"></a>规格ID示例：c1.2xlarge</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row3565234102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p47028347102658"><a name="zh-cn_topic_0057972661_p47028347102658"></a><a name="zh-cn_topic_0057972661_p47028347102658"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p9756133613109"><a name="p9756133613109"></a><a name="p9756133613109"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p51199773102658"><a name="zh-cn_topic_0057972661_p51199773102658"></a><a name="zh-cn_topic_0057972661_p51199773102658"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p41851471102658"><a name="zh-cn_topic_0057972661_p41851471102658"></a><a name="zh-cn_topic_0057972661_p41851471102658"></a>弹性云服务器名称，长度大于0小于256字节。</p>
<div class="note" id="note1631304619446"><a name="note1631304619446"></a><a name="note1631304619446"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1313546134412"><a name="p1313546134412"></a><a name="p1313546134412"></a>云服务器内部主机名(hostname)命名规则遵循 <a href="https://tools.ietf.org/html/rfc952" target="_blank" rel="noopener noreferrer">RFC 952</a>和<a href="https://tools.ietf.org/html/rfc1123" target="_blank" rel="noopener noreferrer">RFC 1123</a>命名规范，建议使用a-zA-z或0-9以及中划线"-"组成的名称命名，"_"将在弹性云服务器内部默认转化为"-"。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row59762533102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p42298537102658"><a name="zh-cn_topic_0057972661_p42298537102658"></a><a name="zh-cn_topic_0057972661_p42298537102658"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p375616363108"><a name="p375616363108"></a><a name="p375616363108"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p3629454102658"><a name="zh-cn_topic_0057972661_p3629454102658"></a><a name="zh-cn_topic_0057972661_p3629454102658"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p14501627151547"><a name="zh-cn_topic_0057972661_p14501627151547"></a><a name="zh-cn_topic_0057972661_p14501627151547"></a>弹性云服务器元数据。参照<a href="#zh-cn_topic_0057972661_table2373623012315">表4</a>。</p>
<a name="zh-cn_topic_0057972661_ul18338492151614"></a><a name="zh-cn_topic_0057972661_ul18338492151614"></a><ul id="zh-cn_topic_0057972661_ul18338492151614"><li>key的长度大于0小于256字节</li><li>value的长度大于等于0小于256字节</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row4553446102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p5856011102658"><a name="zh-cn_topic_0057972661_p5856011102658"></a><a name="zh-cn_topic_0057972661_p5856011102658"></a>adminPass</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p4756133619102"><a name="p4756133619102"></a><a name="p4756133619102"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p4574868102658"><a name="zh-cn_topic_0057972661_p4574868102658"></a><a name="zh-cn_topic_0057972661_p4574868102658"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="p59981754144012"><a name="p59981754144012"></a><a name="p59981754144012"></a>如果需要使用密码方式登录云服务器，可使用adminPass字段指定云服务器管理员帐户初始登录密码。其中，Linux管理员帐户为root，Windows管理员帐户为Administrator。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row19678943102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p44887270102658"><a name="zh-cn_topic_0057972661_p44887270102658"></a><a name="zh-cn_topic_0057972661_p44887270102658"></a>block_device_mapping_v2</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p17569367102"><a name="p17569367102"></a><a name="p17569367102"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p11990221102658"><a name="zh-cn_topic_0057972661_p11990221102658"></a><a name="zh-cn_topic_0057972661_p11990221102658"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p16256306102658"><a name="zh-cn_topic_0057972661_p16256306102658"></a><a name="zh-cn_topic_0057972661_p16256306102658"></a>扩展属性，指定弹性云服务器存储设备的v2接口。是存储资源的新版本接口，指定卷场景不能批创弹性云服务器。参照<a href="#zh-cn_topic_0057972661_table15044407105358">表5</a>。裸金属服务器场景不支持。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row6088188102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p21642473102658"><a name="zh-cn_topic_0057972661_p21642473102658"></a><a name="zh-cn_topic_0057972661_p21642473102658"></a>config_drive</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p07561536191013"><a name="p07561536191013"></a><a name="p07561536191013"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p8209879102658"><a name="zh-cn_topic_0057972661_p8209879102658"></a><a name="zh-cn_topic_0057972661_p8209879102658"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p43710689102658"><a name="zh-cn_topic_0057972661_p43710689102658"></a><a name="zh-cn_topic_0057972661_p43710689102658"></a>扩展属性，开启后在弹性云服务器创建时挂载config_drive向弹性云服务器内部传递信息。</p>
<p id="zh-cn_topic_0057972661_p57851884102658"><a name="zh-cn_topic_0057972661_p57851884102658"></a><a name="zh-cn_topic_0057972661_p57851884102658"></a>当前不支持该功能。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row38867078102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p29656925102658"><a name="zh-cn_topic_0057972661_p29656925102658"></a><a name="zh-cn_topic_0057972661_p29656925102658"></a>security_groups</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p1675653621016"><a name="p1675653621016"></a><a name="p1675653621016"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p53400697102658"><a name="zh-cn_topic_0057972661_p53400697102658"></a><a name="zh-cn_topic_0057972661_p53400697102658"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p45349775152941"><a name="zh-cn_topic_0057972661_p45349775152941"></a><a name="zh-cn_topic_0057972661_p45349775152941"></a>扩展属性，指定弹性云服务器的安全组，默认为default。</p>
<p id="zh-cn_topic_0057972661_p53708280102658"><a name="zh-cn_topic_0057972661_p53708280102658"></a><a name="zh-cn_topic_0057972661_p53708280102658"></a>指定network创建弹性云服务器时该字段有效。对于已存在端口，安全组请求无效。具体请参见<a href="#zh-cn_topic_0057972661_table16920677105453">表6</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row11447375102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p58493193102658"><a name="zh-cn_topic_0057972661_p58493193102658"></a><a name="zh-cn_topic_0057972661_p58493193102658"></a>networks</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p14756143616107"><a name="p14756143616107"></a><a name="p14756143616107"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p40328188102658"><a name="zh-cn_topic_0057972661_p40328188102658"></a><a name="zh-cn_topic_0057972661_p40328188102658"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p50103488102658"><a name="zh-cn_topic_0057972661_p50103488102658"></a><a name="zh-cn_topic_0057972661_p50103488102658"></a>扩展属性，指定弹性云服务器的网卡信息。有多个租户网络时必须指定。参照<a href="#zh-cn_topic_0057972661_table9995892105551">表7</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row62300910102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p62687271102658"><a name="zh-cn_topic_0057972661_p62687271102658"></a><a name="zh-cn_topic_0057972661_p62687271102658"></a>key_name</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p3756236101010"><a name="p3756236101010"></a><a name="p3756236101010"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p44504222102658"><a name="zh-cn_topic_0057972661_p44504222102658"></a><a name="zh-cn_topic_0057972661_p44504222102658"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p1533495102658"><a name="zh-cn_topic_0057972661_p1533495102658"></a><a name="zh-cn_topic_0057972661_p1533495102658"></a>扩展属性，指定keypair的名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row33176070102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p44176647102658"><a name="zh-cn_topic_0057972661_p44176647102658"></a><a name="zh-cn_topic_0057972661_p44176647102658"></a>user_data</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p16756163619108"><a name="p16756163619108"></a><a name="p16756163619108"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p21538656102658"><a name="zh-cn_topic_0057972661_p21538656102658"></a><a name="zh-cn_topic_0057972661_p21538656102658"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p50969357102658"><a name="zh-cn_topic_0057972661_p50969357102658"></a><a name="zh-cn_topic_0057972661_p50969357102658"></a>扩展属性，字符串长度小于65535，且必须是base64加密的。</p>
<p id="p073141119521"><a name="p073141119521"></a><a name="p073141119521"></a>更多关于待注入用户数据的信息，请参见《弹性云服务器用户指南 》的“<a href="https://support.huaweicloud.com/usermanual-ecs/zh-cn_topic_0032380449.html" target="_blank" rel="noopener noreferrer">用户数据注入</a>”章节。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row63798654102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p45459633102658"><a name="zh-cn_topic_0057972661_p45459633102658"></a><a name="zh-cn_topic_0057972661_p45459633102658"></a>availability_zone</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p16756203661019"><a name="p16756203661019"></a><a name="p16756203661019"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p58351639102658"><a name="zh-cn_topic_0057972661_p58351639102658"></a><a name="zh-cn_topic_0057972661_p58351639102658"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p9041942195215"><a name="zh-cn_topic_0057972661_p9041942195215"></a><a name="zh-cn_topic_0057972661_p9041942195215"></a>扩展属性，指定弹性云服务器所在的AZ。</p>
<p id="zh-cn_topic_0057972661_p56149386102658"><a name="zh-cn_topic_0057972661_p56149386102658"></a><a name="zh-cn_topic_0057972661_p56149386102658"></a>创建弹性云服务器时需要填入该参数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row14011337102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p63604766102658"><a name="zh-cn_topic_0057972661_p63604766102658"></a><a name="zh-cn_topic_0057972661_p63604766102658"></a>return_reservation_id</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p13756173611019"><a name="p13756173611019"></a><a name="p13756173611019"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p51712396102658"><a name="zh-cn_topic_0057972661_p51712396102658"></a><a name="zh-cn_topic_0057972661_p51712396102658"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p49723161102658"><a name="zh-cn_topic_0057972661_p49723161102658"></a><a name="zh-cn_topic_0057972661_p49723161102658"></a>扩展属性，是否支持返回批量创建弹性云服务器的reservation_id。通过返回的reservation_id，可以过滤查询到本次创建的弹性云服务器。</p>
<a name="zh-cn_topic_0057972661_ul1627916843419"></a><a name="zh-cn_topic_0057972661_ul1627916843419"></a><ul id="zh-cn_topic_0057972661_ul1627916843419"><li>true，返回reservation_id。</li><li>false，返回弹性云服务器信息。<div class="note" id="zh-cn_topic_0057972661_note1151212192215"><a name="zh-cn_topic_0057972661_note1151212192215"></a><a name="zh-cn_topic_0057972661_note1151212192215"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0057972661_p17513619142119"><a name="zh-cn_topic_0057972661_p17513619142119"></a><a name="zh-cn_topic_0057972661_p17513619142119"></a>批量创建弹性云服务器时，支持使用该字段。</p>
</div></div>
</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row14685215102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p17473992102658"><a name="zh-cn_topic_0057972661_p17473992102658"></a><a name="zh-cn_topic_0057972661_p17473992102658"></a>min_count</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p47571336141013"><a name="p47571336141013"></a><a name="p47571336141013"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p6107265102658"><a name="zh-cn_topic_0057972661_p6107265102658"></a><a name="zh-cn_topic_0057972661_p6107265102658"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p39383468153028"><a name="zh-cn_topic_0057972661_p39383468153028"></a><a name="zh-cn_topic_0057972661_p39383468153028"></a>扩展属性，表示创建弹性云服务器最小数量。</p>
<p id="zh-cn_topic_0057972661_p1358388153054"><a name="zh-cn_topic_0057972661_p1358388153054"></a><a name="zh-cn_topic_0057972661_p1358388153054"></a>默认值为1。</p>
<div class="note" id="zh-cn_topic_0057972661_note5101551193636"><a name="zh-cn_topic_0057972661_note5101551193636"></a><a name="zh-cn_topic_0057972661_note5101551193636"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0057972661_p45913965193636"><a name="zh-cn_topic_0057972661_p45913965193636"></a><a name="zh-cn_topic_0057972661_p45913965193636"></a>指定镜像创建弹性云服务器时，支持使用该字段。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row33216193102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p48294822102658"><a name="zh-cn_topic_0057972661_p48294822102658"></a><a name="zh-cn_topic_0057972661_p48294822102658"></a>max_count</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p575716366106"><a name="p575716366106"></a><a name="p575716366106"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p19566505102658"><a name="zh-cn_topic_0057972661_p19566505102658"></a><a name="zh-cn_topic_0057972661_p19566505102658"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p4122565110275"><a name="zh-cn_topic_0057972661_p4122565110275"></a><a name="zh-cn_topic_0057972661_p4122565110275"></a>表示创建弹性云服务器最大数量。</p>
<p id="zh-cn_topic_0057972661_p771939515316"><a name="zh-cn_topic_0057972661_p771939515316"></a><a name="zh-cn_topic_0057972661_p771939515316"></a>默认值与min_count的取值一致。</p>
<p id="zh-cn_topic_0057972661_p52138865153152"><a name="zh-cn_topic_0057972661_p52138865153152"></a><a name="zh-cn_topic_0057972661_p52138865153152"></a>约束：</p>
<p id="zh-cn_topic_0057972661_p66596602153152"><a name="zh-cn_topic_0057972661_p66596602153152"></a><a name="zh-cn_topic_0057972661_p66596602153152"></a>参数max_count的取值必须大于参数min_count的取值。</p>
<p id="zh-cn_topic_0057972661_p62498506153152"><a name="zh-cn_topic_0057972661_p62498506153152"></a><a name="zh-cn_topic_0057972661_p62498506153152"></a>当min_count、max_count同时设置时，创弹性云服务器的数量取决于服务器的资源情况。根据资源情况，在min_count至max_count的取值范围内创建最大数量的弹性云服务器。</p>
<div class="note" id="zh-cn_topic_0057972661_note20928070193644"><a name="zh-cn_topic_0057972661_note20928070193644"></a><a name="zh-cn_topic_0057972661_note20928070193644"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0057972661_p54134906193644"><a name="zh-cn_topic_0057972661_p54134906193644"></a><a name="zh-cn_topic_0057972661_p54134906193644"></a>指定镜像创建弹性云服务器时，支持使用该字段。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row29652792102639"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p36386296102658"><a name="zh-cn_topic_0057972661_p36386296102658"></a><a name="zh-cn_topic_0057972661_p36386296102658"></a>OS-DCF:diskConfig</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p7757123671012"><a name="p7757123671012"></a><a name="p7757123671012"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p61608878102658"><a name="zh-cn_topic_0057972661_p61608878102658"></a><a name="zh-cn_topic_0057972661_p61608878102658"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p19164491102658"><a name="zh-cn_topic_0057972661_p19164491102658"></a><a name="zh-cn_topic_0057972661_p19164491102658"></a>diskConfig的方式，取值为AUTO、MANUAL。</p>
<a name="zh-cn_topic_0057972661_ul38262699102658"></a><a name="zh-cn_topic_0057972661_ul38262699102658"></a><ul id="zh-cn_topic_0057972661_ul38262699102658"><li>MANUAL，镜像空间不会扩展。</li><li>AUTO，系统盘镜像空间会自动扩展为与flavor大小一致。</li></ul>
<p id="zh-cn_topic_0057972661_p43329035102658"><a name="zh-cn_topic_0057972661_p43329035102658"></a><a name="zh-cn_topic_0057972661_p43329035102658"></a>当前不支持该功能。</p>
</td>
</tr>
<tr id="row15681131174915"><td class="cellrowborder" valign="top" width="19.939999999999998%" headers="mcps1.2.5.1.1 "><p id="p1650191194918"><a name="p1650191194918"></a><a name="p1650191194918"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="13.79%" headers="mcps1.2.5.1.2 "><p id="p19757133619100"><a name="p19757133619100"></a><a name="p19757133619100"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.57%" headers="mcps1.2.5.1.3 "><p id="p14650131154914"><a name="p14650131154914"></a><a name="p14650131154914"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.699999999999996%" headers="mcps1.2.5.1.4 "><p id="p364511262207"><a name="p364511262207"></a><a name="p364511262207"></a>扩展属性，表示弹性云服务器描述信息，默认为空字符串。</p>
<a name="ul176291026182010"></a><a name="ul176291026182010"></a><ul id="ul176291026182010"><li>长度最多允许85个字符。</li><li>不能包含“&lt;” 和 “&gt;”等特殊符号。</li></ul>
<div class="note" id="note318983732010"><a name="note318983732010"></a><a name="note318983732010"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul1919342653912"></a><a name="ul1919342653912"></a><ul id="ul1919342653912"><li>V2接口不支持该字段。</li><li>V2.1接口支持该字段，此时，需在请求Header中增加一组Key-Value值。其中，Key固定为“X-OpenStack-Nova-API-Version” ，Value为微版本号，当Value的值为2.19时，支持使用该字段。</li></ul>
</div></div>
</td>
</tr>
</tbody>
</table>

**表 4**  metadata字段数据结构说明

<a name="zh-cn_topic_0057972661_table2373623012315"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972661_row4787810512315"><th class="cellrowborder" valign="top" width="21.617838216178384%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0057972661_p5292128812315"><a name="zh-cn_topic_0057972661_p5292128812315"></a><a name="zh-cn_topic_0057972661_p5292128812315"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.348665133486653%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0057972661_p5876596012315"><a name="zh-cn_topic_0057972661_p5876596012315"></a><a name="zh-cn_topic_0057972661_p5876596012315"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.66823317668233%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0057972661_p6242233712315"><a name="zh-cn_topic_0057972661_p6242233712315"></a><a name="zh-cn_topic_0057972661_p6242233712315"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.36526347365263%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0057972661_p2304450612315"><a name="zh-cn_topic_0057972661_p2304450612315"></a><a name="zh-cn_topic_0057972661_p2304450612315"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972661_row1717815342412"><td class="cellrowborder" valign="top" width="21.617838216178384%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p91796345418"><a name="zh-cn_topic_0057972661_p91796345418"></a><a name="zh-cn_topic_0057972661_p91796345418"></a>admin_pass</p>
</td>
<td class="cellrowborder" valign="top" width="13.348665133486653%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972661_p131791234844"><a name="zh-cn_topic_0057972661_p131791234844"></a><a name="zh-cn_topic_0057972661_p131791234844"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.66823317668233%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p51791934647"><a name="zh-cn_topic_0057972661_p51791934647"></a><a name="zh-cn_topic_0057972661_p51791934647"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.36526347365263%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p11179163419418"><a name="zh-cn_topic_0057972661_p11179163419418"></a><a name="zh-cn_topic_0057972661_p11179163419418"></a>Windows弹性云服务器Administrator用户的密码。</p>
<p id="zh-cn_topic_0057972661_p1882625312510"><a name="zh-cn_topic_0057972661_p1882625312510"></a><a name="zh-cn_topic_0057972661_p1882625312510"></a>示例：cloud.1234</p>
<div class="note" id="zh-cn_topic_0057972661_note1931159867"><a name="zh-cn_topic_0057972661_note1931159867"></a><a name="zh-cn_topic_0057972661_note1931159867"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0057972661_p15312694619"><a name="zh-cn_topic_0057972661_p15312694619"></a><a name="zh-cn_topic_0057972661_p15312694619"></a>创建密码方式鉴权的Windows弹性云服务器时为必选字段。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

**表 5**  block\_device\_mapping\_v2参数

<a name="zh-cn_topic_0057972661_table15044407105358"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972661_row46099088105358"><th class="cellrowborder" valign="top" width="25.069999999999997%" id="mcps1.2.5.1.1"><p id="p13422222102415"><a name="p13422222102415"></a><a name="p13422222102415"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.93%" id="mcps1.2.5.1.2"><p id="p4437192213248"><a name="p4437192213248"></a><a name="p4437192213248"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="10.979999999999999%" id="mcps1.2.5.1.3"><p id="p1743713226241"><a name="p1743713226241"></a><a name="p1743713226241"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="47.02%" id="mcps1.2.5.1.4"><p id="p114371922172411"><a name="p114371922172411"></a><a name="p114371922172411"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972661_row61925742105358"><td class="cellrowborder" valign="top" width="25.069999999999997%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p3486240110546"><a name="zh-cn_topic_0057972661_p3486240110546"></a><a name="zh-cn_topic_0057972661_p3486240110546"></a>source_type</p>
</td>
<td class="cellrowborder" valign="top" width="16.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972661_p528222710546"><a name="zh-cn_topic_0057972661_p528222710546"></a><a name="zh-cn_topic_0057972661_p528222710546"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="10.979999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p2520722910546"><a name="zh-cn_topic_0057972661_p2520722910546"></a><a name="zh-cn_topic_0057972661_p2520722910546"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.02%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p2851968810546"><a name="zh-cn_topic_0057972661_p2851968810546"></a><a name="zh-cn_topic_0057972661_p2851968810546"></a>卷设备的源头类型，当前只支持volume、image、snapshot、blank类型。</p>
<p id="zh-cn_topic_0057972661_p547651293810"><a name="zh-cn_topic_0057972661_p547651293810"></a><a name="zh-cn_topic_0057972661_p547651293810"></a>当使用卷创建云服务器时，source_type设置为volume；当使用镜像创建云服务器时，source_type设置为image；当使用快照创建云服务器时，source_type设置为snapshot；当创建空数据卷时，source_type设置为blank。</p>
<div class="note" id="zh-cn_topic_0057972661_note25817266173940"><a name="zh-cn_topic_0057972661_note25817266173940"></a><a name="zh-cn_topic_0057972661_note25817266173940"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0057972661_p31028803173940"><a name="zh-cn_topic_0057972661_p31028803173940"></a><a name="zh-cn_topic_0057972661_p31028803173940"></a>当卷设备的源头类型为snapshot时，且boot_index为0，则该快照对应的云硬盘必须为系统盘。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row9923110105358"><td class="cellrowborder" valign="top" width="25.069999999999997%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p5421404410546"><a name="zh-cn_topic_0057972661_p5421404410546"></a><a name="zh-cn_topic_0057972661_p5421404410546"></a>destination_type</p>
</td>
<td class="cellrowborder" valign="top" width="16.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972661_p2926143910546"><a name="zh-cn_topic_0057972661_p2926143910546"></a><a name="zh-cn_topic_0057972661_p2926143910546"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="10.979999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p2136636710546"><a name="zh-cn_topic_0057972661_p2136636710546"></a><a name="zh-cn_topic_0057972661_p2136636710546"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.02%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p5295414710546"><a name="zh-cn_topic_0057972661_p5295414710546"></a><a name="zh-cn_topic_0057972661_p5295414710546"></a>卷设备的当前类型， 当前只支持volume类型。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row9269169105358"><td class="cellrowborder" valign="top" width="25.069999999999997%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p1597666010546"><a name="zh-cn_topic_0057972661_p1597666010546"></a><a name="zh-cn_topic_0057972661_p1597666010546"></a>guest_format</p>
</td>
<td class="cellrowborder" valign="top" width="16.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972661_p1904109010546"><a name="zh-cn_topic_0057972661_p1904109010546"></a><a name="zh-cn_topic_0057972661_p1904109010546"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="10.979999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p6593336110546"><a name="zh-cn_topic_0057972661_p6593336110546"></a><a name="zh-cn_topic_0057972661_p6593336110546"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="47.02%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p3900205710546"><a name="zh-cn_topic_0057972661_p3900205710546"></a><a name="zh-cn_topic_0057972661_p3900205710546"></a>local文件系统格式，例如：swap, ext4。</p>
<p id="zh-cn_topic_0057972661_p1547419510546"><a name="zh-cn_topic_0057972661_p1547419510546"></a><a name="zh-cn_topic_0057972661_p1547419510546"></a>当前不支持该功能。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row32258375105358"><td class="cellrowborder" valign="top" width="25.069999999999997%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p639950510546"><a name="zh-cn_topic_0057972661_p639950510546"></a><a name="zh-cn_topic_0057972661_p639950510546"></a>device_name</p>
</td>
<td class="cellrowborder" valign="top" width="16.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972661_p4859790610546"><a name="zh-cn_topic_0057972661_p4859790610546"></a><a name="zh-cn_topic_0057972661_p4859790610546"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="10.979999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p4411631510546"><a name="zh-cn_topic_0057972661_p4411631510546"></a><a name="zh-cn_topic_0057972661_p4411631510546"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="47.02%" headers="mcps1.2.5.1.4 "><p id="p204864456459"><a name="p204864456459"></a><a name="p204864456459"></a>卷设备名称。</p>
<div class="note" id="note0422219468"><a name="note0422219468"></a><a name="note0422219468"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p12532675472"><a name="p12532675472"></a><a name="p12532675472"></a>该字段已经废弃。</p>
<p id="zh-cn_topic_0057972661_p1665179710546"><a name="zh-cn_topic_0057972661_p1665179710546"></a><a name="zh-cn_topic_0057972661_p1665179710546"></a>用户指定的device_name不会生效，系统会默认生成一个device_name。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row34936617105358"><td class="cellrowborder" valign="top" width="25.069999999999997%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p5956509810546"><a name="zh-cn_topic_0057972661_p5956509810546"></a><a name="zh-cn_topic_0057972661_p5956509810546"></a>delete_on_termination</p>
</td>
<td class="cellrowborder" valign="top" width="16.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972661_p6004360410546"><a name="zh-cn_topic_0057972661_p6004360410546"></a><a name="zh-cn_topic_0057972661_p6004360410546"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="10.979999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p3169373810546"><a name="zh-cn_topic_0057972661_p3169373810546"></a><a name="zh-cn_topic_0057972661_p3169373810546"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="47.02%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p1705602210546"><a name="zh-cn_topic_0057972661_p1705602210546"></a><a name="zh-cn_topic_0057972661_p1705602210546"></a>删除弹性云服务器时，是否删除卷，默认值false。</p>
<p id="p1749452617197"><a name="p1749452617197"></a><a name="p1749452617197"></a>true：删除弹性云服务器时，删除卷</p>
<p id="p1149519268197"><a name="p1149519268197"></a><a name="p1149519268197"></a>false：删除弹性云服务器时，不删除卷</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row18070752105358"><td class="cellrowborder" valign="top" width="25.069999999999997%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p1870026710546"><a name="zh-cn_topic_0057972661_p1870026710546"></a><a name="zh-cn_topic_0057972661_p1870026710546"></a>boot_index</p>
</td>
<td class="cellrowborder" valign="top" width="16.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972661_p3832668110546"><a name="zh-cn_topic_0057972661_p3832668110546"></a><a name="zh-cn_topic_0057972661_p3832668110546"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="10.979999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p1745343110546"><a name="zh-cn_topic_0057972661_p1745343110546"></a><a name="zh-cn_topic_0057972661_p1745343110546"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="47.02%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p444177310546"><a name="zh-cn_topic_0057972661_p444177310546"></a><a name="zh-cn_topic_0057972661_p444177310546"></a>启动标识，“0”代表启动盘，“-1“代表非启动盘。</p>
<div class="note" id="zh-cn_topic_0057972661_note1430479894258"><a name="zh-cn_topic_0057972661_note1430479894258"></a><a name="zh-cn_topic_0057972661_note1430479894258"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0057972661_p6163432094258"><a name="zh-cn_topic_0057972661_p6163432094258"></a><a name="zh-cn_topic_0057972661_p6163432094258"></a>当卷设备的源头类型全为volume时，boot_index的值有一个为0。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row54392189105358"><td class="cellrowborder" valign="top" width="25.069999999999997%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p1682739910546"><a name="zh-cn_topic_0057972661_p1682739910546"></a><a name="zh-cn_topic_0057972661_p1682739910546"></a>uuid</p>
</td>
<td class="cellrowborder" valign="top" width="16.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972661_p2084208210546"><a name="zh-cn_topic_0057972661_p2084208210546"></a><a name="zh-cn_topic_0057972661_p2084208210546"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="10.979999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p1048705710546"><a name="zh-cn_topic_0057972661_p1048705710546"></a><a name="zh-cn_topic_0057972661_p1048705710546"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="47.02%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p4414527710546"><a name="zh-cn_topic_0057972661_p4414527710546"></a><a name="zh-cn_topic_0057972661_p4414527710546"></a>当source_type值是volume时，uuid为卷的uuid；</p>
<p id="p4942173262019"><a name="p4942173262019"></a><a name="p4942173262019"></a>当source_type值是snapshot时，uuid为快照的uuid；</p>
<p id="p15942163242015"><a name="p15942163242015"></a><a name="p15942163242015"></a>当source_type值是image时，uuid为镜像的uuid；</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row43403738105358"><td class="cellrowborder" valign="top" width="25.069999999999997%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p3676107810546"><a name="zh-cn_topic_0057972661_p3676107810546"></a><a name="zh-cn_topic_0057972661_p3676107810546"></a>volume_size</p>
</td>
<td class="cellrowborder" valign="top" width="16.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972661_p2485733610546"><a name="zh-cn_topic_0057972661_p2485733610546"></a><a name="zh-cn_topic_0057972661_p2485733610546"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="10.979999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p17832210546"><a name="zh-cn_topic_0057972661_p17832210546"></a><a name="zh-cn_topic_0057972661_p17832210546"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="47.02%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p1444414110546"><a name="zh-cn_topic_0057972661_p1444414110546"></a><a name="zh-cn_topic_0057972661_p1444414110546"></a>卷大小，整数，在source_type是image或blank，destination_type是volume的时候必选。</p>
<p id="zh-cn_topic_0057972661_p1645936993326"><a name="zh-cn_topic_0057972661_p1645936993326"></a><a name="zh-cn_topic_0057972661_p1645936993326"></a>单位为GB。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row64465110105358"><td class="cellrowborder" valign="top" width="25.069999999999997%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p6079647310546"><a name="zh-cn_topic_0057972661_p6079647310546"></a><a name="zh-cn_topic_0057972661_p6079647310546"></a>volume_type</p>
</td>
<td class="cellrowborder" valign="top" width="16.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0057972661_p2556727610546"><a name="zh-cn_topic_0057972661_p2556727610546"></a><a name="zh-cn_topic_0057972661_p2556727610546"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="10.979999999999999%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p5768348410546"><a name="zh-cn_topic_0057972661_p5768348410546"></a><a name="zh-cn_topic_0057972661_p5768348410546"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="47.02%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p4185060810546"><a name="zh-cn_topic_0057972661_p4185060810546"></a><a name="zh-cn_topic_0057972661_p4185060810546"></a>卷类型，在source_type是image，destination_type是volume时必选。</p>
<p id="p91591843125014"><a name="p91591843125014"></a><a name="p91591843125014"></a>卷类型取值范围请参考 EVS 服务 <a href="https://support.huaweicloud.com/productdesc-evs/zh-cn_topic_0044524691.html" target="_blank" rel="noopener noreferrer">磁盘类型介绍</a> 。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  security\_groups参数

<a name="zh-cn_topic_0057972661_table16920677105453"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972661_row60708739105453"><th class="cellrowborder" valign="top" width="25.740000000000002%" id="mcps1.2.5.1.1"><p id="p14804142712417"><a name="p14804142712417"></a><a name="p14804142712417"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.31%" id="mcps1.2.5.1.2"><p id="p9555122215124"><a name="p9555122215124"></a><a name="p9555122215124"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10.780000000000001%" id="mcps1.2.5.1.3"><p id="p1280402712240"><a name="p1280402712240"></a><a name="p1280402712240"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.17%" id="mcps1.2.5.1.4"><p id="p208181427132416"><a name="p208181427132416"></a><a name="p208181427132416"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972661_row6853617105453"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p3952465110557"><a name="zh-cn_topic_0057972661_p3952465110557"></a><a name="zh-cn_topic_0057972661_p3952465110557"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16.31%" headers="mcps1.2.5.1.2 "><p id="p1755572271210"><a name="p1755572271210"></a><a name="p1755572271210"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="10.780000000000001%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p4738015610557"><a name="zh-cn_topic_0057972661_p4738015610557"></a><a name="zh-cn_topic_0057972661_p4738015610557"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.17%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p1294589010557"><a name="zh-cn_topic_0057972661_p1294589010557"></a><a name="zh-cn_topic_0057972661_p1294589010557"></a>安全组名称或者uuid。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  networks参数

<a name="zh-cn_topic_0057972661_table9995892105551"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972661_row37997114105551"><th class="cellrowborder" valign="top" width="25.740000000000002%" id="mcps1.2.5.1.1"><p id="p184551730132417"><a name="p184551730132417"></a><a name="p184551730132417"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12.94%" id="mcps1.2.5.1.2"><p id="p146295264122"><a name="p146295264122"></a><a name="p146295264122"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.31%" id="mcps1.2.5.1.3"><p id="p15471830142410"><a name="p15471830142410"></a><a name="p15471830142410"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="41.010000000000005%" id="mcps1.2.5.1.4"><p id="p44711430132418"><a name="p44711430132418"></a><a name="p44711430132418"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972661_row27440950105551"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p1501087310563"><a name="zh-cn_topic_0057972661_p1501087310563"></a><a name="zh-cn_topic_0057972661_p1501087310563"></a>port</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.5.1.2 "><p id="p762942681213"><a name="p762942681213"></a><a name="p762942681213"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p792119010563"><a name="zh-cn_topic_0057972661_p792119010563"></a><a name="zh-cn_topic_0057972661_p792119010563"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p2866860910563"><a name="zh-cn_topic_0057972661_p2866860910563"></a><a name="zh-cn_topic_0057972661_p2866860910563"></a>网络port uuid。</p>
<p id="zh-cn_topic_0057972661_p5669089410563"><a name="zh-cn_topic_0057972661_p5669089410563"></a><a name="zh-cn_topic_0057972661_p5669089410563"></a>没有指定网络uuid时必须指定。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row53194686105551"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p5571052610563"><a name="zh-cn_topic_0057972661_p5571052610563"></a><a name="zh-cn_topic_0057972661_p5571052610563"></a>uuid</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.5.1.2 "><p id="p11629142618127"><a name="p11629142618127"></a><a name="p11629142618127"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p1625879010563"><a name="zh-cn_topic_0057972661_p1625879010563"></a><a name="zh-cn_topic_0057972661_p1625879010563"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p3793825410563"><a name="zh-cn_topic_0057972661_p3793825410563"></a><a name="zh-cn_topic_0057972661_p3793825410563"></a>网络uuid。</p>
<p id="zh-cn_topic_0057972661_p589997110563"><a name="zh-cn_topic_0057972661_p589997110563"></a><a name="zh-cn_topic_0057972661_p589997110563"></a>没有指定网络port时必须指定。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row58124020105551"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p611192810563"><a name="zh-cn_topic_0057972661_p611192810563"></a><a name="zh-cn_topic_0057972661_p611192810563"></a>fixed_ip</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.5.1.2 "><p id="p6629326201219"><a name="p6629326201219"></a><a name="p6629326201219"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p2530419410563"><a name="zh-cn_topic_0057972661_p2530419410563"></a><a name="zh-cn_topic_0057972661_p2530419410563"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="41.010000000000005%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p6060160810563"><a name="zh-cn_topic_0057972661_p6060160810563"></a><a name="zh-cn_topic_0057972661_p6060160810563"></a>指定的IP地址。网络的三个参数（port、uuid和fixed_ip）中，port优先级最高；指定fixed_ip时必须指明uuid。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  os:scheduler\_hints参数

<a name="zh-cn_topic_0057972661_table12534817105641"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972661_row26068168105641"><th class="cellrowborder" valign="top" width="25.740000000000002%" id="mcps1.2.5.1.1"><p id="p1858783513243"><a name="p1858783513243"></a><a name="p1858783513243"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="12.46%" id="mcps1.2.5.1.2"><p id="p165381328142"><a name="p165381328142"></a><a name="p165381328142"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21.37%" id="mcps1.2.5.1.3"><p id="p360443592415"><a name="p360443592415"></a><a name="p360443592415"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40.43%" id="mcps1.2.5.1.4"><p id="p160413532410"><a name="p160413532410"></a><a name="p160413532410"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972661_row62928048105641"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p15046690105656"><a name="zh-cn_topic_0057972661_p15046690105656"></a><a name="zh-cn_topic_0057972661_p15046690105656"></a>group</p>
</td>
<td class="cellrowborder" valign="top" width="12.46%" headers="mcps1.2.5.1.2 "><p id="p15539528147"><a name="p15539528147"></a><a name="p15539528147"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.5.1.3 "><p id="p322913253235"><a name="p322913253235"></a><a name="p322913253235"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.5.1.4 "><p id="p1711236145217"><a name="p1711236145217"></a><a name="p1711236145217"></a>反亲和性组信息。</p>
<p id="zh-cn_topic_0057972661_p4240670105656"><a name="zh-cn_topic_0057972661_p4240670105656"></a><a name="zh-cn_topic_0057972661_p4240670105656"></a>UUID格式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row64921661105641"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p39968339105656"><a name="zh-cn_topic_0057972661_p39968339105656"></a><a name="zh-cn_topic_0057972661_p39968339105656"></a>different_host</p>
</td>
<td class="cellrowborder" valign="top" width="12.46%" headers="mcps1.2.5.1.2 "><p id="p75391226145"><a name="p75391226145"></a><a name="p75391226145"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.5.1.3 "><p id="p6465152712239"><a name="p6465152712239"></a><a name="p6465152712239"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p12868562105656"><a name="zh-cn_topic_0057972661_p12868562105656"></a><a name="zh-cn_topic_0057972661_p12868562105656"></a>预留字段，当前不支持该功能。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row30356398105641"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p53049785105656"><a name="zh-cn_topic_0057972661_p53049785105656"></a><a name="zh-cn_topic_0057972661_p53049785105656"></a>same_host</p>
</td>
<td class="cellrowborder" valign="top" width="12.46%" headers="mcps1.2.5.1.2 "><p id="p17539162191416"><a name="p17539162191416"></a><a name="p17539162191416"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0057972661_p2065343105656"><a name="zh-cn_topic_0057972661_p2065343105656"></a><a name="zh-cn_topic_0057972661_p2065343105656"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p19667172105656"><a name="zh-cn_topic_0057972661_p19667172105656"></a><a name="zh-cn_topic_0057972661_p19667172105656"></a>预留字段，当前不支持该功能。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row42773507105641"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p43180380105656"><a name="zh-cn_topic_0057972661_p43180380105656"></a><a name="zh-cn_topic_0057972661_p43180380105656"></a>cidr</p>
</td>
<td class="cellrowborder" valign="top" width="12.46%" headers="mcps1.2.5.1.2 "><p id="p10539172161419"><a name="p10539172161419"></a><a name="p10539172161419"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.5.1.3 "><p id="p133891574237"><a name="p133891574237"></a><a name="p133891574237"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p5287950105656"><a name="zh-cn_topic_0057972661_p5287950105656"></a><a name="zh-cn_topic_0057972661_p5287950105656"></a>预留字段，当前不支持该功能。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row12287877105641"><td class="cellrowborder" valign="top" width="25.740000000000002%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0057972661_p29710531105656"><a name="zh-cn_topic_0057972661_p29710531105656"></a><a name="zh-cn_topic_0057972661_p29710531105656"></a>build_near_host_ip</p>
</td>
<td class="cellrowborder" valign="top" width="12.46%" headers="mcps1.2.5.1.2 "><p id="p35394214149"><a name="p35394214149"></a><a name="p35394214149"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.5.1.3 "><p id="p1670754182311"><a name="p1670754182311"></a><a name="p1670754182311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40.43%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0057972661_p53961881105656"><a name="zh-cn_topic_0057972661_p53961881105656"></a><a name="zh-cn_topic_0057972661_p53961881105656"></a>预留字段，当前不支持该功能。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="zh-cn_topic_0057972661_section32057793"></a>

响应参数如[表9](#table44736746)所示。

**表 9**  响应参数

<a name="table44736746"></a>
<table><thead align="left"><tr id="row8242429"><th class="cellrowborder" valign="top" width="21.11%" id="mcps1.2.4.1.1"><p id="p63657004"><a name="p63657004"></a><a name="p63657004"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.39%" id="mcps1.2.4.1.2"><p id="p35147813"><a name="p35147813"></a><a name="p35147813"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.5%" id="mcps1.2.4.1.3"><p id="p28400574"><a name="p28400574"></a><a name="p28400574"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row18745119"><td class="cellrowborder" valign="top" width="21.11%" headers="mcps1.2.4.1.1 "><p id="p41959665"><a name="p41959665"></a><a name="p41959665"></a>server</p>
</td>
<td class="cellrowborder" valign="top" width="29.39%" headers="mcps1.2.4.1.2 "><p id="p16804102"><a name="p16804102"></a><a name="p16804102"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="49.5%" headers="mcps1.2.4.1.3 "><p id="p36377578"><a name="p36377578"></a><a name="p36377578"></a>云服务器信息，详情请参见<a href="#zh-cn_topic_0057972661_table37882063">表10</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 10**  server字段数据结构说明

<a name="zh-cn_topic_0057972661_table37882063"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057972661_row35582587"><th class="cellrowborder" valign="top" width="28.09%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0057972661_p63617293"><a name="zh-cn_topic_0057972661_p63617293"></a><a name="zh-cn_topic_0057972661_p63617293"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.1%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0057972661_p52727095"><a name="zh-cn_topic_0057972661_p52727095"></a><a name="zh-cn_topic_0057972661_p52727095"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.81%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0057972661_p63390070"><a name="zh-cn_topic_0057972661_p63390070"></a><a name="zh-cn_topic_0057972661_p63390070"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057972661_row1032124"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972661_p16493259"><a name="zh-cn_topic_0057972661_p16493259"></a><a name="zh-cn_topic_0057972661_p16493259"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972661_p60885635"><a name="zh-cn_topic_0057972661_p60885635"></a><a name="zh-cn_topic_0057972661_p60885635"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.81%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972661_p38694667"><a name="zh-cn_topic_0057972661_p38694667"></a><a name="zh-cn_topic_0057972661_p38694667"></a>弹性云服务器ID，UUID格式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row12707688"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972661_p22689808"><a name="zh-cn_topic_0057972661_p22689808"></a><a name="zh-cn_topic_0057972661_p22689808"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972661_p25935173"><a name="zh-cn_topic_0057972661_p25935173"></a><a name="zh-cn_topic_0057972661_p25935173"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="52.81%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972661_p39701876"><a name="zh-cn_topic_0057972661_p39701876"></a><a name="zh-cn_topic_0057972661_p39701876"></a>弹性云服务器URI自描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row21772565"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972661_p18747312"><a name="zh-cn_topic_0057972661_p18747312"></a><a name="zh-cn_topic_0057972661_p18747312"></a>security_groups</p>
</td>
<td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972661_p42137308"><a name="zh-cn_topic_0057972661_p42137308"></a><a name="zh-cn_topic_0057972661_p42137308"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="52.81%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972661_p41469957"><a name="zh-cn_topic_0057972661_p41469957"></a><a name="zh-cn_topic_0057972661_p41469957"></a>弹性云服务器所在安全组。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057972661_row37685299"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972661_p32610412"><a name="zh-cn_topic_0057972661_p32610412"></a><a name="zh-cn_topic_0057972661_p32610412"></a>OS-DCF:diskConfig</p>
</td>
<td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972661_p24197721"><a name="zh-cn_topic_0057972661_p24197721"></a><a name="zh-cn_topic_0057972661_p24197721"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.81%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972661_p48788849"><a name="zh-cn_topic_0057972661_p48788849"></a><a name="zh-cn_topic_0057972661_p48788849"></a>diskConfig方式。</p>
<a name="zh-cn_topic_0057972661_ul36446461"></a><a name="zh-cn_topic_0057972661_ul36446461"></a><ul id="zh-cn_topic_0057972661_ul36446461"><li>MANUAL，镜像空间不会扩展。</li><li>AUTO，系统盘镜像空间会自动扩展为与flavor大小一致。</li></ul>
</td>
</tr>
<tr id="row11302638192316"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.1 "><p id="p18302113820232"><a name="p18302113820232"></a><a name="p18302113820232"></a>reservation_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.4.1.2 "><p id="p9302138142319"><a name="p9302138142319"></a><a name="p9302138142319"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.81%" headers="mcps1.2.4.1.3 "><div class="p" id="p139921927192516"><a name="p139921927192516"></a><a name="p139921927192516"></a>reservation_id：通过返回的reservation_id，可以过滤查询到本次创建的弹性云服务器。<div class="note" id="note11231428132513"><a name="note11231428132513"></a><a name="note11231428132513"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p112322862510"><a name="p112322862510"></a><a name="p112322862510"></a>批量创建弹性云服务器时，支持使用该字段。</p>
</div></div>
</div>
</td>
</tr>
<tr id="row928515498315"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.4.1.1 "><p id="p22879491036"><a name="p22879491036"></a><a name="p22879491036"></a>adminPass</p>
</td>
<td class="cellrowborder" valign="top" width="19.1%" headers="mcps1.2.4.1.2 "><p id="p528713493311"><a name="p528713493311"></a><a name="p528713493311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.81%" headers="mcps1.2.4.1.3 "><p id="p1628710497317"><a name="p1628710497317"></a><a name="p1628710497317"></a>Windows弹性云服务器Administrator用户的密码。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例（创建弹性云服务器）<a name="section8540539202712"></a>

请求URL示例

```
POST https://{endpoint}/v2.1/9c53a566cb3443ab910cf0daebca90c4/servers
```

**示例1：通过block\_device\_mapping\_v2使用镜像创建弹性云服务器**，请求示例如下：

```
 { 
    "server": { 
        "flavorRef": "2", 
        "name": "wjvm48", 
        "metadata": { 
            "name": "name_xx1", 
            "id": "id_xxxx1" 
        }, 
        "block_device_mapping_v2": [{ 
            "source_type": "image", 
            "destination_type": "volume", 
            "uuid": "b023fe17-11db-4efb-b800-78882a0e394b", 
            "delete_on_termination": "False", 
            "boot_index": "0",
            "volume_type": "SAS",
            "volume_size": "40"
        }], 
        "security_groups": [{ 
            "name": "name_xx5_sg" 
        }], 
        "networks": [{ 
            "uuid": "fd40e6f8-942d-4b4e-a7ae-465287b02a2c", 
            "port": "e730a11c-1a19-49cc-8797-cee2ad67af6f", 
            "fixed_ip": "10.20.30.137" 
        }], 
        "key_name": "test", 
        "user_data": "ICAgICAgDQoiQSBjbG91ZCBkb2VzIG5vdCBrbm93IHdoeSBpdCBtb3ZlcyBpbiBqdXN0IHN1Y2ggYSBkaXJlY3Rpb24gYW5kIGF0IHN1Y2ggYSBzcGVlZC4uLkl0IGZlZWxzIGFuIGltcHVsc2lvbi4uLnRoaXMgaXMgdGhlIHBsYWNlIHRvIGdvIG5vdy4gQnV0IHRoZSBza3kga25vd3MgdGhlIHJlYXNvbnMgYW5kIHRoZSBwYXR0ZXJucyBiZWhpbmQgYWxsIGNsb3VkcywgYW5kIHlvdSB3aWxsIGtub3csIHRvbywgd2hlbiB5b3UgbGlmdCB5b3Vyc2VsZiBoaWdoIGVub3VnaCB0byBzZWUgYmV5b25kIGhvcml6b25zLiINCg0KLVJpY2hhcmQgQmFjaA==", 
        "availability_zone":"az1-dc1"
    } 
}
```

**示例2：通过block\_device\_mapping\_v2使用快照创建弹性云服务器**，请求示例如下：

>![](public_sys-resources/icon-note.gif) **说明：**   
>当source\_type为snapshot时，boot\_index为0，且该快照对应的云硬盘必须为系统盘。  

```
{
    "server":{
        "name":"wjvm48",
        "availability_zone":"az1-dc1",
        "block_device_mapping_v2": [
            {
                "source_type":"snapshot",
                "boot_index":"0",
                "uuid":"df51997d-ee35-4fb3-a372-e2ac933a6565", // snapshot id，创建snapshot接口会返回id
                "destination_type":"volume"
            }
        ],
        "flavorRef":"s3.xlarge.2",
        "max_count":1,
        "min_count":1,
        "networks": [
            {
                "uuid":"79a68cef-0936-4e21-b1f4-b800ecb70246"
            }
        ] 
    } 
}
```

**示例3：通过block\_device\_mapping\_v2使用卷创建弹性云服务器**，请求示例如下：

```
{ 
    "server": { 
        "flavorRef": "2", 
        "name": "wjvm48", 
        "metadata": { 
            "name": "name_xx1", 
            "id": "id_xxxx1" 
        }, 
        "block_device_mapping_v2": [{ 
            "source_type": "volume", 
            "destination_type": "volume", 
            "uuid": "bd7e4f86-b004-4745-bea2-a55b1085f107", 
            "delete_on_termination": "False", 
            "boot_index": "0", 
            "volume_type": "dsware",
            "volume_size": "40"
        }], 
        "security_groups": [{ 
            "name": "name_xx5_sg" 
        }], 
        "networks": [{ 
            "uuid": "fd40e6f8-942d-4b4e-a7ae-465287b02a2c", 
            "port": "e730a11c-1a19-49cc-8797-cee2ad67af6f", 
            "fixed_ip": "10.20.30.137" 
        }], 
        "key_name": "test", 
        "user_data": "ICAgICAgDQoiQSBjbG91ZCBkb2VzIG5vdCBrbm93IHdoeSBpdCBtb3ZlcyBpbiBqdXN0IHN1Y2ggYSBkaXJlY3Rpb24gYW5kIGF0IHN1Y2ggYSBzcGVlZC4uLkl0IGZlZWxzIGFuIGltcHVsc2lvbi4uLnRoaXMgaXMgdGhlIHBsYWNlIHRvIGdvIG5vdy4gQnV0IHRoZSBza3kga25vd3MgdGhlIHJlYXNvbnMgYW5kIHRoZSBwYXR0ZXJucyBiZWhpbmQgYWxsIGNsb3VkcywgYW5kIHlvdSB3aWxsIGtub3csIHRvbywgd2hlbiB5b3UgbGlmdCB5b3Vyc2VsZiBoaWdoIGVub3VnaCB0byBzZWUgYmV5b25kIGhvcml6b25zLiINCg0KLVJpY2hhcmQgQmFjaA==", 
        "availability_zone":"az1-dc1"
    } 
}
```

**示例4：使用imageRef创建弹性云服务器**，请求示例如下：

```
{ 
    "server": { 
        "flavorRef": "2", 
        "name": "wjvm48", 
        "metadata": { 
            "name": "name_xx1", 
            "id": "id_xxxx1" 
        }, 
        "adminPass": "name_xx1", 
        "imageRef": "6b344c54-d606-4e1a-a99e-a7d0250c3d14",
        "security_groups": [{ 
            "name": "name_xx5_sg" 
        }], 
        "networks": [{ 
            "uuid": "fd40e6f8-942d-4b4e-a7ae-465287b02a2c",
            "port": "e730a11c-1a19-49cc-8797-cee2ad67af6f",
            "fixed_ip": "10.20.30.137" 
        }], 
        "key_name": "test", 
        "user_data": "ICAgICAgDQoiQSBjbG91ZCBkb2VzIG5vdCBrbm93IHdoeSBpdCBtb3ZlcyBpbiBqdXN0IHN1Y2ggYSBkaXJlY3Rpb24gYW5kIGF0IHN1Y2ggYSBzcGVlZC4uLkl0IGZlZWxzIGFuIGltcHVsc2lvbi4uLnRoaXMgaXMgdGhlIHBsYWNlIHRvIGdvIG5vdy4gQnV0IHRoZSBza3kga25vd3MgdGhlIHJlYXNvbnMgYW5kIHRoZSBwYXR0ZXJucyBiZWhpbmQgYWxsIGNsb3VkcywgYW5kIHlvdSB3aWxsIGtub3csIHRvbywgd2hlbiB5b3UgbGlmdCB5b3Vyc2VsZiBoaWdoIGVub3VnaCB0byBzZWUgYmV5b25kIGhvcml6b25zLiINCg0KLVJpY2hhcmQgQmFjaA==", 
        "availability_zone":"az1-dc1"
    } 
}
```

## 响应示例（创建弹性云服务器）<a name="section5933204164918"></a>

```
{
    "server": {
        "security_groups": [
            {
                "name": "name_xx5_sg"
            }
        ],
        "OS-DCF:diskConfig": " MANUAL",
        "id": "567c1557-0eca-422c-bfce-149d6b8f1bb8",
        "links": [
            {
                "href": "http://192.168.82.230:8774/v2/dc4059e8e7994f2498b514ca04cdaf44/servers/567c1557-0eca-422c-bfce-149d6b8f1bb8",
                "rel": "self"
            },
            {
                "href": "http://192.168.82.230:8774/dc4059e8e7994f2498b514ca04cdaf44/servers/567c1557-0eca-422c-bfce-149d6b8f1bb8",
                "rel": "bookmark"
            }
        ],
        "adminPass": "name_xx1"
    }
}
```

## 请求示例（批量创建弹性云服务器）<a name="section9554114338"></a>

```
{
    "server": {
        "availability_zone":"az1.dc1",
        "name": "test",
        "imageRef": "10ff4f01-35b6-4209-8397-359cb4475fa0",
        "flavorRef": "s1.medium",
        "return_reservation_id": "true",
        "networks": [
            {
                "uuid": "51bead38-d1a3-4d08-be20-0970c24b7cab"
            }
        ],
        "min_count": "2",
        "max_count": "3"
    }
}
```

## 响应示例（批量创建弹性云服务器）<a name="section4462153875112"></a>

```
{
    "reservation_id": "r-3fhpjulh"
}
```

## 返回值<a name="zh-cn_topic_0057972661_section128741313191616"></a>

请参考[通用请求返回值](通用请求返回值.md)。

