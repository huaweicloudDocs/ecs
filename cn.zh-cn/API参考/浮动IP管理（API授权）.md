# 浮动IP管理<a name="ZH-CN_TOPIC_0103072349"></a>

<a name="table597722943219"></a>
<table><thead align="left"><tr id="row20978132943210"><th class="cellrowborder" valign="top" width="35%" id="mcps1.1.5.1.1"><p id="p18978629163212"><a name="p18978629163212"></a><a name="p18978629163212"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="23.000000000000004%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="21.000000000000004%" id="mcps1.1.5.1.3"><p id="p897882917325"><a name="p897882917325"></a><a name="p897882917325"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="21.000000000000004%" id="mcps1.1.5.1.4"><p id="p12155854174313"><a name="p12155854174313"></a><a name="p12155854174313"></a>授权作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row13978152915327"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p881455273212"><a name="p881455273212"></a><a name="p881455273212"></a>POST /v2.1/{project_id}/os-floating-ips</p>
</td>
<td class="cellrowborder" valign="top" width="23.000000000000004%" headers="mcps1.1.5.1.2 "><p id="p7583154214413"><a name="p7583154214413"></a><a name="p7583154214413"></a>创建浮动IP（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.000000000000004%" headers="mcps1.1.5.1.3 "><a name="ul2814752173220"></a><a name="ul2814752173220"></a><ul id="ul2814752173220"><li>ecs:serverFloatingIps:use</li></ul>
<a name="ul881435216324"></a><a name="ul881435216324"></a><ul id="ul881435216324"><li>vpc:floatingIps:get</li><li>vpc:floatingIps:create</li><li>vpc:floatingIps:update</li><li>vpc:ports:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21.000000000000004%" headers="mcps1.1.5.1.4 "><a name="ul355251692"></a><a name="ul355251692"></a><ul id="ul355251692"><li>支持：</li></ul>
<p id="p1255459915"><a name="p1255459915"></a><a name="p1255459915"></a>项目(Project)</p>
<p id="p10552051794"><a name="p10552051794"></a><a name="p10552051794"></a></p>
<a name="ul65575895"></a><a name="ul65575895"></a><ul id="ul65575895"><li>不支持：</li></ul>
<p id="p1171551096"><a name="p1171551096"></a><a name="p1171551096"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row89781529103215"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p581415527327"><a name="p581415527327"></a><a name="p581415527327"></a>GET /v2.1/{project_id}/os-floating-ips</p>
</td>
<td class="cellrowborder" valign="top" width="23.000000000000004%" headers="mcps1.1.5.1.2 "><p id="p0584742164410"><a name="p0584742164410"></a><a name="p0584742164410"></a>查询浮动IP列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.000000000000004%" headers="mcps1.1.5.1.3 "><a name="ul9814155217321"></a><a name="ul9814155217321"></a><ul id="ul9814155217321"><li>ecs:serverFloatingIps:use</li></ul>
<a name="ul3814155213214"></a><a name="ul3814155213214"></a><ul id="ul3814155213214"><li>vpc:floatingIps:get</li><li>vpc:ports:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21.000000000000004%" headers="mcps1.1.5.1.4 "><a name="ul20485628171010"></a><a name="ul20485628171010"></a><ul id="ul20485628171010"><li>支持：</li></ul>
<p id="p850142820105"><a name="p850142820105"></a><a name="p850142820105"></a>项目(Project)</p>
<p id="p2501128141018"><a name="p2501128141018"></a><a name="p2501128141018"></a></p>
<a name="ul11501328201017"></a><a name="ul11501328201017"></a><ul id="ul11501328201017"><li>不支持：</li></ul>
<p id="p18501152813101"><a name="p18501152813101"></a><a name="p18501152813101"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row18978329133213"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p481419523322"><a name="p481419523322"></a><a name="p481419523322"></a>GET /v2.1/{project_id}/os-floating-ips/{floating_ip_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23.000000000000004%" headers="mcps1.1.5.1.2 "><p id="p1758434224416"><a name="p1758434224416"></a><a name="p1758434224416"></a>查询浮动IP（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.000000000000004%" headers="mcps1.1.5.1.3 "><a name="ul081435217326"></a><a name="ul081435217326"></a><ul id="ul081435217326"><li>ecs:serverFloatingIps:use</li></ul>
<a name="ul188144526328"></a><a name="ul188144526328"></a><ul id="ul188144526328"><li>vpc:floatingIps:get</li><li>vpc:ports:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21.000000000000004%" headers="mcps1.1.5.1.4 "><a name="ul1592210302105"></a><a name="ul1592210302105"></a><ul id="ul1592210302105"><li>支持：</li></ul>
<p id="p692211305107"><a name="p692211305107"></a><a name="p692211305107"></a>项目(Project)</p>
<p id="p992218302103"><a name="p992218302103"></a><a name="p992218302103"></a></p>
<a name="ul69220308107"></a><a name="ul69220308107"></a><ul id="ul69220308107"><li>不支持：</li></ul>
<p id="p12922430111014"><a name="p12922430111014"></a><a name="p12922430111014"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row19781429183210"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p181425219321"><a name="p181425219321"></a><a name="p181425219321"></a>DELETE /v2.1/{project_id}/os-floating-ips/{floating_ip_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23.000000000000004%" headers="mcps1.1.5.1.2 "><p id="p3584124220448"><a name="p3584124220448"></a><a name="p3584124220448"></a>删除浮动IP（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.000000000000004%" headers="mcps1.1.5.1.3 "><a name="ul19814145233218"></a><a name="ul19814145233218"></a><ul id="ul19814145233218"><li>ecs:serverFloatingIps:use</li></ul>
<a name="ul7815152203218"></a><a name="ul7815152203218"></a><ul id="ul7815152203218"><li>vpc:floatingIps:get</li><li>vpc:floatingIps:delete</li><li>vpc:floatingIps:update</li><li>vpc:ports:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21.000000000000004%" headers="mcps1.1.5.1.4 "><a name="ul1439117322109"></a><a name="ul1439117322109"></a><ul id="ul1439117322109"><li>支持：</li></ul>
<p id="p93911432201015"><a name="p93911432201015"></a><a name="p93911432201015"></a>项目(Project)</p>
<p id="p1039113221010"><a name="p1039113221010"></a><a name="p1039113221010"></a></p>
<a name="ul43911932131017"></a><a name="ul43911932131017"></a><ul id="ul43911932131017"><li>不支持：</li></ul>
<p id="p139112320101"><a name="p139112320101"></a><a name="p139112320101"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

