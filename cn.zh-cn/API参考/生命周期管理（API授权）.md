# 生命周期管理<a name="ZH-CN_TOPIC_0103071510"></a>

<a name="table1587111571724"></a>
<table><thead align="left"><tr id="row5871165713215"><th class="cellrowborder" valign="top" width="35.039603960396036%" id="mcps1.1.5.1.1"><p id="p11871195719215"><a name="p11871195719215"></a><a name="p11871195719215"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="24.36633663366337%" id="mcps1.1.5.1.2"><p id="p28621644185118"><a name="p28621644185118"></a><a name="p28621644185118"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="20.792079207920793%" id="mcps1.1.5.1.3"><p id="p38711657129"><a name="p38711657129"></a><a name="p38711657129"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="19.801980198019802%" id="mcps1.1.5.1.4"><p id="p12900195215510"><a name="p12900195215510"></a><a name="p12900195215510"></a>授权项作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row6118143811524"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p9828202281915"><a name="p9828202281915"></a><a name="p9828202281915"></a>POST /v1/{project_id}/cloudservers</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p1286344465110"><a name="p1286344465110"></a><a name="p1286344465110"></a>创建云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul9828142210192"></a><a name="ul9828142210192"></a><ul id="ul9828142210192"><li>创建云服务器时新创建弹性IP<a name="ul233121516335"></a><a name="ul233121516335"></a><ul id="ul233121516335"><li>ecs:cloudServers:create</li><li>vpc:publicIps:create</li></ul>
</li><li>创建云服务器时绑定已有的弹性IP<a name="ul1287616455335"></a><a name="ul1287616455335"></a><ul id="ul1287616455335"><li>ecs:cloudServers:create</li><li>vpc:publicIps:update</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul9289914162912"></a><a name="ul9289914162912"></a><ul id="ul9289914162912"><li>支持：</li></ul>
<p id="p1228941411297"><a name="p1228941411297"></a><a name="p1228941411297"></a>项目(Project)</p>
<p id="p4289514182915"><a name="p4289514182915"></a><a name="p4289514182915"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row78644281610"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p1382822218198"><a name="p1382822218198"></a><a name="p1382822218198"></a>POST /v1/{project_id}/cloudservers/delete</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p08634442517"><a name="p08634442517"></a><a name="p08634442517"></a>删除云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul12828162216195"></a><a name="ul12828162216195"></a><ul id="ul12828162216195"><li>ecs:cloudServers:delete</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul11116411202911"></a><a name="ul11116411202911"></a><ul id="ul11116411202911"><li>支持：</li></ul>
<p id="p311615116299"><a name="p311615116299"></a><a name="p311615116299"></a>项目(Project)</p>
<p id="p171167111294"><a name="p171167111294"></a><a name="p171167111294"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row18675729"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p72614261323"><a name="p72614261323"></a><a name="p72614261323"></a>GET /v1/{project_id}/cloudservers/detail</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p1026112261827"><a name="p1026112261827"></a><a name="p1026112261827"></a>查询云服务器详情列表</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul1926113261522"></a><a name="ul1926113261522"></a><ul id="ul1926113261522"><li>ecs:cloudServers:list</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul1526216267219"></a><a name="ul1526216267219"></a><ul id="ul1526216267219"><li>支持：</li></ul>
<p id="p102621126320"><a name="p102621126320"></a><a name="p102621126320"></a>项目(Project)</p>
<p id="p626214261527"><a name="p626214261527"></a><a name="p626214261527"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1321071111217"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p1826214268219"><a name="p1826214268219"></a><a name="p1826214268219"></a>GET /v1/{project_id}/cloudservers/{server_id}</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p126222617214"><a name="p126222617214"></a><a name="p126222617214"></a>查询云服务器详情</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul82623267215"></a><a name="ul82623267215"></a><ul id="ul82623267215"><li>ecs:cloudServers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul82621261727"></a><a name="ul82621261727"></a><ul id="ul82621261727"><li>支持：</li></ul>
<p id="p17262182612218"><a name="p17262182612218"></a><a name="p17262182612218"></a>项目(Project)</p>
<p id="p12622261029"><a name="p12622261029"></a><a name="p12622261029"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1634414911210"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p42624262210"><a name="p42624262210"></a><a name="p42624262210"></a>PUT /v1/{project_id}/cloudservers/{server_id}</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p1262172619215"><a name="p1262172619215"></a><a name="p1262172619215"></a>修改弹性云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul142621026322"></a><a name="ul142621026322"></a><ul id="ul142621026322"><li>ecs:cloudServers:put</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul2262142618210"></a><a name="ul2262142618210"></a><ul id="ul2262142618210"><li>支持：</li></ul>
<p id="p12263226322"><a name="p12263226322"></a><a name="p12263226322"></a>项目(Project)</p>
<p id="p162637261623"><a name="p162637261623"></a><a name="p162637261623"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row38713577219"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p16337193516315"><a name="p16337193516315"></a><a name="p16337193516315"></a>GET /v2.1/{project_id}/servers/detail</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p369615322438"><a name="p369615322438"></a><a name="p369615322438"></a>查询云服务器详情列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul1933753518319"></a><a name="ul1933753518319"></a><ul id="ul1933753518319"><li>ecs:servers:list</li><li>ecs:servers:get</li></ul>
<a name="ul933763510316"></a><a name="ul933763510316"></a><ul id="ul933763510316"><li>ecs:serverVolumes:use</li><li>ecs:diskConfigs:use</li><li>ecs:securityGroups:use</li><li>ecs:serverKeypairs:get</li></ul>
<a name="ul1033718356310"></a><a name="ul1033718356310"></a><ul id="ul1033718356310"><li>vpc:securityGroups:get</li><li>vpc:securityGroupRules:get</li><li>vpc:networks:get</li><li>vpc:subnets:get</li><li>vpc:ports:get</li><li>vpc:routers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul16141662219"></a><a name="ul16141662219"></a><ul id="ul16141662219"><li>支持：</li></ul>
<p id="p5141169228"><a name="p5141169228"></a><a name="p5141169228"></a>项目(Project)</p>
<p id="p81419611221"><a name="p81419611221"></a><a name="p81419611221"></a></p>
<a name="ul101413616229"></a><a name="ul101413616229"></a><ul id="ul101413616229"><li>不支持：</li></ul>
<p id="p131419642219"><a name="p131419642219"></a><a name="p131419642219"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row58713574219"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p172163919520"><a name="p172163919520"></a><a name="p172163919520"></a>GET /v2.1/{project_id}/servers</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p1386254410510"><a name="p1386254410510"></a><a name="p1386254410510"></a>查询云服务器列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul372239658"></a><a name="ul372239658"></a><ul id="ul372239658"><li>ecs:servers:list</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul4406131612715"></a><a name="ul4406131612715"></a><ul id="ul4406131612715"><li>支持：</li></ul>
<p id="p114061816112715"><a name="p114061816112715"></a><a name="p114061816112715"></a>项目(Project)</p>
<p id="p194061516102718"><a name="p194061516102718"></a><a name="p194061516102718"></a></p>
<a name="ul7406716112711"></a><a name="ul7406716112711"></a><ul id="ul7406716112711"><li>不支持：</li></ul>
<p id="p4422516152717"><a name="p4422516152717"></a><a name="p4422516152717"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row88711057321"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p2723392051"><a name="p2723392051"></a><a name="p2723392051"></a>GET /v2.1/{project_id}/servers/{server_id}</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p108621644105118"><a name="p108621644105118"></a><a name="p108621644105118"></a>查询云服务器详情（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul87293914516"></a><a name="ul87293914516"></a><ul id="ul87293914516"><li>ecs:servers:get</li></ul>
<a name="ul169877811527"></a><a name="ul169877811527"></a><ul id="ul169877811527"><li>ecs:serverVolumes:use</li><li>ecs:diskConfigs:use</li><li>ecs:securityGroups:use</li><li>ecs:serverKeypairs:get</li></ul>
<a name="ul1698713811526"></a><a name="ul1698713811526"></a><ul id="ul1698713811526"><li>vpc:securityGroups:get</li><li>vpc:securityGroupRules:get</li><li>vpc:networks:get</li><li>vpc:subnets:get</li><li>vpc:ports:get</li><li>vpc:routers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul7171132892719"></a><a name="ul7171132892719"></a><ul id="ul7171132892719"><li>支持：</li></ul>
<p id="p81711428112717"><a name="p81711428112717"></a><a name="p81711428112717"></a>项目(Project)</p>
<p id="p191871528182714"><a name="p191871528182714"></a><a name="p191871528182714"></a></p>
<a name="ul61872028192714"></a><a name="ul61872028192714"></a><ul id="ul61872028192714"><li>不支持：</li></ul>
<p id="p51878288272"><a name="p51878288272"></a><a name="p51878288272"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row19755103191416"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p5883772911"><a name="p5883772911"></a><a name="p5883772911"></a>POST /v2.1/{project_id}/servers</p>
<p id="p11883670913"><a name="p11883670913"></a><a name="p11883670913"></a>POST /v2.1/{project_id}/os-volumes_boot</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p18605195717538"><a name="p18605195717538"></a><a name="p18605195717538"></a>创建云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul1388313711917"></a><a name="ul1388313711917"></a><ul id="ul1388313711917"><li>ecs:servers:create</li><li>ecs:servers:get</li><li>ecs:serverInterfaces:use</li><li>ecs:serverInterfaces:get</li><li>ecs:flavors:get</li><li>ecs:securityGroups:use</li></ul>
<a name="ul688318715914"></a><a name="ul688318715914"></a><ul id="ul688318715914"><li>evs:volumes:list</li><li>evs:volumes:get</li><li>evs:volumes:create</li><li>evs:volumes:attach</li><li>evs:volumes:manage</li><li>vpc:securityGroups:get</li></ul>
<a name="ul28841471697"></a><a name="ul28841471697"></a><ul id="ul28841471697"><li>vpc:networks:get</li><li>vpc:networks:update</li><li>vpc:subnets:get</li><li>vpc:subnets:update</li><li>vpc:ports:create</li><li>vpc:ports:update</li><li>vpc:ports:get</li><li>vpc:ports:delete</li><li>vpc:networks:create</li><li>vpc:subnets:create</li><li>vpc:routers:get</li><li>vpc:routers:update</li></ul>
<a name="ul13884117497"></a><a name="ul13884117497"></a><ul id="ul13884117497"><li>ims:images:list</li><li>ims:images:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul323164001415"></a><a name="ul323164001415"></a><ul id="ul323164001415"><li>支持：</li></ul>
<p id="p112319405145"><a name="p112319405145"></a><a name="p112319405145"></a>项目(Project)</p>
<p id="p723140121413"><a name="p723140121413"></a><a name="p723140121413"></a></p>
<a name="ul823154010146"></a><a name="ul823154010146"></a><ul id="ul823154010146"><li>不支持：</li></ul>
<p id="p32344071414"><a name="p32344071414"></a><a name="p32344071414"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row328513471419"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p33197248919"><a name="p33197248919"></a><a name="p33197248919"></a>DELETE /v2.1/{project_id}/servers/{server_id}</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p260615717539"><a name="p260615717539"></a><a name="p260615717539"></a>删除云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul1631916243919"></a><a name="ul1631916243919"></a><ul id="ul1631916243919"><li>ecs:servers:delete</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul75624463313"></a><a name="ul75624463313"></a><ul id="ul75624463313"><li>支持：</li></ul>
<p id="p10562646103119"><a name="p10562646103119"></a><a name="p10562646103119"></a>项目(Project)</p>
<p id="p1456215468318"><a name="p1456215468318"></a><a name="p1456215468318"></a></p>
<a name="ul1056244653117"></a><a name="ul1056244653117"></a><ul id="ul1056244653117"><li>不支持：</li></ul>
<p id="p105771946103116"><a name="p105771946103116"></a><a name="p105771946103116"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1262503681417"><td class="cellrowborder" valign="top" width="35.039603960396036%" headers="mcps1.1.5.1.1 "><p id="p731918241919"><a name="p731918241919"></a><a name="p731918241919"></a>PUT /v2.1/{project_id}/servers/{server_id}</p>
</td>
<td class="cellrowborder" valign="top" width="24.36633663366337%" headers="mcps1.1.5.1.2 "><p id="p116062577537"><a name="p116062577537"></a><a name="p116062577537"></a>修改云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul03191224499"></a><a name="ul03191224499"></a><ul id="ul03191224499"><li>ecs:servers:update</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul556185016316"></a><a name="ul556185016316"></a><ul id="ul556185016316"><li>支持：</li></ul>
<p id="p3561850173117"><a name="p3561850173117"></a><a name="p3561850173117"></a>项目(Project)</p>
<p id="p1756155023112"><a name="p1756155023112"></a><a name="p1756155023112"></a></p>
<a name="ul356112504317"></a><a name="ul356112504317"></a><ul id="ul356112504317"><li>不支持：</li></ul>
<p id="p85774506312"><a name="p85774506312"></a><a name="p85774506312"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

