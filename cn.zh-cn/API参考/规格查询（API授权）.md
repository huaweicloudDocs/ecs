# 规格查询<a name="ecs_06_0008"></a>

<a name="table12528123592919"></a>
<table><thead align="left"><tr id="row5528103512910"><th class="cellrowborder" valign="top" width="13.428657134286572%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="27.73722627737226%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="22.737726227377262%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="11.498850114988501%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="8.269173082691731%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row1090113617259"><td class="cellrowborder" valign="top" width="13.428657134286572%" headers="mcps1.1.7.1.1 "><p id="p441812610812"><a name="p441812610812"></a><a name="p441812610812"></a>查询云服务器规格详情和扩展信息列表</p>
</td>
<td class="cellrowborder" valign="top" width="27.73722627737226%" headers="mcps1.1.7.1.2 "><p id="p8987111492511"><a name="p8987111492511"></a><a name="p8987111492511"></a>GET /v1/{project_id}/cloudservers/flavors</p>
</td>
<td class="cellrowborder" valign="top" width="22.737726227377262%" headers="mcps1.1.7.1.3 "><p id="p7882175118157"><a name="p7882175118157"></a><a name="p7882175118157"></a>ecs:cloudServerFlavors:get</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.1.7.1.4 "><p id="p102517171385"><a name="p102517171385"></a><a name="p102517171385"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.498850114988501%" headers="mcps1.1.7.1.5 "><p id="p1664815301497"><a name="p1664815301497"></a><a name="p1664815301497"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.269173082691731%" headers="mcps1.1.7.1.6 "><p id="p13686132019819"><a name="p13686132019819"></a><a name="p13686132019819"></a>√</p>
</td>
</tr>
<tr id="row1750629135711"><td class="cellrowborder" valign="top" width="13.428657134286572%" headers="mcps1.1.7.1.1 "><p id="p17418026985"><a name="p17418026985"></a><a name="p17418026985"></a>查询云服务器规格变更支持列表</p>
</td>
<td class="cellrowborder" valign="top" width="27.73722627737226%" headers="mcps1.1.7.1.2 "><p id="p049813915572"><a name="p049813915572"></a><a name="p049813915572"></a>GET /v1/{project_id}/cloudservers/resize_flavors</p>
</td>
<td class="cellrowborder" valign="top" width="22.737726227377262%" headers="mcps1.1.7.1.3 "><p id="p655535291516"><a name="p655535291516"></a><a name="p655535291516"></a>ecs:cloudServers:list</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.1.7.1.4 "><p id="p22591715814"><a name="p22591715814"></a><a name="p22591715814"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.498850114988501%" headers="mcps1.1.7.1.5 "><p id="p117670331294"><a name="p117670331294"></a><a name="p117670331294"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.269173082691731%" headers="mcps1.1.7.1.6 "><p id="p968602017810"><a name="p968602017810"></a><a name="p968602017810"></a>√</p>
</td>
</tr>
<tr id="row18168121715435"><td class="cellrowborder" valign="top" width="13.428657134286572%" headers="mcps1.1.7.1.1 "><p id="p124180261586"><a name="p124180261586"></a><a name="p124180261586"></a>查询云服务器规格extra_specs的详情（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.73722627737226%" headers="mcps1.1.7.1.2 "><p id="p99081131173310"><a name="p99081131173310"></a><a name="p99081131173310"></a>GET /v2.1/{project_id}/flavors/{flavors_id}/os-extra_specs</p>
</td>
<td class="cellrowborder" valign="top" width="22.737726227377262%" headers="mcps1.1.7.1.3 "><p id="p20273195311157"><a name="p20273195311157"></a><a name="p20273195311157"></a>ecs:flavors:get</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.1.7.1.4 "><p id="p202510170815"><a name="p202510170815"></a><a name="p202510170815"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.498850114988501%" headers="mcps1.1.7.1.5 "><p id="p1420517411778"><a name="p1420517411778"></a><a name="p1420517411778"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.269173082691731%" headers="mcps1.1.7.1.6 "><p id="p1420512411172"><a name="p1420512411172"></a><a name="p1420512411172"></a>×</p>
</td>
</tr>
</tbody>
</table>

