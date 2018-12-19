# 元数据管理<a name="ZH-CN_TOPIC_0103071516"></a>

<a name="table144485372515"></a>
<table><thead align="left"><tr id="row7456538256"><th class="cellrowborder" valign="top" width="44.44444444444444%" id="mcps1.1.4.1.1"><p id="p104512532258"><a name="p104512532258"></a><a name="p104512532258"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="23.456790123456788%" id="mcps1.1.4.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="32.098765432098766%" id="mcps1.1.4.1.3"><p id="p84525314251"><a name="p84525314251"></a><a name="p84525314251"></a>授权项</p>
</th>
</tr>
</thead>
<tbody><tr id="row74519536251"><td class="cellrowborder" valign="top" width="44.44444444444444%" headers="mcps1.1.4.1.1 "><p id="p158971010202610"><a name="p158971010202610"></a><a name="p158971010202610"></a>GET /v2/{tenant_id}/servers/{server_id}/metadata</p>
</td>
<td class="cellrowborder" valign="top" width="23.456790123456788%" headers="mcps1.1.4.1.2 "><p id="p78710464433"><a name="p78710464433"></a><a name="p78710464433"></a>查询云服务器元数据列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="32.098765432098766%" headers="mcps1.1.4.1.3 "><a name="ul58974106263"></a><a name="ul58974106263"></a><ul id="ul58974106263"><li>ecs:servers:listMetadata</li></ul>
</td>
</tr>
<tr id="row154545313252"><td class="cellrowborder" valign="top" width="44.44444444444444%" headers="mcps1.1.4.1.1 "><p id="p1489731013268"><a name="p1489731013268"></a><a name="p1489731013268"></a>GET /v2/{tenant_id}/servers/{server_id}/metadata/{key}</p>
</td>
<td class="cellrowborder" valign="top" width="23.456790123456788%" headers="mcps1.1.4.1.2 "><p id="p087124612434"><a name="p087124612434"></a><a name="p087124612434"></a>获取云服务器指定Key的元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="32.098765432098766%" headers="mcps1.1.4.1.3 "><a name="ul289781082619"></a><a name="ul289781082619"></a><ul id="ul289781082619"><li>ecs:servers:getMetadata</li></ul>
</td>
</tr>
<tr id="row1745115392512"><td class="cellrowborder" valign="top" width="44.44444444444444%" headers="mcps1.1.4.1.1 "><p id="p689781014264"><a name="p689781014264"></a><a name="p689781014264"></a>DELETE /v2/{tenant_id}/servers/{server_id}/metadata/{key}</p>
</td>
<td class="cellrowborder" valign="top" width="23.456790123456788%" headers="mcps1.1.4.1.2 "><p id="p8871646154319"><a name="p8871646154319"></a><a name="p8871646154319"></a>删除云服务器指定元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="32.098765432098766%" headers="mcps1.1.4.1.3 "><a name="ul198970103261"></a><a name="ul198970103261"></a><ul id="ul198970103261"><li>ecs:servers:setMetadata</li></ul>
</td>
</tr>
<tr id="row54513538256"><td class="cellrowborder" valign="top" width="44.44444444444444%" headers="mcps1.1.4.1.1 "><p id="p5897610132616"><a name="p5897610132616"></a><a name="p5897610132616"></a>PUT /v2/{tenant_id}/servers/{server_id}/metadata/{key}</p>
</td>
<td class="cellrowborder" valign="top" width="23.456790123456788%" headers="mcps1.1.4.1.2 "><p id="p1487115466433"><a name="p1487115466433"></a><a name="p1487115466433"></a>修改云服务器指定Key的元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="32.098765432098766%" headers="mcps1.1.4.1.3 "><a name="ul58974107265"></a><a name="ul58974107265"></a><ul id="ul58974107265"><li>ecs:servers:setMetadata</li></ul>
</td>
</tr>
<tr id="row1745205314257"><td class="cellrowborder" valign="top" width="44.44444444444444%" headers="mcps1.1.4.1.1 "><p id="p12898131011269"><a name="p12898131011269"></a><a name="p12898131011269"></a>POST /v2/{tenant_id}/servers/{server_id}/metadata</p>
</td>
<td class="cellrowborder" valign="top" width="23.456790123456788%" headers="mcps1.1.4.1.2 "><p id="p787164611439"><a name="p787164611439"></a><a name="p787164611439"></a>更新云服务器元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="32.098765432098766%" headers="mcps1.1.4.1.3 "><a name="ul7898710162612"></a><a name="ul7898710162612"></a><ul id="ul7898710162612"><li>ecs:servers:setMetadata</li></ul>
</td>
</tr>
<tr id="row7451153152518"><td class="cellrowborder" valign="top" width="44.44444444444444%" headers="mcps1.1.4.1.1 "><p id="p0898410112619"><a name="p0898410112619"></a><a name="p0898410112619"></a>PUT /v2/{tenant_id}/servers/{server_id}/metadata</p>
</td>
<td class="cellrowborder" valign="top" width="23.456790123456788%" headers="mcps1.1.4.1.2 "><p id="p5871114624314"><a name="p5871114624314"></a><a name="p5871114624314"></a>设置云服务器元数据（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="32.098765432098766%" headers="mcps1.1.4.1.3 "><a name="ul88981010182619"></a><a name="ul88981010182619"></a><ul id="ul88981010182619"><li>ecs:servers:setMetadata</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row12910751192118"><td class="cellrowborder" valign="top" width="44.44444444444444%" headers="mcps1.1.4.1.1 "><p id="p5112171122214"><a name="p5112171122214"></a><a name="p5112171122214"></a>PUT /v1/{tenant_id}/cloudservers/{server_id}/autorecovery</p>
</td>
<td class="cellrowborder" valign="top" width="23.456790123456788%" headers="mcps1.1.4.1.2 "><p id="p58711146174315"><a name="p58711146174315"></a><a name="p58711146174315"></a>管理云服务器自动恢复动作</p>
</td>
<td class="cellrowborder" valign="top" width="32.098765432098766%" headers="mcps1.1.4.1.3 "><a name="ul611216112224"></a><a name="ul611216112224"></a><ul id="ul611216112224"><li>ecs:cloudServers:setAutoRecovery</li></ul>
</td>
</tr>
<tr id="row5416859112120"><td class="cellrowborder" valign="top" width="44.44444444444444%" headers="mcps1.1.4.1.1 "><p id="p17112151192212"><a name="p17112151192212"></a><a name="p17112151192212"></a>GET /v1/{tenant_id}/cloudservers/{server_id}/autorecovery</p>
</td>
<td class="cellrowborder" valign="top" width="23.456790123456788%" headers="mcps1.1.4.1.2 "><p id="p58719461431"><a name="p58719461431"></a><a name="p58719461431"></a>查询云服务器是否配置了自动恢复动作</p>
</td>
<td class="cellrowborder" valign="top" width="32.098765432098766%" headers="mcps1.1.4.1.3 "><a name="ul1511215112228"></a><a name="ul1511215112228"></a><ul id="ul1511215112228"><li>ecs:cloudServers:getAutoRecovery</li></ul>
</td>
</tr>
</tbody>
</table>

