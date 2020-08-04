# 元数据管理<a name="ZH-CN_TOPIC_0103071516"></a>

<a name="table144485372515"></a>
<table><thead align="left"><tr id="row7456538256"><th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="28.54%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="23.18%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="17.73%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="9.6%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="8.83%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row74519536251"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.1.7.1.1 "><p id="p15111021151510"><a name="p15111021151510"></a><a name="p15111021151510"></a>查询云服务器元数据列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.1.7.1.2 "><p id="p1153135543716"><a name="p1153135543716"></a><a name="p1153135543716"></a>GET /v2.1/{project_id}/servers/{server_id}/metadata</p>
</td>
<td class="cellrowborder" valign="top" width="23.18%" headers="mcps1.1.7.1.3 "><p id="p14132141712211"><a name="p14132141712211"></a><a name="p14132141712211"></a>ecs:servers:listMetadata</p>
</td>
<td class="cellrowborder" valign="top" width="17.73%" headers="mcps1.1.7.1.4 "><p id="p20960169150"><a name="p20960169150"></a><a name="p20960169150"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.6%" headers="mcps1.1.7.1.5 "><p id="p1726916409147"><a name="p1726916409147"></a><a name="p1726916409147"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.83%" headers="mcps1.1.7.1.6 "><p id="p12269154011420"><a name="p12269154011420"></a><a name="p12269154011420"></a>×</p>
</td>
</tr>
<tr id="row154545313252"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.1.7.1.1 "><p id="p1351112181510"><a name="p1351112181510"></a><a name="p1351112181510"></a>获取云服务器指定Key的元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.1.7.1.2 "><p id="p7601164133811"><a name="p7601164133811"></a><a name="p7601164133811"></a>GET /v2.1/{project_id}/servers/{server_id}/metadata/{key}</p>
</td>
<td class="cellrowborder" valign="top" width="23.18%" headers="mcps1.1.7.1.3 "><p id="p624151832110"><a name="p624151832110"></a><a name="p624151832110"></a>ecs:servers:getMetadata</p>
</td>
<td class="cellrowborder" valign="top" width="17.73%" headers="mcps1.1.7.1.4 "><p id="p79609681514"><a name="p79609681514"></a><a name="p79609681514"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.6%" headers="mcps1.1.7.1.5 "><p id="p4240123831612"><a name="p4240123831612"></a><a name="p4240123831612"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.83%" headers="mcps1.1.7.1.6 "><p id="p624023820165"><a name="p624023820165"></a><a name="p624023820165"></a>×</p>
</td>
</tr>
<tr id="row1745115392512"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.1.7.1.1 "><p id="p25111721141518"><a name="p25111721141518"></a><a name="p25111721141518"></a>删除云服务器指定元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.1.7.1.2 "><p id="p84681716163817"><a name="p84681716163817"></a><a name="p84681716163817"></a>DELETE /v2.1/{project_id}/servers/{server_id}/metadata/{key}</p>
</td>
<td class="cellrowborder" valign="top" width="23.18%" headers="mcps1.1.7.1.3 "><p id="p23294199214"><a name="p23294199214"></a><a name="p23294199214"></a>ecs:servers:setMetadata</p>
</td>
<td class="cellrowborder" valign="top" width="17.73%" headers="mcps1.1.7.1.4 "><p id="p296014691515"><a name="p296014691515"></a><a name="p296014691515"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.6%" headers="mcps1.1.7.1.5 "><p id="p1342473912162"><a name="p1342473912162"></a><a name="p1342473912162"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.83%" headers="mcps1.1.7.1.6 "><p id="p94241039201611"><a name="p94241039201611"></a><a name="p94241039201611"></a>×</p>
</td>
</tr>
<tr id="row54513538256"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.1.7.1.1 "><p id="p20511321151517"><a name="p20511321151517"></a><a name="p20511321151517"></a>修改云服务器指定Key的元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.1.7.1.2 "><p id="p1163717278380"><a name="p1163717278380"></a><a name="p1163717278380"></a>PUT /v2.1/{project_id}/servers/{server_id}/metadata/{key}</p>
</td>
<td class="cellrowborder" valign="top" width="23.18%" headers="mcps1.1.7.1.3 "><p id="p4447182017213"><a name="p4447182017213"></a><a name="p4447182017213"></a>ecs:servers:setMetadata</p>
</td>
<td class="cellrowborder" valign="top" width="17.73%" headers="mcps1.1.7.1.4 "><p id="p119601612154"><a name="p119601612154"></a><a name="p119601612154"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.6%" headers="mcps1.1.7.1.5 "><p id="p19563141171613"><a name="p19563141171613"></a><a name="p19563141171613"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.83%" headers="mcps1.1.7.1.6 "><p id="p19563144112165"><a name="p19563144112165"></a><a name="p19563144112165"></a>×</p>
</td>
</tr>
<tr id="row1745205314257"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.1.7.1.1 "><p id="p19511221111516"><a name="p19511221111516"></a><a name="p19511221111516"></a>更新云服务器元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.1.7.1.2 "><p id="p14427183918386"><a name="p14427183918386"></a><a name="p14427183918386"></a>POST /v2.1/{project_id}/servers/{server_id}/metadata</p>
</td>
<td class="cellrowborder" valign="top" width="23.18%" headers="mcps1.1.7.1.3 "><p id="p19412822102116"><a name="p19412822102116"></a><a name="p19412822102116"></a>ecs:servers:setMetadata</p>
</td>
<td class="cellrowborder" valign="top" width="17.73%" headers="mcps1.1.7.1.4 "><p id="p149601860158"><a name="p149601860158"></a><a name="p149601860158"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.6%" headers="mcps1.1.7.1.5 "><p id="p104161543121619"><a name="p104161543121619"></a><a name="p104161543121619"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.83%" headers="mcps1.1.7.1.6 "><p id="p9416204312164"><a name="p9416204312164"></a><a name="p9416204312164"></a>×</p>
</td>
</tr>
<tr id="row7451153152518"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.1.7.1.1 "><p id="p65111721151514"><a name="p65111721151514"></a><a name="p65111721151514"></a>设置云服务器元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.1.7.1.2 "><p id="p1284135014389"><a name="p1284135014389"></a><a name="p1284135014389"></a>PUT /v2.1/{project_id}/servers/{server_id}/metadata</p>
</td>
<td class="cellrowborder" valign="top" width="23.18%" headers="mcps1.1.7.1.3 "><p id="p848962316215"><a name="p848962316215"></a><a name="p848962316215"></a>ecs:servers:setMetadata</p>
</td>
<td class="cellrowborder" valign="top" width="17.73%" headers="mcps1.1.7.1.4 "><p id="p13112112472112"><a name="p13112112472112"></a><a name="p13112112472112"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="9.6%" headers="mcps1.1.7.1.5 "><p id="p2083213449164"><a name="p2083213449164"></a><a name="p2083213449164"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.83%" headers="mcps1.1.7.1.6 "><p id="p1383234419169"><a name="p1383234419169"></a><a name="p1383234419169"></a>×</p>
</td>
</tr>
<tr id="row12910751192118"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.1.7.1.1 "><p id="p16512122113152"><a name="p16512122113152"></a><a name="p16512122113152"></a>管理云服务器自动恢复动作</p>
</td>
<td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.1.7.1.2 "><p id="p5112171122214"><a name="p5112171122214"></a><a name="p5112171122214"></a>PUT /v1/{project_id}/cloudservers/{server_id}/autorecovery</p>
</td>
<td class="cellrowborder" valign="top" width="23.18%" headers="mcps1.1.7.1.3 "><p id="p14812152515214"><a name="p14812152515214"></a><a name="p14812152515214"></a>ecs:cloudServers:setAutoRecovery</p>
</td>
<td class="cellrowborder" valign="top" width="17.73%" headers="mcps1.1.7.1.4 "><p id="p196076101519"><a name="p196076101519"></a><a name="p196076101519"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.6%" headers="mcps1.1.7.1.5 "><p id="p317872319146"><a name="p317872319146"></a><a name="p317872319146"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.83%" headers="mcps1.1.7.1.6 "><p id="p1117882315143"><a name="p1117882315143"></a><a name="p1117882315143"></a>√</p>
</td>
</tr>
<tr id="row5416859112120"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.1.7.1.1 "><p id="p95121721151515"><a name="p95121721151515"></a><a name="p95121721151515"></a>查询云服务器是否配置了自动恢复动作</p>
</td>
<td class="cellrowborder" valign="top" width="28.54%" headers="mcps1.1.7.1.2 "><p id="p17112151192212"><a name="p17112151192212"></a><a name="p17112151192212"></a>GET /v1/{project_id}/cloudservers/{server_id}/autorecovery</p>
</td>
<td class="cellrowborder" valign="top" width="23.18%" headers="mcps1.1.7.1.3 "><p id="p283292614211"><a name="p283292614211"></a><a name="p283292614211"></a>ecs:cloudServers:getAutoRecovery</p>
</td>
<td class="cellrowborder" valign="top" width="17.73%" headers="mcps1.1.7.1.4 "><p id="p59601361159"><a name="p59601361159"></a><a name="p59601361159"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.6%" headers="mcps1.1.7.1.5 "><p id="p1778771181719"><a name="p1778771181719"></a><a name="p1778771181719"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.83%" headers="mcps1.1.7.1.6 "><p id="p11787181131719"><a name="p11787181131719"></a><a name="p11787181131719"></a>√</p>
</td>
</tr>
</tbody>
</table>

