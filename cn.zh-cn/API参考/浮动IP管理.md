# 浮动IP管理<a name="ecs_06_0015"></a>

<a name="table597722943219"></a>
<table><thead align="left"><tr id="row20978132943210"><th class="cellrowborder" valign="top" width="9.29092909290929%" id="mcps1.1.9.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="17.76177617761776%" id="mcps1.1.9.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="19.45194519451945%" id="mcps1.1.9.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="15.881588158815878%" id="mcps1.1.9.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="8.44084408440844%" id="mcps1.1.9.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="14.7014701470147%" id="mcps1.1.9.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
<th class="cellrowborder" valign="top" width="6.95069506950695%" id="mcps1.1.9.1.7"><p id="p145471353104218"><a name="p145471353104218"></a><a name="p145471353104218"></a>实例授权</p>
</th>
<th class="cellrowborder" valign="top" width="7.520752075207521%" id="mcps1.1.9.1.8"><p id="p1538156134218"><a name="p1538156134218"></a><a name="p1538156134218"></a>标签授权</p>
</th>
</tr>
</thead>
<tbody><tr id="row13978152915327"><td class="cellrowborder" valign="top" width="9.29092909290929%" headers="mcps1.1.9.1.1 "><p id="p1928615162611"><a name="p1928615162611"></a><a name="p1928615162611"></a><a href="创建浮动IP（废弃）.md">创建浮动IP（OpenStack原生）</a></p>
</td>
<td class="cellrowborder" valign="top" width="17.76177617761776%" headers="mcps1.1.9.1.2 "><p id="p1912112154117"><a name="p1912112154117"></a><a name="p1912112154117"></a>POST /v2.1/{project_id}/os-floating-ips</p>
</td>
<td class="cellrowborder" valign="top" width="19.45194519451945%" headers="mcps1.1.9.1.3 "><p id="p2485752142218"><a name="p2485752142218"></a><a name="p2485752142218"></a>ecs:serverFloatingIps:use</p>
</td>
<td class="cellrowborder" valign="top" width="15.881588158815878%" headers="mcps1.1.9.1.4 "><p id="p177981953182215"><a name="p177981953182215"></a><a name="p177981953182215"></a>vpc:floatingIps:get</p>
<p id="p048645482213"><a name="p048645482213"></a><a name="p048645482213"></a>vpc:floatingIps:create</p>
<p id="p328817559226"><a name="p328817559226"></a><a name="p328817559226"></a>vpc:floatingIps:update</p>
<p id="p1221725652212"><a name="p1221725652212"></a><a name="p1221725652212"></a>vpc:ports:get</p>
</td>
<td class="cellrowborder" valign="top" width="8.44084408440844%" headers="mcps1.1.9.1.5 "><p id="p1178918181914"><a name="p1178918181914"></a><a name="p1178918181914"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.7014701470147%" headers="mcps1.1.9.1.6 "><p id="p578171820196"><a name="p578171820196"></a><a name="p578171820196"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="6.95069506950695%" headers="mcps1.1.9.1.7 "><p id="p125471753154216"><a name="p125471753154216"></a><a name="p125471753154216"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.9.1.8 "><p id="p1153814568420"><a name="p1153814568420"></a><a name="p1153814568420"></a>×</p>
</td>
</tr>
<tr id="row89781529103215"><td class="cellrowborder" valign="top" width="9.29092909290929%" headers="mcps1.1.9.1.1 "><p id="p52861458261"><a name="p52861458261"></a><a name="p52861458261"></a><a href="查询浮动IP列表（废弃）.md">查询浮动IP列表（OpenStack原生）</a></p>
</td>
<td class="cellrowborder" valign="top" width="17.76177617761776%" headers="mcps1.1.9.1.2 "><p id="p75051616124113"><a name="p75051616124113"></a><a name="p75051616124113"></a>GET /v2.1/{project_id}/os-floating-ips</p>
</td>
<td class="cellrowborder" valign="top" width="19.45194519451945%" headers="mcps1.1.9.1.3 "><p id="p1092012490221"><a name="p1092012490221"></a><a name="p1092012490221"></a>ecs:serverFloatingIps:use</p>
</td>
<td class="cellrowborder" valign="top" width="15.881588158815878%" headers="mcps1.1.9.1.4 "><p id="p3935125619221"><a name="p3935125619221"></a><a name="p3935125619221"></a>vpc:floatingIps:get</p>
<p id="p859919575228"><a name="p859919575228"></a><a name="p859919575228"></a>vpc:ports:get</p>
</td>
<td class="cellrowborder" valign="top" width="8.44084408440844%" headers="mcps1.1.9.1.5 "><p id="p134071856152613"><a name="p134071856152613"></a><a name="p134071856152613"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.7014701470147%" headers="mcps1.1.9.1.6 "><p id="p7407356112612"><a name="p7407356112612"></a><a name="p7407356112612"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="6.95069506950695%" headers="mcps1.1.9.1.7 "><p id="p1554716539422"><a name="p1554716539422"></a><a name="p1554716539422"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.9.1.8 "><p id="p145381456194213"><a name="p145381456194213"></a><a name="p145381456194213"></a>×</p>
</td>
</tr>
<tr id="row18978329133213"><td class="cellrowborder" valign="top" width="9.29092909290929%" headers="mcps1.1.9.1.1 "><p id="p152861656262"><a name="p152861656262"></a><a name="p152861656262"></a><a href="查询浮动IP（废弃）.md">查询浮动IP（OpenStack原生）</a></p>
</td>
<td class="cellrowborder" valign="top" width="17.76177617761776%" headers="mcps1.1.9.1.2 "><p id="p14179172084116"><a name="p14179172084116"></a><a name="p14179172084116"></a>GET /v2.1/{project_id}/os-floating-ips/{floating_ip_id}</p>
</td>
<td class="cellrowborder" valign="top" width="19.45194519451945%" headers="mcps1.1.9.1.3 "><p id="p109594472222"><a name="p109594472222"></a><a name="p109594472222"></a>ecs:serverFloatingIps:use</p>
</td>
<td class="cellrowborder" valign="top" width="15.881588158815878%" headers="mcps1.1.9.1.4 "><p id="p1472419582228"><a name="p1472419582228"></a><a name="p1472419582228"></a>vpc:floatingIps:get</p>
<p id="p12290959122210"><a name="p12290959122210"></a><a name="p12290959122210"></a>vpc:ports:get</p>
</td>
<td class="cellrowborder" valign="top" width="8.44084408440844%" headers="mcps1.1.9.1.5 "><p id="p551811571269"><a name="p551811571269"></a><a name="p551811571269"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.7014701470147%" headers="mcps1.1.9.1.6 "><p id="p135181357102610"><a name="p135181357102610"></a><a name="p135181357102610"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="6.95069506950695%" headers="mcps1.1.9.1.7 "><p id="p1954745313422"><a name="p1954745313422"></a><a name="p1954745313422"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.9.1.8 "><p id="p1253885624216"><a name="p1253885624216"></a><a name="p1253885624216"></a>×</p>
</td>
</tr>
<tr id="row19781429183210"><td class="cellrowborder" valign="top" width="9.29092909290929%" headers="mcps1.1.9.1.1 "><p id="p828616582617"><a name="p828616582617"></a><a name="p828616582617"></a><a href="删除浮动IP（废弃）.md">删除浮动IP（OpenStack原生）</a></p>
</td>
<td class="cellrowborder" valign="top" width="17.76177617761776%" headers="mcps1.1.9.1.2 "><p id="p9371172418414"><a name="p9371172418414"></a><a name="p9371172418414"></a>DELETE /v2.1/{project_id}/os-floating-ips/{floating_ip_id}</p>
</td>
<td class="cellrowborder" valign="top" width="19.45194519451945%" headers="mcps1.1.9.1.3 "><p id="p1169724610222"><a name="p1169724610222"></a><a name="p1169724610222"></a>ecs:serverFloatingIps:use</p>
</td>
<td class="cellrowborder" valign="top" width="15.881588158815878%" headers="mcps1.1.9.1.4 "><p id="p176471706235"><a name="p176471706235"></a><a name="p176471706235"></a>vpc:floatingIps:get</p>
<p id="p6289141112316"><a name="p6289141112316"></a><a name="p6289141112316"></a>vpc:floatingIps:delete</p>
<p id="p8371223233"><a name="p8371223233"></a><a name="p8371223233"></a>vpc:floatingIps:update</p>
<p id="p715317312318"><a name="p715317312318"></a><a name="p715317312318"></a>vpc:ports:get</p>
</td>
<td class="cellrowborder" valign="top" width="8.44084408440844%" headers="mcps1.1.9.1.5 "><p id="p1213385962620"><a name="p1213385962620"></a><a name="p1213385962620"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="14.7014701470147%" headers="mcps1.1.9.1.6 "><p id="p18133559172612"><a name="p18133559172612"></a><a name="p18133559172612"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="6.95069506950695%" headers="mcps1.1.9.1.7 "><p id="p1054745313422"><a name="p1054745313422"></a><a name="p1054745313422"></a>×</p>
</td>
<td class="cellrowborder" valign="top" width="7.520752075207521%" headers="mcps1.1.9.1.8 "><p id="p11538165664212"><a name="p11538165664212"></a><a name="p11538165664212"></a>×</p>
</td>
</tr>
</tbody>
</table>

