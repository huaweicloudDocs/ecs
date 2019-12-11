# 密码管理<a name="ZH-CN_TOPIC_0161341998"></a>

<a name="table1642432772714"></a>
<table><thead align="left"><tr id="row18424102718278"><th class="cellrowborder" valign="top" width="37%" id="mcps1.1.5.1.1"><p id="p242492712712"><a name="p242492712712"></a><a name="p242492712712"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="24%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.3"><p id="p12424827192710"><a name="p12424827192710"></a><a name="p12424827192710"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.1.5.1.4"><p id="p433072116440"><a name="p433072116440"></a><a name="p433072116440"></a>授权作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row194249274272"><td class="cellrowborder" valign="top" width="37%" headers="mcps1.1.5.1.1 "><p id="p1222154416276"><a name="p1222154416276"></a><a name="p1222154416276"></a>PUT /v1/{project_id}/cloudservers/{server_id}/os-reset-password</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p11463202315453"><a name="p11463202315453"></a><a name="p11463202315453"></a>一键重置弹性云服务器密码（企业项目）</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul0222154410277"></a><a name="ul0222154410277"></a><ul id="ul0222154410277"><li>ecs:cloudServers:resetServerPwd</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul1745764217118"></a><a name="ul1745764217118"></a><ul id="ul1745764217118"><li>支持：</li></ul>
<p id="p1645712421117"><a name="p1645712421117"></a><a name="p1645712421117"></a>项目(Project)</p>
<p id="p1045714211120"><a name="p1045714211120"></a><a name="p1045714211120"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row12055017318"><td class="cellrowborder" valign="top" width="37%" headers="mcps1.1.5.1.1 "><p id="p157805612311"><a name="p157805612311"></a><a name="p157805612311"></a>GET /v1/{project_id}/cloudservers/{server_id}/os-resetpwd-flag</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p1378020643119"><a name="p1378020643119"></a><a name="p1378020643119"></a>查询云服务器是否支持重置密码</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul1478066193116"></a><a name="ul1478066193116"></a><ul id="ul1478066193116"><li>ecs:cloudServers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul127801161319"></a><a name="ul127801161319"></a><ul id="ul127801161319"><li>支持：</li></ul>
<p id="p107804653118"><a name="p107804653118"></a><a name="p107804653118"></a>项目(Project)</p>
<p id="p6780156193117"><a name="p6780156193117"></a><a name="p6780156193117"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row10925193112"><td class="cellrowborder" valign="top" width="37%" headers="mcps1.1.5.1.1 "><p id="p11781968315"><a name="p11781968315"></a><a name="p11781968315"></a>GET /v1/{project_id}/cloudservers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p197816618310"><a name="p197816618310"></a><a name="p197816618310"></a>Windows云服务器获取密码</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul5781126173114"></a><a name="ul5781126173114"></a><ul id="ul5781126173114"><li>ecs:cloudServers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul11781166133113"></a><a name="ul11781166133113"></a><ul id="ul11781166133113"><li>支持：</li></ul>
<p id="p157816615319"><a name="p157816615319"></a><a name="p157816615319"></a>项目(Project)</p>
<p id="p1178112613112"><a name="p1178112613112"></a><a name="p1178112613112"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row101014513118"><td class="cellrowborder" valign="top" width="37%" headers="mcps1.1.5.1.1 "><p id="p1478266163112"><a name="p1478266163112"></a><a name="p1478266163112"></a>DELETE /v1/{project_id}/cloudservers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p187821667316"><a name="p187821667316"></a><a name="p187821667316"></a>Windows云服务器清除密码</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul97821964311"></a><a name="ul97821964311"></a><ul id="ul97821964311"><li>ecs:cloudServers:deletePassword</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul1078216618315"></a><a name="ul1078216618315"></a><ul id="ul1078216618315"><li>支持：</li></ul>
<p id="p4782206153114"><a name="p4782206153114"></a><a name="p4782206153114"></a>项目(Project)</p>
<p id="p9782156163119"><a name="p9782156163119"></a><a name="p9782156163119"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row7588153714318"><td class="cellrowborder" valign="top" width="37%" headers="mcps1.1.5.1.1 "><p id="p10589173784318"><a name="p10589173784318"></a><a name="p10589173784318"></a>PUT /v2.1/{project_id}/servers/{server_id}/os-reset-password</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p19589183713432"><a name="p19589183713432"></a><a name="p19589183713432"></a>一键重置弹性云服务器云主机密码</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul189614211435"></a><a name="ul189614211435"></a><ul id="ul189614211435"><li>ecs:cloudServers:resetServerPwd</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul5363250184313"></a><a name="ul5363250184313"></a><ul id="ul5363250184313"><li>支持：</li></ul>
<p id="p14363105034312"><a name="p14363105034312"></a><a name="p14363105034312"></a>项目(Project)</p>
<p id="p13635506438"><a name="p13635506438"></a><a name="p13635506438"></a></p>
<a name="ul1736395016439"></a><a name="ul1736395016439"></a><ul id="ul1736395016439"><li>不支持：</li></ul>
<p id="p1936312501431"><a name="p1936312501431"></a><a name="p1936312501431"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row103333346171"><td class="cellrowborder" valign="top" width="37%" headers="mcps1.1.5.1.1 "><p id="p6932412182715"><a name="p6932412182715"></a><a name="p6932412182715"></a>GET /v2.1/{project_id}/servers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p19606175714531"><a name="p19606175714531"></a><a name="p19606175714531"></a>Windows云服务器获取密码（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul1693212126274"></a><a name="ul1693212126274"></a><ul id="ul1693212126274"><li>ecs:serverPasswords:manage</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul17101722163712"></a><a name="ul17101722163712"></a><ul id="ul17101722163712"><li>支持：</li></ul>
<p id="p7101172214374"><a name="p7101172214374"></a><a name="p7101172214374"></a>项目(Project)</p>
<p id="p5277175123817"><a name="p5277175123817"></a><a name="p5277175123817"></a></p>
<a name="ul61161222103710"></a><a name="ul61161222103710"></a><ul id="ul61161222103710"><li>不支持：</li></ul>
<p id="p611620222375"><a name="p611620222375"></a><a name="p611620222375"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row41213781718"><td class="cellrowborder" valign="top" width="37%" headers="mcps1.1.5.1.1 "><p id="p3932161252712"><a name="p3932161252712"></a><a name="p3932161252712"></a>DELETE /v2.1/{project_id}/servers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" width="24%" headers="mcps1.1.5.1.2 "><p id="p20606175785313"><a name="p20606175785313"></a><a name="p20606175785313"></a>Windows云服务器清除密码（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.3 "><a name="ul1693381214271"></a><a name="ul1693381214271"></a><ul id="ul1693381214271"><li>ecs:serverPasswords:manage</li></ul>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.5.1.4 "><a name="ul882062418378"></a><a name="ul882062418378"></a><ul id="ul882062418378"><li>支持：</li></ul>
<p id="p8820182417378"><a name="p8820182417378"></a><a name="p8820182417378"></a>项目(Project)</p>
<p id="p1383935333816"><a name="p1383935333816"></a><a name="p1383935333816"></a></p>
<a name="ul98351424143719"></a><a name="ul98351424143719"></a><ul id="ul98351424143719"><li>不支持：</li></ul>
<p id="p1835152411370"><a name="p1835152411370"></a><a name="p1835152411370"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

