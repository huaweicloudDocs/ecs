# 标签管理<a name="ZH-CN_TOPIC_0103071521"></a>

<a name="table4509123112811"></a>
<table><thead align="left"><tr id="row19509193152818"><th class="cellrowborder" valign="top" width="46.835443037974684%" id="mcps1.1.4.1.1"><p id="p55099315280"><a name="p55099315280"></a><a name="p55099315280"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="31.645569620253163%" id="mcps1.1.4.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="21.518987341772153%" id="mcps1.1.4.1.3"><p id="p175092031182817"><a name="p175092031182817"></a><a name="p175092031182817"></a>授权项</p>
</th>
</tr>
</thead>
<tbody><tr id="row850993116285"><td class="cellrowborder" valign="top" width="46.835443037974684%" headers="mcps1.1.4.1.1 "><p id="p162031917142912"><a name="p162031917142912"></a><a name="p162031917142912"></a>GET /v2/{tenant_id}/servers/{server_id}/tags</p>
<p id="p182041917172916"><a name="p182041917172916"></a><a name="p182041917172916"></a>GET /v2.1/{tenant_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="31.645569620253163%" headers="mcps1.1.4.1.2 "><p id="p6777313164513"><a name="p6777313164513"></a><a name="p6777313164513"></a>查询指定云服务器标签列表(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="21.518987341772153%" headers="mcps1.1.4.1.3 "><a name="ul12203171720294"></a><a name="ul12203171720294"></a><ul id="ul12203171720294"><li>ecs:servers:getTags</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row4509431142818"><td class="cellrowborder" valign="top" width="46.835443037974684%" headers="mcps1.1.4.1.1 "><p id="p11203417182912"><a name="p11203417182912"></a><a name="p11203417182912"></a>PUT /v2/{tenant_id}/servers/{server_id}/tags/{tag}</p>
<p id="p620491713292"><a name="p620491713292"></a><a name="p620491713292"></a>PUT /v2.1/{tenant_id}/servers/{server_id}/tags/{tag}</p>
</td>
<td class="cellrowborder" valign="top" width="31.645569620253163%" headers="mcps1.1.4.1.2 "><p id="p127779131452"><a name="p127779131452"></a><a name="p127779131452"></a>给指定弹性云服务器添加标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="21.518987341772153%" headers="mcps1.1.4.1.3 "><a name="ul4203517112918"></a><a name="ul4203517112918"></a><ul id="ul4203517112918"><li>ecs:servers:setTags</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row650993114285"><td class="cellrowborder" valign="top" width="46.835443037974684%" headers="mcps1.1.4.1.1 "><p id="p620301782915"><a name="p620301782915"></a><a name="p620301782915"></a>PUT /v2/{tenant_id}/servers/{server_id}/tags</p>
<p id="p4204141712920"><a name="p4204141712920"></a><a name="p4204141712920"></a>PUT /v2.1/{tenant_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="31.645569620253163%" headers="mcps1.1.4.1.2 "><p id="p16892173262012"><a name="p16892173262012"></a><a name="p16892173262012"></a>创建云服务器标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="21.518987341772153%" headers="mcps1.1.4.1.3 "><a name="ul162031917192915"></a><a name="ul162031917192915"></a><ul id="ul162031917192915"><li>ecs:servers:setTags</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row1150963117282"><td class="cellrowborder" valign="top" width="46.835443037974684%" headers="mcps1.1.4.1.1 "><p id="p1820321713292"><a name="p1820321713292"></a><a name="p1820321713292"></a>DELETE /v2/{tenant_id}/servers/{server_id}/tags/{tag}</p>
<p id="p1220471762911"><a name="p1220471762911"></a><a name="p1220471762911"></a>DELETE /v2.1/{tenant_id}/servers/{server_id}/tags/{tag}</p>
</td>
<td class="cellrowborder" valign="top" width="31.645569620253163%" headers="mcps1.1.4.1.2 "><p id="p1777171317458"><a name="p1777171317458"></a><a name="p1777171317458"></a>删除云服务器的指定标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="21.518987341772153%" headers="mcps1.1.4.1.3 "><a name="ul1020320173290"></a><a name="ul1020320173290"></a><ul id="ul1020320173290"><li>ecs:servers:setTags</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row1509631192817"><td class="cellrowborder" valign="top" width="46.835443037974684%" headers="mcps1.1.4.1.1 "><p id="p5204217162916"><a name="p5204217162916"></a><a name="p5204217162916"></a>GET /v2/{tenant_id}/servers/{server_id}/tags/{tag}</p>
<p id="p16118833162110"><a name="p16118833162110"></a><a name="p16118833162110"></a>GET /v2.1/{tenant_id}/servers/{server_id}/tags/{tag}</p>
</td>
<td class="cellrowborder" valign="top" width="31.645569620253163%" headers="mcps1.1.4.1.2 "><p id="p3777151318458"><a name="p3777151318458"></a><a name="p3777151318458"></a>查询云服务器是否存在指定标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="21.518987341772153%" headers="mcps1.1.4.1.3 "><a name="ul102041817132912"></a><a name="ul102041817132912"></a><ul id="ul102041817132912"><li>ecs:servers:getTags</li><li>ecs:servers:get</li></ul>
</td>
</tr>
<tr id="row15091131182810"><td class="cellrowborder" valign="top" width="46.835443037974684%" headers="mcps1.1.4.1.1 "><p id="p220441742916"><a name="p220441742916"></a><a name="p220441742916"></a>DELETE /v2/{tenant_id}/servers/{server_id}/tags</p>
<p id="p1420571720295"><a name="p1420571720295"></a><a name="p1420571720295"></a>DELETE /v2.1/{tenant_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="31.645569620253163%" headers="mcps1.1.4.1.2 "><p id="p19777111310454"><a name="p19777111310454"></a><a name="p19777111310454"></a>删除云服务器所有标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="21.518987341772153%" headers="mcps1.1.4.1.3 "><a name="ul9204517182913"></a><a name="ul9204517182913"></a><ul id="ul9204517182913"><li>ecs:servers:setTags</li><li>ecs:servers:get</li></ul>
</td>
</tr>
</tbody>
</table>

