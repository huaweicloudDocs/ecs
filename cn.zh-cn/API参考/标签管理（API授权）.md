# 标签管理<a name="ecs_06_0019"></a>

<a name="table4509123112811"></a>
<table><thead align="left"><tr id="row19509193152818"><th class="cellrowborder" valign="top" width="10.12101210121012%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="30.56305630563056%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="24.422442244224417%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="20.062006200620058%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="7.31073107310731%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="7.520752075207521%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row169138403108"><td class="cellrowborder" valign="top" width="10.12101210121012%" headers="mcps1.1.7.1.1 "><p id="p1835316215324"><a name="p1835316215324"></a><a name="p1835316215324"></a>批量添加云服务器标签/批量删除云服务器标签</p>
</td>
<td class="cellrowborder" valign="top" width="30.56305630563056%" headers="mcps1.1.7.1.2 "><p id="p613135211104"><a name="p613135211104"></a><a name="p613135211104"></a>POST  /v1/{project_id}/cloudservers/{server_id}/tags/action</p>
</td>
<td class="cellrowborder" valign="top" width="24.422442244224417%" headers="mcps1.1.7.1.3 "><p id="p5273124014252"><a name="p5273124014252"></a><a name="p5273124014252"></a>ecs:cloudServers:put</p>
</td>
<td class="cellrowborder" valign="top" width="20.062006200620058%" headers="mcps1.1.7.1.4 "><p id="p355051118342"><a name="p355051118342"></a><a name="p355051118342"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.31073107310731%" headers="mcps1.1.7.1.5 "><p id="p8354597291"><a name="p8354597291"></a><a name="p8354597291"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p16354159132918"><a name="p16354159132918"></a><a name="p16354159132918"></a>√</p>
</td>
</tr>
<tr id="row528011248461"><td class="cellrowborder" valign="top" width="10.12101210121012%" headers="mcps1.1.7.1.1 "><p id="p13353162143218"><a name="p13353162143218"></a><a name="p13353162143218"></a>查询项目标签</p>
</td>
<td class="cellrowborder" valign="top" width="30.56305630563056%" headers="mcps1.1.7.1.2 "><p id="p162801924124620"><a name="p162801924124620"></a><a name="p162801924124620"></a>GET /v1/{project_id}/cloudservers/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.422442244224417%" headers="mcps1.1.7.1.3 "><p id="p1466177271"><a name="p1466177271"></a><a name="p1466177271"></a>ecs:cloudServers:list</p>
</td>
<td class="cellrowborder" valign="top" width="20.062006200620058%" headers="mcps1.1.7.1.4 "><p id="p16550171114347"><a name="p16550171114347"></a><a name="p16550171114347"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.31073107310731%" headers="mcps1.1.7.1.5 "><p id="p16488195512347"><a name="p16488195512347"></a><a name="p16488195512347"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p10488155103418"><a name="p10488155103418"></a><a name="p10488155103418"></a>√</p>
</td>
</tr>
<tr id="row261813360"><td class="cellrowborder" valign="top" width="10.12101210121012%" headers="mcps1.1.7.1.1 "><p id="p1235311216328"><a name="p1235311216328"></a><a name="p1235311216328"></a>查询云服务器标签</p>
</td>
<td class="cellrowborder" valign="top" width="30.56305630563056%" headers="mcps1.1.7.1.2 "><p id="p958291073619"><a name="p958291073619"></a><a name="p958291073619"></a>GET /v1/{project_id}/cloudservers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.422442244224417%" headers="mcps1.1.7.1.3 "><p id="p17605615112714"><a name="p17605615112714"></a><a name="p17605615112714"></a>ecs:cloudServers:get</p>
</td>
<td class="cellrowborder" valign="top" width="20.062006200620058%" headers="mcps1.1.7.1.4 "><p id="p1550181153411"><a name="p1550181153411"></a><a name="p1550181153411"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.31073107310731%" headers="mcps1.1.7.1.5 "><p id="p1727105693417"><a name="p1727105693417"></a><a name="p1727105693417"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p157271556103417"><a name="p157271556103417"></a><a name="p157271556103417"></a>√</p>
</td>
</tr>
<tr id="row676275515115"><td class="cellrowborder" valign="top" width="10.12101210121012%" headers="mcps1.1.7.1.1 "><p id="p1135319253214"><a name="p1135319253214"></a><a name="p1135319253214"></a>查询云服务器标签</p>
</td>
<td class="cellrowborder" valign="top" width="30.56305630563056%" headers="mcps1.1.7.1.2 "><p id="p776319551911"><a name="p776319551911"></a><a name="p776319551911"></a>GET /v1/{project_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.422442244224417%" headers="mcps1.1.7.1.3 "><p id="p15340161212715"><a name="p15340161212715"></a><a name="p15340161212715"></a>ecs:servers:getTags</p>
</td>
<td class="cellrowborder" valign="top" width="20.062006200620058%" headers="mcps1.1.7.1.4 "><p id="p15551181113416"><a name="p15551181113416"></a><a name="p15551181113416"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.31073107310731%" headers="mcps1.1.7.1.5 "><p id="p18440111143510"><a name="p18440111143510"></a><a name="p18440111143510"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p744091115351"><a name="p744091115351"></a><a name="p744091115351"></a>×</p>
</td>
</tr>
<tr id="row175291830184314"><td class="cellrowborder" valign="top" width="10.12101210121012%" headers="mcps1.1.7.1.1 "><p id="p53532219322"><a name="p53532219322"></a><a name="p53532219322"></a>查询指定云服务器标签列表(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="30.56305630563056%" headers="mcps1.1.7.1.2 "><p id="p4238141844315"><a name="p4238141844315"></a><a name="p4238141844315"></a>GET /v2.1/{project_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.422442244224417%" headers="mcps1.1.7.1.3 "><p id="p1761618162720"><a name="p1761618162720"></a><a name="p1761618162720"></a>ecs:servers:getTags</p>
</td>
<td class="cellrowborder" valign="top" width="20.062006200620058%" headers="mcps1.1.7.1.4 "><p id="p7712105275"><a name="p7712105275"></a><a name="p7712105275"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="7.31073107310731%" headers="mcps1.1.7.1.5 "><p id="p8211013163519"><a name="p8211013163519"></a><a name="p8211013163519"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p17211513163516"><a name="p17211513163516"></a><a name="p17211513163516"></a>×</p>
</td>
</tr>
<tr id="row553163014438"><td class="cellrowborder" valign="top" width="10.12101210121012%" headers="mcps1.1.7.1.1 "><p id="p2353182143213"><a name="p2353182143213"></a><a name="p2353182143213"></a>给指定弹性云服务器添加标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="30.56305630563056%" headers="mcps1.1.7.1.2 "><p id="p447082244315"><a name="p447082244315"></a><a name="p447082244315"></a>PUT /v2.1/{project_id}/servers/{server_id}/tags/{tag}</p>
</td>
<td class="cellrowborder" valign="top" width="24.422442244224417%" headers="mcps1.1.7.1.3 "><p id="p67717252713"><a name="p67717252713"></a><a name="p67717252713"></a>ecs:servers:setTags</p>
</td>
<td class="cellrowborder" valign="top" width="20.062006200620058%" headers="mcps1.1.7.1.4 "><p id="p175511611173411"><a name="p175511611173411"></a><a name="p175511611173411"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="7.31073107310731%" headers="mcps1.1.7.1.5 "><p id="p173971515352"><a name="p173971515352"></a><a name="p173971515352"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p83941516355"><a name="p83941516355"></a><a name="p83941516355"></a>×</p>
</td>
</tr>
<tr id="row1661113346435"><td class="cellrowborder" valign="top" width="10.12101210121012%" headers="mcps1.1.7.1.1 "><p id="p1635314293214"><a name="p1635314293214"></a><a name="p1635314293214"></a>创建云服务器标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="30.56305630563056%" headers="mcps1.1.7.1.2 "><p id="p988313810430"><a name="p988313810430"></a><a name="p988313810430"></a>PUT /v2.1/{project_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.422442244224417%" headers="mcps1.1.7.1.3 "><p id="p176826545265"><a name="p176826545265"></a><a name="p176826545265"></a>ecs:servers:setTags</p>
</td>
<td class="cellrowborder" valign="top" width="20.062006200620058%" headers="mcps1.1.7.1.4 "><p id="p13451165392614"><a name="p13451165392614"></a><a name="p13451165392614"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="7.31073107310731%" headers="mcps1.1.7.1.5 "><p id="p1638621617356"><a name="p1638621617356"></a><a name="p1638621617356"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p17386191623510"><a name="p17386191623510"></a><a name="p17386191623510"></a>×</p>
</td>
</tr>
<tr id="row105321930104310"><td class="cellrowborder" valign="top" width="10.12101210121012%" headers="mcps1.1.7.1.1 "><p id="p835312183219"><a name="p835312183219"></a><a name="p835312183219"></a>删除云服务器的指定标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="30.56305630563056%" headers="mcps1.1.7.1.2 "><p id="p127395094318"><a name="p127395094318"></a><a name="p127395094318"></a>DELETE /v2.1/{project_id}/servers/{server_id}/tags/{tag}</p>
</td>
<td class="cellrowborder" valign="top" width="24.422442244224417%" headers="mcps1.1.7.1.3 "><p id="p1332614742618"><a name="p1332614742618"></a><a name="p1332614742618"></a>ecs:servers:setTags</p>
</td>
<td class="cellrowborder" valign="top" width="20.062006200620058%" headers="mcps1.1.7.1.4 "><p id="p6551161110343"><a name="p6551161110343"></a><a name="p6551161110343"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="7.31073107310731%" headers="mcps1.1.7.1.5 "><p id="p1698661713355"><a name="p1698661713355"></a><a name="p1698661713355"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p14986121714357"><a name="p14986121714357"></a><a name="p14986121714357"></a>×</p>
</td>
</tr>
<tr id="row353283018431"><td class="cellrowborder" valign="top" width="10.12101210121012%" headers="mcps1.1.7.1.1 "><p id="p16353226323"><a name="p16353226323"></a><a name="p16353226323"></a>查询云服务器是否存在指定标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="30.56305630563056%" headers="mcps1.1.7.1.2 "><p id="p181272014417"><a name="p181272014417"></a><a name="p181272014417"></a>GET /v2.1/{project_id}/servers/{server_id}/tags/{tag}</p>
</td>
<td class="cellrowborder" valign="top" width="24.422442244224417%" headers="mcps1.1.7.1.3 "><p id="p659164019263"><a name="p659164019263"></a><a name="p659164019263"></a>ecs:servers:getTags</p>
</td>
<td class="cellrowborder" valign="top" width="20.062006200620058%" headers="mcps1.1.7.1.4 "><p id="p17551171118346"><a name="p17551171118346"></a><a name="p17551171118346"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="7.31073107310731%" headers="mcps1.1.7.1.5 "><p id="p152581918359"><a name="p152581918359"></a><a name="p152581918359"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p025919143513"><a name="p025919143513"></a><a name="p025919143513"></a>×</p>
</td>
</tr>
<tr id="row10532193004319"><td class="cellrowborder" valign="top" width="10.12101210121012%" headers="mcps1.1.7.1.1 "><p id="p1735382193216"><a name="p1735382193216"></a><a name="p1735382193216"></a>删除云服务器所有标签(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="30.56305630563056%" headers="mcps1.1.7.1.2 "><p id="p7726121014414"><a name="p7726121014414"></a><a name="p7726121014414"></a>DELETE /v2.1/{project_id}/servers/{server_id}/tags</p>
</td>
<td class="cellrowborder" valign="top" width="24.422442244224417%" headers="mcps1.1.7.1.3 "><p id="p1781833432619"><a name="p1781833432619"></a><a name="p1781833432619"></a>ecs:servers:setTags</p>
</td>
<td class="cellrowborder" valign="top" width="20.062006200620058%" headers="mcps1.1.7.1.4 "><p id="p25511311183410"><a name="p25511311183410"></a><a name="p25511311183410"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="7.31073107310731%" headers="mcps1.1.7.1.5 "><p id="p102651820163512"><a name="p102651820163512"></a><a name="p102651820163512"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p1926512013352"><a name="p1926512013352"></a><a name="p1926512013352"></a>×</p>
</td>
</tr>
</tbody>
</table>

