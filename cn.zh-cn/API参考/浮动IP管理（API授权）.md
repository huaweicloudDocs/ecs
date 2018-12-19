# 浮动IP管理<a name="ZH-CN_TOPIC_0103072349"></a>

<a name="table597722943219"></a>
<table><thead align="left"><tr id="row20978132943210"><th class="cellrowborder" valign="top" width="44.30379746835443%" id="mcps1.1.4.1.1"><p id="p18978629163212"><a name="p18978629163212"></a><a name="p18978629163212"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="29.113924050632917%" id="mcps1.1.4.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="26.58227848101266%" id="mcps1.1.4.1.3"><p id="p897882917325"><a name="p897882917325"></a><a name="p897882917325"></a>授权项</p>
</th>
</tr>
</thead>
<tbody><tr id="row13978152915327"><td class="cellrowborder" valign="top" width="44.30379746835443%" headers="mcps1.1.4.1.1 "><p id="p881455273212"><a name="p881455273212"></a><a name="p881455273212"></a>POST /v2/{tenant_id}/os-floating-ips</p>
</td>
<td class="cellrowborder" valign="top" width="29.113924050632917%" headers="mcps1.1.4.1.2 "><p id="p7583154214413"><a name="p7583154214413"></a><a name="p7583154214413"></a>创建浮动IP（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="26.58227848101266%" headers="mcps1.1.4.1.3 "><a name="ul2814752173220"></a><a name="ul2814752173220"></a><ul id="ul2814752173220"><li>ecs:serverFloatingIps:use</li></ul>
<a name="ul881435216324"></a><a name="ul881435216324"></a><ul id="ul881435216324"><li>vpc:floatingIps:get</li><li>vpc:floatingIps:create</li><li>vpc:floatingIps:update</li><li>vpc:ports:get</li></ul>
</td>
</tr>
<tr id="row89781529103215"><td class="cellrowborder" valign="top" width="44.30379746835443%" headers="mcps1.1.4.1.1 "><p id="p581415527327"><a name="p581415527327"></a><a name="p581415527327"></a>GET /v2/{tenant_id}/os-floating-ips</p>
</td>
<td class="cellrowborder" valign="top" width="29.113924050632917%" headers="mcps1.1.4.1.2 "><p id="p0584742164410"><a name="p0584742164410"></a><a name="p0584742164410"></a>查询浮动IP列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="26.58227848101266%" headers="mcps1.1.4.1.3 "><a name="ul9814155217321"></a><a name="ul9814155217321"></a><ul id="ul9814155217321"><li>ecs:serverFloatingIps:use</li></ul>
<a name="ul3814155213214"></a><a name="ul3814155213214"></a><ul id="ul3814155213214"><li>vpc:floatingIps:get</li><li>vpc:ports:get</li></ul>
</td>
</tr>
<tr id="row18978329133213"><td class="cellrowborder" valign="top" width="44.30379746835443%" headers="mcps1.1.4.1.1 "><p id="p481419523322"><a name="p481419523322"></a><a name="p481419523322"></a>GET /v2/{tenant_id}/os-floating-ips/{floating_ip_id}</p>
</td>
<td class="cellrowborder" valign="top" width="29.113924050632917%" headers="mcps1.1.4.1.2 "><p id="p1758434224416"><a name="p1758434224416"></a><a name="p1758434224416"></a>查询浮动IP（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="26.58227848101266%" headers="mcps1.1.4.1.3 "><a name="ul081435217326"></a><a name="ul081435217326"></a><ul id="ul081435217326"><li>ecs:serverFloatingIps:use</li></ul>
<a name="ul188144526328"></a><a name="ul188144526328"></a><ul id="ul188144526328"><li>vpc:floatingIps:get</li><li>vpc:ports:get</li></ul>
</td>
</tr>
<tr id="row19781429183210"><td class="cellrowborder" valign="top" width="44.30379746835443%" headers="mcps1.1.4.1.1 "><p id="p181425219321"><a name="p181425219321"></a><a name="p181425219321"></a>DELETE /v2/{tenant_id}/os-floating-ips/{floating_ip_id}</p>
</td>
<td class="cellrowborder" valign="top" width="29.113924050632917%" headers="mcps1.1.4.1.2 "><p id="p3584124220448"><a name="p3584124220448"></a><a name="p3584124220448"></a>删除浮动IP（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="26.58227848101266%" headers="mcps1.1.4.1.3 "><a name="ul19814145233218"></a><a name="ul19814145233218"></a><ul id="ul19814145233218"><li>ecs:serverFloatingIps:use</li></ul>
<a name="ul7815152203218"></a><a name="ul7815152203218"></a><ul id="ul7815152203218"><li>vpc:floatingIps:get</li><li>vpc:floatingIps:delete</li><li>vpc:floatingIps:update</li><li>vpc:ports:get</li></ul>
</td>
</tr>
</tbody>
</table>

