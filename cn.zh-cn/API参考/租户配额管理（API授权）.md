# 租户配额管理<a name="ZH-CN_TOPIC_0103071517"></a>

<a name="table151682922617"></a>
<table><thead align="left"><tr id="row19171029162611"><th class="cellrowborder" valign="top" width="11.498850114988501%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="29.237076292370762%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="23.45765423457654%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="17.648235176482352%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="9.919008099190082%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="8.239176082391761%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row67071724254"><td class="cellrowborder" valign="top" width="11.498850114988501%" headers="mcps1.1.7.1.1 "><p id="p92081218182"><a name="p92081218182"></a><a name="p92081218182"></a>查询租户配额</p>
</td>
<td class="cellrowborder" valign="top" width="29.237076292370762%" headers="mcps1.1.7.1.2 "><p id="p159161514254"><a name="p159161514254"></a><a name="p159161514254"></a>GET /v1/{project_id}/cloudservers/limits</p>
</td>
<td class="cellrowborder" valign="top" width="23.45765423457654%" headers="mcps1.1.7.1.3 "><p id="p652014495217"><a name="p652014495217"></a><a name="p652014495217"></a>ecs:cloudServerQuotas:get</p>
</td>
<td class="cellrowborder" valign="top" width="17.648235176482352%" headers="mcps1.1.7.1.4 "><p id="p874319931812"><a name="p874319931812"></a><a name="p874319931812"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.919008099190082%" headers="mcps1.1.7.1.5 "><p id="p79824201716"><a name="p79824201716"></a><a name="p79824201716"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.239176082391761%" headers="mcps1.1.7.1.6 "><p id="p1098219212179"><a name="p1098219212179"></a><a name="p1098219212179"></a>√</p>
</td>
</tr>
<tr id="row4171029192612"><td class="cellrowborder" valign="top" width="11.498850114988501%" headers="mcps1.1.7.1.1 "><p id="p1220832121816"><a name="p1220832121816"></a><a name="p1220832121816"></a>查询租户配额（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="29.237076292370762%" headers="mcps1.1.7.1.2 "><p id="p16953157123914"><a name="p16953157123914"></a><a name="p16953157123914"></a>GET /v2.1/{project_id}/os-quota-sets/{project_id}?user_id={user_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23.45765423457654%" headers="mcps1.1.7.1.3 "><p id="p1245013503217"><a name="p1245013503217"></a><a name="p1245013503217"></a>ecs:quotas:get</p>
</td>
<td class="cellrowborder" valign="top" width="17.648235176482352%" headers="mcps1.1.7.1.4 "><p id="p97437961818"><a name="p97437961818"></a><a name="p97437961818"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.919008099190082%" headers="mcps1.1.7.1.5 "><p id="p19563141171613"><a name="p19563141171613"></a><a name="p19563141171613"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.239176082391761%" headers="mcps1.1.7.1.6 "><p id="p19563144112165"><a name="p19563144112165"></a><a name="p19563144112165"></a>×</p>
</td>
</tr>
<tr id="row8177294260"><td class="cellrowborder" valign="top" width="11.498850114988501%" headers="mcps1.1.7.1.1 "><p id="p12208102151815"><a name="p12208102151815"></a><a name="p12208102151815"></a>查询默认配额（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="29.237076292370762%" headers="mcps1.1.7.1.2 "><p id="p1233141273910"><a name="p1233141273910"></a><a name="p1233141273910"></a>GET /v2.1/{project_id}/os-quota-sets/{project_id}/defaults</p>
</td>
<td class="cellrowborder" valign="top" width="23.45765423457654%" headers="mcps1.1.7.1.3 "><p id="p5433115117211"><a name="p5433115117211"></a><a name="p5433115117211"></a>ecs:quotas:get</p>
</td>
<td class="cellrowborder" valign="top" width="17.648235176482352%" headers="mcps1.1.7.1.4 "><p id="p8743129191812"><a name="p8743129191812"></a><a name="p8743129191812"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.919008099190082%" headers="mcps1.1.7.1.5 "><p id="p1178918181914"><a name="p1178918181914"></a><a name="p1178918181914"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.239176082391761%" headers="mcps1.1.7.1.6 "><p id="p578171820196"><a name="p578171820196"></a><a name="p578171820196"></a>×</p>
</td>
</tr>
</tbody>
</table>

