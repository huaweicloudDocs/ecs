# 镜像管理<a name="ZH-CN_TOPIC_0103072348"></a>

<a name="table141517564301"></a>
<table><thead align="left"><tr id="row8415105683017"><th class="cellrowborder" valign="top" width="40%" id="mcps1.1.5.1.1"><p id="p15415105620309"><a name="p15415105620309"></a><a name="p15415105620309"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="16%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.3"><p id="p194156565302"><a name="p194156565302"></a><a name="p194156565302"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.4"><p id="p92571440143717"><a name="p92571440143717"></a><a name="p92571440143717"></a>授权项作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row17415185618309"><td class="cellrowborder" valign="top" width="40%" headers="mcps1.1.5.1.1 "><p id="p562611164316"><a name="p562611164316"></a><a name="p562611164316"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.2 "><p id="p95829616422"><a name="p95829616422"></a><a name="p95829616422"></a>创建镜像（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><a name="ul71771911103111"></a><a name="ul71771911103111"></a><ul id="ul71771911103111"><li>ecs:servers:createImage</li><li>evs:volumes:get</li><li>evs:snapshots:create</li></ul>
<a name="ul14179141119318"></a><a name="ul14179141119318"></a><ul id="ul14179141119318"><li>ims:images:create</li><li>ims:images:get</li><li>ims:images:list</li><li>ims:images:update</li><li>ims:images:delete</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul131481927113717"></a><a name="ul131481927113717"></a><ul id="ul131481927113717"><li>支持：</li></ul>
<p id="p1148132753713"><a name="p1148132753713"></a><a name="p1148132753713"></a>项目(Project)</p>
<p id="p176367599382"><a name="p176367599382"></a><a name="p176367599382"></a></p>
<a name="ul12164122716370"></a><a name="ul12164122716370"></a><ul id="ul12164122716370"><li>不支持：</li></ul>
<p id="p416411277372"><a name="p416411277372"></a><a name="p416411277372"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

