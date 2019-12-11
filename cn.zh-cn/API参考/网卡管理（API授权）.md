# 网卡管理<a name="ZH-CN_TOPIC_0103071513"></a>

<a name="table166711250142311"></a>
<table><thead align="left"><tr id="row16721750172310"><th class="cellrowborder" valign="top" width="38.97%" id="mcps1.1.5.1.1"><p id="p1567220502233"><a name="p1567220502233"></a><a name="p1567220502233"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="20.03%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="21%" id="mcps1.1.5.1.3"><p id="p93075832319"><a name="p93075832319"></a><a name="p93075832319"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.1.5.1.4"><p id="p1130844411428"><a name="p1130844411428"></a><a name="p1130844411428"></a>授权项作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row9867181434418"><td class="cellrowborder" valign="top" width="38.97%" headers="mcps1.1.5.1.1 "><p id="p183578185443"><a name="p183578185443"></a><a name="p183578185443"></a>PUT /v1/{project_id}/cloudservers/nics/{nic_id}</p>
</td>
<td class="cellrowborder" valign="top" width="20.03%" headers="mcps1.1.5.1.2 "><p id="p1035771820449"><a name="p1035771820449"></a><a name="p1035771820449"></a>云服务器网卡配置私有IP</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.3 "><a name="ul5357121817444"></a><a name="ul5357121817444"></a><ul id="ul5357121817444"><li>ecs:cloudServerNics:update</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul5358118114412"></a><a name="ul5358118114412"></a><ul id="ul5358118114412"><li>支持：</li></ul>
<p id="p23581618204416"><a name="p23581618204416"></a><a name="p23581618204416"></a>项目(Project)</p>
<p id="p1535891813446"><a name="p1535891813446"></a><a name="p1535891813446"></a></p>
<a name="ul1135816181442"></a><a name="ul1135816181442"></a><ul id="ul1135816181442"><li>不支持：</li></ul>
<p id="p13358171824410"><a name="p13358171824410"></a><a name="p13358171824410"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1791015116446"><td class="cellrowborder" valign="top" width="38.97%" headers="mcps1.1.5.1.1 "><p id="p18358191824417"><a name="p18358191824417"></a><a name="p18358191824417"></a>POST /v1/{project_id}/cloudservers/{server_id}/nics/delete</p>
</td>
<td class="cellrowborder" valign="top" width="20.03%" headers="mcps1.1.5.1.2 "><p id="p73585185447"><a name="p73585185447"></a><a name="p73585185447"></a>批量删除云服务器网卡</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.3 "><a name="ul3358181815441"></a><a name="ul3358181815441"></a><ul id="ul3358181815441"><li>ecs:cloudServerNics:delete</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul23581118114412"></a><a name="ul23581118114412"></a><ul id="ul23581118114412"><li>支持：</li></ul>
<p id="p103591118194411"><a name="p103591118194411"></a><a name="p103591118194411"></a>项目(Project)</p>
<p id="p14359918104415"><a name="p14359918104415"></a><a name="p14359918104415"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row13910171120449"><td class="cellrowborder" valign="top" width="38.97%" headers="mcps1.1.5.1.1 "><p id="p1435951874411"><a name="p1435951874411"></a><a name="p1435951874411"></a>POST /v1/{project_id}/cloudservers/{server_id}/nics</p>
</td>
<td class="cellrowborder" valign="top" width="20.03%" headers="mcps1.1.5.1.2 "><p id="p12359141874418"><a name="p12359141874418"></a><a name="p12359141874418"></a>批量添加云服务器网卡</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.3 "><a name="ul7359151814415"></a><a name="ul7359151814415"></a><ul id="ul7359151814415"><li>ecs:cloudServers:addNics</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul1135921814411"></a><a name="ul1135921814411"></a><ul id="ul1135921814411"><li>支持：</li></ul>
<p id="p15359618134416"><a name="p15359618134416"></a><a name="p15359618134416"></a>项目(Project)</p>
<p id="p173598188445"><a name="p173598188445"></a><a name="p173598188445"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1973917711447"><td class="cellrowborder" valign="top" width="38.97%" headers="mcps1.1.5.1.1 "><p id="p63609181440"><a name="p63609181440"></a><a name="p63609181440"></a>GET /v1/{project_id}/cloudservers/{server_id}/os-interface</p>
</td>
<td class="cellrowborder" valign="top" width="20.03%" headers="mcps1.1.5.1.2 "><p id="p103603180442"><a name="p103603180442"></a><a name="p103603180442"></a>查询云服务器网卡信息</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.3 "><a name="ul10360171814440"></a><a name="ul10360171814440"></a><ul id="ul10360171814440"><li>ecs:cloudServers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul8360101854415"></a><a name="ul8360101854415"></a><ul id="ul8360101854415"><li>支持：</li></ul>
<p id="p143608185440"><a name="p143608185440"></a><a name="p143608185440"></a>项目(Project)</p>
<p id="p13360918194416"><a name="p13360918194416"></a><a name="p13360918194416"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row2672125032316"><td class="cellrowborder" valign="top" width="38.97%" headers="mcps1.1.5.1.1 "><p id="p33882125248"><a name="p33882125248"></a><a name="p33882125248"></a>POST /v2.1/{project_id}/servers/{server_id}/os-interface</p>
</td>
<td class="cellrowborder" valign="top" width="20.03%" headers="mcps1.1.5.1.2 "><p id="p02271056433"><a name="p02271056433"></a><a name="p02271056433"></a>添加云服务器网卡（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.3 "><a name="ul1388912122416"></a><a name="ul1388912122416"></a><ul id="ul1388912122416"><li>ecs:serverInterfaces:use</li><li>ecs:serverInterfaces:get</li></ul>
<a name="ul18388612152416"></a><a name="ul18388612152416"></a><ul id="ul18388612152416"><li>vpc:networks:get</li><li>vpc:networks:update</li><li>vpc:subnets:get</li><li>vpc:subnets:update</li><li>vpc:ports:create</li><li>vpc:ports:update</li><li>vpc:ports:get</li><li>vpc:networks:create</li><li>vpc:subnets:create</li><li>vpc:routers:get</li><li>vpc:routers:update</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul93731813713"></a><a name="ul93731813713"></a><ul id="ul93731813713"><li>支持：</li></ul>
<p id="p33888131113"><a name="p33888131113"></a><a name="p33888131113"></a>项目(Project)</p>
<p id="p1538820131514"><a name="p1538820131514"></a><a name="p1538820131514"></a></p>
<a name="ul23881813710"></a><a name="ul23881813710"></a><ul id="ul23881813710"><li>不支持：</li></ul>
<p id="p1338891314114"><a name="p1338891314114"></a><a name="p1338891314114"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row06721150152313"><td class="cellrowborder" valign="top" width="38.97%" headers="mcps1.1.5.1.1 "><p id="p1738911218249"><a name="p1738911218249"></a><a name="p1738911218249"></a>DELETE /v2.1/{project_id}/servers/{server_id}/os-interface/{id}</p>
</td>
<td class="cellrowborder" valign="top" width="20.03%" headers="mcps1.1.5.1.2 "><p id="p152273515431"><a name="p152273515431"></a><a name="p152273515431"></a>删除云服务器网卡（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.3 "><a name="ul193891312182411"></a><a name="ul193891312182411"></a><ul id="ul193891312182411"><li>ecs:serverInterfaces:use</li><li>ecs:serverInterfaces:get</li><li>ecs:servers:get</li></ul>
<a name="ul2038921282413"></a><a name="ul2038921282413"></a><ul id="ul2038921282413"><li>vpc:networks:create</li><li>vpc:subnets:create</li><li>vpc:networks:get</li><li>vpc:networks:update</li><li>vpc:subnets:get</li><li>vpc:subnets:update</li><li>vpc:ports:delete</li><li>vpc:ports:update</li><li>vpc:ports:get</li><li>vpc:routers:get</li><li>vpc:routers:update</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul182031577214"></a><a name="ul182031577214"></a><ul id="ul182031577214"><li>支持：</li></ul>
<p id="p42038570219"><a name="p42038570219"></a><a name="p42038570219"></a>项目(Project)</p>
<p id="p112031957621"><a name="p112031957621"></a><a name="p112031957621"></a></p>
<a name="ul5203557221"></a><a name="ul5203557221"></a><ul id="ul5203557221"><li>不支持：</li></ul>
<p id="p1320365710210"><a name="p1320365710210"></a><a name="p1320365710210"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row46721250112312"><td class="cellrowborder" valign="top" width="38.97%" headers="mcps1.1.5.1.1 "><p id="p1339151212245"><a name="p1339151212245"></a><a name="p1339151212245"></a>GET /v2.1/{project_id}/servers/{server_id}/os-interface</p>
</td>
<td class="cellrowborder" valign="top" width="20.03%" headers="mcps1.1.5.1.2 "><p id="p172276511435"><a name="p172276511435"></a><a name="p172276511435"></a>查询云服务器网卡信息列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.3 "><a name="ul1339121242413"></a><a name="ul1339121242413"></a><ul id="ul1339121242413"><li>ecs:serverInterfaces:get</li></ul>
<a name="ul1339161262419"></a><a name="ul1339161262419"></a><ul id="ul1339161262419"><li>vpc:ports:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul16107210320"></a><a name="ul16107210320"></a><ul id="ul16107210320"><li>支持：</li></ul>
<p id="p166101821238"><a name="p166101821238"></a><a name="p166101821238"></a>项目(Project)</p>
<p id="p8610921034"><a name="p8610921034"></a><a name="p8610921034"></a></p>
<a name="ul17610526319"></a><a name="ul17610526319"></a><ul id="ul17610526319"><li>不支持：</li></ul>
<p id="p5626622318"><a name="p5626622318"></a><a name="p5626622318"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row14673195092318"><td class="cellrowborder" valign="top" width="38.97%" headers="mcps1.1.5.1.1 "><p id="p3392131218246"><a name="p3392131218246"></a><a name="p3392131218246"></a>GET /v2.1/{project_id}/servers/{server_id}/os-interface/{id}</p>
</td>
<td class="cellrowborder" valign="top" width="20.03%" headers="mcps1.1.5.1.2 "><p id="p1022718514437"><a name="p1022718514437"></a><a name="p1022718514437"></a>查询指定云服务器网卡信息（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.3 "><a name="ul8392181232411"></a><a name="ul8392181232411"></a><ul id="ul8392181232411"><li>ecs:serverInterfaces:get</li></ul>
<a name="ul1392171214243"></a><a name="ul1392171214243"></a><ul id="ul1392171214243"><li>vpc:ports:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul173291154317"></a><a name="ul173291154317"></a><ul id="ul173291154317"><li>支持：</li></ul>
<p id="p19329155132"><a name="p19329155132"></a><a name="p19329155132"></a>项目(Project)</p>
<p id="p103292051534"><a name="p103292051534"></a><a name="p103292051534"></a></p>
<a name="ul1732935133"></a><a name="ul1732935133"></a><ul id="ul1732935133"><li>不支持：</li></ul>
<p id="p123459516318"><a name="p123459516318"></a><a name="p123459516318"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

