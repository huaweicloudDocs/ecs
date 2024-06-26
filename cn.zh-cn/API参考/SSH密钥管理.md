# SSH密钥管理<a name="ecs_06_0013"></a>

<a name="table796561272518"></a>
<table><thead align="left"><tr id="row10966111213255"><th class="cellrowborder" valign="top" width="9.69%" id="mcps1.1.9.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="17.27%" id="mcps1.1.9.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="19.3%" id="mcps1.1.9.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="15.590000000000002%" id="mcps1.1.9.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="9.17%" id="mcps1.1.9.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="14.499999999999998%" id="mcps1.1.9.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
<th class="cellrowborder" valign="top" width="6.959999999999999%" id="mcps1.1.9.1.7"><p id="p208711814017"><a name="p208711814017"></a><a name="p208711814017"></a>实例授权</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.9.1.8"><p id="p448411313408"><a name="p448411313408"></a><a name="p448411313408"></a>标签授权</p>
</th>
</tr>
</thead>
<tbody><tr id="row796681232520"><td class="cellrowborder" valign="top" width="9.69%" headers="mcps1.1.9.1.1 "><p id="p36571412162316"><a name="p36571412162316"></a><a name="p36571412162316"></a><a href="创建和导入SSH密钥.md">创建和导入SSH密钥（OpenStack原生）</a></p>
</td>
<td class="cellrowborder" valign="top" width="17.27%" headers="mcps1.1.9.1.2 "><p id="p2217113414398"><a name="p2217113414398"></a><a name="p2217113414398"></a>POST /v2.1/{project_id}/os-keypairs</p>
</td>
<td class="cellrowborder" valign="top" width="19.3%" headers="mcps1.1.9.1.3 "><p id="p202471359152116"><a name="p202471359152116"></a><a name="p202471359152116"></a>ecs:serverKeypairs:create</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.1.9.1.4 "><p id="p12288111932314"><a name="p12288111932314"></a><a name="p12288111932314"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.17%" headers="mcps1.1.9.1.5 "><p id="p1178918181914"><a name="p1178918181914"></a><a name="p1178918181914"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.499999999999998%" headers="mcps1.1.9.1.6 "><p id="p578171820196"><a name="p578171820196"></a><a name="p578171820196"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="6.959999999999999%" headers="mcps1.1.9.1.7 "><p id="p1987110813408"><a name="p1987110813408"></a><a name="p1987110813408"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.9.1.8 "><p id="p11484713144018"><a name="p11484713144018"></a><a name="p11484713144018"></a>×</p>
</td>
</tr>
<tr id="row179662012132520"><td class="cellrowborder" valign="top" width="9.69%" headers="mcps1.1.9.1.1 "><p id="p565712127235"><a name="p565712127235"></a><a name="p565712127235"></a><a href="查询SSH密钥详情.md">查询SSH密钥详情（OpenStack原生）</a></p>
</td>
<td class="cellrowborder" valign="top" width="17.27%" headers="mcps1.1.9.1.2 "><p id="p2360123823916"><a name="p2360123823916"></a><a name="p2360123823916"></a>GET /v2.1/{project_id}/os-keypairs/{keypair_name}</p>
</td>
<td class="cellrowborder" valign="top" width="19.3%" headers="mcps1.1.9.1.3 "><p id="p1329680112212"><a name="p1329680112212"></a><a name="p1329680112212"></a>ecs:serverKeypairs:get</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.1.9.1.4 "><p id="p15288181913238"><a name="p15288181913238"></a><a name="p15288181913238"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.17%" headers="mcps1.1.9.1.5 "><p id="p1423520574243"><a name="p1423520574243"></a><a name="p1423520574243"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.499999999999998%" headers="mcps1.1.9.1.6 "><p id="p723515719248"><a name="p723515719248"></a><a name="p723515719248"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="6.959999999999999%" headers="mcps1.1.9.1.7 "><p id="p587117813409"><a name="p587117813409"></a><a name="p587117813409"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.9.1.8 "><p id="p1648401320402"><a name="p1648401320402"></a><a name="p1648401320402"></a>×</p>
</td>
</tr>
<tr id="row2096611215254"><td class="cellrowborder" valign="top" width="9.69%" headers="mcps1.1.9.1.1 "><p id="p16571612142319"><a name="p16571612142319"></a><a name="p16571612142319"></a><a href="查询SSH密钥列表.md">查询SSH密钥列表（OpenStack原生）</a></p>
</td>
<td class="cellrowborder" valign="top" width="17.27%" headers="mcps1.1.9.1.2 "><p id="p203891743103910"><a name="p203891743103910"></a><a name="p203891743103910"></a>GET /v2.1/{project_id}/os-keypairs</p>
</td>
<td class="cellrowborder" valign="top" width="19.3%" headers="mcps1.1.9.1.3 "><p id="p543601132220"><a name="p543601132220"></a><a name="p543601132220"></a>ecs:serverKeypairs:list</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.1.9.1.4 "><p id="p182889191234"><a name="p182889191234"></a><a name="p182889191234"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.17%" headers="mcps1.1.9.1.5 "><p id="p1064255862418"><a name="p1064255862418"></a><a name="p1064255862418"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.499999999999998%" headers="mcps1.1.9.1.6 "><p id="p176425585248"><a name="p176425585248"></a><a name="p176425585248"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="6.959999999999999%" headers="mcps1.1.9.1.7 "><p id="p68717824017"><a name="p68717824017"></a><a name="p68717824017"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.9.1.8 "><p id="p1248416131402"><a name="p1248416131402"></a><a name="p1248416131402"></a>×</p>
</td>
</tr>
<tr id="row1896617127258"><td class="cellrowborder" valign="top" width="9.69%" headers="mcps1.1.9.1.1 "><p id="p126572127231"><a name="p126572127231"></a><a name="p126572127231"></a><a href="删除SSH密钥.md">删除SSH密钥（OpenStack原生）</a></p>
</td>
<td class="cellrowborder" valign="top" width="17.27%" headers="mcps1.1.9.1.2 "><p id="p160084713911"><a name="p160084713911"></a><a name="p160084713911"></a>DELETE /v2.1/{project_id}/os-keypairs/{keypair_name}</p>
</td>
<td class="cellrowborder" valign="top" width="19.3%" headers="mcps1.1.9.1.3 "><p id="p535318242220"><a name="p535318242220"></a><a name="p535318242220"></a>ecs:serverKeypairs:delete</p>
</td>
<td class="cellrowborder" valign="top" width="15.590000000000002%" headers="mcps1.1.9.1.4 "><p id="p182881519132314"><a name="p182881519132314"></a><a name="p182881519132314"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="9.17%" headers="mcps1.1.9.1.5 "><p id="p18798195932419"><a name="p18798195932419"></a><a name="p18798195932419"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.499999999999998%" headers="mcps1.1.9.1.6 "><p id="p3798135912420"><a name="p3798135912420"></a><a name="p3798135912420"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="6.959999999999999%" headers="mcps1.1.9.1.7 "><p id="p18871085400"><a name="p18871085400"></a><a name="p18871085400"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.9.1.8 "><p id="p194846137409"><a name="p194846137409"></a><a name="p194846137409"></a>×</p>
</td>
</tr>
</tbody>
</table>

