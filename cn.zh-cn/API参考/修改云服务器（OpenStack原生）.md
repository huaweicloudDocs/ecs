# 修改云服务器<a name="ZH-CN_TOPIC_0020212692"></a>

## 功能介绍<a name="section15039321"></a>

修改云服务器信息，目前支持修改云服务器名称及描述。

## URI<a name="section1136168"></a>

PUT /v2.1/\{project\_id\}/servers/\{server\_id\}

参数说明请参见[表1](#table44564854)。

**表 1**  参数说明

<a name="table44564854"></a>
<table><thead align="left"><tr id="row553045"><th class="cellrowborder" valign="top" width="17.54%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.36%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="65.10000000000001%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row10515475"><td class="cellrowborder" valign="top" width="17.54%" headers="mcps1.2.4.1.1 "><p id="p46447150"><a name="p46447150"></a><a name="p46447150"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.2.4.1.2 "><p id="p4122781"><a name="p4122781"></a><a name="p4122781"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="65.10000000000001%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row26436338165316"><td class="cellrowborder" valign="top" width="17.54%" headers="mcps1.2.4.1.1 "><p id="p31999978165316"><a name="p31999978165316"></a><a name="p31999978165316"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.2.4.1.2 "><p id="p41861457165316"><a name="p41861457165316"></a><a name="p41861457165316"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="65.10000000000001%" headers="mcps1.2.4.1.3 "><p id="p35334819165316"><a name="p35334819165316"></a><a name="p35334819165316"></a>云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section10225512"></a>

请求参数如[表2](#table13100926)所示。

**表 2**  请求参数

<a name="table13100926"></a>
<table><thead align="left"><tr id="row35303864"><th class="cellrowborder" valign="top" width="17.48%" id="mcps1.2.5.1.1"><p id="p41040744"><a name="p41040744"></a><a name="p41040744"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.29%" id="mcps1.2.5.1.2"><p id="p35965948"><a name="p35965948"></a><a name="p35965948"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="29.14%" id="mcps1.2.5.1.3"><p id="p27560669"><a name="p27560669"></a><a name="p27560669"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="36.09%" id="mcps1.2.5.1.4"><p id="p17821682"><a name="p17821682"></a><a name="p17821682"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row34270115"><td class="cellrowborder" valign="top" width="17.48%" headers="mcps1.2.5.1.1 "><p id="p24415962"><a name="p24415962"></a><a name="p24415962"></a>server</p>
</td>
<td class="cellrowborder" valign="top" width="17.29%" headers="mcps1.2.5.1.2 "><p id="p31535868"><a name="p31535868"></a><a name="p31535868"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="29.14%" headers="mcps1.2.5.1.3 "><p id="p4268531"><a name="p4268531"></a><a name="p4268531"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="36.09%" headers="mcps1.2.5.1.4 "><p id="p24751971"><a name="p24751971"></a><a name="p24751971"></a>云服务器数据结构，详情请参见<a href="#table26827213163326">表3</a></p>
</td>
</tr>
</tbody>
</table>

**表 3**  server字段数据结构说明

<a name="table26827213163326"></a>
<table><thead align="left"><tr id="row36672866163326"><th class="cellrowborder" valign="top" width="17.478252174782526%" id="mcps1.2.5.1.1"><p id="p128484161419"><a name="p128484161419"></a><a name="p128484161419"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.2982701729827%" id="mcps1.2.5.1.2"><p id="p98416417142"><a name="p98416417142"></a><a name="p98416417142"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="29.137086291370863%" id="mcps1.2.5.1.3"><p id="p118418421415"><a name="p118418421415"></a><a name="p118418421415"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="36.086391360863914%" id="mcps1.2.5.1.4"><p id="p010104141410"><a name="p010104141410"></a><a name="p010104141410"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row31760590163326"><td class="cellrowborder" valign="top" width="17.478252174782526%" headers="mcps1.2.5.1.1 "><p id="p22470979163326"><a name="p22470979163326"></a><a name="p22470979163326"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="17.2982701729827%" headers="mcps1.2.5.1.2 "><p id="p8210025163326"><a name="p8210025163326"></a><a name="p8210025163326"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="29.137086291370863%" headers="mcps1.2.5.1.3 "><p id="p61032295163326"><a name="p61032295163326"></a><a name="p61032295163326"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="36.086391360863914%" headers="mcps1.2.5.1.4 "><p id="p66475806163326"><a name="p66475806163326"></a><a name="p66475806163326"></a>修改后的云服务器名称</p>
<a name="ul1408039616488"></a><a name="ul1408039616488"></a><ul id="ul1408039616488"><li>长度大于0小于256</li></ul>
</td>
</tr>
<tr id="row1590615702514"><td class="cellrowborder" valign="top" width="17.478252174782526%" headers="mcps1.2.5.1.1 "><p id="p185271320121118"><a name="p185271320121118"></a><a name="p185271320121118"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="17.2982701729827%" headers="mcps1.2.5.1.2 "><p id="p75277203114"><a name="p75277203114"></a><a name="p75277203114"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="29.137086291370863%" headers="mcps1.2.5.1.3 "><p id="p195271620111110"><a name="p195271620111110"></a><a name="p195271620111110"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="36.086391360863914%" headers="mcps1.2.5.1.4 "><p id="p165273207113"><a name="p165273207113"></a><a name="p165273207113"></a>对弹性云服务器的任意描述，最大255字节。</p>
<p id="p5471142121113"><a name="p5471142121113"></a><a name="p5471142121113"></a>2.19版本新增</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section24920747"></a>

响应参数如[表4](#table44736746)所示。

**表 4**  响应参数

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
<td class="cellrowborder" valign="top" width="49.5%" headers="mcps1.2.4.1.3 "><p id="p36377578"><a name="p36377578"></a><a name="p36377578"></a>云服务器信息</p>
</td>
</tr>
</tbody>
</table>

**表 5**  server字段数据结构说明

<a name="table11253402"></a>
<table><thead align="left"><tr id="row10267559"><th class="cellrowborder" valign="top" width="21.05%" id="mcps1.2.4.1.1"><p id="p49911341191514"><a name="p49911341191514"></a><a name="p49911341191514"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.69%" id="mcps1.2.4.1.2"><p id="p157164271511"><a name="p157164271511"></a><a name="p157164271511"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.26%" id="mcps1.2.4.1.3"><p id="p187164216157"><a name="p187164216157"></a><a name="p187164216157"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row15663"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p1268752"><a name="p1268752"></a><a name="p1268752"></a>tenant_id</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p2786131"><a name="p2786131"></a><a name="p2786131"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p24350086"><a name="p24350086"></a><a name="p24350086"></a>租户ID或项目ID。</p>
</td>
</tr>
<tr id="row17824184"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p34472770"><a name="p34472770"></a><a name="p34472770"></a>image</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p18974148"><a name="p18974148"></a><a name="p18974148"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p1146019416233"><a name="p1146019416233"></a><a name="p1146019416233"></a>镜像ID。</p>
</td>
</tr>
<tr id="row7727977"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p21986423"><a name="p21986423"></a><a name="p21986423"></a>accessIPv4</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p1266224310514"><a name="p1266224310514"></a><a name="p1266224310514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p449319209247"><a name="p449319209247"></a><a name="p449319209247"></a>预留属性。</p>
</td>
</tr>
<tr id="row17881104563115"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p148814457312"><a name="p148814457312"></a><a name="p148814457312"></a>addresses</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p1830765712513"><a name="p1830765712513"></a><a name="p1830765712513"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p188114593120"><a name="p188114593120"></a><a name="p188114593120"></a>云服务器对应的网络地址信息。详情请参见<a href="#table3730161">表6</a>。</p>
</td>
</tr>
<tr id="row12379948143212"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p337954823220"><a name="p337954823220"></a><a name="p337954823220"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p53791648203212"><a name="p53791648203212"></a><a name="p53791648203212"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p12379154816322"><a name="p12379154816322"></a><a name="p12379154816322"></a>云服务器元数据。</p>
</td>
</tr>
<tr id="row157021310336"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p2070231193310"><a name="p2070231193310"></a><a name="p2070231193310"></a>accessIPv6</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p107026111331"><a name="p107026111331"></a><a name="p107026111331"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p2702610337"><a name="p2702610337"></a><a name="p2702610337"></a>预留属性。</p>
</td>
</tr>
<tr id="row1357051111330"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p10571121123317"><a name="p10571121123317"></a><a name="p10571121123317"></a>created</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p1057181153310"><a name="p1057181153310"></a><a name="p1057181153310"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p145717115334"><a name="p145717115334"></a><a name="p145717115334"></a>云服务器创建时间。时间格式例如：2019-05-22T03:19:19Z</p>
</td>
</tr>
<tr id="row44021729173312"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p1040292913331"><a name="p1040292913331"></a><a name="p1040292913331"></a>hostId</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p7403122973316"><a name="p7403122973316"></a><a name="p7403122973316"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p15403729103310"><a name="p15403729103310"></a><a name="p15403729103310"></a>云服务器对应的主机ID。</p>
</td>
</tr>
<tr id="row1687495133318"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p1874145116332"><a name="p1874145116332"></a><a name="p1874145116332"></a>flavor</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p1834114812515"><a name="p1834114812515"></a><a name="p1834114812515"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p1487435113336"><a name="p1487435113336"></a><a name="p1487435113336"></a>云服务器类型。</p>
</td>
</tr>
<tr id="row64807110488"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p248041174813"><a name="p248041174813"></a><a name="p248041174813"></a>OS-DCF:diskConfig</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p1848012164812"><a name="p1848012164812"></a><a name="p1848012164812"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p2048819204245"><a name="p2048819204245"></a><a name="p2048819204245"></a>扩展属性，磁盘配置方式。对镜像启动云服务器生效。</p>
</td>
</tr>
<tr id="row1625113556487"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p1025111555484"><a name="p1025111555484"></a><a name="p1025111555484"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p125175594818"><a name="p125175594818"></a><a name="p125175594818"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p192511555114814"><a name="p192511555114814"></a><a name="p192511555114814"></a>云服务器所属用户ID。</p>
</td>
</tr>
<tr id="row1696711163499"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p9968141624920"><a name="p9968141624920"></a><a name="p9968141624920"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p19968716144915"><a name="p19968716144915"></a><a name="p19968716144915"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p12968111615495"><a name="p12968111615495"></a><a name="p12968111615495"></a>修改后的云服务器名称。</p>
</td>
</tr>
<tr id="row6518308499"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p13519301498"><a name="p13519301498"></a><a name="p13519301498"></a>progress</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p13523018490"><a name="p13523018490"></a><a name="p13523018490"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p15730134916"><a name="p15730134916"></a><a name="p15730134916"></a>预留属性。</p>
</td>
</tr>
<tr id="row9985124116491"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p498534117495"><a name="p498534117495"></a><a name="p498534117495"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p35973707"><a name="p35973707"></a><a name="p35973707"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p169324165111"><a name="p169324165111"></a><a name="p169324165111"></a>云服务器相关快捷链接信息，详情请参见<a href="#table64121649">表9</a>。</p>
</td>
</tr>
<tr id="row1833531795016"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p3335417195015"><a name="p3335417195015"></a><a name="p3335417195015"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p93353179506"><a name="p93353179506"></a><a name="p93353179506"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p16335121765010"><a name="p16335121765010"></a><a name="p16335121765010"></a>云服务器唯一标识。</p>
</td>
</tr>
<tr id="row19934421115017"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p1934192114503"><a name="p1934192114503"></a><a name="p1934192114503"></a>updated</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p5466712110"><a name="p5466712110"></a><a name="p5466712110"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p3934721115015"><a name="p3934721115015"></a><a name="p3934721115015"></a>云服务器上一次更新时间。</p>
<p id="p79461929272"><a name="p79461929272"></a><a name="p79461929272"></a>时间格式例如：2019-05-22T03:19:19Z</p>
</td>
</tr>
<tr id="row43315475142"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p1253710242210"><a name="p1253710242210"></a><a name="p1253710242210"></a>locked</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p1653720241521"><a name="p1653720241521"></a><a name="p1653720241521"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p18537624422"><a name="p18537624422"></a><a name="p18537624422"></a>当云服务器被锁时为True，否则为False。</p>
<p id="p13993454402"><a name="p13993454402"></a><a name="p13993454402"></a>微版本2.9后支持</p>
</td>
</tr>
<tr id="row2806910181520"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057972887_p57463526"><a name="zh-cn_topic_0057972887_p57463526"></a><a name="zh-cn_topic_0057972887_p57463526"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057972887_p24034004"><a name="zh-cn_topic_0057972887_p24034004"></a><a name="zh-cn_topic_0057972887_p24034004"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057972887_p48379233"><a name="zh-cn_topic_0057972887_p48379233"></a><a name="zh-cn_topic_0057972887_p48379233"></a>弹性云服务器的描述信息。</p>
<p id="p28201545155518"><a name="p28201545155518"></a><a name="p28201545155518"></a>微版本2.19后支持</p>
</td>
</tr>
<tr id="row8354844101514"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p749372082418"><a name="p749372082418"></a><a name="p749372082418"></a>tags</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p14493420142420"><a name="p14493420142420"></a><a name="p14493420142420"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p1620274611333"><a name="p1620274611333"></a><a name="p1620274611333"></a>云服务器的标签列表。</p>
<p id="p1149310203247"><a name="p1149310203247"></a><a name="p1149310203247"></a>微版本2.26后支持，如果不使用微版本查询，响应中无tags字段。</p>
<div class="p" id="p7300949059"><a name="p7300949059"></a><a name="p7300949059"></a>系统近期对标签功能进行了升级，升级后，返回的tag值遵循如下规则：<a name="zh-cn_topic_0020212689_ul871515496611"></a><a name="zh-cn_topic_0020212689_ul871515496611"></a><ul id="zh-cn_topic_0020212689_ul871515496611"><li>key与value使用“=”连接，如“key=value”。</li><li>如果value为空字符串，则仅返回key。</li></ul>
</div>
<a name="zh-cn_topic_0020212689_ul871515496611_1"></a><a name="zh-cn_topic_0020212689_ul871515496611_1"></a><ul id="zh-cn_topic_0020212689_ul871515496611_1"><li>key与value使用“=”连接，如“key=value”。</li><li>如果value为空字符串，则仅返回key。</li></ul>
</td>
</tr>
<tr id="row61813343508"><td class="cellrowborder" valign="top" width="21.05%" headers="mcps1.2.4.1.1 "><p id="p131883455011"><a name="p131883455011"></a><a name="p131883455011"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.4.1.2 "><p id="p518143415010"><a name="p518143415010"></a><a name="p518143415010"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.26%" headers="mcps1.2.4.1.3 "><p id="p2018153465013"><a name="p2018153465013"></a><a name="p2018153465013"></a>云服务器状态。</p>
<p id="p3162102155817"><a name="p3162102155817"></a><a name="p3162102155817"></a>取值范围：</p>
<p id="p10449173112588"><a name="p10449173112588"></a><a name="p10449173112588"></a>ACTIVE， BUILD，ERROR，HARD_REBOOT，MIGRATING，REBOOT，RESIZE，REVERT_RESIZE，SHELVED，SHELVED_OFFLOADED，SHUTOFF，UNKNOWN，VERIFY_RESIZE</p>
<p id="p19518218542"><a name="p19518218542"></a><a name="p19518218542"></a>弹性云服务器状态说明请参考<a href="云服务器状态.md">云服务器状态</a></p>
</td>
</tr>
</tbody>
</table>

**表 6**  addresses字段数据结构说明

<a name="table3730161"></a>
<table><thead align="left"><tr id="row20014316"><th class="cellrowborder" valign="top" width="21.497850214978502%" id="mcps1.2.4.1.1"><p id="p1191618499157"><a name="p1191618499157"></a><a name="p1191618499157"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.947005299470053%" id="mcps1.2.4.1.2"><p id="p9916194916152"><a name="p9916194916152"></a><a name="p9916194916152"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.555144485551445%" id="mcps1.2.4.1.3"><p id="p391614915151"><a name="p391614915151"></a><a name="p391614915151"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row57432766"><td class="cellrowborder" valign="top" width="21.497850214978502%" headers="mcps1.2.4.1.1 "><p id="p2057412833316"><a name="p2057412833316"></a><a name="p2057412833316"></a>弹性云服务器所属网络的名称。</p>
</td>
<td class="cellrowborder" valign="top" width="29.947005299470053%" headers="mcps1.2.4.1.2 "><p id="p4439518115623"><a name="p4439518115623"></a><a name="p4439518115623"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48.555144485551445%" headers="mcps1.2.4.1.3 "><p id="p19891184119819"><a name="p19891184119819"></a><a name="p19891184119819"></a>弹性云服务器所属网络信息。</p>
<a name="ul1197110522819"></a><a name="ul1197110522819"></a><ul id="ul1197110522819"><li>key为网络名名称，如“demo_net”。</li><li>value为网络详细信息。</li></ul>
<p id="p204137567134"><a name="p204137567134"></a><a name="p204137567134"></a>详情请参见<a href="#table1656029015527">表7</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  弹性云服务器所属网络信息数据结构说明

<a name="table1656029015527"></a>
<table><thead align="left"><tr id="row2645284715527"><th class="cellrowborder" valign="top" width="22.772277227722775%" id="mcps1.2.4.1.1"><p id="p1986420536154"><a name="p1986420536154"></a><a name="p1986420536154"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="28.71287128712871%" id="mcps1.2.4.1.2"><p id="p148649536156"><a name="p148649536156"></a><a name="p148649536156"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.51485148514851%" id="mcps1.2.4.1.3"><p id="p486414537159"><a name="p486414537159"></a><a name="p486414537159"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5009697415527"><td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.1 "><p id="p3132311415527"><a name="p3132311415527"></a><a name="p3132311415527"></a>addr</p>
</td>
<td class="cellrowborder" valign="top" width="28.71287128712871%" headers="mcps1.2.4.1.2 "><p id="p5414433915527"><a name="p5414433915527"></a><a name="p5414433915527"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.51485148514851%" headers="mcps1.2.4.1.3 "><p id="p2361534415527"><a name="p2361534415527"></a><a name="p2361534415527"></a>IP地址信息。</p>
</td>
</tr>
<tr id="row1121151015527"><td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.1 "><p id="p3571711715527"><a name="p3571711715527"></a><a name="p3571711715527"></a>version</p>
</td>
<td class="cellrowborder" valign="top" width="28.71287128712871%" headers="mcps1.2.4.1.2 "><p id="p740535615527"><a name="p740535615527"></a><a name="p740535615527"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="48.51485148514851%" headers="mcps1.2.4.1.3 "><p id="p6296298815527"><a name="p6296298815527"></a><a name="p6296298815527"></a>IP地址类型，值为4或6。</p>
<a name="ul2979598615527"></a><a name="ul2979598615527"></a><ul id="ul2979598615527"><li>4：IP地址类型是IPv4</li><li>6：IP地址类型是IPv6</li></ul>
</td>
</tr>
</tbody>
</table>

**表 8**  flavor字段数据结构说明

<a name="table19588408"></a>
<table><thead align="left"><tr id="row65668512"><th class="cellrowborder" valign="top" width="21.37%" id="mcps1.2.4.1.1"><p id="p445185741513"><a name="p445185741513"></a><a name="p445185741513"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.2%" id="mcps1.2.4.1.2"><p id="p6466185761518"><a name="p6466185761518"></a><a name="p6466185761518"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.43%" id="mcps1.2.4.1.3"><p id="p1546645715151"><a name="p1546645715151"></a><a name="p1546645715151"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row54114449"><td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.4.1.1 "><p id="p21194271"><a name="p21194271"></a><a name="p21194271"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="30.2%" headers="mcps1.2.4.1.2 "><p id="p6046963"><a name="p6046963"></a><a name="p6046963"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.43%" headers="mcps1.2.4.1.3 "><p id="p20041994"><a name="p20041994"></a><a name="p20041994"></a>云服务器类型ID。</p>
</td>
</tr>
<tr id="row46160221"><td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.4.1.1 "><p id="p47990424"><a name="p47990424"></a><a name="p47990424"></a>links</p>
</td>
<td class="cellrowborder" valign="top" width="30.2%" headers="mcps1.2.4.1.2 "><p id="p57492083"><a name="p57492083"></a><a name="p57492083"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="48.43%" headers="mcps1.2.4.1.3 "><p id="p35797372"><a name="p35797372"></a><a name="p35797372"></a>云服务器类型相关快捷链接信息，详情请参见<a href="#table64121649">表9</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  links字段数据结构说明

<a name="table64121649"></a>
<table><thead align="left"><tr id="row59320951"><th class="cellrowborder" valign="top" width="21.18%" id="mcps1.2.4.1.1"><p id="p19525409166"><a name="p19525409166"></a><a name="p19525409166"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="29.64%" id="mcps1.2.4.1.2"><p id="p15255041613"><a name="p15255041613"></a><a name="p15255041613"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.18%" id="mcps1.2.4.1.3"><p id="p452516061611"><a name="p452516061611"></a><a name="p452516061611"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row61486274"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.4.1.1 "><p id="p14332335"><a name="p14332335"></a><a name="p14332335"></a>rel</p>
</td>
<td class="cellrowborder" valign="top" width="29.64%" headers="mcps1.2.4.1.2 "><p id="p14933841"><a name="p14933841"></a><a name="p14933841"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.18%" headers="mcps1.2.4.1.3 "><p id="p1681623"><a name="p1681623"></a><a name="p1681623"></a>快捷链接标记名称。</p>
</td>
</tr>
<tr id="row15134612"><td class="cellrowborder" valign="top" width="21.18%" headers="mcps1.2.4.1.1 "><p id="p17944037"><a name="p17944037"></a><a name="p17944037"></a>href</p>
</td>
<td class="cellrowborder" valign="top" width="29.64%" headers="mcps1.2.4.1.2 "><p id="p21885054"><a name="p21885054"></a><a name="p21885054"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="49.18%" headers="mcps1.2.4.1.3 "><p id="p27858965"><a name="p27858965"></a><a name="p27858965"></a>对应快捷链接。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section191304136165"></a>

```
PUT https://{endpoint}/v2.1/{project_id}/servers/{server_id}
```

```
{
    "server": {
        "name": "new-server-test"
    }
}
```

## 响应示例<a name="section1845702716524"></a>

```
{
  "server": {
    "tenant_id": "7910a6e50b80402ba028c8d96c1b31fe",
    "image": "",
    "accessIPv4": "",
    "addresses": {
      "03be5c1e-e05d-4905-a105-c3bd9b730bdc": [
        {
          "addr": "192.168.0.72",
          "version": 4
        }
      ]
    },
    "metadata": {},
    "accessIPv6": "",
    "created": "2018-05-17T03:15:48Z",
    "hostId": "7dc82f6b1d406200fc63e395cf4829cbffcb49de0e9c75c5773f201f",
    "flavor": {
      "links": [
        {
          "rel": "bookmark",
          "href": "https://None/7910a6e50b80402ba028c8d96c1b31fe/flavors/c3.1U1G"
        }
      ],
      "id": "c3.1U1G"
    },
    "OS-DCF:diskConfig": "MANUAL",
    "user_id": "d698a78532ca430f8daec1858f2b500e",
    "name": "new-server-test",
    "progress": 0,
    "links": [
      {
        "rel": "self",
        "href": "https://None/v2/7910a6e50b80402ba028c8d96c1b31fe/servers/1a19ef4f-be0a-4526-bf2f-14b4464d536a"
      },
      {
        "rel": "bookmark",
        "href": "https://None/7910a6e50b80402ba028c8d96c1b31fe/servers/1a19ef4f-be0a-4526-bf2f-14b4464d536a"
      }
    ],
    "id": "1a19ef4f-be0a-4526-bf2f-14b4464d536a",
    "updated": "2018-05-21T00:36:27Z",
    "status": "ACTIVE"
  }
}
```

## 返回值<a name="section22960139"></a>

请参考[通用请求返回值](通用请求返回值.md)。

