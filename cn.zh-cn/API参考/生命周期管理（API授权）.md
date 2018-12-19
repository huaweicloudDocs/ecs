# 生命周期管理<a name="ZH-CN_TOPIC_0103071510"></a>

<a name="table1587111571724"></a>
<table><thead align="left"><tr id="row5871165713215"><th class="cellrowborder" valign="top" width="44.44444444444445%" id="mcps1.1.4.1.1"><p id="p11871195719215"><a name="p11871195719215"></a><a name="p11871195719215"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="29.629629629629626%" id="mcps1.1.4.1.2"><p id="p28621644185118"><a name="p28621644185118"></a><a name="p28621644185118"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25.925925925925924%" id="mcps1.1.4.1.3"><p id="p38711657129"><a name="p38711657129"></a><a name="p38711657129"></a>授权项</p>
</th>
</tr>
</thead>
<tbody><tr id="row38713577219"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p123373351310"><a name="p123373351310"></a><a name="p123373351310"></a>GET /v2/{project_id}/servers/detail</p>
<p id="p16337193516315"><a name="p16337193516315"></a><a name="p16337193516315"></a>GET /v2.1/{project_id}/servers/detail</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p369615322438"><a name="p369615322438"></a><a name="p369615322438"></a>查询云服务器详情列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul1933753518319"></a><a name="ul1933753518319"></a><ul id="ul1933753518319"><li>ecs:servers:list</li><li>ecs:servers:get</li></ul>
<a name="ul933763510316"></a><a name="ul933763510316"></a><ul id="ul933763510316"><li>ecs:serverVolumes:use</li><li>ecs:diskConfigs:use</li><li>ecs:securityGroups:use</li><li>ecs:serverKeypairs:get</li></ul>
<a name="ul1033718356310"></a><a name="ul1033718356310"></a><ul id="ul1033718356310"><li>vpc:securityGroups:list</li><li>vpc:securityGroups:get</li><li>vpc:securityGroupRules:get</li><li>vpc:networks:get</li><li>vpc:subnets:get</li><li>vpc:ports:get</li><li>vpc:routers:get</li></ul>
</td>
</tr>
<tr id="row58713574219"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p172163919520"><a name="p172163919520"></a><a name="p172163919520"></a>GET /v2/{tenant_id}/servers</p>
<p id="p9721639357"><a name="p9721639357"></a><a name="p9721639357"></a>GET /v2.1/{tenant_id}/servers</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p1386254410510"><a name="p1386254410510"></a><a name="p1386254410510"></a>查询云服务器列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul372239658"></a><a name="ul372239658"></a><ul id="ul372239658"><li>ecs:servers:list</li></ul>
</td>
</tr>
<tr id="row88711057321"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p7726391956"><a name="p7726391956"></a><a name="p7726391956"></a>GET /v2/{project_id}/servers/{server_id}</p>
<p id="p2723392051"><a name="p2723392051"></a><a name="p2723392051"></a>GET /v2.1/{project_id}/servers/{server_id}</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p108621644105118"><a name="p108621644105118"></a><a name="p108621644105118"></a>查询云服务器详情（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul87293914516"></a><a name="ul87293914516"></a><ul id="ul87293914516"><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row8261737111713"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p1478183141917"><a name="p1478183141917"></a><a name="p1478183141917"></a>POST /v2/{tenant_id}/cloudservers/{server_id}/changeos</p>
<p id="p144788317197"><a name="p144788317197"></a><a name="p144788317197"></a>POST /v1/{tenant_id}/cloudservers/{server_id}/changeos</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p4183378205559"><a name="p4183378205559"></a><a name="p4183378205559"></a>切换弹性云服务器操作系统</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul747812371910"></a><a name="ul747812371910"></a><ul id="ul747812371910"><li>ecs:cloudServers:changeOS</li></ul>
</td>
</tr>
<tr id="row1542514408176"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p54781035190"><a name="p54781035190"></a><a name="p54781035190"></a>POST /v2/{tenant_id}/cloudservers/{server_id}/reinstallos</p>
<p id="p134786313191"><a name="p134786313191"></a><a name="p134786313191"></a>POST /v1/{tenant_id}/cloudservers/{server_id}/reinstallos</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p1993921813394"><a name="p1993921813394"></a><a name="p1993921813394"></a>重装弹性云服务器操作系统</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul047811315199"></a><a name="ul047811315199"></a><ul id="ul047811315199"><li>ecs:cloudServers:rebuild</li></ul>
</td>
</tr>
<tr id="row176116473177"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p204781139197"><a name="p204781139197"></a><a name="p204781139197"></a>POST /v1/{tenant_id}/cloudservers/{server_id}/resize</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p1686224415113"><a name="p1686224415113"></a><a name="p1686224415113"></a>变更云服务器规格</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul194781331914"></a><a name="ul194781331914"></a><ul id="ul194781331914"><li>ecs:cloudServers:resize</li></ul>
</td>
</tr>
<tr id="row137611507177"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p1479123111913"><a name="p1479123111913"></a><a name="p1479123111913"></a>POST /v1/{tenant_id}/cloudservers/action</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p138621244115117"><a name="p138621244115117"></a><a name="p138621244115117"></a>批量关闭云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul1747923181916"></a><a name="ul1747923181916"></a><ul id="ul1747923181916"><li>ecs:cloudServers:stop</li></ul>
</td>
</tr>
<tr id="row17373916184"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p78289223194"><a name="p78289223194"></a><a name="p78289223194"></a>POST /v1/{tenant_id}/cloudservers/action</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p086234415116"><a name="p086234415116"></a><a name="p086234415116"></a>批量重启云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul78281922151917"></a><a name="ul78281922151917"></a><ul id="ul78281922151917"><li>ecs:cloudServers:reboot</li></ul>
</td>
</tr>
<tr id="row293217122187"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p138281922141912"><a name="p138281922141912"></a><a name="p138281922141912"></a>POST /v1/{tenant_id}/cloudservers/action</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p10531190133710"><a name="p10531190133710"></a><a name="p10531190133710"></a>批量启动云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul188281122151915"></a><a name="ul188281122151915"></a><ul id="ul188281122151915"><li>ecs:cloudServers:start</li></ul>
</td>
</tr>
<tr id="row74181618188"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p1382822218198"><a name="p1382822218198"></a><a name="p1382822218198"></a>POST /v1/{tenant_id}/cloudservers/delete</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p08634442517"><a name="p08634442517"></a><a name="p08634442517"></a>删除云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul12828162216195"></a><a name="ul12828162216195"></a><ul id="ul12828162216195"><li>ecs:cloudServers:delete</li></ul>
</td>
</tr>
<tr id="row14434415191919"><td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.1 "><p id="p9828202281915"><a name="p9828202281915"></a><a name="p9828202281915"></a>POST /v1/{tenant_id}/cloudservers</p>
</td>
<td class="cellrowborder" valign="top" width="29.629629629629626%" headers="mcps1.1.4.1.2 "><p id="p1286344465110"><a name="p1286344465110"></a><a name="p1286344465110"></a>创建云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul9828142210192"></a><a name="ul9828142210192"></a><ul id="ul9828142210192"><li>ecs:cloudServers:create</li></ul>
</td>
</tr>
</tbody>
</table>

