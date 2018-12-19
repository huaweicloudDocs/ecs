# SSH密钥管理<a name="ZH-CN_TOPIC_0103071515"></a>

<a name="table796561272518"></a>
<table><thead align="left"><tr id="row10966111213255"><th class="cellrowborder" valign="top" width="43.74999999999999%" id="mcps1.1.4.1.1"><p id="p7966131215253"><a name="p7966131215253"></a><a name="p7966131215253"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="32.5%" id="mcps1.1.4.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="23.75%" id="mcps1.1.4.1.3"><p id="p18966181212258"><a name="p18966181212258"></a><a name="p18966181212258"></a>授权项</p>
</th>
</tr>
</thead>
<tbody><tr id="row796681232520"><td class="cellrowborder" valign="top" width="43.74999999999999%" headers="mcps1.1.4.1.1 "><p id="p1299333610258"><a name="p1299333610258"></a><a name="p1299333610258"></a>POST /v2/{tenant_id}/os-keypairs</p>
</td>
<td class="cellrowborder" valign="top" width="32.5%" headers="mcps1.1.4.1.2 "><p id="p1438222944415"><a name="p1438222944415"></a><a name="p1438222944415"></a>创建和导入SSH密钥（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.1.4.1.3 "><a name="ul39939369259"></a><a name="ul39939369259"></a><ul id="ul39939369259"><li>ecs:serverKeypairs:create</li></ul>
</td>
</tr>
<tr id="row179662012132520"><td class="cellrowborder" valign="top" width="43.74999999999999%" headers="mcps1.1.4.1.1 "><p id="p5994183614256"><a name="p5994183614256"></a><a name="p5994183614256"></a>GET /v2/{tenant_id}/os-keypairs/{keypair_name}</p>
</td>
<td class="cellrowborder" valign="top" width="32.5%" headers="mcps1.1.4.1.2 "><p id="p11382329114412"><a name="p11382329114412"></a><a name="p11382329114412"></a>查询SSH密钥详情（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.1.4.1.3 "><a name="ul19942362254"></a><a name="ul19942362254"></a><ul id="ul19942362254"><li>ecs:serverKeypairs:get</li></ul>
</td>
</tr>
<tr id="row2096611215254"><td class="cellrowborder" valign="top" width="43.74999999999999%" headers="mcps1.1.4.1.1 "><p id="p119941036182515"><a name="p119941036182515"></a><a name="p119941036182515"></a>GET /v2/{tenant_id}/os-keypairs</p>
</td>
<td class="cellrowborder" valign="top" width="32.5%" headers="mcps1.1.4.1.2 "><p id="p123821029194415"><a name="p123821029194415"></a><a name="p123821029194415"></a>查询SSH密钥列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.1.4.1.3 "><a name="ul11994203652513"></a><a name="ul11994203652513"></a><ul id="ul11994203652513"><li>ecs:serverKeypairs:list</li></ul>
</td>
</tr>
<tr id="row1896617127258"><td class="cellrowborder" valign="top" width="43.74999999999999%" headers="mcps1.1.4.1.1 "><p id="p399463622514"><a name="p399463622514"></a><a name="p399463622514"></a>DELETE /v2/{tenant_id}/os-keypairs/{keypair_name}</p>
</td>
<td class="cellrowborder" valign="top" width="32.5%" headers="mcps1.1.4.1.2 "><p id="p138332964410"><a name="p138332964410"></a><a name="p138332964410"></a>删除SSH密钥（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="23.75%" headers="mcps1.1.4.1.3 "><a name="ul199473652519"></a><a name="ul199473652519"></a><ul id="ul199473652519"><li>ecs:serverKeypairs:delete</li></ul>
</td>
</tr>
</tbody>
</table>

