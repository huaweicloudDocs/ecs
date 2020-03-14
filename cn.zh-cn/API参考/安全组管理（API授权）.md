# 安全组管理<a name="ZH-CN_TOPIC_0103072347"></a>

<a name="table614680103012"></a>
<table><thead align="left"><tr id="row121463017301"><th class="cellrowborder" valign="top" width="35%" id="mcps1.1.5.1.1"><p id="p201463083017"><a name="p201463083017"></a><a name="p201463083017"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="23%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="24%" id="mcps1.1.5.1.3"><p id="p51461506309"><a name="p51461506309"></a><a name="p51461506309"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="18%" id="mcps1.1.5.1.4"><p id="p362061417425"><a name="p362061417425"></a><a name="p362061417425"></a>授权项作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row141469023019"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p174241828203118"><a name="p174241828203118"></a><a name="p174241828203118"></a>POST /v2.1/{project_id}/os-security-groups</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p1610821144210"><a name="p1610821144210"></a><a name="p1610821144210"></a>创建安全组(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.3 "><a name="ul119581321306"></a><a name="ul119581321306"></a><ul id="ul119581321306"><li>ecs:securityGroups:use</li></ul>
<a name="ul1958632173018"></a><a name="ul1958632173018"></a><ul id="ul1958632173018"><li>vpc:securityGroups:get</li><li>vpc:securityGroups:create</li><li>vpc:securityGroups:update</li></ul>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.1.5.1.4 "><a name="ul1123814145713"></a><a name="ul1123814145713"></a><ul id="ul1123814145713"><li>支持：</li></ul>
<p id="p132386418574"><a name="p132386418574"></a><a name="p132386418574"></a>项目(Project)</p>
<p id="p132381946577"><a name="p132381946577"></a><a name="p132381946577"></a></p>
<a name="ul132387411578"></a><a name="ul132387411578"></a><ul id="ul132387411578"><li>不支持：</li></ul>
<p id="p202522485716"><a name="p202522485716"></a><a name="p202522485716"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row714610173016"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p1572117398318"><a name="p1572117398318"></a><a name="p1572117398318"></a>DELETE /v2.1/{project_id}/os-security-groups/{security_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p111012111429"><a name="p111012111429"></a><a name="p111012111429"></a>删除安全组(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.3 "><a name="ul4958153215300"></a><a name="ul4958153215300"></a><ul id="ul4958153215300"><li>ecs:securityGroups:use</li></ul>
<a name="ul129581832173018"></a><a name="ul129581832173018"></a><ul id="ul129581832173018"><li>vpc:securityGroups:get</li><li>vpc:securityGroups:delete</li><li>vpc:securityGroups:update</li></ul>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.1.5.1.4 "><a name="ul895449105915"></a><a name="ul895449105915"></a><ul id="ul895449105915"><li>支持：</li></ul>
<p id="p119685915592"><a name="p119685915592"></a><a name="p119685915592"></a>项目(Project)</p>
<p id="p496819945914"><a name="p496819945914"></a><a name="p496819945914"></a></p>
<a name="ul16968595590"></a><a name="ul16968595590"></a><ul id="ul16968595590"><li>不支持：</li></ul>
<p id="p696820917592"><a name="p696820917592"></a><a name="p696820917592"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row111468093016"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p16711195820310"><a name="p16711195820310"></a><a name="p16711195820310"></a>GET /v2.1/{project_id}/os-security-groups/{security_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p1010132174219"><a name="p1010132174219"></a><a name="p1010132174219"></a>查询安全组详细信息(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.3 "><a name="ul29591632103018"></a><a name="ul29591632103018"></a><ul id="ul29591632103018"><li>ecs:securityGroups:use</li></ul>
<a name="ul396053212304"></a><a name="ul396053212304"></a><ul id="ul396053212304"><li>vpc:securityGroups:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.1.5.1.4 "><a name="ul18594101215913"></a><a name="ul18594101215913"></a><ul id="ul18594101215913"><li>支持：</li></ul>
<p id="p760981214593"><a name="p760981214593"></a><a name="p760981214593"></a>项目(Project)</p>
<p id="p19609812125912"><a name="p19609812125912"></a><a name="p19609812125912"></a></p>
<a name="ul860941265912"></a><a name="ul860941265912"></a><ul id="ul860941265912"><li>不支持：</li></ul>
<p id="p1060931218592"><a name="p1060931218592"></a><a name="p1060931218592"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1914610012300"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p11337939321"><a name="p11337939321"></a><a name="p11337939321"></a>GET /v2.1/{project_id}/os-security-groups</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p310221114218"><a name="p310221114218"></a><a name="p310221114218"></a>查询安全组列表(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.3 "><a name="ul696013326305"></a><a name="ul696013326305"></a><ul id="ul696013326305"><li>ecs:securityGroups:use</li></ul>
<a name="ul13960732183020"></a><a name="ul13960732183020"></a><ul id="ul13960732183020"><li>vpc:securityGroups:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.1.5.1.4 "><a name="ul33911814165917"></a><a name="ul33911814165917"></a><ul id="ul33911814165917"><li>支持：</li></ul>
<p id="p17391171405912"><a name="p17391171405912"></a><a name="p17391171405912"></a>项目(Project)</p>
<p id="p193911014185914"><a name="p193911014185914"></a><a name="p193911014185914"></a></p>
<a name="ul2391151416595"></a><a name="ul2391151416595"></a><ul id="ul2391151416595"><li>不支持：</li></ul>
<p id="p13407121425918"><a name="p13407121425918"></a><a name="p13407121425918"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row9146903301"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p15127771327"><a name="p15127771327"></a><a name="p15127771327"></a>POST /v2.1/{project_id}/os-security-group-rules</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p20101421114212"><a name="p20101421114212"></a><a name="p20101421114212"></a>创建安全组规则(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.3 "><a name="ul196063215305"></a><a name="ul196063215305"></a><ul id="ul196063215305"><li>ecs:securityGroups:use</li></ul>
<a name="ul12960193215307"></a><a name="ul12960193215307"></a><ul id="ul12960193215307"><li>vpc:securityGroups:get</li><li>vpc:securityGroups:update</li><li>vpc:securityGroupRules:get</li><li>vpc:securityGroupRules:create</li></ul>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.1.5.1.4 "><a name="ul18438716125914"></a><a name="ul18438716125914"></a><ul id="ul18438716125914"><li>支持：</li></ul>
<p id="p745471612598"><a name="p745471612598"></a><a name="p745471612598"></a>项目(Project)</p>
<p id="p945451619596"><a name="p945451619596"></a><a name="p945451619596"></a></p>
<a name="ul13454171616594"></a><a name="ul13454171616594"></a><ul id="ul13454171616594"><li>不支持：</li></ul>
<p id="p184543165599"><a name="p184543165599"></a><a name="p184543165599"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row19146707308"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p554073153218"><a name="p554073153218"></a><a name="p554073153218"></a>DELETE /v2.1/{project_id}/os-security-group-rules/{security_group_rule_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p161062164211"><a name="p161062164211"></a><a name="p161062164211"></a>删除安全组规则(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.3 "><a name="ul1896013217300"></a><a name="ul1896013217300"></a><ul id="ul1896013217300"><li>ecs:securityGroups:use</li></ul>
<a name="ul59602032133019"></a><a name="ul59602032133019"></a><ul id="ul59602032133019"><li>vpc:securityGroups:get</li><li>vpc:securityGroups:update</li><li>vpc:securityGroupRules:get</li><li>vpc:securityGroupRules:delete</li></ul>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.1.5.1.4 "><a name="ul114123075916"></a><a name="ul114123075916"></a><ul id="ul114123075916"><li>支持：</li></ul>
<p id="p15141173012593"><a name="p15141173012593"></a><a name="p15141173012593"></a>项目(Project)</p>
<p id="p81412306592"><a name="p81412306592"></a><a name="p81412306592"></a></p>
<a name="ul10157123065912"></a><a name="ul10157123065912"></a><ul id="ul10157123065912"><li>不支持：</li></ul>
<p id="p4157330125916"><a name="p4157330125916"></a><a name="p4157330125916"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row5146906301"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p1623064263217"><a name="p1623064263217"></a><a name="p1623064263217"></a>PUT /v2.1/{project_id}/os-security-groups/{security_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p811102104214"><a name="p811102104214"></a><a name="p811102104214"></a>更新安全组信息(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.3 "><a name="ul189601632173011"></a><a name="ul189601632173011"></a><ul id="ul189601632173011"><li>ecs:securityGroups:use</li></ul>
<a name="ul16960153212306"></a><a name="ul16960153212306"></a><ul id="ul16960153212306"><li>vpc:securityGroups:get</li><li>vpc:securityGroups:update</li></ul>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.1.5.1.4 "><a name="ul19546163245912"></a><a name="ul19546163245912"></a><ul id="ul19546163245912"><li>支持：</li></ul>
<p id="p1454693285916"><a name="p1454693285916"></a><a name="p1454693285916"></a>项目(Project)</p>
<p id="p205462328591"><a name="p205462328591"></a><a name="p205462328591"></a></p>
<a name="ul25468324596"></a><a name="ul25468324596"></a><ul id="ul25468324596"><li>不支持：</li></ul>
<p id="p35461321593"><a name="p35461321593"></a><a name="p35461321593"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row511081915302"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p56631353123214"><a name="p56631353123214"></a><a name="p56631353123214"></a>GET /v2.1/{project_id}/servers/{server_id}/os-security-groups</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p101132114219"><a name="p101132114219"></a><a name="p101132114219"></a>查询指定云服务器安全组列表(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.3 "><a name="ul69612324300"></a><a name="ul69612324300"></a><ul id="ul69612324300"><li>ecs:securityGroups:use</li></ul>
<a name="ul17961143212308"></a><a name="ul17961143212308"></a><ul id="ul17961143212308"><li>vpc:securityGroups:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.1.5.1.4 "><a name="ul33441836185914"></a><a name="ul33441836185914"></a><ul id="ul33441836185914"><li>支持：</li></ul>
<p id="p1134416367596"><a name="p1134416367596"></a><a name="p1134416367596"></a>项目(Project)</p>
<p id="p183607363599"><a name="p183607363599"></a><a name="p183607363599"></a></p>
<a name="ul13360836155915"></a><a name="ul13360836155915"></a><ul id="ul13360836155915"><li>不支持：</li></ul>
<p id="p236083616594"><a name="p236083616594"></a><a name="p236083616594"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row41101119143010"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p99431459183215"><a name="p99431459183215"></a><a name="p99431459183215"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p81112111424"><a name="p81112111424"></a><a name="p81112111424"></a>添加安全组（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.3 "><a name="ul1796133213309"></a><a name="ul1796133213309"></a><ul id="ul1796133213309"><li>ecs:securityGroups:use</li><li>ecs:servers:get</li></ul>
<a name="ul16961133293017"></a><a name="ul16961133293017"></a><ul id="ul16961133293017"><li>vpc:securityGroups:get</li><li>vpc:securityGroups:create</li><li>vpc:securityGroups:update</li><li>vpc:ports:get</li><li>vpc:ports:update</li></ul>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.1.5.1.4 "><a name="ul137511639115913"></a><a name="ul137511639115913"></a><ul id="ul137511639115913"><li>支持：</li></ul>
<p id="p07662394599"><a name="p07662394599"></a><a name="p07662394599"></a>项目(Project)</p>
<p id="p19766939125913"><a name="p19766939125913"></a><a name="p19766939125913"></a></p>
<a name="ul776683914597"></a><a name="ul776683914597"></a><ul id="ul776683914597"><li>不支持：</li></ul>
<p id="p12766193913596"><a name="p12766193913596"></a><a name="p12766193913596"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row51102019153019"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p54371318143319"><a name="p54371318143319"></a><a name="p54371318143319"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.5.1.2 "><p id="p161172134216"><a name="p161172134216"></a><a name="p161172134216"></a>移除安全组（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.3 "><a name="ul59611132123017"></a><a name="ul59611132123017"></a><ul id="ul59611132123017"><li>ecs:securityGroups:use</li><li>ecs:servers:get</li></ul>
<a name="ul199611432183017"></a><a name="ul199611432183017"></a><ul id="ul199611432183017"><li>vpc:securityGroups:get</li><li>vpc:securityGroups:delete</li><li>vpc:securityGroups:update</li><li>vpc:ports:get</li><li>vpc:ports:update</li></ul>
</td>
<td class="cellrowborder" valign="top" width="18%" headers="mcps1.1.5.1.4 "><a name="ul8156164216594"></a><a name="ul8156164216594"></a><ul id="ul8156164216594"><li>支持：</li></ul>
<p id="p61561342135917"><a name="p61561342135917"></a><a name="p61561342135917"></a>项目(Project)</p>
<p id="p215620426597"><a name="p215620426597"></a><a name="p215620426597"></a></p>
<a name="ul1415694215914"></a><a name="ul1415694215914"></a><ul id="ul1415694215914"><li>不支持：</li></ul>
<p id="p2156134210591"><a name="p2156134210591"></a><a name="p2156134210591"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

