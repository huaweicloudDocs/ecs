# 磁盘管理<a name="ZH-CN_TOPIC_0103071514"></a>

<a name="table88951955182420"></a>
<table><thead align="left"><tr id="row2670183317019"><th class="cellrowborder" valign="top" width="39.50617283950617%" id="mcps1.1.4.1.1"><p id="p1567220502233"><a name="p1567220502233"></a><a name="p1567220502233"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="25.925925925925924%" id="mcps1.1.4.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="34.567901234567906%" id="mcps1.1.4.1.3"><p id="p93075832319"><a name="p93075832319"></a><a name="p93075832319"></a>授权项</p>
</th>
</tr>
</thead>
<tbody><tr id="row1340155610247"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p540195672410"><a name="p540195672410"></a><a name="p540195672410"></a>POST /v2/{tenant_id}/servers/{server_id}/os-volume_attachments</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p20893163618439"><a name="p20893163618439"></a><a name="p20893163618439"></a>弹性云服务器挂载磁盘(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul18401056122412"></a><a name="ul18401056122412"></a><ul id="ul18401056122412"><li>ecs:serverVolumeAttachments:create</li><li>ecs:serverVolumes:use</li></ul>
<a name="ul8405568242"></a><a name="ul8405568242"></a><ul id="ul8405568242"><li>evs:volumes:list</li><li>evs:volumes:get</li><li>evs:volumes:update</li><li>evs:volumes:attach</li><li>evs:volumes:manage</li></ul>
</td>
</tr>
<tr id="row5406567247"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p240175662414"><a name="p240175662414"></a><a name="p240175662414"></a>DELETE /v2/{tenant_id}/servers/{server_id}/os-volume_attachments/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p1489313612433"><a name="p1489313612433"></a><a name="p1489313612433"></a>卸载云服务器磁盘（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul540105612413"></a><a name="ul540105612413"></a><ul id="ul540105612413"><li>ecs:serverVolumeAttachments:delete</li><li>ecs:serverVolumes:use</li></ul>
<a name="ul12408561246"></a><a name="ul12408561246"></a><ul id="ul12408561246"><li>evs:volumes:list</li><li>evs:volumes:get</li><li>evs:volumes:update</li><li>evs:volumes:detach</li><li>evs:volumes:manage</li></ul>
</td>
</tr>
<tr id="row17421856102419"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p542195642417"><a name="p542195642417"></a><a name="p542195642417"></a>GET /v2/{tenant_id}/servers/{server_id}/os-volume_attachments</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p6893123654310"><a name="p6893123654310"></a><a name="p6893123654310"></a>查询弹性云服务器挂载磁盘信息列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul2421156152418"></a><a name="ul2421156152418"></a><ul id="ul2421156152418"><li>ecs:serverVolumeAttachments:list</li><li>ecs:serverVolumes:use</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row442115692417"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p1142156162410"><a name="p1142156162410"></a><a name="p1142156162410"></a>GET /v2/{tenant_id}/servers/{server_id}/os-volume_attachments/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p989313363436"><a name="p989313363436"></a><a name="p989313363436"></a>查询弹性云服务器挂载的单个磁盘信息（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul19421856172420"></a><a name="ul19421856172420"></a><ul id="ul19421856172420"><li>ecs:serverVolumeAttachments:get</li><li>ecs:serverVolumes:use</li></ul>
</td>
</tr>
<tr id="row642956172419"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p104215566246"><a name="p104215566246"></a><a name="p104215566246"></a>POST /v2/{tenant_id}/os-volumes</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p1089383614311"><a name="p1089383614311"></a><a name="p1089383614311"></a>创建磁盘（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul1842155611244"></a><a name="ul1842155611244"></a><ul id="ul1842155611244"><li>ecs:serverVolumes:use</li></ul>
<a name="ul542185619240"></a><a name="ul542185619240"></a><ul id="ul542185619240"><li>evs:volumes:create</li></ul>
</td>
</tr>
<tr id="row94245610244"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p242185616249"><a name="p242185616249"></a><a name="p242185616249"></a>DELETE /v2/{tenant_id}/os-volumes/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p11893336194311"><a name="p11893336194311"></a><a name="p11893336194311"></a>删除磁盘（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul184212562247"></a><a name="ul184212562247"></a><ul id="ul184212562247"><li>ecs:serverVolumes:use</li></ul>
<a name="ul194235632419"></a><a name="ul194235632419"></a><ul id="ul194235632419"><li>evs:volumes:get</li><li>evs:volumes:delete</li></ul>
</td>
</tr>
<tr id="row84245616246"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p13421556132420"><a name="p13421556132420"></a><a name="p13421556132420"></a>GET /v2/{tenant_id}/os-volumes/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p5893173610439"><a name="p5893173610439"></a><a name="p5893173610439"></a>查询指定磁盘信息（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul642256162415"></a><a name="ul642256162415"></a><ul id="ul642256162415"><li>ecs:serverVolumes:use</li></ul>
<a name="ul164275612415"></a><a name="ul164275612415"></a><ul id="ul164275612415"><li>evs:volumes:get</li></ul>
</td>
</tr>
<tr id="row1842135618247"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p14255602413"><a name="p14255602413"></a><a name="p14255602413"></a>GET /v2/{tenant_id}/os-volumes</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p12893153654314"><a name="p12893153654314"></a><a name="p12893153654314"></a>查询磁盘列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul17429568246"></a><a name="ul17429568246"></a><ul id="ul17429568246"><li>ecs:serverVolumes:use</li></ul>
<a name="ul114285615246"></a><a name="ul114285615246"></a><ul id="ul114285615246"><li>evs:volumes:get</li><li>evs:volumes:list</li></ul>
</td>
</tr>
<tr id="row04205682413"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p114235612243"><a name="p114235612243"></a><a name="p114235612243"></a>GET /v2/{tenant_id}/os-volumes/detail</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p4893123611433"><a name="p4893123611433"></a><a name="p4893123611433"></a>查询磁盘详情列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul1142456102410"></a><a name="ul1142456102410"></a><ul id="ul1142456102410"><li>ecs:serverVolumes:use</li></ul>
<a name="ul1344125652414"></a><a name="ul1344125652414"></a><ul id="ul1344125652414"><li>evs:volumes:get</li><li>evs:volumes:list</li></ul>
</td>
</tr>
<tr id="row1893621632116"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p865419331215"><a name="p865419331215"></a><a name="p865419331215"></a>DELETE /v1/{tenant_id}/cloudservers/{server_id}/detachvolume/{attachment_id}</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p0893123616432"><a name="p0893123616432"></a><a name="p0893123616432"></a>卸载指定弹性云服务器的磁盘</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul86541333202118"></a><a name="ul86541333202118"></a><ul id="ul86541333202118"><li>ecs:cloudServers:detachVolume</li></ul>
</td>
</tr>
<tr id="row15734520162118"><td class="cellrowborder" valign="top" width="39.50617283950617%" headers="mcps1.1.4.1.1 "><p id="p3654133142110"><a name="p3654133142110"></a><a name="p3654133142110"></a>POST /v1/{tenant_id}/cloudservers/{server_id}/attachvolume</p>
</td>
<td class="cellrowborder" valign="top" width="25.925925925925924%" headers="mcps1.1.4.1.2 "><p id="p989316367430"><a name="p989316367430"></a><a name="p989316367430"></a>向指定弹性云服务器挂载磁盘</p>
</td>
<td class="cellrowborder" valign="top" width="34.567901234567906%" headers="mcps1.1.4.1.3 "><a name="ul16654183313217"></a><a name="ul16654183313217"></a><ul id="ul16654183313217"><li>ecs:cloudServers:attach</li></ul>
</td>
</tr>
</tbody>
</table>

