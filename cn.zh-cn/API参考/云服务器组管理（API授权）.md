# 云服务器组管理<a name="ZH-CN_TOPIC_0103071520"></a>

<a name="table818845922715"></a>
<table><thead align="left"><tr id="row7188175902716"><th class="cellrowborder" valign="top" width="10.421042104210422%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="30.503050305030506%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="23.912391239123913%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="19.23192319231923%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="8.12081208120812%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="7.81078107810781%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row1739712213368"><td class="cellrowborder" valign="top" width="10.421042104210422%" headers="mcps1.1.7.1.1 "><p id="p13350192320273"><a name="p13350192320273"></a><a name="p13350192320273"></a>删除云服务器组</p>
</td>
<td class="cellrowborder" valign="top" width="30.503050305030506%" headers="mcps1.1.7.1.2 "><p id="p1657484819494"><a name="p1657484819494"></a><a name="p1657484819494"></a>DELETE /v1/{project_id}/cloudservers/os-server-groups/{server_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23.912391239123913%" headers="mcps1.1.7.1.3 "><p id="p1274584810234"><a name="p1274584810234"></a><a name="p1274584810234"></a>ecs:cloudServers:delete</p>
</td>
<td class="cellrowborder" valign="top" width="19.23192319231923%" headers="mcps1.1.7.1.4 "><p id="p1584903011278"><a name="p1584903011278"></a><a name="p1584903011278"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.12081208120812%" headers="mcps1.1.7.1.5 "><p id="p79824201716"><a name="p79824201716"></a><a name="p79824201716"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.81078107810781%" headers="mcps1.1.7.1.6 "><p id="p1098219212179"><a name="p1098219212179"></a><a name="p1098219212179"></a>√</p>
</td>
</tr>
<tr id="row1039722293615"><td class="cellrowborder" valign="top" width="10.421042104210422%" headers="mcps1.1.7.1.1 "><p id="p1835022315276"><a name="p1835022315276"></a><a name="p1835022315276"></a>创建云服务器组</p>
</td>
<td class="cellrowborder" valign="top" width="30.503050305030506%" headers="mcps1.1.7.1.2 "><p id="p95442162314"><a name="p95442162314"></a><a name="p95442162314"></a>POST /v1{project_id}/cloudservers/os-server-groups</p>
</td>
<td class="cellrowborder" valign="top" width="23.912391239123913%" headers="mcps1.1.7.1.3 "><p id="p208565404263"><a name="p208565404263"></a><a name="p208565404263"></a>ecs:cloudServers:create</p>
</td>
<td class="cellrowborder" valign="top" width="19.23192319231923%" headers="mcps1.1.7.1.4 "><p id="p584903082717"><a name="p584903082717"></a><a name="p584903082717"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.12081208120812%" headers="mcps1.1.7.1.5 "><p id="p074330192911"><a name="p074330192911"></a><a name="p074330192911"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.81078107810781%" headers="mcps1.1.7.1.6 "><p id="p107432015296"><a name="p107432015296"></a><a name="p107432015296"></a>√</p>
</td>
</tr>
<tr id="row1939702214363"><td class="cellrowborder" valign="top" width="10.421042104210422%" headers="mcps1.1.7.1.1 "><p id="p19350122316279"><a name="p19350122316279"></a><a name="p19350122316279"></a>云服务器组添加成员</p>
</td>
<td class="cellrowborder" valign="top" width="30.503050305030506%" headers="mcps1.1.7.1.2 "><p id="p84911316183615"><a name="p84911316183615"></a><a name="p84911316183615"></a>POST /v1/{project_id}/cloudservers/os-server-groups/{server_group_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="23.912391239123913%" headers="mcps1.1.7.1.3 "><p id="p1468917516588"><a name="p1468917516588"></a><a name="p1468917516588"></a>ecs:cloudServers:create</p>
</td>
<td class="cellrowborder" valign="top" width="19.23192319231923%" headers="mcps1.1.7.1.4 "><p id="p784919300273"><a name="p784919300273"></a><a name="p784919300273"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.12081208120812%" headers="mcps1.1.7.1.5 "><p id="p5371182152910"><a name="p5371182152910"></a><a name="p5371182152910"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.81078107810781%" headers="mcps1.1.7.1.6 "><p id="p837114213295"><a name="p837114213295"></a><a name="p837114213295"></a>√</p>
</td>
</tr>
<tr id="row19398922143617"><td class="cellrowborder" valign="top" width="10.421042104210422%" headers="mcps1.1.7.1.1 "><p id="p18350162362718"><a name="p18350162362718"></a><a name="p18350162362718"></a>云服务器组删除成员</p>
</td>
<td class="cellrowborder" valign="top" width="30.503050305030506%" headers="mcps1.1.7.1.2 "><p id="p73117467262"><a name="p73117467262"></a><a name="p73117467262"></a>POST /v1/{project_id}/cloudservers/os-server-groups/{server_group_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="23.912391239123913%" headers="mcps1.1.7.1.3 "><p id="p9381117115812"><a name="p9381117115812"></a><a name="p9381117115812"></a>ecs:cloudServers:delete</p>
</td>
<td class="cellrowborder" valign="top" width="19.23192319231923%" headers="mcps1.1.7.1.4 "><p id="p4849103016275"><a name="p4849103016275"></a><a name="p4849103016275"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.12081208120812%" headers="mcps1.1.7.1.5 "><p id="p46116310294"><a name="p46116310294"></a><a name="p46116310294"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.81078107810781%" headers="mcps1.1.7.1.6 "><p id="p166111316298"><a name="p166111316298"></a><a name="p166111316298"></a>√</p>
</td>
</tr>
<tr id="row1919025918277"><td class="cellrowborder" valign="top" width="10.421042104210422%" headers="mcps1.1.7.1.1 "><p id="p635082310276"><a name="p635082310276"></a><a name="p635082310276"></a>创建云服务器组（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="30.503050305030506%" headers="mcps1.1.7.1.2 "><p id="p1261552114219"><a name="p1261552114219"></a><a name="p1261552114219"></a>POST /v2.1/{project_id}/os-server-groups</p>
</td>
<td class="cellrowborder" valign="top" width="23.912391239123913%" headers="mcps1.1.7.1.3 "><p id="p467571520586"><a name="p467571520586"></a><a name="p467571520586"></a>ecs:serverGroups:manage</p>
</td>
<td class="cellrowborder" valign="top" width="19.23192319231923%" headers="mcps1.1.7.1.4 "><p id="p1584943018273"><a name="p1584943018273"></a><a name="p1584943018273"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.12081208120812%" headers="mcps1.1.7.1.5 "><p id="p551811571269"><a name="p551811571269"></a><a name="p551811571269"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.81078107810781%" headers="mcps1.1.7.1.6 "><p id="p135181357102610"><a name="p135181357102610"></a><a name="p135181357102610"></a>×</p>
</td>
</tr>
<tr id="row2190135914273"><td class="cellrowborder" valign="top" width="10.421042104210422%" headers="mcps1.1.7.1.1 "><p id="p12351182315279"><a name="p12351182315279"></a><a name="p12351182315279"></a>查询云服务器组列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="30.503050305030506%" headers="mcps1.1.7.1.2 "><p id="p3901573429"><a name="p3901573429"></a><a name="p3901573429"></a>GET /v2.1/{project_id}/os-server-groups</p>
</td>
<td class="cellrowborder" valign="top" width="23.912391239123913%" headers="mcps1.1.7.1.3 "><p id="p13672101811581"><a name="p13672101811581"></a><a name="p13672101811581"></a>ecs:serverGroups:manage</p>
</td>
<td class="cellrowborder" valign="top" width="19.23192319231923%" headers="mcps1.1.7.1.4 "><p id="p178491930122716"><a name="p178491930122716"></a><a name="p178491930122716"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.12081208120812%" headers="mcps1.1.7.1.5 "><p id="p1287351772913"><a name="p1287351772913"></a><a name="p1287351772913"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.81078107810781%" headers="mcps1.1.7.1.6 "><p id="p1187318172291"><a name="p1187318172291"></a><a name="p1187318172291"></a>×</p>
</td>
</tr>
<tr id="row278754211811"><td class="cellrowborder" valign="top" width="10.421042104210422%" headers="mcps1.1.7.1.1 "><p id="p93515234276"><a name="p93515234276"></a><a name="p93515234276"></a>查询云服务器组详情（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="30.503050305030506%" headers="mcps1.1.7.1.2 "><p id="p7494181134210"><a name="p7494181134210"></a><a name="p7494181134210"></a>GET /v2.1/{project_id}/os-server-groups/{server_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23.912391239123913%" headers="mcps1.1.7.1.3 "><p id="p187419208581"><a name="p187419208581"></a><a name="p187419208581"></a>ecs:serverGroups:manage</p>
</td>
<td class="cellrowborder" valign="top" width="19.23192319231923%" headers="mcps1.1.7.1.4 "><p id="p1984993062714"><a name="p1984993062714"></a><a name="p1984993062714"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.12081208120812%" headers="mcps1.1.7.1.5 "><p id="p735371917294"><a name="p735371917294"></a><a name="p735371917294"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.81078107810781%" headers="mcps1.1.7.1.6 "><p id="p1335317191299"><a name="p1335317191299"></a><a name="p1335317191299"></a>×</p>
</td>
</tr>
<tr id="row13190135952716"><td class="cellrowborder" valign="top" width="10.421042104210422%" headers="mcps1.1.7.1.1 "><p id="p33511323152714"><a name="p33511323152714"></a><a name="p33511323152714"></a>删除云服务器组（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="30.503050305030506%" headers="mcps1.1.7.1.2 "><p id="p73221016204211"><a name="p73221016204211"></a><a name="p73221016204211"></a>DELETE /v2.1/{project_id}/os-server-groups/{server_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23.912391239123913%" headers="mcps1.1.7.1.3 "><p id="p372392155815"><a name="p372392155815"></a><a name="p372392155815"></a>ecs:serverGroups:manage</p>
</td>
<td class="cellrowborder" valign="top" width="19.23192319231923%" headers="mcps1.1.7.1.4 "><p id="p2084913307276"><a name="p2084913307276"></a><a name="p2084913307276"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.12081208120812%" headers="mcps1.1.7.1.5 "><p id="p184321204293"><a name="p184321204293"></a><a name="p184321204293"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.81078107810781%" headers="mcps1.1.7.1.6 "><p id="p174321720172913"><a name="p174321720172913"></a><a name="p174321720172913"></a>×</p>
</td>
</tr>
</tbody>
</table>

