# 网卡管理<a name="ZH-CN_TOPIC_0103071513"></a>

<a name="table166711250142311"></a>
<table><thead align="left"><tr id="row16721750172310"><th class="cellrowborder" valign="top" width="12.64%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="28.449999999999996%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="23.53%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="16.150000000000002%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="10.8%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="8.43%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row9867181434418"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.1.7.1.1 "><p id="p1068222319101"><a name="p1068222319101"></a><a name="p1068222319101"></a>云服务器网卡配置私有IP</p>
</td>
<td class="cellrowborder" valign="top" width="28.449999999999996%" headers="mcps1.1.7.1.2 "><p id="p183578185443"><a name="p183578185443"></a><a name="p183578185443"></a>PUT /v1/{project_id}/cloudservers/nics/{nic_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.1.7.1.3 "><p id="p125912581156"><a name="p125912581156"></a><a name="p125912581156"></a>ecs:cloudServerNics:update</p>
</td>
<td class="cellrowborder" valign="top" width="16.150000000000002%" headers="mcps1.1.7.1.4 "><p id="p136271643191017"><a name="p136271643191017"></a><a name="p136271643191017"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.8%" headers="mcps1.1.7.1.5 "><p id="p1420517411778"><a name="p1420517411778"></a><a name="p1420517411778"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.43%" headers="mcps1.1.7.1.6 "><p id="p1420512411172"><a name="p1420512411172"></a><a name="p1420512411172"></a>×</p>
</td>
</tr>
<tr id="row1791015116446"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.1.7.1.1 "><p id="p12682152312102"><a name="p12682152312102"></a><a name="p12682152312102"></a>批量删除云服务器网卡</p>
</td>
<td class="cellrowborder" valign="top" width="28.449999999999996%" headers="mcps1.1.7.1.2 "><p id="p18358191824417"><a name="p18358191824417"></a><a name="p18358191824417"></a>POST /v1/{project_id}/cloudservers/{server_id}/nics/delete</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.1.7.1.3 "><p id="p1132105912153"><a name="p1132105912153"></a><a name="p1132105912153"></a>ecs:cloudServerNics:delete</p>
</td>
<td class="cellrowborder" valign="top" width="16.150000000000002%" headers="mcps1.1.7.1.4 "><p id="p16274436104"><a name="p16274436104"></a><a name="p16274436104"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.8%" headers="mcps1.1.7.1.5 "><p id="p1664815301497"><a name="p1664815301497"></a><a name="p1664815301497"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.43%" headers="mcps1.1.7.1.6 "><p id="p13686132019819"><a name="p13686132019819"></a><a name="p13686132019819"></a>√</p>
</td>
</tr>
<tr id="row13910171120449"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.1.7.1.1 "><p id="p06821523181013"><a name="p06821523181013"></a><a name="p06821523181013"></a>批量添加云服务器网卡</p>
</td>
<td class="cellrowborder" valign="top" width="28.449999999999996%" headers="mcps1.1.7.1.2 "><p id="p1435951874411"><a name="p1435951874411"></a><a name="p1435951874411"></a>POST /v1/{project_id}/cloudservers/{server_id}/nics</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.1.7.1.3 "><p id="p1379095914150"><a name="p1379095914150"></a><a name="p1379095914150"></a>ecs:cloudServers:addNics</p>
</td>
<td class="cellrowborder" valign="top" width="16.150000000000002%" headers="mcps1.1.7.1.4 "><p id="p166271143121010"><a name="p166271143121010"></a><a name="p166271143121010"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.8%" headers="mcps1.1.7.1.5 "><p id="p101241559171118"><a name="p101241559171118"></a><a name="p101241559171118"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.43%" headers="mcps1.1.7.1.6 "><p id="p9124195910119"><a name="p9124195910119"></a><a name="p9124195910119"></a>√</p>
</td>
</tr>
<tr id="row1973917711447"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.1.7.1.1 "><p id="p2682192371010"><a name="p2682192371010"></a><a name="p2682192371010"></a>查询云服务器网卡信息</p>
</td>
<td class="cellrowborder" valign="top" width="28.449999999999996%" headers="mcps1.1.7.1.2 "><p id="p63609181440"><a name="p63609181440"></a><a name="p63609181440"></a>GET /v1/{project_id}/cloudservers/{server_id}/os-interface</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.1.7.1.3 "><p id="p1074317051618"><a name="p1074317051618"></a><a name="p1074317051618"></a>ecs:cloudServers:get</p>
</td>
<td class="cellrowborder" valign="top" width="16.150000000000002%" headers="mcps1.1.7.1.4 "><p id="p11627743171010"><a name="p11627743171010"></a><a name="p11627743171010"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.8%" headers="mcps1.1.7.1.5 "><p id="p1391201120"><a name="p1391201120"></a><a name="p1391201120"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.43%" headers="mcps1.1.7.1.6 "><p id="p10913013120"><a name="p10913013120"></a><a name="p10913013120"></a>√</p>
</td>
</tr>
<tr id="row2672125032316"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.1.7.1.1 "><p id="p156821823161013"><a name="p156821823161013"></a><a name="p156821823161013"></a>添加云服务器网卡（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.449999999999996%" headers="mcps1.1.7.1.2 "><p id="p1210593418340"><a name="p1210593418340"></a><a name="p1210593418340"></a>POST /v2.1/{project_id}/servers/{server_id}/os-interface</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.1.7.1.3 "><p id="p78433901616"><a name="p78433901616"></a><a name="p78433901616"></a>ecs:serverInterfaces:use</p>
</td>
<td class="cellrowborder" valign="top" width="16.150000000000002%" headers="mcps1.1.7.1.4 "><p id="p172591116167"><a name="p172591116167"></a><a name="p172591116167"></a>ecs:serverInterfaces:get</p>
<p id="p1268831221614"><a name="p1268831221614"></a><a name="p1268831221614"></a>vpc:networks:get</p>
<p id="p7319713161611"><a name="p7319713161611"></a><a name="p7319713161611"></a>vpc:networks:update</p>
<p id="p1820301431613"><a name="p1820301431613"></a><a name="p1820301431613"></a>vpc:subnets:get</p>
<p id="p168551591611"><a name="p168551591611"></a><a name="p168551591611"></a>vpc:subnets:update</p>
<p id="p296111581614"><a name="p296111581614"></a><a name="p296111581614"></a>vpc:ports:create</p>
<p id="p20825151611165"><a name="p20825151611165"></a><a name="p20825151611165"></a>vpc:ports:update</p>
<p id="p16691201714168"><a name="p16691201714168"></a><a name="p16691201714168"></a>vpc:ports:get</p>
<p id="p1832917182160"><a name="p1832917182160"></a><a name="p1832917182160"></a>vpc:networks:create</p>
<p id="p131356195166"><a name="p131356195166"></a><a name="p131356195166"></a>vpc:subnets:create</p>
<p id="p182606202160"><a name="p182606202160"></a><a name="p182606202160"></a>vpc:routers:get</p>
<p id="p17254102114164"><a name="p17254102114164"></a><a name="p17254102114164"></a>vpc:routers:update</p>
</td>
<td class="cellrowborder" valign="top" width="10.8%" headers="mcps1.1.7.1.5 "><p id="p11499174511110"><a name="p11499174511110"></a><a name="p11499174511110"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.43%" headers="mcps1.1.7.1.6 "><p id="p7499184519112"><a name="p7499184519112"></a><a name="p7499184519112"></a>×</p>
</td>
</tr>
<tr id="row06721150152313"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.1.7.1.1 "><p id="p6682152312102"><a name="p6682152312102"></a><a name="p6682152312102"></a>删除云服务器网卡（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.449999999999996%" headers="mcps1.1.7.1.2 "><p id="p1821244653411"><a name="p1821244653411"></a><a name="p1821244653411"></a>DELETE /v2.1/{project_id}/servers/{server_id}/os-interface/{id}</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.1.7.1.3 "><p id="p1480422731616"><a name="p1480422731616"></a><a name="p1480422731616"></a>ecs:serverInterfaces:use</p>
</td>
<td class="cellrowborder" valign="top" width="16.150000000000002%" headers="mcps1.1.7.1.4 "><p id="p179808295168"><a name="p179808295168"></a><a name="p179808295168"></a>ecs:serverInterfaces:get</p>
<p id="p191821831141619"><a name="p191821831141619"></a><a name="p191821831141619"></a>ecs:servers:get</p>
<p id="p389633171615"><a name="p389633171615"></a><a name="p389633171615"></a>vpc:networks:create</p>
<p id="p359311321169"><a name="p359311321169"></a><a name="p359311321169"></a>vpc:subnets:create</p>
<p id="p8170133131615"><a name="p8170133131615"></a><a name="p8170133131615"></a>vpc:networks:get</p>
<p id="p18724133111615"><a name="p18724133111615"></a><a name="p18724133111615"></a>vpc:networks:update</p>
<p id="p85481342161"><a name="p85481342161"></a><a name="p85481342161"></a>vpc:subnets:get</p>
<p id="p104832035111615"><a name="p104832035111615"></a><a name="p104832035111615"></a>vpc:subnets:update</p>
<p id="p7294136111617"><a name="p7294136111617"></a><a name="p7294136111617"></a>vpc:ports:delete</p>
<p id="p2954173613166"><a name="p2954173613166"></a><a name="p2954173613166"></a>vpc:ports:update</p>
<p id="p366913717162"><a name="p366913717162"></a><a name="p366913717162"></a>vpc:ports:get</p>
<p id="p44421838181613"><a name="p44421838181613"></a><a name="p44421838181613"></a>vpc:routers:get</p>
<p id="p14216183916168"><a name="p14216183916168"></a><a name="p14216183916168"></a>vpc:routers:update</p>
</td>
<td class="cellrowborder" valign="top" width="10.8%" headers="mcps1.1.7.1.5 "><p id="p1866264716110"><a name="p1866264716110"></a><a name="p1866264716110"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.43%" headers="mcps1.1.7.1.6 "><p id="p466216470118"><a name="p466216470118"></a><a name="p466216470118"></a>×</p>
</td>
</tr>
<tr id="row46721250112312"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.1.7.1.1 "><p id="p1868215234102"><a name="p1868215234102"></a><a name="p1868215234102"></a>查询云服务器网卡信息列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.449999999999996%" headers="mcps1.1.7.1.2 "><p id="p126512573342"><a name="p126512573342"></a><a name="p126512573342"></a>GET /v2.1/{project_id}/servers/{server_id}/os-interface</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.1.7.1.3 "><p id="p198714421612"><a name="p198714421612"></a><a name="p198714421612"></a>ecs:serverInterfaces:get</p>
</td>
<td class="cellrowborder" valign="top" width="16.150000000000002%" headers="mcps1.1.7.1.4 "><p id="p17627174310103"><a name="p17627174310103"></a><a name="p17627174310103"></a>vpc:ports:get</p>
</td>
<td class="cellrowborder" valign="top" width="10.8%" headers="mcps1.1.7.1.5 "><p id="p13829114921116"><a name="p13829114921116"></a><a name="p13829114921116"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.43%" headers="mcps1.1.7.1.6 "><p id="p68299491116"><a name="p68299491116"></a><a name="p68299491116"></a>×</p>
</td>
</tr>
<tr id="row14673195092318"><td class="cellrowborder" valign="top" width="12.64%" headers="mcps1.1.7.1.1 "><p id="p96824239102"><a name="p96824239102"></a><a name="p96824239102"></a>查询指定云服务器网卡信息（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.449999999999996%" headers="mcps1.1.7.1.2 "><p id="p84616163514"><a name="p84616163514"></a><a name="p84616163514"></a>GET /v2.1/{project_id}/servers/{server_id}/os-interface/{id}</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.1.7.1.3 "><p id="p3761145017162"><a name="p3761145017162"></a><a name="p3761145017162"></a>ecs:serverInterfaces:get</p>
</td>
<td class="cellrowborder" valign="top" width="16.150000000000002%" headers="mcps1.1.7.1.4 "><p id="p730774919163"><a name="p730774919163"></a><a name="p730774919163"></a>vpc:ports:get</p>
</td>
<td class="cellrowborder" valign="top" width="10.8%" headers="mcps1.1.7.1.5 "><p id="p16339125181119"><a name="p16339125181119"></a><a name="p16339125181119"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.43%" headers="mcps1.1.7.1.6 "><p id="p633919516113"><a name="p633919516113"></a><a name="p633919516113"></a>×</p>
</td>
</tr>
</tbody>
</table>

