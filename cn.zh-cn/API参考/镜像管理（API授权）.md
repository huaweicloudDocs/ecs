# 镜像管理<a name="ecs_06_0006"></a>

<a name="table326212151339"></a>
<table><thead align="left"><tr id="row3262101519333"><th class="cellrowborder" valign="top" width="13.96139613961396%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="27.662766276627664%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="21.08210821082108%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="16.14161416141614%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="11.8011801180118%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="9.350935093509351%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row1426217152337"><td class="cellrowborder" valign="top" width="13.96139613961396%" headers="mcps1.1.7.1.1 "><p id="p18528333846"><a name="p18528333846"></a><a name="p18528333846"></a>创建镜像（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.662766276627664%" headers="mcps1.1.7.1.2 "><p id="p7567412418"><a name="p7567412418"></a><a name="p7567412418"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="21.08210821082108%" headers="mcps1.1.7.1.3 "><p id="p4257120191310"><a name="p4257120191310"></a><a name="p4257120191310"></a>ecs:servers:createImage</p>
</td>
<td class="cellrowborder" valign="top" width="16.14161416141614%" headers="mcps1.1.7.1.4 "><p id="p1276762117130"><a name="p1276762117130"></a><a name="p1276762117130"></a>evs:volumes:get</p>
<p id="p144261522151314"><a name="p144261522151314"></a><a name="p144261522151314"></a>evs:snapshots:create</p>
<p id="p51562311311"><a name="p51562311311"></a><a name="p51562311311"></a>ims:images:create</p>
<p id="p176925234135"><a name="p176925234135"></a><a name="p176925234135"></a>ims:images:get</p>
<p id="p143671624131317"><a name="p143671624131317"></a><a name="p143671624131317"></a>ims:images:list</p>
<p id="p4787132561319"><a name="p4787132561319"></a><a name="p4787132561319"></a>ims:images:update</p>
<p id="p10778152613131"><a name="p10778152613131"></a><a name="p10778152613131"></a>ims:images:delete</p>
</td>
<td class="cellrowborder" valign="top" width="11.8011801180118%" headers="mcps1.1.7.1.5 "><p id="p57081518165916"><a name="p57081518165916"></a><a name="p57081518165916"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.350935093509351%" headers="mcps1.1.7.1.6 "><p id="p9708718185916"><a name="p9708718185916"></a><a name="p9708718185916"></a>×</p>
</td>
</tr>
</tbody>
</table>

