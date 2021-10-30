# 密码管理<a name="ecs_06_0014"></a>

<a name="table1642432772714"></a>
<table><thead align="left"><tr id="row18424102718278"><th class="cellrowborder" valign="top" width="11.028897110288971%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="29.417058294170584%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="22.737726227377262%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="18.688131186881314%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="10.078992100789922%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="8.049195080491952%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row194249274272"><td class="cellrowborder" valign="top" width="11.028897110288971%" headers="mcps1.1.7.1.1 "><p id="p0911222172413"><a name="p0911222172413"></a><a name="p0911222172413"></a>一键重置弹性云服务器密码（企业项目）</p>
</td>
<td class="cellrowborder" valign="top" width="29.417058294170584%" headers="mcps1.1.7.1.2 "><p id="p1222154416276"><a name="p1222154416276"></a><a name="p1222154416276"></a>PUT /v1/{project_id}/cloudservers/{server_id}/os-reset-password</p>
</td>
<td class="cellrowborder" valign="top" width="22.737726227377262%" headers="mcps1.1.7.1.3 "><p id="p37437519223"><a name="p37437519223"></a><a name="p37437519223"></a>ecs:cloudServers:resetServerPwd</p>
</td>
<td class="cellrowborder" valign="top" width="18.688131186881314%" headers="mcps1.1.7.1.4 "><p id="p154310319245"><a name="p154310319245"></a><a name="p154310319245"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.078992100789922%" headers="mcps1.1.7.1.5 "><p id="p79824201716"><a name="p79824201716"></a><a name="p79824201716"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.049195080491952%" headers="mcps1.1.7.1.6 "><p id="p1098219212179"><a name="p1098219212179"></a><a name="p1098219212179"></a>√</p>
</td>
</tr>
<tr id="row12055017318"><td class="cellrowborder" valign="top" width="11.028897110288971%" headers="mcps1.1.7.1.1 "><p id="p1191152242414"><a name="p1191152242414"></a><a name="p1191152242414"></a>查询云服务器是否支持重置密码</p>
</td>
<td class="cellrowborder" valign="top" width="29.417058294170584%" headers="mcps1.1.7.1.2 "><p id="p157805612311"><a name="p157805612311"></a><a name="p157805612311"></a>GET /v1/{project_id}/cloudservers/{server_id}/os-resetpwd-flag</p>
</td>
<td class="cellrowborder" valign="top" width="22.737726227377262%" headers="mcps1.1.7.1.3 "><p id="p73656732216"><a name="p73656732216"></a><a name="p73656732216"></a>ecs:cloudServers:get</p>
</td>
<td class="cellrowborder" valign="top" width="18.688131186881314%" headers="mcps1.1.7.1.4 "><p id="p164310312244"><a name="p164310312244"></a><a name="p164310312244"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.078992100789922%" headers="mcps1.1.7.1.5 "><p id="p18887926112520"><a name="p18887926112520"></a><a name="p18887926112520"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.049195080491952%" headers="mcps1.1.7.1.6 "><p id="p5887826132517"><a name="p5887826132517"></a><a name="p5887826132517"></a>√</p>
</td>
</tr>
<tr id="row10925193112"><td class="cellrowborder" valign="top" width="11.028897110288971%" headers="mcps1.1.7.1.1 "><p id="p4911152215241"><a name="p4911152215241"></a><a name="p4911152215241"></a>获取Windows云服务器密码</p>
</td>
<td class="cellrowborder" valign="top" width="29.417058294170584%" headers="mcps1.1.7.1.2 "><p id="p11781968315"><a name="p11781968315"></a><a name="p11781968315"></a>GET /v1/{project_id}/cloudservers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" width="22.737726227377262%" headers="mcps1.1.7.1.3 "><p id="p1260019812213"><a name="p1260019812213"></a><a name="p1260019812213"></a>ecs:cloudServers:get</p>
</td>
<td class="cellrowborder" valign="top" width="18.688131186881314%" headers="mcps1.1.7.1.4 "><p id="p543103102411"><a name="p543103102411"></a><a name="p543103102411"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.078992100789922%" headers="mcps1.1.7.1.5 "><p id="p835011282259"><a name="p835011282259"></a><a name="p835011282259"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.049195080491952%" headers="mcps1.1.7.1.6 "><p id="p1535052812512"><a name="p1535052812512"></a><a name="p1535052812512"></a>√</p>
</td>
</tr>
<tr id="row101014513118"><td class="cellrowborder" valign="top" width="11.028897110288971%" headers="mcps1.1.7.1.1 "><p id="p19111222142418"><a name="p19111222142418"></a><a name="p19111222142418"></a>清除Windows云服务器密码</p>
</td>
<td class="cellrowborder" valign="top" width="29.417058294170584%" headers="mcps1.1.7.1.2 "><p id="p1478266163112"><a name="p1478266163112"></a><a name="p1478266163112"></a>DELETE /v1/{project_id}/cloudservers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" width="22.737726227377262%" headers="mcps1.1.7.1.3 "><p id="p1698918913225"><a name="p1698918913225"></a><a name="p1698918913225"></a>ecs:cloudServers:deletePassword</p>
</td>
<td class="cellrowborder" valign="top" width="18.688131186881314%" headers="mcps1.1.7.1.4 "><p id="p943103110243"><a name="p943103110243"></a><a name="p943103110243"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.078992100789922%" headers="mcps1.1.7.1.5 "><p id="p3391429182515"><a name="p3391429182515"></a><a name="p3391429182515"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.049195080491952%" headers="mcps1.1.7.1.6 "><p id="p1939119293254"><a name="p1939119293254"></a><a name="p1939119293254"></a>√</p>
</td>
</tr>
<tr id="row7588153714318"><td class="cellrowborder" valign="top" width="11.028897110288971%" headers="mcps1.1.7.1.1 "><p id="p19911122218241"><a name="p19911122218241"></a><a name="p19911122218241"></a>一键重置<span id="text15631544134015"><a name="text15631544134015"></a><a name="text15631544134015"></a>云服务器</span>密码</p>
</td>
<td class="cellrowborder" valign="top" width="29.417058294170584%" headers="mcps1.1.7.1.2 "><p id="p10589173784318"><a name="p10589173784318"></a><a name="p10589173784318"></a>PUT /v2.1/{project_id}/servers/{server_id}/os-reset-password</p>
</td>
<td class="cellrowborder" valign="top" width="22.737726227377262%" headers="mcps1.1.7.1.3 "><p id="p1171312114229"><a name="p1171312114229"></a><a name="p1171312114229"></a>ecs:cloudServers:resetServerPwd</p>
</td>
<td class="cellrowborder" valign="top" width="18.688131186881314%" headers="mcps1.1.7.1.4 "><p id="p12431931192410"><a name="p12431931192410"></a><a name="p12431931192410"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.078992100789922%" headers="mcps1.1.7.1.5 "><p id="p64302189255"><a name="p64302189255"></a><a name="p64302189255"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.049195080491952%" headers="mcps1.1.7.1.6 "><p id="p10430718132510"><a name="p10430718132510"></a><a name="p10430718132510"></a>×</p>
</td>
</tr>
<tr id="row103333346171"><td class="cellrowborder" valign="top" width="11.028897110288971%" headers="mcps1.1.7.1.1 "><p id="p9911922192411"><a name="p9911922192411"></a><a name="p9911922192411"></a>获取Windows云服务器密码（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="29.417058294170584%" headers="mcps1.1.7.1.2 "><p id="p1110173415408"><a name="p1110173415408"></a><a name="p1110173415408"></a>GET /v2.1/{project_id}/servers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" width="22.737726227377262%" headers="mcps1.1.7.1.3 "><p id="p75891812122211"><a name="p75891812122211"></a><a name="p75891812122211"></a>ecs:serverPasswords:manage</p>
</td>
<td class="cellrowborder" valign="top" width="18.688131186881314%" headers="mcps1.1.7.1.4 "><p id="p20434316245"><a name="p20434316245"></a><a name="p20434316245"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.078992100789922%" headers="mcps1.1.7.1.5 "><p id="p1351721652520"><a name="p1351721652520"></a><a name="p1351721652520"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.049195080491952%" headers="mcps1.1.7.1.6 "><p id="p75174166259"><a name="p75174166259"></a><a name="p75174166259"></a>×</p>
</td>
</tr>
<tr id="row41213781718"><td class="cellrowborder" valign="top" width="11.028897110288971%" headers="mcps1.1.7.1.1 "><p id="p2911622182416"><a name="p2911622182416"></a><a name="p2911622182416"></a>清楚Windows云服务器密码（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="29.417058294170584%" headers="mcps1.1.7.1.2 "><p id="p9407142144014"><a name="p9407142144014"></a><a name="p9407142144014"></a>DELETE /v2.1/{project_id}/servers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" width="22.737726227377262%" headers="mcps1.1.7.1.3 "><p id="p2074411342218"><a name="p2074411342218"></a><a name="p2074411342218"></a>ecs:serverPasswords:manage</p>
</td>
<td class="cellrowborder" valign="top" width="18.688131186881314%" headers="mcps1.1.7.1.4 "><p id="p543173142411"><a name="p543173142411"></a><a name="p543173142411"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.078992100789922%" headers="mcps1.1.7.1.5 "><p id="p1178918181914"><a name="p1178918181914"></a><a name="p1178918181914"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.049195080491952%" headers="mcps1.1.7.1.6 "><p id="p578171820196"><a name="p578171820196"></a><a name="p578171820196"></a>×</p>
</td>
</tr>
</tbody>
</table>

