# 批量操作<a name="ecs_06_0004"></a>

<a name="table1587111571724"></a>
<table><thead align="left"><tr id="row20307121620133"><th class="cellrowborder" valign="top" width="14.3985601439856%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="26.42735726427357%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="21.067893210678932%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="16.93830616938306%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="11.678832116788321%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="9.48905109489051%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row137611507177"><td class="cellrowborder" valign="top" width="14.3985601439856%" headers="mcps1.1.7.1.1 "><p id="p133074307010"><a name="p133074307010"></a><a name="p133074307010"></a>批量关闭云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="26.42735726427357%" headers="mcps1.1.7.1.2 "><p id="p1479123111913"><a name="p1479123111913"></a><a name="p1479123111913"></a>POST /v1/{project_id}/cloudservers/action</p>
</td>
<td class="cellrowborder" valign="top" width="21.067893210678932%" headers="mcps1.1.7.1.3 "><p id="p95657581064"><a name="p95657581064"></a><a name="p95657581064"></a>ecs:cloudServers:stop</p>
</td>
<td class="cellrowborder" valign="top" width="16.93830616938306%" headers="mcps1.1.7.1.4 "><p id="p1954741618013"><a name="p1954741618013"></a><a name="p1954741618013"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.678832116788321%" headers="mcps1.1.7.1.5 "><p id="p3788175992810"><a name="p3788175992810"></a><a name="p3788175992810"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.48905109489051%" headers="mcps1.1.7.1.6 "><p id="p1467172313012"><a name="p1467172313012"></a><a name="p1467172313012"></a>√</p>
</td>
</tr>
<tr id="row17373916184"><td class="cellrowborder" valign="top" width="14.3985601439856%" headers="mcps1.1.7.1.1 "><p id="p17307173016014"><a name="p17307173016014"></a><a name="p17307173016014"></a>批量重启云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="26.42735726427357%" headers="mcps1.1.7.1.2 "><p id="p78289223194"><a name="p78289223194"></a><a name="p78289223194"></a>POST /v1/{project_id}/cloudservers/action</p>
</td>
<td class="cellrowborder" valign="top" width="21.067893210678932%" headers="mcps1.1.7.1.3 "><p id="p1445335919615"><a name="p1445335919615"></a><a name="p1445335919615"></a>ecs:cloudServers:reboot</p>
</td>
<td class="cellrowborder" valign="top" width="16.93830616938306%" headers="mcps1.1.7.1.4 "><p id="p55472169017"><a name="p55472169017"></a><a name="p55472169017"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.678832116788321%" headers="mcps1.1.7.1.5 "><p id="p728395010219"><a name="p728395010219"></a><a name="p728395010219"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.48905109489051%" headers="mcps1.1.7.1.6 "><p id="p128315505219"><a name="p128315505219"></a><a name="p128315505219"></a>√</p>
</td>
</tr>
<tr id="row293217122187"><td class="cellrowborder" valign="top" width="14.3985601439856%" headers="mcps1.1.7.1.1 "><p id="p9307113011011"><a name="p9307113011011"></a><a name="p9307113011011"></a>批量启动云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="26.42735726427357%" headers="mcps1.1.7.1.2 "><p id="p138281922141912"><a name="p138281922141912"></a><a name="p138281922141912"></a>POST /v1/{project_id}/cloudservers/action</p>
</td>
<td class="cellrowborder" valign="top" width="21.067893210678932%" headers="mcps1.1.7.1.3 "><p id="p162812013714"><a name="p162812013714"></a><a name="p162812013714"></a>ecs:cloudServers:start</p>
</td>
<td class="cellrowborder" valign="top" width="16.93830616938306%" headers="mcps1.1.7.1.4 "><p id="p1954721616017"><a name="p1954721616017"></a><a name="p1954721616017"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.678832116788321%" headers="mcps1.1.7.1.5 "><p id="p176185111214"><a name="p176185111214"></a><a name="p176185111214"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.48905109489051%" headers="mcps1.1.7.1.6 "><p id="p97612051629"><a name="p97612051629"></a><a name="p97612051629"></a>√</p>
</td>
</tr>
<tr id="row157372392127"><td class="cellrowborder" valign="top" width="14.3985601439856%" headers="mcps1.1.7.1.1 "><p id="p18308113012012"><a name="p18308113012012"></a><a name="p18308113012012"></a>批量修改弹性云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="26.42735726427357%" headers="mcps1.1.7.1.2 "><p id="p1398516132315"><a name="p1398516132315"></a><a name="p1398516132315"></a>PUT /v1/{project_id}/cloudservers/server-name</p>
</td>
<td class="cellrowborder" valign="top" width="21.067893210678932%" headers="mcps1.1.7.1.3 "><p id="p679311014716"><a name="p679311014716"></a><a name="p679311014716"></a>ecs:cloudServers:put</p>
</td>
<td class="cellrowborder" valign="top" width="16.93830616938306%" headers="mcps1.1.7.1.4 "><p id="p1754716162014"><a name="p1754716162014"></a><a name="p1754716162014"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.678832116788321%" headers="mcps1.1.7.1.5 "><p id="p1558165419217"><a name="p1558165419217"></a><a name="p1558165419217"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.48905109489051%" headers="mcps1.1.7.1.6 "><p id="p145818541824"><a name="p145818541824"></a><a name="p145818541824"></a>√</p>
</td>
</tr>
<tr id="row135911332185819"><td class="cellrowborder" valign="top" width="14.3985601439856%" headers="mcps1.1.7.1.1 "><p id="p930810301900"><a name="p930810301900"></a><a name="p930810301900"></a>批量挂载指定共享盘</p>
</td>
<td class="cellrowborder" valign="top" width="26.42735726427357%" headers="mcps1.1.7.1.2 "><p id="p1565303311219"><a name="p1565303311219"></a><a name="p1565303311219"></a>POST /v1/{project_id}/batchaction/attachvolumes/{volume_id}</p>
</td>
<td class="cellrowborder" valign="top" width="21.067893210678932%" headers="mcps1.1.7.1.3 "><p id="p277716215715"><a name="p277716215715"></a><a name="p277716215715"></a>ecs:cloudServers:attachSharedVolume</p>
</td>
<td class="cellrowborder" valign="top" width="16.93830616938306%" headers="mcps1.1.7.1.4 "><p id="p1092819466118"><a name="p1092819466118"></a><a name="p1092819466118"></a>evs:volumes:use</p>
</td>
<td class="cellrowborder" valign="top" width="11.678832116788321%" headers="mcps1.1.7.1.5 "><p id="p10290195717213"><a name="p10290195717213"></a><a name="p10290195717213"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.48905109489051%" headers="mcps1.1.7.1.6 "><p id="p82908571722"><a name="p82908571722"></a><a name="p82908571722"></a>√</p>
</td>
</tr>
</tbody>
</table>

