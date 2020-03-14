# 云服务器组管理<a name="ZH-CN_TOPIC_0103071520"></a>

<a name="table818845922715"></a>
<table><thead align="left"><tr id="row7188175902716"><th class="cellrowborder" valign="top" width="40.21212121212122%" id="mcps1.1.5.1.1"><p id="p2188659102719"><a name="p2188659102719"></a><a name="p2188659102719"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="16.90909090909091%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="23.686868686868685%" id="mcps1.1.5.1.3"><p id="p319018598276"><a name="p319018598276"></a><a name="p319018598276"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="19.191919191919194%" id="mcps1.1.5.1.4"><p id="p65185294419"><a name="p65185294419"></a><a name="p65185294419"></a>授权作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row1739712213368"><td class="cellrowborder" valign="top" width="40.21212121212122%" headers="mcps1.1.5.1.1 "><p id="p1657484819494"><a name="p1657484819494"></a><a name="p1657484819494"></a>DELETE /v1/{project_id}/cloudservers/os-server-groups/{server_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="16.90909090909091%" headers="mcps1.1.5.1.2 "><p id="p1575164811495"><a name="p1575164811495"></a><a name="p1575164811495"></a>删除云服务器组</p>
</td>
<td class="cellrowborder" valign="top" width="23.686868686868685%" headers="mcps1.1.5.1.3 "><p id="p1274584810234"><a name="p1274584810234"></a><a name="p1274584810234"></a>ecs:cloudServers:delete</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.1.5.1.4 "><a name="ul1957511483494"></a><a name="ul1957511483494"></a><ul id="ul1957511483494"><li>支持：</li></ul>
<p id="p16575648184911"><a name="p16575648184911"></a><a name="p16575648184911"></a>项目(Project)</p>
<p id="p17575194854911"><a name="p17575194854911"></a><a name="p17575194854911"></a></p>
<a name="ul18575164814912"></a><a name="ul18575164814912"></a><ul id="ul18575164814912"><li>支持：</li></ul>
<p id="p14577648184917"><a name="p14577648184917"></a><a name="p14577648184917"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1039722293615"><td class="cellrowborder" valign="top" width="40.21212121212122%" headers="mcps1.1.5.1.1 "><p id="p95442162314"><a name="p95442162314"></a><a name="p95442162314"></a>POST /v1{project_id}/cloudservers/os-server-groups</p>
</td>
<td class="cellrowborder" valign="top" width="16.90909090909091%" headers="mcps1.1.5.1.2 "><p id="p75420219238"><a name="p75420219238"></a><a name="p75420219238"></a>创建云服务器组</p>
</td>
<td class="cellrowborder" valign="top" width="23.686868686868685%" headers="mcps1.1.5.1.3 "><p id="p208565404263"><a name="p208565404263"></a><a name="p208565404263"></a>ecs:cloudServers:create</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.1.5.1.4 "><a name="ul35419214232"></a><a name="ul35419214232"></a><ul id="ul35419214232"><li>支持：</li></ul>
<p id="p13541821132320"><a name="p13541821132320"></a><a name="p13541821132320"></a>项目(Project)</p>
<p id="p1454421182317"><a name="p1454421182317"></a><a name="p1454421182317"></a></p>
<a name="ul1054152162318"></a><a name="ul1054152162318"></a><ul id="ul1054152162318"><li>支持：</li></ul>
<p id="p65410211232"><a name="p65410211232"></a><a name="p65410211232"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1939702214363"><td class="cellrowborder" valign="top" width="40.21212121212122%" headers="mcps1.1.5.1.1 "><p id="p84911316183615"><a name="p84911316183615"></a><a name="p84911316183615"></a>POST /v1/{project_id}/cloudservers/os-server-groups/{server_group_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="16.90909090909091%" headers="mcps1.1.5.1.2 "><p id="p72697214365"><a name="p72697214365"></a><a name="p72697214365"></a>云服务器云主机组添加成员</p>
</td>
<td class="cellrowborder" valign="top" width="23.686868686868685%" headers="mcps1.1.5.1.3 "><p id="p1468917516588"><a name="p1468917516588"></a><a name="p1468917516588"></a>ecs:cloudServers:create</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.1.5.1.4 "><a name="ul192794712366"></a><a name="ul192794712366"></a><ul id="ul192794712366"><li>支持：</li></ul>
<p id="p2279127193617"><a name="p2279127193617"></a><a name="p2279127193617"></a>项目(Project)</p>
<p id="p1227918753610"><a name="p1227918753610"></a><a name="p1227918753610"></a></p>
<a name="ul727918712368"></a><a name="ul727918712368"></a><ul id="ul727918712368"><li>支持：</li></ul>
<p id="p4279127133615"><a name="p4279127133615"></a><a name="p4279127133615"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row19398922143617"><td class="cellrowborder" valign="top" width="40.21212121212122%" headers="mcps1.1.5.1.1 "><p id="p73117467262"><a name="p73117467262"></a><a name="p73117467262"></a>POST /v1/{project_id}/cloudservers/os-server-groups/{server_group_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="16.90909090909091%" headers="mcps1.1.5.1.2 "><p id="p19927185164112"><a name="p19927185164112"></a><a name="p19927185164112"></a>云服务器组删除成员</p>
</td>
<td class="cellrowborder" valign="top" width="23.686868686868685%" headers="mcps1.1.5.1.3 "><p id="p9381117115812"><a name="p9381117115812"></a><a name="p9381117115812"></a>ecs:cloudServers:delete</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.1.5.1.4 "><a name="ul1792715164119"></a><a name="ul1792715164119"></a><ul id="ul1792715164119"><li>支持：</li></ul>
<p id="p19285512414"><a name="p19285512414"></a><a name="p19285512414"></a>项目(Project)</p>
<p id="p169283544118"><a name="p169283544118"></a><a name="p169283544118"></a></p>
<a name="ul59281352412"></a><a name="ul59281352412"></a><ul id="ul59281352412"><li>支持：</li></ul>
<p id="p129289534111"><a name="p129289534111"></a><a name="p129289534111"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1919025918277"><td class="cellrowborder" valign="top" width="40.21212121212122%" headers="mcps1.1.5.1.1 "><p id="p1261552114219"><a name="p1261552114219"></a><a name="p1261552114219"></a>POST /v2.1/{project_id}/os-server-groups</p>
</td>
<td class="cellrowborder" valign="top" width="16.90909090909091%" headers="mcps1.1.5.1.2 "><p id="p51751858144418"><a name="p51751858144418"></a><a name="p51751858144418"></a>创建云服务器组（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="23.686868686868685%" headers="mcps1.1.5.1.3 "><p id="p467571520586"><a name="p467571520586"></a><a name="p467571520586"></a>ecs:serverGroups:manage</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.1.5.1.4 "><a name="ul1439117322109"></a><a name="ul1439117322109"></a><ul id="ul1439117322109"><li>支持：</li></ul>
<p id="p93911432201015"><a name="p93911432201015"></a><a name="p93911432201015"></a>项目(Project)</p>
<p id="p1039113221010"><a name="p1039113221010"></a><a name="p1039113221010"></a></p>
<a name="ul43911932131017"></a><a name="ul43911932131017"></a><ul id="ul43911932131017"><li>不支持：</li></ul>
<p id="p139112320101"><a name="p139112320101"></a><a name="p139112320101"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row2190135914273"><td class="cellrowborder" valign="top" width="40.21212121212122%" headers="mcps1.1.5.1.1 "><p id="p3901573429"><a name="p3901573429"></a><a name="p3901573429"></a>GET /v2.1/{project_id}/os-server-groups</p>
</td>
<td class="cellrowborder" valign="top" width="16.90909090909091%" headers="mcps1.1.5.1.2 "><p id="p131751358184415"><a name="p131751358184415"></a><a name="p131751358184415"></a>查询云服务器组列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="23.686868686868685%" headers="mcps1.1.5.1.3 "><p id="p13672101811581"><a name="p13672101811581"></a><a name="p13672101811581"></a>ecs:serverGroups:manage</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.1.5.1.4 "><a name="ul191125861014"></a><a name="ul191125861014"></a><ul id="ul191125861014"><li>支持：</li></ul>
<p id="p71658101014"><a name="p71658101014"></a><a name="p71658101014"></a>项目(Project)</p>
<p id="p121558131020"><a name="p121558131020"></a><a name="p121558131020"></a></p>
<a name="ul18113584100"></a><a name="ul18113584100"></a><ul id="ul18113584100"><li>不支持：</li></ul>
<p id="p71195871019"><a name="p71195871019"></a><a name="p71195871019"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row278754211811"><td class="cellrowborder" valign="top" width="40.21212121212122%" headers="mcps1.1.5.1.1 "><p id="p7494181134210"><a name="p7494181134210"></a><a name="p7494181134210"></a>GET /v2.1/{project_id}/os-server-groups/{server_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="16.90909090909091%" headers="mcps1.1.5.1.2 "><p id="p95762046684"><a name="p95762046684"></a><a name="p95762046684"></a>查询云服务器组详情（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="23.686868686868685%" headers="mcps1.1.5.1.3 "><p id="p187419208581"><a name="p187419208581"></a><a name="p187419208581"></a>ecs:serverGroups:manage</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.1.5.1.4 "><a name="ul45762461816"></a><a name="ul45762461816"></a><ul id="ul45762461816"><li>支持：</li></ul>
<p id="p11576114611819"><a name="p11576114611819"></a><a name="p11576114611819"></a>项目(Project)</p>
<p id="p357684615812"><a name="p357684615812"></a><a name="p357684615812"></a></p>
<a name="ul75761446586"></a><a name="ul75761446586"></a><ul id="ul75761446586"><li>不支持：</li></ul>
<p id="p4576124616811"><a name="p4576124616811"></a><a name="p4576124616811"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row13190135952716"><td class="cellrowborder" valign="top" width="40.21212121212122%" headers="mcps1.1.5.1.1 "><p id="p73221016204211"><a name="p73221016204211"></a><a name="p73221016204211"></a>DELETE /v2.1/{project_id}/os-server-groups/{server_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="16.90909090909091%" headers="mcps1.1.5.1.2 "><p id="p1017511584446"><a name="p1017511584446"></a><a name="p1017511584446"></a>删除云服务器组（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="23.686868686868685%" headers="mcps1.1.5.1.3 "><p id="p372392155815"><a name="p372392155815"></a><a name="p372392155815"></a>ecs:serverGroups:manage</p>
</td>
<td class="cellrowborder" valign="top" width="19.191919191919194%" headers="mcps1.1.5.1.4 "><a name="ul3719111191111"></a><a name="ul3719111191111"></a><ul id="ul3719111191111"><li>支持：</li></ul>
<p id="p1871918114116"><a name="p1871918114116"></a><a name="p1871918114116"></a>项目(Project)</p>
<p id="p1971971171117"><a name="p1971971171117"></a><a name="p1971971171117"></a></p>
<a name="ul167191318110"></a><a name="ul167191318110"></a><ul id="ul167191318110"><li>不支持：</li></ul>
<p id="p171913171112"><a name="p171913171112"></a><a name="p171913171112"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

