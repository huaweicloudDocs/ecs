# 云服务器控制台管理<a name="ZH-CN_TOPIC_0184192952"></a>

<a name="table12570457816"></a>
<table><thead align="left"><tr id="row95826401976"><th class="cellrowborder" valign="top" width="10.12%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="31.2%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="23.71%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="19.439999999999998%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="8.01%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="7.5200000000000005%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row188634369342"><td class="cellrowborder" valign="top" width="10.12%" headers="mcps1.1.7.1.1 "><p id="p16826247152917"><a name="p16826247152917"></a><a name="p16826247152917"></a>获取控制台VNC地址</p>
</td>
<td class="cellrowborder" valign="top" width="31.2%" headers="mcps1.1.7.1.2 "><p id="p12104194812426"><a name="p12104194812426"></a><a name="p12104194812426"></a>POST /v2.1/{project_id}/servers/{server_id}/remote-consoles</p>
</td>
<td class="cellrowborder" valign="top" width="23.71%" headers="mcps1.1.7.1.3 "><p id="p1153913012512"><a name="p1153913012512"></a><a name="p1153913012512"></a>ecs:servers:createConsole</p>
</td>
<td class="cellrowborder" valign="top" width="19.439999999999998%" headers="mcps1.1.7.1.4 "><p id="p166138202311"><a name="p166138202311"></a><a name="p166138202311"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="8.01%" headers="mcps1.1.7.1.5 "><p id="p551811571269"><a name="p551811571269"></a><a name="p551811571269"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.7.1.6 "><p id="p135181357102610"><a name="p135181357102610"></a><a name="p135181357102610"></a>×</p>
</td>
</tr>
<tr id="row380212812584"><td class="cellrowborder" valign="top" width="10.12%" headers="mcps1.1.7.1.1 "><p id="p9826747182916"><a name="p9826747182916"></a><a name="p9826747182916"></a>获取弹性云服务器VNC地址</p>
</td>
<td class="cellrowborder" valign="top" width="31.2%" headers="mcps1.1.7.1.2 "><p id="p19802112820588"><a name="p19802112820588"></a><a name="p19802112820588"></a>POST /v1/{project_id}/cloudservers/{server_id}/remote_console</p>
</td>
<td class="cellrowborder" valign="top" width="23.71%" headers="mcps1.1.7.1.3 "><p id="p74681031112513"><a name="p74681031112513"></a><a name="p74681031112513"></a>ecs:cloudServers:vnc</p>
</td>
<td class="cellrowborder" valign="top" width="19.439999999999998%" headers="mcps1.1.7.1.4 "><p id="p1887919311239"><a name="p1887919311239"></a><a name="p1887919311239"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="8.01%" headers="mcps1.1.7.1.5 "><p id="p8354597291"><a name="p8354597291"></a><a name="p8354597291"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.5200000000000005%" headers="mcps1.1.7.1.6 "><p id="p16354159132918"><a name="p16354159132918"></a><a name="p16354159132918"></a>√</p>
</td>
</tr>
</tbody>
</table>

