# 状态管理<a name="ZH-CN_TOPIC_0103071511"></a>

<a name="table12570457816"></a>
<table><thead align="left"><tr id="row2025712451682"><th class="cellrowborder" valign="top" width="14.57%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="25.77%" id="mcps1.1.7.1.2"><p id="p72571745883"><a name="p72571745883"></a><a name="p72571745883"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="20.72%" id="mcps1.1.7.1.3"><p id="p162571745883"><a name="p162571745883"></a><a name="p162571745883"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="17.36%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="12.21%" id="mcps1.1.7.1.5"><p id="p12900195215510"><a name="p12900195215510"></a><a name="p12900195215510"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="9.370000000000001%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row43301239171419"><td class="cellrowborder" valign="top" width="14.57%" headers="mcps1.1.7.1.1 "><p id="p1715602614464"><a name="p1715602614464"></a><a name="p1715602614464"></a>切换弹性云服务器操作系统</p>
</td>
<td class="cellrowborder" valign="top" width="25.77%" headers="mcps1.1.7.1.2 "><p id="p1478183141917"><a name="p1478183141917"></a><a name="p1478183141917"></a>POST /v2/{project_id}/cloudservers/{server_id}/changeos</p>
<p id="p144788317197"><a name="p144788317197"></a><a name="p144788317197"></a>POST /v1/{project_id}/cloudservers/{server_id}/changeos</p>
</td>
<td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.7.1.3 "><p id="p06381852369"><a name="p06381852369"></a><a name="p06381852369"></a>ecs:cloudServers:changeOS</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.1.7.1.4 "><p id="p102516317459"><a name="p102516317459"></a><a name="p102516317459"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="12.21%" headers="mcps1.1.7.1.5 "><p id="p6972173513280"><a name="p6972173513280"></a><a name="p6972173513280"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.370000000000001%" headers="mcps1.1.7.1.6 "><p id="p1661123005817"><a name="p1661123005817"></a><a name="p1661123005817"></a>√</p>
</td>
</tr>
<tr id="row1225714451388"><td class="cellrowborder" valign="top" width="14.57%" headers="mcps1.1.7.1.1 "><p id="p12156326154614"><a name="p12156326154614"></a><a name="p12156326154614"></a>重装弹性云服务器操作系统</p>
</td>
<td class="cellrowborder" valign="top" width="25.77%" headers="mcps1.1.7.1.2 "><p id="p54781035190"><a name="p54781035190"></a><a name="p54781035190"></a>POST /v2/{project_id}/cloudservers/{server_id}/reinstallos</p>
<p id="p134786313191"><a name="p134786313191"></a><a name="p134786313191"></a>POST /v1/{project_id}/cloudservers/{server_id}/reinstallos</p>
</td>
<td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.7.1.3 "><p id="p8605951769"><a name="p8605951769"></a><a name="p8605951769"></a>ecs:cloudServers:rebuild</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.1.7.1.4 "><p id="p325183111458"><a name="p325183111458"></a><a name="p325183111458"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="12.21%" headers="mcps1.1.7.1.5 "><p id="p1455873517589"><a name="p1455873517589"></a><a name="p1455873517589"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.370000000000001%" headers="mcps1.1.7.1.6 "><p id="p145586350585"><a name="p145586350585"></a><a name="p145586350585"></a>√</p>
</td>
</tr>
<tr id="row39793162377"><td class="cellrowborder" valign="top" width="14.57%" headers="mcps1.1.7.1.1 "><p id="p3156162624610"><a name="p3156162624610"></a><a name="p3156162624610"></a>变更云服务器规格</p>
</td>
<td class="cellrowborder" valign="top" width="25.77%" headers="mcps1.1.7.1.2 "><p id="p79800164370"><a name="p79800164370"></a><a name="p79800164370"></a>POST /v1.1/{project_id}/cloudservers/{server_id}/resize</p>
</td>
<td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.7.1.3 "><p id="p10731124916617"><a name="p10731124916617"></a><a name="p10731124916617"></a>ecs:cloudServers:resize</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.1.7.1.4 "><p id="p525113110458"><a name="p525113110458"></a><a name="p525113110458"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="12.21%" headers="mcps1.1.7.1.5 "><p id="p118621837115815"><a name="p118621837115815"></a><a name="p118621837115815"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.370000000000001%" headers="mcps1.1.7.1.6 "><p id="p18862173714588"><a name="p18862173714588"></a><a name="p18862173714588"></a>√</p>
</td>
</tr>
<tr id="row113711517144014"><td class="cellrowborder" valign="top" width="14.57%" headers="mcps1.1.7.1.1 "><p id="p71569268463"><a name="p71569268463"></a><a name="p71569268463"></a>变更云服务器规格（按需）</p>
</td>
<td class="cellrowborder" valign="top" width="25.77%" headers="mcps1.1.7.1.2 "><p id="p204781139197"><a name="p204781139197"></a><a name="p204781139197"></a>POST /v1/{project_id}/cloudservers/{server_id}/resize</p>
</td>
<td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.7.1.3 "><p id="p148961148062"><a name="p148961148062"></a><a name="p148961148062"></a>ecs:cloudServers:resize</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.1.7.1.4 "><p id="p20253311457"><a name="p20253311457"></a><a name="p20253311457"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="12.21%" headers="mcps1.1.7.1.5 "><p id="p623219398588"><a name="p623219398588"></a><a name="p623219398588"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.370000000000001%" headers="mcps1.1.7.1.6 "><p id="p3232183915813"><a name="p3232183915813"></a><a name="p3232183915813"></a>√</p>
</td>
</tr>
<tr id="row12332174073420"><td class="cellrowborder" valign="top" width="14.57%" headers="mcps1.1.7.1.1 "><p id="p51561326194611"><a name="p51561326194611"></a><a name="p51561326194611"></a>冷迁移云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="25.77%" headers="mcps1.1.7.1.2 "><p id="p1497201991811"><a name="p1497201991811"></a><a name="p1497201991811"></a>POST /v1/{project_id}/cloudservers/{server_id}/migrate</p>
</td>
<td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.7.1.3 "><p id="p118331747167"><a name="p118331747167"></a><a name="p118331747167"></a>ecs:cloudServers:migrate</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.1.7.1.4 "><p id="p1925183114519"><a name="p1925183114519"></a><a name="p1925183114519"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="12.21%" headers="mcps1.1.7.1.5 "><p id="p17773154119589"><a name="p17773154119589"></a><a name="p17773154119589"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.370000000000001%" headers="mcps1.1.7.1.6 "><p id="p1677314105816"><a name="p1677314105816"></a><a name="p1677314105816"></a>√</p>
</td>
</tr>
<tr id="row52571745582"><td class="cellrowborder" valign="top" width="14.57%" headers="mcps1.1.7.1.1 "><p id="p81565268467"><a name="p81565268467"></a><a name="p81565268467"></a>关闭云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.77%" headers="mcps1.1.7.1.2 "><p id="p032112243919"><a name="p032112243919"></a><a name="p032112243919"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.7.1.3 "><p id="p181016445618"><a name="p181016445618"></a><a name="p181016445618"></a>ecs:servers:stop</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.1.7.1.4 "><p id="p82516310456"><a name="p82516310456"></a><a name="p82516310456"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="12.21%" headers="mcps1.1.7.1.5 "><p id="p10535183195917"><a name="p10535183195917"></a><a name="p10535183195917"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.370000000000001%" headers="mcps1.1.7.1.6 "><p id="p499283424513"><a name="p499283424513"></a><a name="p499283424513"></a>×</p>
</td>
</tr>
<tr id="row172571445985"><td class="cellrowborder" valign="top" width="14.57%" headers="mcps1.1.7.1.1 "><p id="p1815642654615"><a name="p1815642654615"></a><a name="p1815642654615"></a>重启云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.77%" headers="mcps1.1.7.1.2 "><p id="p19321824193"><a name="p19321824193"></a><a name="p19321824193"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.7.1.3 "><p id="p1614411381460"><a name="p1614411381460"></a><a name="p1614411381460"></a>ecs:servers:reboot</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.1.7.1.4 "><p id="p3853103619618"><a name="p3853103619618"></a><a name="p3853103619618"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="12.21%" headers="mcps1.1.7.1.5 "><p id="p079901011597"><a name="p079901011597"></a><a name="p079901011597"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.370000000000001%" headers="mcps1.1.7.1.6 "><p id="p6799610145918"><a name="p6799610145918"></a><a name="p6799610145918"></a>×</p>
</td>
</tr>
<tr id="row1525717451489"><td class="cellrowborder" valign="top" width="14.57%" headers="mcps1.1.7.1.1 "><p id="p9156326134617"><a name="p9156326134617"></a><a name="p9156326134617"></a>变更云服务器规格（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.77%" headers="mcps1.1.7.1.2 "><p id="p032110243914"><a name="p032110243914"></a><a name="p032110243914"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.7.1.3 "><p id="p1368916142613"><a name="p1368916142613"></a><a name="p1368916142613"></a>ecs:servers:resize</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.1.7.1.4 "><p id="p0991141512613"><a name="p0991141512613"></a><a name="p0991141512613"></a>ecs:servers:get</p>
<p id="p1965615165619"><a name="p1965615165619"></a><a name="p1965615165619"></a>evs:volumes:list</p>
<p id="p11367151720612"><a name="p11367151720612"></a><a name="p11367151720612"></a>evs:volumes:create</p>
<p id="p1122131816617"><a name="p1122131816617"></a><a name="p1122131816617"></a>evs:volumes:get</p>
<p id="p1910417195616"><a name="p1910417195616"></a><a name="p1910417195616"></a>evs:volumes:attach</p>
<p id="p1118132010614"><a name="p1118132010614"></a><a name="p1118132010614"></a>evs:volumes:detach</p>
<p id="p92786211867"><a name="p92786211867"></a><a name="p92786211867"></a>evs:volumes:manage</p>
<p id="p417182214619"><a name="p417182214619"></a><a name="p417182214619"></a>vpc:ports:get</p>
<p id="p14715182215619"><a name="p14715182215619"></a><a name="p14715182215619"></a>vpc:ports:update</p>
<p id="p5478623462"><a name="p5478623462"></a><a name="p5478623462"></a>vpc:ports:creare</p>
<p id="p05736241867"><a name="p05736241867"></a><a name="p05736241867"></a>vpc:ports:delete</p>
</td>
<td class="cellrowborder" valign="top" width="12.21%" headers="mcps1.1.7.1.5 "><p id="p1911241315919"><a name="p1911241315919"></a><a name="p1911241315919"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.370000000000001%" headers="mcps1.1.7.1.6 "><p id="p811211365912"><a name="p811211365912"></a><a name="p811211365912"></a>×</p>
</td>
</tr>
<tr id="row19808934597"><td class="cellrowborder" valign="top" width="14.57%" headers="mcps1.1.7.1.1 "><p id="p71561426134614"><a name="p71561426134614"></a><a name="p71561426134614"></a>锁定云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.77%" headers="mcps1.1.7.1.2 "><p id="p16597019203015"><a name="p16597019203015"></a><a name="p16597019203015"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.7.1.3 "><p id="p410012550517"><a name="p410012550517"></a><a name="p410012550517"></a>ecs:servers:lock</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.1.7.1.4 "><p id="p1265514534517"><a name="p1265514534517"></a><a name="p1265514534517"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="12.21%" headers="mcps1.1.7.1.5 "><p id="p652641714597"><a name="p652641714597"></a><a name="p652641714597"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.370000000000001%" headers="mcps1.1.7.1.6 "><p id="p85261917155920"><a name="p85261917155920"></a><a name="p85261917155920"></a>×</p>
</td>
</tr>
<tr id="row1180814349912"><td class="cellrowborder" valign="top" width="14.57%" headers="mcps1.1.7.1.1 "><p id="p14157112618463"><a name="p14157112618463"></a><a name="p14157112618463"></a>解锁定云服务器（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="25.77%" headers="mcps1.1.7.1.2 "><p id="p3361132313017"><a name="p3361132313017"></a><a name="p3361132313017"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="20.72%" headers="mcps1.1.7.1.3 "><p id="p24991246257"><a name="p24991246257"></a><a name="p24991246257"></a>ecs:servers:unlock</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.1.7.1.4 "><p id="p6258314450"><a name="p6258314450"></a><a name="p6258314450"></a>ecs:servers:get</p>
</td>
<td class="cellrowborder" valign="top" width="12.21%" headers="mcps1.1.7.1.5 "><p id="p57081518165916"><a name="p57081518165916"></a><a name="p57081518165916"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="9.370000000000001%" headers="mcps1.1.7.1.6 "><p id="p9708718185916"><a name="p9708718185916"></a><a name="p9708718185916"></a>×</p>
</td>
</tr>
</tbody>
</table>

