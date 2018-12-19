# 状态管理<a name="ZH-CN_TOPIC_0103071511"></a>

<a name="table12570457816"></a>
<table><thead align="left"><tr id="row2025712451682"><th class="cellrowborder" valign="top" width="43.20987654320987%" id="mcps1.1.4.1.1"><p id="p72571745883"><a name="p72571745883"></a><a name="p72571745883"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="30.864197530864203%" id="mcps1.1.4.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25.925925925925924%" id="mcps1.1.4.1.3"><p id="p162571745883"><a name="p162571745883"></a><a name="p162571745883"></a>授权项</p>
</th>
</tr>
</thead>
<tbody><tr id="row72577450815"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p5883772911"><a name="p5883772911"></a><a name="p5883772911"></a>POST /v2/{tenant_id}/servers</p>
<p id="p11883670913"><a name="p11883670913"></a><a name="p11883670913"></a>POST /v2/{tenant_id}/os-volumes_boot</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p18605195717538"><a name="p18605195717538"></a><a name="p18605195717538"></a>创建云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul1388313711917"></a><a name="ul1388313711917"></a><ul id="ul1388313711917"><li>ecs:servers:create</li><li>ecs:servers:get</li><li>ecs:serverInterfaces:use</li><li>ecs:serverInterfaces:get</li><li>ecs:flavors:get</li><li>ecs:securityGroups:use</li></ul>
<a name="ul688318715914"></a><a name="ul688318715914"></a><ul id="ul688318715914"><li>evs:volumes:list</li><li>evs:volumes:get</li><li>evs:volumes:create</li><li>evs:volumes:attach</li><li>evs:volumes:manage</li><li>vpc:securityGroups:get</li></ul>
<a name="ul28841471697"></a><a name="ul28841471697"></a><ul id="ul28841471697"><li>vpc:networks:get</li><li>vpc:networks:update</li><li>vpc:subnets:get</li><li>vpc:subnets:update</li><li>vpc:ports:create</li><li>vpc:ports:update</li><li>vpc:ports:get</li><li>vpc:ports:delete</li><li>vpc:networks:create</li><li>vpc:subnets:create</li><li>vpc:routers:get</li><li>vpc:routers:update</li></ul>
<a name="ul13884117497"></a><a name="ul13884117497"></a><ul id="ul13884117497"><li>ims:images:list</li><li>ims:images:get</li></ul>
</td>
</tr>
<tr id="row325714451286"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p33197248919"><a name="p33197248919"></a><a name="p33197248919"></a>DELETE /v2/{tenant_id}/servers/{server_id}</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p260615717539"><a name="p260615717539"></a><a name="p260615717539"></a>删除云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul1631916243919"></a><a name="ul1631916243919"></a><ul id="ul1631916243919"><li>ecs:servers:delete</li></ul>
</td>
</tr>
<tr id="row1325719451486"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p731918241919"><a name="p731918241919"></a><a name="p731918241919"></a>PUT /v2/{tenant_id}/servers/{server_id}</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p116062577537"><a name="p116062577537"></a><a name="p116062577537"></a>修改云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul03191224499"></a><a name="ul03191224499"></a><ul id="ul03191224499"><li>ecs:servers:update</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row1225714451388"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p13321924494"><a name="p13321924494"></a><a name="p13321924494"></a>POST /v2/{tenant_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p1606257145310"><a name="p1606257145310"></a><a name="p1606257145310"></a>启动云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul8321192417911"></a><a name="ul8321192417911"></a><ul id="ul8321192417911"><li>ecs:servers:start</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row52571745582"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p032112243919"><a name="p032112243919"></a><a name="p032112243919"></a>POST /v2/{tenant_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p76061457195316"><a name="p76061457195316"></a><a name="p76061457195316"></a>关闭云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul632116243917"></a><a name="ul632116243917"></a><ul id="ul632116243917"><li>ecs:servers:stop</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row172571445985"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p19321824193"><a name="p19321824193"></a><a name="p19321824193"></a>POST /v2/{tenant_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p860675714535"><a name="p860675714535"></a><a name="p860675714535"></a>重启云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul1332192415914"></a><a name="ul1332192415914"></a><ul id="ul1332192415914"><li>ecs:servers:reboot</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row1525717451489"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p032110243914"><a name="p032110243914"></a><a name="p032110243914"></a>POST /v2/{tenant_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p186061757165319"><a name="p186061757165319"></a><a name="p186061757165319"></a>变更云服务器规格（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul1632115247916"></a><a name="ul1632115247916"></a><ul id="ul1632115247916"><li>ecs:servers:resize</li><li>ecs:servers:get</li></ul>
<a name="ul13212241396"></a><a name="ul13212241396"></a><ul id="ul13212241396"><li>evs:volumes:list</li><li>evs:volumes:create</li><li>evs:volumes:get</li><li>evs:volumes:attach</li><li>evs:volumes:detach</li><li>evs:volumes:manage</li></ul>
<a name="ul193211124399"></a><a name="ul193211124399"></a><ul id="ul193211124399"><li>vpc:ports:get</li><li>vpc:ports:update</li><li>vpc:ports:creare</li><li>vpc:ports:delete</li></ul>
</td>
</tr>
<tr id="row48081934497"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p45019471894"><a name="p45019471894"></a><a name="p45019471894"></a>POST /v2/{tenant_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p6606557155319"><a name="p6606557155319"></a><a name="p6606557155319"></a>重建弹性云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul550124712916"></a><a name="ul550124712916"></a><ul id="ul550124712916"><li>ecs:servers:rebuild</li><li>ecs:servers:get</li><li>ecs:servers:update</li></ul>
<a name="ul9507479910"></a><a name="ul9507479910"></a><ul id="ul9507479910"><li>ims:images:get</li><li>ims:images:list</li><li>ims:images:update</li></ul>
</td>
</tr>
<tr id="row19808934597"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p1550144717916"><a name="p1550144717916"></a><a name="p1550144717916"></a>POST /v2/{tenant_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p960685795319"><a name="p960685795319"></a><a name="p960685795319"></a>锁定云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul1850647494"></a><a name="ul1850647494"></a><ul id="ul1850647494"><li>ecs:servers:lock</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row1180814349912"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p550164716914"><a name="p550164716914"></a><a name="p550164716914"></a>POST /v2/{tenant_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p560645745312"><a name="p560645745312"></a><a name="p560645745312"></a>解锁定云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul15020472098"></a><a name="ul15020472098"></a><ul id="ul15020472098"><li>ecs:servers:unlock</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row06901173312"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p6932412182715"><a name="p6932412182715"></a><a name="p6932412182715"></a>GET /v2/{tenant_id}/servers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p19606175714531"><a name="p19606175714531"></a><a name="p19606175714531"></a>Windows云服务器获取密码（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul1693212126274"></a><a name="ul1693212126274"></a><ul id="ul1693212126274"><li>ecs:serverPasswords:manage</li></ul>
</td>
</tr>
<tr id="row042422017319"><td class="cellrowborder" valign="top" width="43.20987654320987%" headers="mcps1.1.4.1.1 "><p id="p3932161252712"><a name="p3932161252712"></a><a name="p3932161252712"></a>DELETE /v2/{tenant_id}/servers/{server_id}/os-server-password</p>
</td>
<td class="cellrowborder" valign="top" width="30.864197530864203%" headers="mcps1.1.4.1.2 "><p id="p20606175785313"><a name="p20606175785313"></a><a name="p20606175785313"></a>Windows云服务器清除密码（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.3 "><a name="ul1693381214271"></a><a name="ul1693381214271"></a><ul id="ul1693381214271"><li>ecs:serverPasswords:manage</li></ul>
</td>
</tr>
</tbody>
</table>

