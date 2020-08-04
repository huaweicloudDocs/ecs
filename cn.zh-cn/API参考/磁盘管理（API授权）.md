# 磁盘管理<a name="ZH-CN_TOPIC_0103071514"></a>

<a name="table88951955182420"></a>
<table><thead align="left"><tr id="row2670183317019"><th class="cellrowborder" valign="top" width="12.121212121212121%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="28.972897289728973%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="22.21222122212221%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="18.271827182718273%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="10.181018101810182%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="8.24082408240824%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row1893621632116"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p46472315137"><a name="p46472315137"></a><a name="p46472315137"></a>卸载指定弹性云服务器的磁盘</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p865419331215"><a name="p865419331215"></a><a name="p865419331215"></a>DELETE /v1/{project_id}/cloudservers/{server_id}/detachvolume/{attachment_id}</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p19414139181712"><a name="p19414139181712"></a><a name="p19414139181712"></a>ecs:cloudServers:detachVolume</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p1653821612139"><a name="p1653821612139"></a><a name="p1653821612139"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p533531191217"><a name="p533531191217"></a><a name="p533531191217"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p63353120124"><a name="p63353120124"></a><a name="p63353120124"></a>√</p>
</td>
</tr>
<tr id="row15734520162118"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p9647193101310"><a name="p9647193101310"></a><a name="p9647193101310"></a><span id="text06111723563"><a name="text06111723563"></a><a name="text06111723563"></a>弹性云服务器</span>挂载磁盘</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p3654133142110"><a name="p3654133142110"></a><a name="p3654133142110"></a>POST /v1/{project_id}/cloudservers/{server_id}/attachvolume</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p14731162881716"><a name="p14731162881716"></a><a name="p14731162881716"></a>ecs:cloudServers:attach</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p49761529101710"><a name="p49761529101710"></a><a name="p49761529101710"></a>evs:volumes:use</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p16163112051410"><a name="p16163112051410"></a><a name="p16163112051410"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p14163152041419"><a name="p14163152041419"></a><a name="p14163152041419"></a>√</p>
</td>
</tr>
<tr id="row19372485254"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p36473361311"><a name="p36473361311"></a><a name="p36473361311"></a>查询弹性云服务器磁盘信息</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p173726811250"><a name="p173726811250"></a><a name="p173726811250"></a>GET /v1/{project_id}/cloudservers/{server_id}/block_device</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p19869172571911"><a name="p19869172571911"></a><a name="p19869172571911"></a>ecs:cloudServers:get</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p253831614134"><a name="p253831614134"></a><a name="p253831614134"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p215302171418"><a name="p215302171418"></a><a name="p215302171418"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p8153132110142"><a name="p8153132110142"></a><a name="p8153132110142"></a>√</p>
</td>
</tr>
<tr id="row1860721413253"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p264712315138"><a name="p264712315138"></a><a name="p264712315138"></a>查询弹性云服务器挂载卷信息</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p196071514102517"><a name="p196071514102517"></a><a name="p196071514102517"></a>GET /v1/{project_id}/cloudservers/{server_id}/os-volume_attachments</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p918252719191"><a name="p918252719191"></a><a name="p918252719191"></a>ecs:cloudServers:get</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p853831612137"><a name="p853831612137"></a><a name="p853831612137"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p168114222146"><a name="p168114222146"></a><a name="p168114222146"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p7811922181412"><a name="p7811922181412"></a><a name="p7811922181412"></a>√</p>
</td>
</tr>
<tr id="row136039493553"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p19647733137"><a name="p19647733137"></a><a name="p19647733137"></a>查询<span id="text7402624265"><a name="text7402624265"></a><a name="text7402624265"></a>弹性云服务器</span>单个磁盘挂载信息</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="zh-cn_topic_0101860614_p248418710335"><a name="zh-cn_topic_0101860614_p248418710335"></a><a name="zh-cn_topic_0101860614_p248418710335"></a>GET /v1/cloudservers/{server_id}/block_device/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p03113282193"><a name="p03113282193"></a><a name="p03113282193"></a>ecs:cloudServers:get</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p5538101610134"><a name="p5538101610134"></a><a name="p5538101610134"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p317872319146"><a name="p317872319146"></a><a name="p317872319146"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p1117882315143"><a name="p1117882315143"></a><a name="p1117882315143"></a>√</p>
</td>
</tr>
<tr id="row18432110194915"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p206470318138"><a name="p206470318138"></a><a name="p206470318138"></a>弹性云服务器挂载磁盘(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p14236125619354"><a name="p14236125619354"></a><a name="p14236125619354"></a>POST /v2.1/{project_id}/servers/{server_id}/os-volume_attachments</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p1299043519196"><a name="p1299043519196"></a><a name="p1299043519196"></a>ecs:serverVolumeAttachments:create</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p58973374195"><a name="p58973374195"></a><a name="p58973374195"></a>ecs:serverVolumes:use</p>
<p id="p135414379191"><a name="p135414379191"></a><a name="p135414379191"></a>evs:volumes:list</p>
<p id="p1289115385198"><a name="p1289115385198"></a><a name="p1289115385198"></a>evs:volumes:get</p>
<p id="p18620139101919"><a name="p18620139101919"></a><a name="p18620139101919"></a>evs:volumes:update</p>
<p id="p10356144013199"><a name="p10356144013199"></a><a name="p10356144013199"></a>evs:volumes:attach</p>
<p id="p132091041171915"><a name="p132091041171915"></a><a name="p132091041171915"></a>evs:volumes:manage</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p16339125181119"><a name="p16339125181119"></a><a name="p16339125181119"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p633919516113"><a name="p633919516113"></a><a name="p633919516113"></a>×</p>
</td>
</tr>
<tr id="row74321703496"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p146473331315"><a name="p146473331315"></a><a name="p146473331315"></a>卸载云服务器磁盘（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p1297435133610"><a name="p1297435133610"></a><a name="p1297435133610"></a>DELETE /v2.1/{project_id}/servers/{server_id}/os-volume_attachments/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p11938125012193"><a name="p11938125012193"></a><a name="p11938125012193"></a>ecs:serverVolumeAttachments:delete</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p13143953151911"><a name="p13143953151911"></a><a name="p13143953151911"></a>ecs:serverVolumes:use</p>
<p id="p14984953171919"><a name="p14984953171919"></a><a name="p14984953171919"></a>evs:volumes:list</p>
<p id="p136541654161918"><a name="p136541654161918"></a><a name="p136541654161918"></a>evs:volumes:get</p>
<p id="p2031445541913"><a name="p2031445541913"></a><a name="p2031445541913"></a>evs:volumes:update</p>
<p id="p523205641916"><a name="p523205641916"></a><a name="p523205641916"></a>evs:volumes:detach</p>
<p id="p1419516578191"><a name="p1419516578191"></a><a name="p1419516578191"></a>evs:volumes:manage</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p1298113031410"><a name="p1298113031410"></a><a name="p1298113031410"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p19863015148"><a name="p19863015148"></a><a name="p19863015148"></a>×</p>
</td>
</tr>
<tr id="row74328064918"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p14647738134"><a name="p14647738134"></a><a name="p14647738134"></a>查询弹性云服务器挂载磁盘信息列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p260410182367"><a name="p260410182367"></a><a name="p260410182367"></a>GET /v2.1/{project_id}/servers/{server_id}/os-volume_attachments</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p1268258205"><a name="p1268258205"></a><a name="p1268258205"></a>ecs:serverVolumeAttachments:list</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p102003618205"><a name="p102003618205"></a><a name="p102003618205"></a>ecs:serverVolumes:use</p>
<p id="p2241137152020"><a name="p2241137152020"></a><a name="p2241137152020"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p182673119147"><a name="p182673119147"></a><a name="p182673119147"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p682611315145"><a name="p682611315145"></a><a name="p682611315145"></a>×</p>
</td>
</tr>
<tr id="row1434619574918"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p1364733121315"><a name="p1364733121315"></a><a name="p1364733121315"></a>查询弹性云服务器挂载的单个磁盘信息（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p15134624103611"><a name="p15134624103611"></a><a name="p15134624103611"></a>GET /v2.1/{project_id}/servers/{server_id}/os-volume_attachments/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p192649146206"><a name="p192649146206"></a><a name="p192649146206"></a>ecs:serverVolumeAttachments:get</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p19538181619134"><a name="p19538181619134"></a><a name="p19538181619134"></a>ecs:serverVolumes:use</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p1739320333146"><a name="p1739320333146"></a><a name="p1739320333146"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p1839310332144"><a name="p1839310332144"></a><a name="p1839310332144"></a>×</p>
</td>
</tr>
<tr id="row1976111120493"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p1264718321317"><a name="p1264718321317"></a><a name="p1264718321317"></a>创建磁盘（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p6189165412361"><a name="p6189165412361"></a><a name="p6189165412361"></a>POST /v2.1/{project_id}/os-volumes</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p1551641914204"><a name="p1551641914204"></a><a name="p1551641914204"></a>ecs:serverVolumes:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p115381816191310"><a name="p115381816191310"></a><a name="p115381816191310"></a>evs:volumes:create</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p1166123571417"><a name="p1166123571417"></a><a name="p1166123571417"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p3166153511413"><a name="p3166153511413"></a><a name="p3166153511413"></a>×</p>
</td>
</tr>
<tr id="row14762113499"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p764713181313"><a name="p764713181313"></a><a name="p764713181313"></a>删除磁盘（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p20452165923617"><a name="p20452165923617"></a><a name="p20452165923617"></a>DELETE /v2.1/{project_id}/os-volumes/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p366219489208"><a name="p366219489208"></a><a name="p366219489208"></a>ecs:serverVolumes:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p035864616203"><a name="p035864616203"></a><a name="p035864616203"></a>evs:volumes:get</p>
<p id="p7446747192011"><a name="p7446747192011"></a><a name="p7446747192011"></a>evs:volumes:delete</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p753912365142"><a name="p753912365142"></a><a name="p753912365142"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p18539103681419"><a name="p18539103681419"></a><a name="p18539103681419"></a>×</p>
</td>
</tr>
<tr id="row97710116497"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p1364712318132"><a name="p1364712318132"></a><a name="p1364712318132"></a>查询指定磁盘信息（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p179594113716"><a name="p179594113716"></a><a name="p179594113716"></a>GET /v2.1/{project_id}/os-volumes/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p19632105372017"><a name="p19632105372017"></a><a name="p19632105372017"></a>ecs:serverVolumes:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p253816169132"><a name="p253816169132"></a><a name="p253816169132"></a>evs:volumes:get</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p1969023791415"><a name="p1969023791415"></a><a name="p1969023791415"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p1169013731413"><a name="p1169013731413"></a><a name="p1169013731413"></a>×</p>
</td>
</tr>
<tr id="row37741114911"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p664733161310"><a name="p664733161310"></a><a name="p664733161310"></a>查询磁盘列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p984217813370"><a name="p984217813370"></a><a name="p984217813370"></a>GET /v2.1/{project_id}/os-volumes</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p1830611162111"><a name="p1830611162111"></a><a name="p1830611162111"></a>ecs:serverVolumes:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p10421359192014"><a name="p10421359192014"></a><a name="p10421359192014"></a>evs:volumes:get</p>
<p id="p378714590208"><a name="p378714590208"></a><a name="p378714590208"></a>evs:volumes:list</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p14203203941413"><a name="p14203203941413"></a><a name="p14203203941413"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p132031939181420"><a name="p132031939181420"></a><a name="p132031939181420"></a>×</p>
</td>
</tr>
<tr id="row43471056491"><td class="cellrowborder" valign="top" width="12.121212121212121%" headers="mcps1.1.7.1.1 "><p id="p13647123121319"><a name="p13647123121319"></a><a name="p13647123121319"></a>查询磁盘详情列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="28.972897289728973%" headers="mcps1.1.7.1.2 "><p id="p1125381323710"><a name="p1125381323710"></a><a name="p1125381323710"></a>GET /v2.1/{project_id}/os-volumes/detail</p>
</td>
<td class="cellrowborder" valign="top" width="22.21222122212221%" headers="mcps1.1.7.1.3 "><p id="p6367889213"><a name="p6367889213"></a><a name="p6367889213"></a>ecs:serverVolumes:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.271827182718273%" headers="mcps1.1.7.1.4 "><p id="p112015612116"><a name="p112015612116"></a><a name="p112015612116"></a>evs:volumes:get</p>
<p id="p6162207172119"><a name="p6162207172119"></a><a name="p6162207172119"></a>evs:volumes:list</p>
</td>
<td class="cellrowborder" valign="top" width="10.181018101810182%" headers="mcps1.1.7.1.5 "><p id="p1726916409147"><a name="p1726916409147"></a><a name="p1726916409147"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.24082408240824%" headers="mcps1.1.7.1.6 "><p id="p12269154011420"><a name="p12269154011420"></a><a name="p12269154011420"></a>×</p>
</td>
</tr>
</tbody>
</table>

