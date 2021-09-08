# FPGA逻辑文件管理<a name="ZH-CN_TOPIC_0132778339"></a>

<a name="table141517564301"></a>
<table><thead align="left"><tr id="row8415105683017"><th class="cellrowborder" valign="top" width="9.050905090509051%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="31.113111311131114%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="24.71247124712471%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="20.25202520252025%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="7.35073507350735%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="7.520752075207521%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row2651640102215"><td class="cellrowborder" valign="top" width="9.050905090509051%" headers="mcps1.1.7.1.1 "><p id="p3266115911350"><a name="p3266115911350"></a><a name="p3266115911350"></a>查询关联列表</p>
</td>
<td class="cellrowborder" valign="top" width="31.113111311131114%" headers="mcps1.1.7.1.2 "><p id="p1516821032316"><a name="p1516821032316"></a><a name="p1516821032316"></a>GET /v1/{project_id}/cloudservers/fpga_image/associations{?image_id,fpga_image_id,page,size}</p>
</td>
<td class="cellrowborder" valign="top" width="24.71247124712471%" headers="mcps1.1.7.1.3 "><p id="p19724113892713"><a name="p19724113892713"></a><a name="p19724113892713"></a>ecs:cloudServerFpgaImages:getRelations</p>
</td>
<td class="cellrowborder" valign="top" width="20.25202520252025%" headers="mcps1.1.7.1.4 "><p id="p17104710364"><a name="p17104710364"></a><a name="p17104710364"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.35073507350735%" headers="mcps1.1.7.1.5 "><p id="p11694151153615"><a name="p11694151153615"></a><a name="p11694151153615"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p56948519367"><a name="p56948519367"></a><a name="p56948519367"></a>×</p>
</td>
</tr>
<tr id="row876855342215"><td class="cellrowborder" valign="top" width="9.050905090509051%" headers="mcps1.1.7.1.1 "><p id="p6266115914355"><a name="p6266115914355"></a><a name="p6266115914355"></a>解关联FPGA镜像与弹性云服务器镜像</p>
</td>
<td class="cellrowborder" valign="top" width="31.113111311131114%" headers="mcps1.1.7.1.2 "><p id="p111681310102310"><a name="p111681310102310"></a><a name="p111681310102310"></a>DELETE /v1/{project_id}/cloudservers/fpga_image/{fpga_image_id}/association</p>
</td>
<td class="cellrowborder" valign="top" width="24.71247124712471%" headers="mcps1.1.7.1.3 "><p id="p121851540192715"><a name="p121851540192715"></a><a name="p121851540192715"></a>ecs:cloudServerFpgaImags:unrelate</p>
</td>
<td class="cellrowborder" valign="top" width="20.25202520252025%" headers="mcps1.1.7.1.4 "><p id="p1102714366"><a name="p1102714366"></a><a name="p1102714366"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.35073507350735%" headers="mcps1.1.7.1.5 "><p id="p1386611524365"><a name="p1386611524365"></a><a name="p1386611524365"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p198661352103613"><a name="p198661352103613"></a><a name="p198661352103613"></a>×</p>
</td>
</tr>
<tr id="row1053216597228"><td class="cellrowborder" valign="top" width="9.050905090509051%" headers="mcps1.1.7.1.1 "><p id="p726615911359"><a name="p726615911359"></a><a name="p726615911359"></a>查询FPGA镜像详情列表</p>
</td>
<td class="cellrowborder" valign="top" width="31.113111311131114%" headers="mcps1.1.7.1.2 "><p id="p181681910192315"><a name="p181681910192315"></a><a name="p181681910192315"></a>GET /v1/{project_id}/cloudservers/fpga_image/detail</p>
</td>
<td class="cellrowborder" valign="top" width="24.71247124712471%" headers="mcps1.1.7.1.3 "><p id="p164534162715"><a name="p164534162715"></a><a name="p164534162715"></a>ecs:cloudServerFpgaImages:list</p>
</td>
<td class="cellrowborder" valign="top" width="20.25202520252025%" headers="mcps1.1.7.1.4 "><p id="p4101675366"><a name="p4101675366"></a><a name="p4101675366"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.35073507350735%" headers="mcps1.1.7.1.5 "><p id="p203491854133611"><a name="p203491854133611"></a><a name="p203491854133611"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p11349185433620"><a name="p11349185433620"></a><a name="p11349185433620"></a>×</p>
</td>
</tr>
<tr id="row17471104342218"><td class="cellrowborder" valign="top" width="9.050905090509051%" headers="mcps1.1.7.1.1 "><p id="p1726675993519"><a name="p1726675993519"></a><a name="p1726675993519"></a>删除FPGA镜像</p>
</td>
<td class="cellrowborder" valign="top" width="31.113111311131114%" headers="mcps1.1.7.1.2 "><p id="p616891020237"><a name="p616891020237"></a><a name="p616891020237"></a>DELETE /v1/{project_id}/cloudservers/fpga_image/{fpga_image_id}</p>
</td>
<td class="cellrowborder" valign="top" width="24.71247124712471%" headers="mcps1.1.7.1.3 "><p id="p715610425273"><a name="p715610425273"></a><a name="p715610425273"></a>ecs:cloudServerFpgaImages:delete</p>
</td>
<td class="cellrowborder" valign="top" width="20.25202520252025%" headers="mcps1.1.7.1.4 "><p id="p181015773612"><a name="p181015773612"></a><a name="p181015773612"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.35073507350735%" headers="mcps1.1.7.1.5 "><p id="p99464558363"><a name="p99464558363"></a><a name="p99464558363"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p09465555369"><a name="p09465555369"></a><a name="p09465555369"></a>×</p>
</td>
</tr>
<tr id="row152011446132211"><td class="cellrowborder" valign="top" width="9.050905090509051%" headers="mcps1.1.7.1.1 "><p id="p1726617596359"><a name="p1726617596359"></a><a name="p1726617596359"></a>关联FPGA镜像与弹性云服务器镜像</p>
</td>
<td class="cellrowborder" valign="top" width="31.113111311131114%" headers="mcps1.1.7.1.2 "><p id="p10168171072318"><a name="p10168171072318"></a><a name="p10168171072318"></a>POST /v1/{project_id}/cloudservers/fpga_image/{fpga_image_id}/association</p>
</td>
<td class="cellrowborder" valign="top" width="24.71247124712471%" headers="mcps1.1.7.1.3 "><p id="p849712437276"><a name="p849712437276"></a><a name="p849712437276"></a>ecs:cloudServerFpgaImages:relate</p>
</td>
<td class="cellrowborder" valign="top" width="20.25202520252025%" headers="mcps1.1.7.1.4 "><p id="p201057203619"><a name="p201057203619"></a><a name="p201057203619"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.35073507350735%" headers="mcps1.1.7.1.5 "><p id="p66105743618"><a name="p66105743618"></a><a name="p66105743618"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p468573364"><a name="p468573364"></a><a name="p468573364"></a>×</p>
</td>
</tr>
<tr id="row137161050132212"><td class="cellrowborder" valign="top" width="9.050905090509051%" headers="mcps1.1.7.1.1 "><p id="p182661759163510"><a name="p182661759163510"></a><a name="p182661759163510"></a>注册FPGA镜像</p>
</td>
<td class="cellrowborder" valign="top" width="31.113111311131114%" headers="mcps1.1.7.1.2 "><p id="p616810109231"><a name="p616810109231"></a><a name="p616810109231"></a>POST /v1/{project_id}/cloudservers/fpga_image</p>
</td>
<td class="cellrowborder" valign="top" width="24.71247124712471%" headers="mcps1.1.7.1.3 "><p id="p129474565270"><a name="p129474565270"></a><a name="p129474565270"></a>ecs:cloudServerFpgaImages:register</p>
</td>
<td class="cellrowborder" valign="top" width="20.25202520252025%" headers="mcps1.1.7.1.4 "><p id="p210117143615"><a name="p210117143615"></a><a name="p210117143615"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="7.35073507350735%" headers="mcps1.1.7.1.5 "><p id="p95461558173611"><a name="p95461558173611"></a><a name="p95461558173611"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.7.1.6 "><p id="p554611587365"><a name="p554611587365"></a><a name="p554611587365"></a>×</p>
</td>
</tr>
</tbody>
</table>

