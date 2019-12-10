# 租户配额管理<a name="ZH-CN_TOPIC_0103071517"></a>

<a name="table151682922617"></a>
<table><thead align="left"><tr id="row19171029162611"><th class="cellrowborder" valign="top" width="35.64356435643564%" id="mcps1.1.5.1.1"><p id="p417102942614"><a name="p417102942614"></a><a name="p417102942614"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="20.792079207920793%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="21.782178217821784%" id="mcps1.1.5.1.3"><p id="p14177299263"><a name="p14177299263"></a><a name="p14177299263"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="21.782178217821784%" id="mcps1.1.5.1.4"><p id="p168588341437"><a name="p168588341437"></a><a name="p168588341437"></a>授权作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row67071724254"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p159161514254"><a name="p159161514254"></a><a name="p159161514254"></a>GET /v1/{project_id}/cloudservers/limits</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.2 "><p id="p5916450254"><a name="p5916450254"></a><a name="p5916450254"></a>查询租户配额</p>
</td>
<td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.1.5.1.3 "><a name="ul7916155102513"></a><a name="ul7916155102513"></a><ul id="ul7916155102513"><li>ecs:cloudServerQuotas:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.1.5.1.4 "><a name="ul17916145102515"></a><a name="ul17916145102515"></a><ul id="ul17916145102515"><li>支持：</li></ul>
<p id="p159161758259"><a name="p159161758259"></a><a name="p159161758259"></a>项目(Project)</p>
<p id="p481074001113"><a name="p481074001113"></a><a name="p481074001113"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row4171029192612"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p6985345192613"><a name="p6985345192613"></a><a name="p6985345192613"></a>GET /v2.1/{project_id}/os-quota-sets/{project_id}?user_id={user_id}</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.2 "><p id="p1171215418449"><a name="p1171215418449"></a><a name="p1171215418449"></a>查询租户配额（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.1.5.1.3 "><a name="ul3985154519264"></a><a name="ul3985154519264"></a><ul id="ul3985154519264"><li>ecs:quotas:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.1.5.1.4 "><a name="ul121568314614"></a><a name="ul121568314614"></a><ul id="ul121568314614"><li>支持：</li></ul>
<p id="p20172231366"><a name="p20172231366"></a><a name="p20172231366"></a>项目(Project)</p>
<p id="p1017203111615"><a name="p1017203111615"></a><a name="p1017203111615"></a></p>
<a name="ul217253111616"></a><a name="ul217253111616"></a><ul id="ul217253111616"><li>不支持：</li></ul>
<p id="p1617210317615"><a name="p1617210317615"></a><a name="p1617210317615"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row8177294260"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p14985445102614"><a name="p14985445102614"></a><a name="p14985445102614"></a>GET /v2.1/{project_id}/os-quota-sets/{project_id}/defaults</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.2 "><p id="p971212424418"><a name="p971212424418"></a><a name="p971212424418"></a>查询默认配额（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.1.5.1.3 "><a name="ul7985104532610"></a><a name="ul7985104532610"></a><ul id="ul7985104532610"><li>ecs:quotas:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21.782178217821784%" headers="mcps1.1.5.1.4 "><a name="ul82851353779"></a><a name="ul82851353779"></a><ul id="ul82851353779"><li>支持：</li></ul>
<p id="p112858531578"><a name="p112858531578"></a><a name="p112858531578"></a>项目(Project)</p>
<p id="p102851353979"><a name="p102851353979"></a><a name="p102851353979"></a></p>
<a name="ul428518533711"></a><a name="ul428518533711"></a><ul id="ul428518533711"><li>不支持：</li></ul>
<p id="p19285953878"><a name="p19285953878"></a><a name="p19285953878"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

