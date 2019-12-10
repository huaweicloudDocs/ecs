# FPGA逻辑文件管理<a name="ZH-CN_TOPIC_0132778339"></a>

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
<tbody><tr id="row2651640102215"><td class="cellrowborder" valign="top" width="40%" headers="mcps1.1.5.1.1 "><p id="p1516821032316"><a name="p1516821032316"></a><a name="p1516821032316"></a>GET /v1/{project_id}/cloudservers/fpga_image/associations{?image_id,fpga_image_id,page,size}</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.2 "><p id="p958218610428"><a name="p958218610428"></a><a name="p958218610428"></a>查询关联列表</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><a name="ul21681105233"></a><a name="ul21681105233"></a><ul id="ul21681105233"><li>ecs:cloudServerFpgaImages:getRelations</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul1120525295612"></a><a name="ul1120525295612"></a><ul id="ul1120525295612"><li>支持：</li></ul>
<p id="p7205175225615"><a name="p7205175225615"></a><a name="p7205175225615"></a>项目(Project)</p>
<p id="p52051152135613"><a name="p52051152135613"></a><a name="p52051152135613"></a></p>
<a name="ul20205165212562"></a><a name="ul20205165212562"></a><ul id="ul20205165212562"><li>不支持：</li></ul>
<p id="p720585265619"><a name="p720585265619"></a><a name="p720585265619"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row876855342215"><td class="cellrowborder" valign="top" width="40%" headers="mcps1.1.5.1.1 "><p id="p111681310102310"><a name="p111681310102310"></a><a name="p111681310102310"></a>DELETE /v1/{project_id}/cloudservers/fpga_image/{fpga_image_id}/association</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.2 "><p id="p1758286104210"><a name="p1758286104210"></a><a name="p1758286104210"></a>解关联FPGA镜像与弹性云服务器镜像</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><a name="ul151681010152313"></a><a name="ul151681010152313"></a><ul id="ul151681010152313"><li>ecs:cloudServerFpgaImags:unrelate</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul48014540565"></a><a name="ul48014540565"></a><ul id="ul48014540565"><li>支持：</li></ul>
<p id="p68085416565"><a name="p68085416565"></a><a name="p68085416565"></a>项目(Project)</p>
<p id="p3801554105611"><a name="p3801554105611"></a><a name="p3801554105611"></a></p>
<a name="ul88005418563"></a><a name="ul88005418563"></a><ul id="ul88005418563"><li>不支持：</li></ul>
<p id="p148035412561"><a name="p148035412561"></a><a name="p148035412561"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1053216597228"><td class="cellrowborder" valign="top" width="40%" headers="mcps1.1.5.1.1 "><p id="p181681910192315"><a name="p181681910192315"></a><a name="p181681910192315"></a>GET /v1/{project_id}/cloudservers/fpga_image/detail</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.2 "><p id="p658212624218"><a name="p658212624218"></a><a name="p658212624218"></a>查询FPGA镜像详情列表</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><a name="ul5168910122319"></a><a name="ul5168910122319"></a><ul id="ul5168910122319"><li>ecs:cloudServerFpgaImages:list</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul4941115645610"></a><a name="ul4941115645610"></a><ul id="ul4941115645610"><li>支持：</li></ul>
<p id="p195575645618"><a name="p195575645618"></a><a name="p195575645618"></a>项目(Project)</p>
<p id="p1595585695613"><a name="p1595585695613"></a><a name="p1595585695613"></a></p>
<a name="ul169551856125616"></a><a name="ul169551856125616"></a><ul id="ul169551856125616"><li>不支持：</li></ul>
<p id="p15955556135618"><a name="p15955556135618"></a><a name="p15955556135618"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row17471104342218"><td class="cellrowborder" valign="top" width="40%" headers="mcps1.1.5.1.1 "><p id="p616891020237"><a name="p616891020237"></a><a name="p616891020237"></a>DELETE /v1/{project_id}/cloudservers/fpga_image/{fpga_image_id}</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.2 "><p id="p8522122481317"><a name="p8522122481317"></a><a name="p8522122481317"></a>删除FPGA镜像</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><a name="ul416831042313"></a><a name="ul416831042313"></a><ul id="ul416831042313"><li>ecs:cloudServerFpgaImages:delete</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul586255835610"></a><a name="ul586255835610"></a><ul id="ul586255835610"><li>支持：</li></ul>
<p id="p6862205845615"><a name="p6862205845615"></a><a name="p6862205845615"></a>项目(Project)</p>
<p id="p186245815611"><a name="p186245815611"></a><a name="p186245815611"></a></p>
<a name="ul1686225819569"></a><a name="ul1686225819569"></a><ul id="ul1686225819569"><li>不支持：</li></ul>
<p id="p1787718588561"><a name="p1787718588561"></a><a name="p1787718588561"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row152011446132211"><td class="cellrowborder" valign="top" width="40%" headers="mcps1.1.5.1.1 "><p id="p10168171072318"><a name="p10168171072318"></a><a name="p10168171072318"></a>POST /v1/{project_id}/cloudservers/fpga_image/{fpga_image_id}/association</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.2 "><p id="p15583106164215"><a name="p15583106164215"></a><a name="p15583106164215"></a>关联FPGA镜像与弹性云服务器镜像</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><a name="ul1616841011231"></a><a name="ul1616841011231"></a><ul id="ul1616841011231"><li>ecs:cloudServerFpgaImages:relate</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul44081815576"></a><a name="ul44081815576"></a><ul id="ul44081815576"><li>支持：</li></ul>
<p id="p74081611570"><a name="p74081611570"></a><a name="p74081611570"></a>项目(Project)</p>
<p id="p04084115718"><a name="p04084115718"></a><a name="p04084115718"></a></p>
<a name="ul1440814175712"></a><a name="ul1440814175712"></a><ul id="ul1440814175712"><li>不支持：</li></ul>
<p id="p24081514578"><a name="p24081514578"></a><a name="p24081514578"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row137161050132212"><td class="cellrowborder" valign="top" width="40%" headers="mcps1.1.5.1.1 "><p id="p616810109231"><a name="p616810109231"></a><a name="p616810109231"></a>POST /v1/{project_id}/cloudservers/fpga_image</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.1.5.1.2 "><p id="p05830634217"><a name="p05830634217"></a><a name="p05830634217"></a>注册FPGA镜像</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><a name="ul15168410192311"></a><a name="ul15168410192311"></a><ul id="ul15168410192311"><li>ecs:cloudServerFpgaImages:register</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul1123814145713"></a><a name="ul1123814145713"></a><ul id="ul1123814145713"><li>支持：</li></ul>
<p id="p132386418574"><a name="p132386418574"></a><a name="p132386418574"></a>项目(Project)</p>
<p id="p132381946577"><a name="p132381946577"></a><a name="p132381946577"></a></p>
<a name="ul132387411578"></a><a name="ul132387411578"></a><ul id="ul132387411578"><li>不支持：</li></ul>
<p id="p202522485716"><a name="p202522485716"></a><a name="p202522485716"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

