# 磁盘管理<a name="ZH-CN_TOPIC_0103071514"></a>

<a name="table88951955182420"></a>
<table><thead align="left"><tr id="row2670183317019"><th class="cellrowborder" valign="top" width="32.029999999999994%" id="mcps1.1.5.1.1"><p id="p1567220502233"><a name="p1567220502233"></a><a name="p1567220502233"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="21%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="27.97%" id="mcps1.1.5.1.3"><p id="p93075832319"><a name="p93075832319"></a><a name="p93075832319"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.4"><p id="p1130844411428"><a name="p1130844411428"></a><a name="p1130844411428"></a>授权项作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row1893621632116"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p865419331215"><a name="p865419331215"></a><a name="p865419331215"></a>DELETE /v1/{project_id}/cloudservers/{server_id}/detachvolume/{attachment_id}</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p0893123616432"><a name="p0893123616432"></a><a name="p0893123616432"></a>卸载指定弹性云服务器的磁盘</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul86541333202118"></a><a name="ul86541333202118"></a><ul id="ul86541333202118"><li>ecs:cloudServers:detachVolume</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul38809599234"></a><a name="ul38809599234"></a><ul id="ul38809599234"><li>支持：</li></ul>
<p id="p148971159142314"><a name="p148971159142314"></a><a name="p148971159142314"></a>项目(Project)</p>
<p id="p148971592237"><a name="p148971592237"></a><a name="p148971592237"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row15734520162118"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p3654133142110"><a name="p3654133142110"></a><a name="p3654133142110"></a>POST /v1/{project_id}/cloudservers/{server_id}/attachvolume</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p989316367430"><a name="p989316367430"></a><a name="p989316367430"></a>弹性云服务器云主机挂载磁盘</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul16654183313217"></a><a name="ul16654183313217"></a><ul id="ul16654183313217"><li>ecs:cloudServers:attach</li><li>evs:volumes:use</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul10931122412248"></a><a name="ul10931122412248"></a><ul id="ul10931122412248"><li>支持：</li></ul>
<p id="p3947122412412"><a name="p3947122412412"></a><a name="p3947122412412"></a>项目(Project)</p>
<p id="p8947724122413"><a name="p8947724122413"></a><a name="p8947724122413"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row19372485254"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p173726811250"><a name="p173726811250"></a><a name="p173726811250"></a>GET /v1/{project_id}/cloudservers/{server_id}/block_device</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p437228132515"><a name="p437228132515"></a><a name="p437228132515"></a>查询弹性云服务器磁盘信息</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul137241245122710"></a><a name="ul137241245122710"></a><ul id="ul137241245122710"><li>ecs:cloudServers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul1233415616286"></a><a name="ul1233415616286"></a><ul id="ul1233415616286"><li>支持：</li></ul>
<p id="p83341166285"><a name="p83341166285"></a><a name="p83341166285"></a>项目(Project)</p>
<p id="p9349168287"><a name="p9349168287"></a><a name="p9349168287"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1860721413253"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p196071514102517"><a name="p196071514102517"></a><a name="p196071514102517"></a>GET /v1/{project_id}/cloudservers/{server_id}/os-volume_attachments</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p72871918132711"><a name="p72871918132711"></a><a name="p72871918132711"></a>查询弹性云服务器挂载卷信息</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul27401251142718"></a><a name="ul27401251142718"></a><ul id="ul27401251142718"><li>ecs:cloudServers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul2838187132820"></a><a name="ul2838187132820"></a><ul id="ul2838187132820"><li>支持：</li></ul>
<p id="p1083817716284"><a name="p1083817716284"></a><a name="p1083817716284"></a>项目(Project)</p>
<p id="p148384752811"><a name="p148384752811"></a><a name="p148384752811"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row136039493553"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0101860614_p248418710335"><a name="zh-cn_topic_0101860614_p248418710335"></a><a name="zh-cn_topic_0101860614_p248418710335"></a>GET /v1/cloudservers/{server_id}/block_device/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p1227675511558"><a name="p1227675511558"></a><a name="p1227675511558"></a>查询弹性云服务器云主机单个磁盘挂载信息</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul15506161810562"></a><a name="ul15506161810562"></a><ul id="ul15506161810562"><li>ecs:cloudServers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul125971649105514"></a><a name="ul125971649105514"></a><ul id="ul125971649105514"><li>支持：</li></ul>
<p id="p45979496550"><a name="p45979496550"></a><a name="p45979496550"></a>项目(Project)</p>
<p id="p559774917552"><a name="p559774917552"></a><a name="p559774917552"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row18432110194915"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p14854133274912"><a name="p14854133274912"></a><a name="p14854133274912"></a>POST /v2.1/{project_id}/servers/{server_id}/os-volume_attachments</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p16854163215491"><a name="p16854163215491"></a><a name="p16854163215491"></a>弹性云服务器挂载磁盘(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul9854832114918"></a><a name="ul9854832114918"></a><ul id="ul9854832114918"><li>ecs:serverVolumeAttachments:create</li><li>ecs:serverVolumes:use</li></ul>
<a name="ul19854153254917"></a><a name="ul19854153254917"></a><ul id="ul19854153254917"><li>evs:volumes:list</li><li>evs:volumes:get</li><li>evs:volumes:update</li><li>evs:volumes:attach</li><li>evs:volumes:manage</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul3855232124912"></a><a name="ul3855232124912"></a><ul id="ul3855232124912"><li>支持：</li></ul>
<p id="p15855153294913"><a name="p15855153294913"></a><a name="p15855153294913"></a>项目(Project)</p>
<p id="p1685583224920"><a name="p1685583224920"></a><a name="p1685583224920"></a></p>
<a name="ul48551232184912"></a><a name="ul48551232184912"></a><ul id="ul48551232184912"><li>不支持：</li></ul>
<p id="p885520328492"><a name="p885520328492"></a><a name="p885520328492"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row74321703496"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p1785543254911"><a name="p1785543254911"></a><a name="p1785543254911"></a>DELETE /v2.1/{project_id}/servers/{server_id}/os-volume_attachments/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p12855432154911"><a name="p12855432154911"></a><a name="p12855432154911"></a>卸载云服务器磁盘（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul1985513327496"></a><a name="ul1985513327496"></a><ul id="ul1985513327496"><li>ecs:serverVolumeAttachments:delete</li><li>ecs:serverVolumes:use</li></ul>
<a name="ul18551322491"></a><a name="ul18551322491"></a><ul id="ul18551322491"><li>evs:volumes:list</li><li>evs:volumes:get</li><li>evs:volumes:update</li><li>evs:volumes:detach</li><li>evs:volumes:manage</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul108561932164910"></a><a name="ul108561932164910"></a><ul id="ul108561932164910"><li>支持：</li></ul>
<p id="p158561332154914"><a name="p158561332154914"></a><a name="p158561332154914"></a>项目(Project)</p>
<p id="p485613325497"><a name="p485613325497"></a><a name="p485613325497"></a></p>
<a name="ul10856203212494"></a><a name="ul10856203212494"></a><ul id="ul10856203212494"><li>不支持：</li></ul>
<p id="p685633294916"><a name="p685633294916"></a><a name="p685633294916"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row74328064918"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p68561032144910"><a name="p68561032144910"></a><a name="p68561032144910"></a>GET /v2.1/{project_id}/servers/{server_id}/os-volume_attachments</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p17856332134918"><a name="p17856332134918"></a><a name="p17856332134918"></a>查询弹性云服务器挂载磁盘信息列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul14856183244920"></a><a name="ul14856183244920"></a><ul id="ul14856183244920"><li>ecs:serverVolumeAttachments:list</li><li>ecs:serverVolumes:use</li><li>ecs:servers:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul178567322496"></a><a name="ul178567322496"></a><ul id="ul178567322496"><li>支持：</li></ul>
<p id="p885663218491"><a name="p885663218491"></a><a name="p885663218491"></a>项目(Project)</p>
<p id="p285683284910"><a name="p285683284910"></a><a name="p285683284910"></a></p>
<a name="ul1885663216491"></a><a name="ul1885663216491"></a><ul id="ul1885663216491"><li>不支持：</li></ul>
<p id="p108561132154914"><a name="p108561132154914"></a><a name="p108561132154914"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1434619574918"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p138567323496"><a name="p138567323496"></a><a name="p138567323496"></a>GET /v2.1/{project_id}/servers/{server_id}/os-volume_attachments/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p7856103211494"><a name="p7856103211494"></a><a name="p7856103211494"></a>查询弹性云服务器挂载的单个磁盘信息（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul5857132104912"></a><a name="ul5857132104912"></a><ul id="ul5857132104912"><li>ecs:serverVolumeAttachments:get</li><li>ecs:serverVolumes:use</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul7857143212499"></a><a name="ul7857143212499"></a><ul id="ul7857143212499"><li>支持：</li></ul>
<p id="p285783294917"><a name="p285783294917"></a><a name="p285783294917"></a>项目(Project)</p>
<p id="p2085743254916"><a name="p2085743254916"></a><a name="p2085743254916"></a></p>
<a name="ul198571032154911"></a><a name="ul198571032154911"></a><ul id="ul198571032154911"><li>不支持：</li></ul>
<p id="p085783244918"><a name="p085783244918"></a><a name="p085783244918"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1976111120493"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p148571432194918"><a name="p148571432194918"></a><a name="p148571432194918"></a>POST /v2.1/{project_id}/os-volumes</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p16857183219496"><a name="p16857183219496"></a><a name="p16857183219496"></a>创建磁盘（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul13857732194912"></a><a name="ul13857732194912"></a><ul id="ul13857732194912"><li>ecs:serverVolumes:use</li></ul>
<a name="ul585743217493"></a><a name="ul585743217493"></a><ul id="ul585743217493"><li>evs:volumes:create</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul15857193217498"></a><a name="ul15857193217498"></a><ul id="ul15857193217498"><li>支持：</li></ul>
<p id="p685733210494"><a name="p685733210494"></a><a name="p685733210494"></a>项目(Project)</p>
<p id="p8857332164915"><a name="p8857332164915"></a><a name="p8857332164915"></a></p>
<a name="ul9857203212498"></a><a name="ul9857203212498"></a><ul id="ul9857203212498"><li>不支持：</li></ul>
<p id="p285743215495"><a name="p285743215495"></a><a name="p285743215495"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row14762113499"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p168571532144916"><a name="p168571532144916"></a><a name="p168571532144916"></a>DELETE /v2.1/{project_id}/os-volumes/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p14858153214493"><a name="p14858153214493"></a><a name="p14858153214493"></a>删除磁盘（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul485893264919"></a><a name="ul485893264919"></a><ul id="ul485893264919"><li>ecs:serverVolumes:use</li></ul>
<a name="ul1185803217490"></a><a name="ul1185803217490"></a><ul id="ul1185803217490"><li>evs:volumes:get</li><li>evs:volumes:delete</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul13858732194910"></a><a name="ul13858732194910"></a><ul id="ul13858732194910"><li>支持：</li></ul>
<p id="p38581032144916"><a name="p38581032144916"></a><a name="p38581032144916"></a>项目(Project)</p>
<p id="p785818324491"><a name="p785818324491"></a><a name="p785818324491"></a></p>
<a name="ul12858332164912"></a><a name="ul12858332164912"></a><ul id="ul12858332164912"><li>不支持：</li></ul>
<p id="p10858193264911"><a name="p10858193264911"></a><a name="p10858193264911"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row97710116497"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p198589328499"><a name="p198589328499"></a><a name="p198589328499"></a>GET /v2.1/{project_id}/os-volumes/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p12858932104910"><a name="p12858932104910"></a><a name="p12858932104910"></a>查询指定磁盘信息（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul188581532104917"></a><a name="ul188581532104917"></a><ul id="ul188581532104917"><li>ecs:serverVolumes:use</li></ul>
<a name="ul1858183274913"></a><a name="ul1858183274913"></a><ul id="ul1858183274913"><li>evs:volumes:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul5858153254915"></a><a name="ul5858153254915"></a><ul id="ul5858153254915"><li>支持：</li></ul>
<p id="p785883294913"><a name="p785883294913"></a><a name="p785883294913"></a>项目(Project)</p>
<p id="p208581632124918"><a name="p208581632124918"></a><a name="p208581632124918"></a></p>
<a name="ul985963284918"></a><a name="ul985963284918"></a><ul id="ul985963284918"><li>不支持：</li></ul>
<p id="p9859143217492"><a name="p9859143217492"></a><a name="p9859143217492"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row37741114911"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p947117562504"><a name="p947117562504"></a><a name="p947117562504"></a>GET /v2.1/{project_id}/os-volumes</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p1447115611501"><a name="p1447115611501"></a><a name="p1447115611501"></a>查询磁盘列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul94711356155014"></a><a name="ul94711356155014"></a><ul id="ul94711356155014"><li>ecs:serverVolumes:use</li></ul>
<a name="ul44711756105016"></a><a name="ul44711756105016"></a><ul id="ul44711756105016"><li>evs:volumes:get</li><li>evs:volumes:list</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul17471155625015"></a><a name="ul17471155625015"></a><ul id="ul17471155625015"><li>支持：</li></ul>
<p id="p194715567505"><a name="p194715567505"></a><a name="p194715567505"></a>项目(Project)</p>
<p id="p154711656175010"><a name="p154711656175010"></a><a name="p154711656175010"></a></p>
<a name="ul247125685016"></a><a name="ul247125685016"></a><ul id="ul247125685016"><li>不支持：</li></ul>
<p id="p547185625016"><a name="p547185625016"></a><a name="p547185625016"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row43471056491"><td class="cellrowborder" valign="top" width="32.029999999999994%" headers="mcps1.1.5.1.1 "><p id="p164711856145011"><a name="p164711856145011"></a><a name="p164711856145011"></a>GET /v2.1/{project_id}/os-volumes/detail</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.1.5.1.2 "><p id="p12471115618504"><a name="p12471115618504"></a><a name="p12471115618504"></a>查询磁盘详情列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.97%" headers="mcps1.1.5.1.3 "><a name="ul647118564506"></a><a name="ul647118564506"></a><ul id="ul647118564506"><li>ecs:serverVolumes:use</li></ul>
<a name="ul6471155645012"></a><a name="ul6471155645012"></a><ul id="ul6471155645012"><li>evs:volumes:get</li><li>evs:volumes:list</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.4 "><a name="ul447235655012"></a><a name="ul447235655012"></a><ul id="ul447235655012"><li>支持：</li></ul>
<p id="p6472125645012"><a name="p6472125645012"></a><a name="p6472125645012"></a>项目(Project)</p>
<p id="p44721256195016"><a name="p44721256195016"></a><a name="p44721256195016"></a></p>
<a name="ul104721856155016"></a><a name="ul104721856155016"></a><ul id="ul104721856155016"><li>不支持：</li></ul>
<p id="p11472185635014"><a name="p11472185635014"></a><a name="p11472185635014"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

