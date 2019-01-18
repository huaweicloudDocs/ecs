# 网卡管理<a name="ZH-CN_TOPIC_0103071513"></a>

**表 1** 

<a name="table166711250142311"></a>
<table><thead align="left"><tr id="row16721750172310"><th class="cellrowborder" valign="top" width="48.75%" id="mcps1.2.4.1.1"><p id="p1567220502233"><a name="p1567220502233"></a><a name="p1567220502233"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.4.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="26.249999999999996%" id="mcps1.2.4.1.3"><p id="p93075832319"><a name="p93075832319"></a><a name="p93075832319"></a>授权项</p>
</th>
</tr>
</thead>
<tbody><tr id="row2672125032316"><td class="cellrowborder" valign="top" width="48.75%" headers="mcps1.2.4.1.1 "><p id="p33882125248"><a name="p33882125248"></a><a name="p33882125248"></a>POST /v2/{tenant_id}/servers/{server_id}/os-interface</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.2 "><p id="p02271056433"><a name="p02271056433"></a><a name="p02271056433"></a>添加云服务器网卡（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="26.249999999999996%" headers="mcps1.2.4.1.3 "><a name="ul1388912122416"></a><a name="ul1388912122416"></a><ul id="ul1388912122416"><li>ecs:serverInterfaces:use</li><li>ecs:serverInterfaces:get</li></ul>
<a name="ul18388612152416"></a><a name="ul18388612152416"></a><ul id="ul18388612152416"><li>vpc:networks:get</li><li>vpc:networks:update</li><li>vpc:subnets:get</li><li>vpc:subnets:update</li><li>vpc:ports:create</li><li>vpc:ports:update</li><li>vpc:ports:get</li><li>vpc:networks:create</li><li>vpc:subnets:create</li><li>vpc:routers:get</li><li>vpc:routers:update</li></ul>
</td>
</tr>
<tr id="row06721150152313"><td class="cellrowborder" valign="top" width="48.75%" headers="mcps1.2.4.1.1 "><p id="p1738911218249"><a name="p1738911218249"></a><a name="p1738911218249"></a>DELETE /v2/{tenant_id}/servers/{server_id}/os-interface/{id}</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.2 "><p id="p152273515431"><a name="p152273515431"></a><a name="p152273515431"></a>删除云服务器网卡（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="26.249999999999996%" headers="mcps1.2.4.1.3 "><a name="ul193891312182411"></a><a name="ul193891312182411"></a><ul id="ul193891312182411"><li>ecs:serverInterfaces:use</li><li>ecs:serverInterfaces:get</li><li>ecs:servers:get</li></ul>
<a name="ul2038921282413"></a><a name="ul2038921282413"></a><ul id="ul2038921282413"><li>vpc:networks:create</li><li>vpc:subnets:create</li><li>vpc:networks:get</li><li>vpc:networks:update</li><li>vpc:subnets:get</li><li>vpc:subnets:update</li><li>vpc:ports:delete</li><li>vpc:ports:update</li><li>vpc:ports:get</li><li>vpc:routers:get</li><li>vpc:routers:update</li></ul>
</td>
</tr>
<tr id="row46721250112312"><td class="cellrowborder" valign="top" width="48.75%" headers="mcps1.2.4.1.1 "><p id="p1339151212245"><a name="p1339151212245"></a><a name="p1339151212245"></a>GET /v2/{tenant_id}/servers/{server_id}/os-interface</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.2 "><p id="p172276511435"><a name="p172276511435"></a><a name="p172276511435"></a>查询云服务器网卡信息列表（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="26.249999999999996%" headers="mcps1.2.4.1.3 "><a name="ul1339121242413"></a><a name="ul1339121242413"></a><ul id="ul1339121242413"><li>ecs:serverInterfaces:get</li></ul>
<a name="ul1339161262419"></a><a name="ul1339161262419"></a><ul id="ul1339161262419"><li>vpc:ports:get</li></ul>
</td>
</tr>
<tr id="row14673195092318"><td class="cellrowborder" valign="top" width="48.75%" headers="mcps1.2.4.1.1 "><p id="p3392131218246"><a name="p3392131218246"></a><a name="p3392131218246"></a>GET /v2/{tenant_id}/servers/{server_id}/os-interface/{id}</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.2 "><p id="p1022718514437"><a name="p1022718514437"></a><a name="p1022718514437"></a>查询指定云服务器网卡信息（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="26.249999999999996%" headers="mcps1.2.4.1.3 "><a name="ul8392181232411"></a><a name="ul8392181232411"></a><ul id="ul8392181232411"><li>ecs:serverInterfaces:get</li></ul>
<a name="ul1392171214243"></a><a name="ul1392171214243"></a><ul id="ul1392171214243"><li>vpc:ports:get</li></ul>
</td>
</tr>
<tr id="row1973020307205"><td class="cellrowborder" valign="top" width="48.75%" headers="mcps1.2.4.1.1 "><p id="p191461344182020"><a name="p191461344182020"></a><a name="p191461344182020"></a>POST /v1/{tenant_id}/cloudservers/{server_id}/nics/delete</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.2 "><p id="p92271859434"><a name="p92271859434"></a><a name="p92271859434"></a>批量删除云服务器网卡</p>
</td>
<td class="cellrowborder" valign="top" width="26.249999999999996%" headers="mcps1.2.4.1.3 "><a name="ul814613441202"></a><a name="ul814613441202"></a><ul id="ul814613441202"><li>ecs:cloudServerNics:delete</li></ul>
</td>
</tr>
<tr id="row13868733122016"><td class="cellrowborder" valign="top" width="48.75%" headers="mcps1.2.4.1.1 "><p id="p7146124419208"><a name="p7146124419208"></a><a name="p7146124419208"></a>POST /v1/{tenant_id}/cloudservers/{server_id}/nics</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.2 "><p id="p0227115184313"><a name="p0227115184313"></a><a name="p0227115184313"></a>批量添加云服务器网卡</p>
</td>
<td class="cellrowborder" valign="top" width="26.249999999999996%" headers="mcps1.2.4.1.3 "><a name="ul13146044152020"></a><a name="ul13146044152020"></a><ul id="ul13146044152020"><li>ecs:cloudServers:addNics</li></ul>
</td>
</tr>
</tbody>
</table>

