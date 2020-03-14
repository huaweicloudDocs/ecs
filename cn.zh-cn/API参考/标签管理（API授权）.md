# 标签管理<a name="ZH-CN_TOPIC_0103071521"></a>

<a name="table4509123112811"></a>
<table><thead align="left"><tr id="row19509193152818"><th class="cellrowborder" valign="top" width="37.05%" id="mcps1.1.5.1.1"><p id="p55099315280"><a name="p55099315280"></a><a name="p55099315280"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="24.95%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="17%" id="mcps1.1.5.1.3"><p id="p175092031182817"><a name="p175092031182817"></a><a name="p175092031182817"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="21%" id="mcps1.1.5.1.4"><p id="p1734131020449"><a name="p1734131020449"></a><a name="p1734131020449"></a>授权作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row169138403108"><td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.1.5.1.1 "><p id="p613135211104"><a name="p613135211104"></a><a name="p613135211104"></a>POST  /v1/{project_id}/cloudservers/{server_id}/tags/action</p>
</td>
<td class="cellrowborder" valign="top" width="24.95%" headers="mcps1.1.5.1.2 "><p id="p168128381113"><a name="p168128381113"></a><a name="p168128381113"></a>批量添加云服务器标签/批量删除云服务器标签</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.3 "><a name="ul741213010125"></a><a name="ul741213010125"></a><ul id="ul741213010125"><li>ecs:cloudServers:put</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.4 "><a name="ul1792715164119"></a><a name="ul1792715164119"></a><ul id="ul1792715164119"><li>支持：</li></ul>
<p id="p19285512414"><a name="p19285512414"></a><a name="p19285512414"></a>项目(Project)</p>
<p id="p169283544118"><a name="p169283544118"></a><a name="p169283544118"></a></p>
<a name="ul59281352412"></a><a name="ul59281352412"></a><ul id="ul59281352412"><li>支持：</li></ul>
<p id="p129289534111"><a name="p129289534111"></a><a name="p129289534111"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row528011248461"><td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.1.5.1.1 "><p id="p162801924124620"><a name="p162801924124620"></a><a name="p162801924124620"></a>GET /v1/{project_id}/cloudservers/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.95%" headers="mcps1.1.5.1.2 "><p id="p3280524124613"><a name="p3280524124613"></a><a name="p3280524124613"></a>查询项目标签</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.3 "><a name="ul55661041174613"></a><a name="ul55661041174613"></a><ul id="ul55661041174613"><li>ecs:cloudServers:list</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.4 "><a name="ul1592594913469"></a><a name="ul1592594913469"></a><ul id="ul1592594913469"><li>支持：</li></ul>
<p id="p2092564912462"><a name="p2092564912462"></a><a name="p2092564912462"></a>项目(Project)</p>
<p id="p2092684910464"><a name="p2092684910464"></a><a name="p2092684910464"></a></p>
<a name="ul1926104904614"></a><a name="ul1926104904614"></a><ul id="ul1926104904614"><li>支持：</li></ul>
<p id="p20926949144616"><a name="p20926949144616"></a><a name="p20926949144616"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row261813360"><td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.1.5.1.1 "><p id="p958291073619"><a name="p958291073619"></a><a name="p958291073619"></a>GET /v1/{project_id}/cloudservers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.95%" headers="mcps1.1.5.1.2 "><p id="p19887191353611"><a name="p19887191353611"></a><a name="p19887191353611"></a>查询云服务器标签</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.3 "><a name="ul169981975368"></a><a name="ul169981975368"></a><ul id="ul169981975368"><li>ecs:cloudServers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.4 "><a name="ul18998574366"></a><a name="ul18998574366"></a><ul id="ul18998574366"><li>支持：</li></ul>
<p id="p1199857113616"><a name="p1199857113616"></a><a name="p1199857113616"></a>项目(Project)</p>
<p id="p139981977369"><a name="p139981977369"></a><a name="p139981977369"></a></p>
<a name="ul19982753615"></a><a name="ul19982753615"></a><ul id="ul19982753615"><li>支持：</li></ul>
<p id="p599818703618"><a name="p599818703618"></a><a name="p599818703618"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row676275515115"><td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.1.5.1.1 "><p id="p776319551911"><a name="p776319551911"></a><a name="p776319551911"></a>GET /v1/{project_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.95%" headers="mcps1.1.5.1.2 "><p id="p137631355512"><a name="p137631355512"></a><a name="p137631355512"></a>查询云服务器标签</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.3 "><a name="ul1589193215382"></a><a name="ul1589193215382"></a><ul id="ul1589193215382"><li>ecs:servers:getTags</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.4 "><a name="ul12465193561010"></a><a name="ul12465193561010"></a><ul id="ul12465193561010"><li>支持：</li></ul>
<p id="p1846523518100"><a name="p1846523518100"></a><a name="p1846523518100"></a>项目(Project)</p>
</td>
</tr>
<tr id="row175291830184314"><td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.1.5.1.1 "><p id="p4238141844315"><a name="p4238141844315"></a><a name="p4238141844315"></a>GET /v2.1/{project_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.95%" headers="mcps1.1.5.1.2 "><p id="p1098533511434"><a name="p1098533511434"></a><a name="p1098533511434"></a>查询指定云服务器标签列表(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.3 "><a name="ul1898593515437"></a><a name="ul1898593515437"></a><ul id="ul1898593515437"><li>ecs:servers:getTags</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.4 "><a name="ul16985113512432"></a><a name="ul16985113512432"></a><ul id="ul16985113512432"><li>支持：</li></ul>
<p id="p79851835174312"><a name="p79851835174312"></a><a name="p79851835174312"></a>项目(Project)</p>
<p id="p10985163512436"><a name="p10985163512436"></a><a name="p10985163512436"></a></p>
<a name="ul149851735194312"></a><a name="ul149851735194312"></a><ul id="ul149851735194312"><li>不支持：</li></ul>
<p id="p598518358430"><a name="p598518358430"></a><a name="p598518358430"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row553163014438"><td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.1.5.1.1 "><p id="p447082244315"><a name="p447082244315"></a><a name="p447082244315"></a>PUT /v2.1/{project_id}/servers/{server_id}/tags/{tag}</p>
</td>
<td class="cellrowborder" valign="top" width="24.95%" headers="mcps1.1.5.1.2 "><p id="p3986435184317"><a name="p3986435184317"></a><a name="p3986435184317"></a>给指定弹性云服务器添加标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.3 "><a name="ul29861535184313"></a><a name="ul29861535184313"></a><ul id="ul29861535184313"><li>ecs:servers:setTags</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.4 "><a name="ul998683511436"></a><a name="ul998683511436"></a><ul id="ul998683511436"><li>支持：</li></ul>
<p id="p8986103513437"><a name="p8986103513437"></a><a name="p8986103513437"></a>项目(Project)</p>
<p id="p0986103511438"><a name="p0986103511438"></a><a name="p0986103511438"></a></p>
<a name="ul8986123519436"></a><a name="ul8986123519436"></a><ul id="ul8986123519436"><li>不支持：</li></ul>
<p id="p1298617351431"><a name="p1298617351431"></a><a name="p1298617351431"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1661113346435"><td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.1.5.1.1 "><p id="p988313810430"><a name="p988313810430"></a><a name="p988313810430"></a>PUT /v2.1/{project_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.95%" headers="mcps1.1.5.1.2 "><p id="p1998673512438"><a name="p1998673512438"></a><a name="p1998673512438"></a>创建云服务器标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.3 "><a name="ul298663534316"></a><a name="ul298663534316"></a><ul id="ul298663534316"><li>ecs:servers:setTags</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.4 "><a name="ul398683511432"></a><a name="ul398683511432"></a><ul id="ul398683511432"><li>支持：</li></ul>
<p id="p199861535164316"><a name="p199861535164316"></a><a name="p199861535164316"></a>项目(Project)</p>
<p id="p5986143524313"><a name="p5986143524313"></a><a name="p5986143524313"></a></p>
<a name="ul898633524311"></a><a name="ul898633524311"></a><ul id="ul898633524311"><li>不支持：</li></ul>
<p id="p49862357434"><a name="p49862357434"></a><a name="p49862357434"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row105321930104310"><td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.1.5.1.1 "><p id="p127395094318"><a name="p127395094318"></a><a name="p127395094318"></a>DELETE /v2.1/{project_id}/servers/{server_id}/tags/{tag}</p>
</td>
<td class="cellrowborder" valign="top" width="24.95%" headers="mcps1.1.5.1.2 "><p id="p2987153514433"><a name="p2987153514433"></a><a name="p2987153514433"></a>删除云服务器的指定标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.3 "><a name="ul49875351438"></a><a name="ul49875351438"></a><ul id="ul49875351438"><li>ecs:servers:setTags</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.4 "><a name="ul298719358431"></a><a name="ul298719358431"></a><ul id="ul298719358431"><li>支持：</li></ul>
<p id="p4987035104310"><a name="p4987035104310"></a><a name="p4987035104310"></a>项目(Project)</p>
<p id="p6987143504319"><a name="p6987143504319"></a><a name="p6987143504319"></a></p>
<a name="ul15987123524311"></a><a name="ul15987123524311"></a><ul id="ul15987123524311"><li>不支持：</li></ul>
<p id="p209873355433"><a name="p209873355433"></a><a name="p209873355433"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row353283018431"><td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.1.5.1.1 "><p id="p181272014417"><a name="p181272014417"></a><a name="p181272014417"></a>GET /v2.1/{project_id}/servers/{server_id}/tags/{tag}</p>
</td>
<td class="cellrowborder" valign="top" width="24.95%" headers="mcps1.1.5.1.2 "><p id="p798713517430"><a name="p798713517430"></a><a name="p798713517430"></a>查询云服务器是否存在指定标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.3 "><a name="ul59871835174319"></a><a name="ul59871835174319"></a><ul id="ul59871835174319"><li>ecs:servers:getTags</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.4 "><a name="ul198713355436"></a><a name="ul198713355436"></a><ul id="ul198713355436"><li>支持：</li></ul>
<p id="p1398717357434"><a name="p1398717357434"></a><a name="p1398717357434"></a>项目(Project)</p>
<p id="p1498733511430"><a name="p1498733511430"></a><a name="p1498733511430"></a></p>
<a name="ul12987203512438"></a><a name="ul12987203512438"></a><ul id="ul12987203512438"><li>不支持：</li></ul>
<p id="p209871835124317"><a name="p209871835124317"></a><a name="p209871835124317"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row10532193004319"><td class="cellrowborder" valign="top" width="37.05%" headers="mcps1.1.5.1.1 "><p id="p7726121014414"><a name="p7726121014414"></a><a name="p7726121014414"></a>DELETE /v2.1/{project_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.95%" headers="mcps1.1.5.1.2 "><p id="p129881935204317"><a name="p129881935204317"></a><a name="p129881935204317"></a>删除云服务器所有标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.3 "><a name="ul109881035104318"></a><a name="ul109881035104318"></a><ul id="ul109881035104318"><li>ecs:servers:setTags</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.4 "><a name="ul59881635154318"></a><a name="ul59881635154318"></a><ul id="ul59881635154318"><li>支持：</li></ul>
<p id="p698883524318"><a name="p698883524318"></a><a name="p698883524318"></a>项目(Project)</p>
<p id="p298873514439"><a name="p298873514439"></a><a name="p298873514439"></a></p>
<a name="ul10988135204315"></a><a name="ul10988135204315"></a><ul id="ul10988135204315"><li>不支持：</li></ul>
<p id="p189881357436"><a name="p189881357436"></a><a name="p189881357436"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

