# 元数据管理<a name="ZH-CN_TOPIC_0103071516"></a>

<a name="table144485372515"></a>
<table><thead align="left"><tr id="row7456538256"><th class="cellrowborder" valign="top" width="35.64356435643564%" id="mcps1.1.5.1.1"><p id="p104512532258"><a name="p104512532258"></a><a name="p104512532258"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="18.81188118811881%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25.742574257425744%" id="mcps1.1.5.1.3"><p id="p84525314251"><a name="p84525314251"></a><a name="p84525314251"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="19.801980198019802%" id="mcps1.1.5.1.4"><p id="p11249625124315"><a name="p11249625124315"></a><a name="p11249625124315"></a>授权项作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row74519536251"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p158971010202610"><a name="p158971010202610"></a><a name="p158971010202610"></a>GET /v2.1/{project_id}/servers/{server_id}/metadata</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.2 "><p id="p78710464433"><a name="p78710464433"></a><a name="p78710464433"></a>查询云服务器元数据列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.1.5.1.3 "><a name="ul58974106263"></a><a name="ul58974106263"></a><ul id="ul58974106263"><li>ecs:servers:listMetadata</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul0489728233"></a><a name="ul0489728233"></a><ul id="ul0489728233"><li>支持：</li></ul>
<p id="p4505928837"><a name="p4505928837"></a><a name="p4505928837"></a>项目(Project)</p>
<p id="p1950519283318"><a name="p1950519283318"></a><a name="p1950519283318"></a></p>
<a name="ul950582810311"></a><a name="ul950582810311"></a><ul id="ul950582810311"><li>不支持：</li></ul>
<p id="p250522819317"><a name="p250522819317"></a><a name="p250522819317"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row154545313252"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p1489731013268"><a name="p1489731013268"></a><a name="p1489731013268"></a>GET /v2.1/{project_id}/servers/{server_id}/metadata/{key}</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.2 "><p id="p087124612434"><a name="p087124612434"></a><a name="p087124612434"></a>获取云服务器指定Key的元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.1.5.1.3 "><a name="ul289781082619"></a><a name="ul289781082619"></a><ul id="ul289781082619"><li>ecs:servers:getMetadata</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul121568314614"></a><a name="ul121568314614"></a><ul id="ul121568314614"><li>支持：</li></ul>
<p id="p20172231366"><a name="p20172231366"></a><a name="p20172231366"></a>项目(Project)</p>
<p id="p1017203111615"><a name="p1017203111615"></a><a name="p1017203111615"></a></p>
<a name="ul217253111616"></a><a name="ul217253111616"></a><ul id="ul217253111616"><li>不支持：</li></ul>
<p id="p1617210317615"><a name="p1617210317615"></a><a name="p1617210317615"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1745115392512"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p689781014264"><a name="p689781014264"></a><a name="p689781014264"></a>DELETE /v2.1/{project_id}/servers/{server_id}/metadata/{key}</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.2 "><p id="p8871646154319"><a name="p8871646154319"></a><a name="p8871646154319"></a>删除云服务器指定元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.1.5.1.3 "><a name="ul198970103261"></a><a name="ul198970103261"></a><ul id="ul198970103261"><li>ecs:servers:setMetadata</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul1514211409616"></a><a name="ul1514211409616"></a><ul id="ul1514211409616"><li>支持：</li></ul>
<p id="p3142140264"><a name="p3142140264"></a><a name="p3142140264"></a>项目(Project)</p>
<p id="p151428409616"><a name="p151428409616"></a><a name="p151428409616"></a></p>
<a name="ul9142740961"></a><a name="ul9142740961"></a><ul id="ul9142740961"><li>不支持：</li></ul>
<p id="p8142540261"><a name="p8142540261"></a><a name="p8142540261"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row54513538256"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p5897610132616"><a name="p5897610132616"></a><a name="p5897610132616"></a>PUT /v2.1/{project_id}/servers/{server_id}/metadata/{key}</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.2 "><p id="p1487115466433"><a name="p1487115466433"></a><a name="p1487115466433"></a>修改云服务器指定Key的元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.1.5.1.3 "><a name="ul58974107265"></a><a name="ul58974107265"></a><ul id="ul58974107265"><li>ecs:servers:setMetadata</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul17844344162"></a><a name="ul17844344162"></a><ul id="ul17844344162"><li>支持：</li></ul>
<p id="p17860164413618"><a name="p17860164413618"></a><a name="p17860164413618"></a>项目(Project)</p>
<p id="p16860114412616"><a name="p16860114412616"></a><a name="p16860114412616"></a></p>
<a name="ul9860164411614"></a><a name="ul9860164411614"></a><ul id="ul9860164411614"><li>不支持：</li></ul>
<p id="p1986019446611"><a name="p1986019446611"></a><a name="p1986019446611"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1745205314257"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p12898131011269"><a name="p12898131011269"></a><a name="p12898131011269"></a>POST /v2.1/{project_id}/servers/{server_id}/metadata</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.2 "><p id="p787164611439"><a name="p787164611439"></a><a name="p787164611439"></a>更新云服务器元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.1.5.1.3 "><a name="ul7898710162612"></a><a name="ul7898710162612"></a><ul id="ul7898710162612"><li>ecs:servers:setMetadata</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul3516946562"></a><a name="ul3516946562"></a><ul id="ul3516946562"><li>支持：</li></ul>
<p id="p75324466617"><a name="p75324466617"></a><a name="p75324466617"></a>项目(Project)</p>
<p id="p25329468610"><a name="p25329468610"></a><a name="p25329468610"></a></p>
<a name="ul55324463616"></a><a name="ul55324463616"></a><ul id="ul55324463616"><li>不支持：</li></ul>
<p id="p1553216461963"><a name="p1553216461963"></a><a name="p1553216461963"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row7451153152518"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p0898410112619"><a name="p0898410112619"></a><a name="p0898410112619"></a>PUT /v2.1/{project_id}/servers/{server_id}/metadata</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.2 "><p id="p5871114624314"><a name="p5871114624314"></a><a name="p5871114624314"></a>设置云服务器元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.1.5.1.3 "><a name="ul88981010182619"></a><a name="ul88981010182619"></a><ul id="ul88981010182619"><li>ecs:servers:setMetadata</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul59225481565"></a><a name="ul59225481565"></a><ul id="ul59225481565"><li>支持：</li></ul>
<p id="p2092264811617"><a name="p2092264811617"></a><a name="p2092264811617"></a>项目(Project)</p>
<p id="p1692219481564"><a name="p1692219481564"></a><a name="p1692219481564"></a></p>
<a name="ul12922848869"></a><a name="ul12922848869"></a><ul id="ul12922848869"><li>不支持：</li></ul>
<p id="p99226485614"><a name="p99226485614"></a><a name="p99226485614"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row12910751192118"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p5112171122214"><a name="p5112171122214"></a><a name="p5112171122214"></a>PUT /v1/{project_id}/cloudservers/{server_id}/autorecovery</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.2 "><p id="p58711146174315"><a name="p58711146174315"></a><a name="p58711146174315"></a>管理云服务器自动恢复动作</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.1.5.1.3 "><a name="ul611216112224"></a><a name="ul611216112224"></a><ul id="ul611216112224"><li>ecs:cloudServers:setAutoRecovery</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul13703155018619"></a><a name="ul13703155018619"></a><ul id="ul13703155018619"><li>支持：</li></ul>
<p id="p77031501365"><a name="p77031501365"></a><a name="p77031501365"></a>项目(Project)</p>
<p id="p27032507619"><a name="p27032507619"></a><a name="p27032507619"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row5416859112120"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p17112151192212"><a name="p17112151192212"></a><a name="p17112151192212"></a>GET /v1/{project_id}/cloudservers/{server_id}/autorecovery</p>
</td>
<td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.2 "><p id="p58719461431"><a name="p58719461431"></a><a name="p58719461431"></a>查询云服务器是否配置了自动恢复动作</p>
</td>
<td class="cellrowborder" valign="top" width="25.742574257425744%" headers="mcps1.1.5.1.3 "><a name="ul1511215112228"></a><a name="ul1511215112228"></a><ul id="ul1511215112228"><li>ecs:cloudServers:getAutoRecovery</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul43280521466"></a><a name="ul43280521466"></a><ul id="ul43280521466"><li>支持：</li></ul>
<p id="p1032815215610"><a name="p1032815215610"></a><a name="p1032815215610"></a>项目(Project)</p>
<p id="p1132815521367"><a name="p1132815521367"></a><a name="p1132815521367"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

