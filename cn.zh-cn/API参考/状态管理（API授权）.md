# 状态管理<a name="ZH-CN_TOPIC_0103071511"></a>

<a name="table12570457816"></a>
<table><thead align="left"><tr id="row2025712451682"><th class="cellrowborder" valign="top" width="35%" id="mcps1.1.5.1.1"><p id="p72571745883"><a name="p72571745883"></a><a name="p72571745883"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="24.94%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="21.060000000000002%" id="mcps1.1.5.1.3"><p id="p162571745883"><a name="p162571745883"></a><a name="p162571745883"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.4"><p id="p12900195215510"><a name="p12900195215510"></a><a name="p12900195215510"></a>授权项作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row43301239171419"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p1478183141917"><a name="p1478183141917"></a><a name="p1478183141917"></a>POST /v2/{project_id}/cloudservers/{server_id}/changeos</p>
<p id="p144788317197"><a name="p144788317197"></a><a name="p144788317197"></a>POST /v1/{project_id}/cloudservers/{server_id}/changeos</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p4183378205559"><a name="p4183378205559"></a><a name="p4183378205559"></a>切换弹性云服务器操作系统</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul747812371910"></a><a name="ul747812371910"></a><ul id="ul747812371910"><li>ecs:cloudServers:changeOS</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul5972153512283"></a><a name="ul5972153512283"></a><ul id="ul5972153512283"><li>支持：</li></ul>
<p id="p179721135152811"><a name="p179721135152811"></a><a name="p179721135152811"></a>项目(Project)</p>
<p id="p6972173513280"><a name="p6972173513280"></a><a name="p6972173513280"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1225714451388"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p54781035190"><a name="p54781035190"></a><a name="p54781035190"></a>POST /v2/{project_id}/cloudservers/{server_id}/reinstallos</p>
<p id="p134786313191"><a name="p134786313191"></a><a name="p134786313191"></a>POST /v1/{project_id}/cloudservers/{server_id}/reinstallos</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p1993921813394"><a name="p1993921813394"></a><a name="p1993921813394"></a>重装弹性云服务器操作系统</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul047811315199"></a><a name="ul047811315199"></a><ul id="ul047811315199"><li>ecs:cloudServers:rebuild</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul773819399280"></a><a name="ul773819399280"></a><ul id="ul773819399280"><li>支持：</li></ul>
<p id="p18738133913281"><a name="p18738133913281"></a><a name="p18738133913281"></a>项目(Project)</p>
<p id="p673803914281"><a name="p673803914281"></a><a name="p673803914281"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row113711517144014"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p204781139197"><a name="p204781139197"></a><a name="p204781139197"></a>POST /v1/{project_id}/cloudservers/{server_id}/resize</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p1686224415113"><a name="p1686224415113"></a><a name="p1686224415113"></a>变更云服务器规格</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul194781331914"></a><a name="ul194781331914"></a><ul id="ul194781331914"><li>ecs:cloudServers:resize</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul128584412288"></a><a name="ul128584412288"></a><ul id="ul128584412288"><li>支持：</li></ul>
<p id="p1028584492817"><a name="p1028584492817"></a><a name="p1028584492817"></a>项目(Project)</p>
<p id="p928518446289"><a name="p928518446289"></a><a name="p928518446289"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row12332174073420"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p1497201991811"><a name="p1497201991811"></a><a name="p1497201991811"></a>POST /v1/{project_id}/cloudservers/{server_id}/migrate</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p17497171917188"><a name="p17497171917188"></a><a name="p17497171917188"></a>冷迁移云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul42841353172214"></a><a name="ul42841353172214"></a><ul id="ul42841353172214"><li>ecs:cloudServers:migrate</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul95081446141810"></a><a name="ul95081446141810"></a><ul id="ul95081446141810"><li>支持：</li></ul>
<p id="p145081946131811"><a name="p145081946131811"></a><a name="p145081946131811"></a>项目(Project)</p>
<p id="p8508124621818"><a name="p8508124621818"></a><a name="p8508124621818"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row52571745582"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p032112243919"><a name="p032112243919"></a><a name="p032112243919"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p76061457195316"><a name="p76061457195316"></a><a name="p76061457195316"></a>关闭云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul632116243917"></a><a name="ul632116243917"></a><ul id="ul632116243917"><li>ecs:servers:stop</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul1620295715315"></a><a name="ul1620295715315"></a><ul id="ul1620295715315"><li>支持：</li></ul>
<p id="p2020215710319"><a name="p2020215710319"></a><a name="p2020215710319"></a>项目(Project)</p>
<p id="p3219357153111"><a name="p3219357153111"></a><a name="p3219357153111"></a></p>
<a name="ul321975718315"></a><a name="ul321975718315"></a><ul id="ul321975718315"><li>不支持：</li></ul>
<p id="p621965723115"><a name="p621965723115"></a><a name="p621965723115"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row172571445985"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p19321824193"><a name="p19321824193"></a><a name="p19321824193"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p860675714535"><a name="p860675714535"></a><a name="p860675714535"></a>重启云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul1332192415914"></a><a name="ul1332192415914"></a><ul id="ul1332192415914"><li>ecs:servers:reboot</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul16410704321"></a><a name="ul16410704321"></a><ul id="ul16410704321"><li>支持：</li></ul>
<p id="p1641016010322"><a name="p1641016010322"></a><a name="p1641016010322"></a>项目(Project)</p>
<p id="p14101405320"><a name="p14101405320"></a><a name="p14101405320"></a></p>
<a name="ul14268083218"></a><a name="ul14268083218"></a><ul id="ul14268083218"><li>不支持：</li></ul>
<p id="p1542660143215"><a name="p1542660143215"></a><a name="p1542660143215"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1525717451489"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p032110243914"><a name="p032110243914"></a><a name="p032110243914"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p186061757165319"><a name="p186061757165319"></a><a name="p186061757165319"></a>变更云服务器规格（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul1632115247916"></a><a name="ul1632115247916"></a><ul id="ul1632115247916"><li>ecs:servers:resize</li><li>ecs:servers:get</li></ul>
<a name="ul13212241396"></a><a name="ul13212241396"></a><ul id="ul13212241396"><li>evs:volumes:list</li><li>evs:volumes:create</li><li>evs:volumes:get</li><li>evs:volumes:attach</li><li>evs:volumes:detach</li><li>evs:volumes:manage</li></ul>
<a name="ul193211124399"></a><a name="ul193211124399"></a><ul id="ul193211124399"><li>vpc:ports:get</li><li>vpc:ports:update</li><li>vpc:ports:creare</li><li>vpc:ports:delete</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul09737153211"></a><a name="ul09737153211"></a><ul id="ul09737153211"><li>支持：</li></ul>
<p id="p1698771153215"><a name="p1698771153215"></a><a name="p1698771153215"></a>项目(Project)</p>
<p id="p18987121203218"><a name="p18987121203218"></a><a name="p18987121203218"></a></p>
<a name="ul1298771123212"></a><a name="ul1298771123212"></a><ul id="ul1298771123212"><li>不支持：</li></ul>
<p id="p11987101183213"><a name="p11987101183213"></a><a name="p11987101183213"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row19808934597"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p1550144717916"><a name="p1550144717916"></a><a name="p1550144717916"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p960685795319"><a name="p960685795319"></a><a name="p960685795319"></a>锁定云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul1850647494"></a><a name="ul1850647494"></a><ul id="ul1850647494"><li>ecs:servers:lock</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul1789517733214"></a><a name="ul1789517733214"></a><ul id="ul1789517733214"><li>支持：</li></ul>
<p id="p8909157193219"><a name="p8909157193219"></a><a name="p8909157193219"></a>项目(Project)</p>
<p id="p19909157203213"><a name="p19909157203213"></a><a name="p19909157203213"></a></p>
<a name="ul12909137113214"></a><a name="ul12909137113214"></a><ul id="ul12909137113214"><li>不支持：</li></ul>
<p id="p5909147203214"><a name="p5909147203214"></a><a name="p5909147203214"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1180814349912"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p550164716914"><a name="p550164716914"></a><a name="p550164716914"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p560645745312"><a name="p560645745312"></a><a name="p560645745312"></a>解锁定云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul15020472098"></a><a name="ul15020472098"></a><ul id="ul15020472098"><li>ecs:servers:unlock</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul281589193212"></a><a name="ul281589193212"></a><ul id="ul281589193212"><li>支持：</li></ul>
<p id="p183219163217"><a name="p183219163217"></a><a name="p183219163217"></a>项目(Project)</p>
<p id="p19832195321"><a name="p19832195321"></a><a name="p19832195321"></a></p>
<a name="ul683211911327"></a><a name="ul683211911327"></a><ul id="ul683211911327"><li>不支持：</li></ul>
<p id="p10832119123218"><a name="p10832119123218"></a><a name="p10832119123218"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

