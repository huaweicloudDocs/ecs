# SSH密钥管理<a name="ZH-CN_TOPIC_0103071515"></a>

<a name="table796561272518"></a>
<table><thead align="left"><tr id="row10966111213255"><th class="cellrowborder" valign="top" width="35%" id="mcps1.1.5.1.1"><p id="p7966131215253"><a name="p7966131215253"></a><a name="p7966131215253"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="26%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.3"><p id="p18966181212258"><a name="p18966181212258"></a><a name="p18966181212258"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.1.5.1.4"><p id="p315184384315"><a name="p315184384315"></a><a name="p315184384315"></a>授权作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row796681232520"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p1299333610258"><a name="p1299333610258"></a><a name="p1299333610258"></a>POST /v2.1/{project_id}/os-keypairs</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.1.5.1.2 "><p id="p1438222944415"><a name="p1438222944415"></a><a name="p1438222944415"></a>创建和导入SSH密钥（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul39939369259"></a><a name="ul39939369259"></a><ul id="ul39939369259"><li>ecs:serverKeypairs:create</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul6379555674"></a><a name="ul6379555674"></a><ul id="ul6379555674"><li>支持：</li></ul>
<p id="p1737915512717"><a name="p1737915512717"></a><a name="p1737915512717"></a>项目(Project)</p>
<p id="p537965518712"><a name="p537965518712"></a><a name="p537965518712"></a></p>
<a name="ul037935519716"></a><a name="ul037935519716"></a><ul id="ul037935519716"><li>不支持：</li></ul>
<p id="p837916555715"><a name="p837916555715"></a><a name="p837916555715"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row179662012132520"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p5994183614256"><a name="p5994183614256"></a><a name="p5994183614256"></a>GET /v2.1/{project_id}/os-keypairs/{keypair_name}</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.1.5.1.2 "><p id="p11382329114412"><a name="p11382329114412"></a><a name="p11382329114412"></a>查询SSH密钥详情（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul19942362254"></a><a name="ul19942362254"></a><ul id="ul19942362254"><li>ecs:serverKeypairs:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul54618113915"></a><a name="ul54618113915"></a><ul id="ul54618113915"><li>支持：</li></ul>
<p id="p34616115914"><a name="p34616115914"></a><a name="p34616115914"></a>项目(Project)</p>
<p id="p74771717916"><a name="p74771717916"></a><a name="p74771717916"></a></p>
<a name="ul14771811798"></a><a name="ul14771811798"></a><ul id="ul14771811798"><li>不支持：</li></ul>
<p id="p84778110917"><a name="p84778110917"></a><a name="p84778110917"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row2096611215254"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p119941036182515"><a name="p119941036182515"></a><a name="p119941036182515"></a>GET /v2.1/{project_id}/os-keypairs</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.1.5.1.2 "><p id="p123821029194415"><a name="p123821029194415"></a><a name="p123821029194415"></a>查询SSH密钥列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul11994203652513"></a><a name="ul11994203652513"></a><ul id="ul11994203652513"><li>ecs:serverKeypairs:list</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul636812310910"></a><a name="ul636812310910"></a><ul id="ul636812310910"><li>支持：</li></ul>
<p id="p4368935917"><a name="p4368935917"></a><a name="p4368935917"></a>项目(Project)</p>
<p id="p73680311915"><a name="p73680311915"></a><a name="p73680311915"></a></p>
<a name="ul113681632099"></a><a name="ul113681632099"></a><ul id="ul113681632099"><li>不支持：</li></ul>
<p id="p836853297"><a name="p836853297"></a><a name="p836853297"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1896617127258"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p399463622514"><a name="p399463622514"></a><a name="p399463622514"></a>DELETE /v2.1/{project_id}/os-keypairs/{keypair_name}</p>
</td>
<td class="cellrowborder" valign="top" width="26%" headers="mcps1.1.5.1.2 "><p id="p138332964410"><a name="p138332964410"></a><a name="p138332964410"></a>删除SSH密钥（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul199473652519"></a><a name="ul199473652519"></a><ul id="ul199473652519"><li>ecs:serverKeypairs:delete</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul355251692"></a><a name="ul355251692"></a><ul id="ul355251692"><li>支持：</li></ul>
<p id="p1255459915"><a name="p1255459915"></a><a name="p1255459915"></a>项目(Project)</p>
<p id="p10552051794"><a name="p10552051794"></a><a name="p10552051794"></a></p>
<a name="ul65575895"></a><a name="ul65575895"></a><ul id="ul65575895"><li>不支持：</li></ul>
<p id="p1171551096"><a name="p1171551096"></a><a name="p1171551096"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

