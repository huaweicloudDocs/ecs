# 云服务器控制台管理<a name="ZH-CN_TOPIC_0184192952"></a>

<a name="table12570457816"></a>
<table><thead align="left"><tr id="row95826401976"><th class="cellrowborder" valign="top" width="35%" id="mcps1.1.5.1.1"><p id="p242492712712"><a name="p242492712712"></a><a name="p242492712712"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="24.94%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="21.060000000000002%" id="mcps1.1.5.1.3"><p id="p12424827192710"><a name="p12424827192710"></a><a name="p12424827192710"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.4"><p id="p433072116440"><a name="p433072116440"></a><a name="p433072116440"></a>授权作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row188634369342"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p13966163782315"><a name="p13966163782315"></a><a name="p13966163782315"></a>POST /v2.1/{project_id}/servers/{server_id}/remote-consoles</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p16061857125316"><a name="p16061857125316"></a><a name="p16061857125316"></a>获取控制台VNC地址</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul1396633712313"></a><a name="ul1396633712313"></a><ul id="ul1396633712313"><li>ecs:servers:createConsole</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul14508183319332"></a><a name="ul14508183319332"></a><ul id="ul14508183319332"><li>支持：</li></ul>
<p id="p552333353314"><a name="p552333353314"></a><a name="p552333353314"></a>项目(Project)</p>
<p id="p258184953817"><a name="p258184953817"></a><a name="p258184953817"></a></p>
<a name="ul1452363323311"></a><a name="ul1452363323311"></a><ul id="ul1452363323311"><li>不支持：</li></ul>
<p id="p11539033143310"><a name="p11539033143310"></a><a name="p11539033143310"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row380212812584"><td class="cellrowborder" valign="top" width="35%" headers="mcps1.1.5.1.1 "><p id="p19802112820588"><a name="p19802112820588"></a><a name="p19802112820588"></a>POST /v1/{project_id}/cloudservers/{server_id}/remote_console</p>
</td>
<td class="cellrowborder" valign="top" width="24.94%" headers="mcps1.1.5.1.2 "><p id="p1351013548583"><a name="p1351013548583"></a><a name="p1351013548583"></a>获取弹性云服务器VNC地址</p>
</td>
<td class="cellrowborder" valign="top" width="21.060000000000002%" headers="mcps1.1.5.1.3 "><a name="ul165561232593"></a><a name="ul165561232593"></a><ul id="ul165561232593"><li>ecs:cloudServers:vnc</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul1125993475913"></a><a name="ul1125993475913"></a><ul id="ul1125993475913"><li>支持：</li></ul>
<p id="p11274203495913"><a name="p11274203495913"></a><a name="p11274203495913"></a>项目(Project)</p>
<p id="p329123425910"><a name="p329123425910"></a><a name="p329123425910"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

