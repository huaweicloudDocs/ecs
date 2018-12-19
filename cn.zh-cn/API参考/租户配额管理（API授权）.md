# 租户配额管理<a name="ZH-CN_TOPIC_0103071517"></a>

<a name="table151682922617"></a>
<table><thead align="left"><tr id="row19171029162611"><th class="cellrowborder" valign="top" width="45.56962025316456%" id="mcps1.1.4.1.1"><p id="p417102942614"><a name="p417102942614"></a><a name="p417102942614"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="26.58227848101266%" id="mcps1.1.4.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="27.848101265822788%" id="mcps1.1.4.1.3"><p id="p14177299263"><a name="p14177299263"></a><a name="p14177299263"></a>授权项</p>
</th>
</tr>
</thead>
<tbody><tr id="row4171029192612"><td class="cellrowborder" valign="top" width="45.56962025316456%" headers="mcps1.1.4.1.1 "><p id="p6985345192613"><a name="p6985345192613"></a><a name="p6985345192613"></a>GET /v2/{tenant_id}/os-quota-sets/{tenant_id}?user_id={user_id}</p>
</td>
<td class="cellrowborder" valign="top" width="26.58227848101266%" headers="mcps1.1.4.1.2 "><p id="p1171215418449"><a name="p1171215418449"></a><a name="p1171215418449"></a>查询租户配额（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.848101265822788%" headers="mcps1.1.4.1.3 "><a name="ul3985154519264"></a><a name="ul3985154519264"></a><ul id="ul3985154519264"><li>ecs:quotas:get</li></ul>
</td>
</tr>
<tr id="row8177294260"><td class="cellrowborder" valign="top" width="45.56962025316456%" headers="mcps1.1.4.1.1 "><p id="p14985445102614"><a name="p14985445102614"></a><a name="p14985445102614"></a>GET /v2/{tenant_id}/os-quota-sets/{tenant_id}/defaults</p>
</td>
<td class="cellrowborder" valign="top" width="26.58227848101266%" headers="mcps1.1.4.1.2 "><p id="p971212424418"><a name="p971212424418"></a><a name="p971212424418"></a>查询默认配额（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.848101265822788%" headers="mcps1.1.4.1.3 "><a name="ul7985104532610"></a><a name="ul7985104532610"></a><ul id="ul7985104532610"><li>ecs:quotas:get</li></ul>
</td>
</tr>
<tr id="row14919142362515"><td class="cellrowborder" valign="top" width="45.56962025316456%" headers="mcps1.1.4.1.1 "><p id="p172841231192513"><a name="p172841231192513"></a><a name="p172841231192513"></a>GET /v1/{tenant_id}/cloudservers/limits</p>
</td>
<td class="cellrowborder" valign="top" width="26.58227848101266%" headers="mcps1.1.4.1.2 "><p id="p3712184134413"><a name="p3712184134413"></a><a name="p3712184134413"></a>查询租户配额</p>
</td>
<td class="cellrowborder" valign="top" width="27.848101265822788%" headers="mcps1.1.4.1.3 "><a name="ul6284931102519"></a><a name="ul6284931102519"></a><ul id="ul6284931102519"><li>ecs:cloudServerQuotas:get</li></ul>
</td>
</tr>
</tbody>
</table>

