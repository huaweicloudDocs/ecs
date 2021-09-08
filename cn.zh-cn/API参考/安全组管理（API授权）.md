# 安全组管理<a name="ZH-CN_TOPIC_0103072347"></a>

<a name="table614680103012"></a>
<table><thead align="left"><tr id="row121463017301"><th class="cellrowborder" valign="top" width="13.87%" id="mcps1.1.7.1.1"><p id="p1959712364512"><a name="p1959712364512"></a><a name="p1959712364512"></a>权限</p>
</th>
<th class="cellrowborder" valign="top" width="27.76%" id="mcps1.1.7.1.2"><p id="p8402164419019"><a name="p8402164419019"></a><a name="p8402164419019"></a>对应的API接口</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.1.7.1.3"><p id="p2040214445018"><a name="p2040214445018"></a><a name="p2040214445018"></a>授权项（Action）</p>
</th>
<th class="cellrowborder" valign="top" width="18.099999999999998%" id="mcps1.1.7.1.4"><p id="p22519318453"><a name="p22519318453"></a><a name="p22519318453"></a>依赖的授权项</p>
</th>
<th class="cellrowborder" valign="top" width="11.43%" id="mcps1.1.7.1.5"><p id="p84029445019"><a name="p84029445019"></a><a name="p84029445019"></a>IAM项目</p>
<p id="p12578131324712"><a name="p12578131324712"></a><a name="p12578131324712"></a>(Project)</p>
</th>
<th class="cellrowborder" valign="top" width="8.84%" id="mcps1.1.7.1.6"><p id="p1999212348459"><a name="p1999212348459"></a><a name="p1999212348459"></a>企业项目</p>
<p id="p1026502118478"><a name="p1026502118478"></a><a name="p1026502118478"></a>(Enterprise Project)</p>
</th>
</tr>
</thead>
<tbody><tr id="row141469023019"><td class="cellrowborder" valign="top" width="13.87%" headers="mcps1.1.7.1.1 "><p id="p1229134216516"><a name="p1229134216516"></a><a name="p1229134216516"></a>创建安全组(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="27.76%" headers="mcps1.1.7.1.2 "><p id="p174241828203118"><a name="p174241828203118"></a><a name="p174241828203118"></a>POST /v2.1/{project_id}/os-security-groups</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.7.1.3 "><p id="p783486134"><a name="p783486134"></a><a name="p783486134"></a>ecs:securityGroups:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.099999999999998%" headers="mcps1.1.7.1.4 "><p id="p13287349121319"><a name="p13287349121319"></a><a name="p13287349121319"></a>vpc:securityGroups:get</p>
<p id="p19241145019131"><a name="p19241145019131"></a><a name="p19241145019131"></a>vpc:securityGroups:create</p>
<p id="p43591551101320"><a name="p43591551101320"></a><a name="p43591551101320"></a>vpc:securityGroups:update</p>
</td>
<td class="cellrowborder" valign="top" width="11.43%" headers="mcps1.1.7.1.5 "><p id="p57081518165916"><a name="p57081518165916"></a><a name="p57081518165916"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.84%" headers="mcps1.1.7.1.6 "><p id="p9708718185916"><a name="p9708718185916"></a><a name="p9708718185916"></a>×</p>
</td>
</tr>
<tr id="row714610173016"><td class="cellrowborder" valign="top" width="13.87%" headers="mcps1.1.7.1.1 "><p id="p82299422055"><a name="p82299422055"></a><a name="p82299422055"></a>删除安全组(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="27.76%" headers="mcps1.1.7.1.2 "><p id="p1572117398318"><a name="p1572117398318"></a><a name="p1572117398318"></a>DELETE /v2.1/{project_id}/os-security-groups/{security_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.7.1.3 "><p id="p172281307145"><a name="p172281307145"></a><a name="p172281307145"></a>ecs:securityGroups:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.099999999999998%" headers="mcps1.1.7.1.4 "><p id="p411417572137"><a name="p411417572137"></a><a name="p411417572137"></a>vpc:securityGroups:get</p>
<p id="p95755818131"><a name="p95755818131"></a><a name="p95755818131"></a>vpc:securityGroups:delete</p>
<p id="p1887035881318"><a name="p1887035881318"></a><a name="p1887035881318"></a>vpc:securityGroups:update</p>
</td>
<td class="cellrowborder" valign="top" width="11.43%" headers="mcps1.1.7.1.5 "><p id="p19279628772"><a name="p19279628772"></a><a name="p19279628772"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.84%" headers="mcps1.1.7.1.6 "><p id="p62795281876"><a name="p62795281876"></a><a name="p62795281876"></a>×</p>
</td>
</tr>
<tr id="row111468093016"><td class="cellrowborder" valign="top" width="13.87%" headers="mcps1.1.7.1.1 "><p id="p32298421950"><a name="p32298421950"></a><a name="p32298421950"></a>查询安全组详细信息(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="27.76%" headers="mcps1.1.7.1.2 "><p id="p16711195820310"><a name="p16711195820310"></a><a name="p16711195820310"></a>GET /v2.1/{project_id}/os-security-groups/{security_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.7.1.3 "><p id="p19969771149"><a name="p19969771149"></a><a name="p19969771149"></a>ecs:securityGroups:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.099999999999998%" headers="mcps1.1.7.1.4 "><p id="p91530920144"><a name="p91530920144"></a><a name="p91530920144"></a>vpc:securityGroups:get</p>
</td>
<td class="cellrowborder" valign="top" width="11.43%" headers="mcps1.1.7.1.5 "><p id="p198223291371"><a name="p198223291371"></a><a name="p198223291371"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.84%" headers="mcps1.1.7.1.6 "><p id="p18221229775"><a name="p18221229775"></a><a name="p18221229775"></a>×</p>
</td>
</tr>
<tr id="row1914610012300"><td class="cellrowborder" valign="top" width="13.87%" headers="mcps1.1.7.1.1 "><p id="p202291042356"><a name="p202291042356"></a><a name="p202291042356"></a>查询安全组列表(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="27.76%" headers="mcps1.1.7.1.2 "><p id="p11337939321"><a name="p11337939321"></a><a name="p11337939321"></a>GET /v2.1/{project_id}/os-security-groups</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.7.1.3 "><p id="p16349715181415"><a name="p16349715181415"></a><a name="p16349715181415"></a>ecs:securityGroups:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.099999999999998%" headers="mcps1.1.7.1.4 "><p id="p56101815613"><a name="p56101815613"></a><a name="p56101815613"></a>vpc:securityGroups:get</p>
</td>
<td class="cellrowborder" valign="top" width="11.43%" headers="mcps1.1.7.1.5 "><p id="p651210312719"><a name="p651210312719"></a><a name="p651210312719"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.84%" headers="mcps1.1.7.1.6 "><p id="p135125311077"><a name="p135125311077"></a><a name="p135125311077"></a>×</p>
</td>
</tr>
<tr id="row9146903301"><td class="cellrowborder" valign="top" width="13.87%" headers="mcps1.1.7.1.1 "><p id="p3229134217516"><a name="p3229134217516"></a><a name="p3229134217516"></a>创建安全组规则(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="27.76%" headers="mcps1.1.7.1.2 "><p id="p15127771327"><a name="p15127771327"></a><a name="p15127771327"></a>POST /v2.1/{project_id}/os-security-group-rules</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.7.1.3 "><p id="p5834620181420"><a name="p5834620181420"></a><a name="p5834620181420"></a>ecs:securityGroups:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.099999999999998%" headers="mcps1.1.7.1.4 "><p id="p111172451415"><a name="p111172451415"></a><a name="p111172451415"></a>vpc:securityGroups:get</p>
<p id="p15976724151414"><a name="p15976724151414"></a><a name="p15976724151414"></a>vpc:securityGroups:update</p>
<p id="p354112691418"><a name="p354112691418"></a><a name="p354112691418"></a>vpc:securityGroupRules:get</p>
<p id="p95832761412"><a name="p95832761412"></a><a name="p95832761412"></a>vpc:securityGroupRules:create</p>
</td>
<td class="cellrowborder" valign="top" width="11.43%" headers="mcps1.1.7.1.5 "><p id="p18261103312712"><a name="p18261103312712"></a><a name="p18261103312712"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.84%" headers="mcps1.1.7.1.6 "><p id="p1526112331273"><a name="p1526112331273"></a><a name="p1526112331273"></a>×</p>
</td>
</tr>
<tr id="row19146707308"><td class="cellrowborder" valign="top" width="13.87%" headers="mcps1.1.7.1.1 "><p id="p13229164215513"><a name="p13229164215513"></a><a name="p13229164215513"></a>删除安全组规则(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="27.76%" headers="mcps1.1.7.1.2 "><p id="p554073153218"><a name="p554073153218"></a><a name="p554073153218"></a>DELETE /v2.1/{project_id}/os-security-group-rules/{security_group_rule_id}</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.7.1.3 "><p id="p961084619144"><a name="p961084619144"></a><a name="p961084619144"></a>ecs:securityGroups:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.099999999999998%" headers="mcps1.1.7.1.4 "><p id="p3265144211145"><a name="p3265144211145"></a><a name="p3265144211145"></a>vpc:securityGroups:get</p>
<p id="p894174312147"><a name="p894174312147"></a><a name="p894174312147"></a>vpc:securityGroups:update</p>
<p id="p19154144421410"><a name="p19154144421410"></a><a name="p19154144421410"></a>vpc:securityGroupRules:get</p>
<p id="p14973124451417"><a name="p14973124451417"></a><a name="p14973124451417"></a>vpc:securityGroupRules:delete</p>
</td>
<td class="cellrowborder" valign="top" width="11.43%" headers="mcps1.1.7.1.5 "><p id="p492614341714"><a name="p492614341714"></a><a name="p492614341714"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.84%" headers="mcps1.1.7.1.6 "><p id="p11926153414720"><a name="p11926153414720"></a><a name="p11926153414720"></a>×</p>
</td>
</tr>
<tr id="row5146906301"><td class="cellrowborder" valign="top" width="13.87%" headers="mcps1.1.7.1.1 "><p id="p722912420514"><a name="p722912420514"></a><a name="p722912420514"></a>更新安全组信息(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="27.76%" headers="mcps1.1.7.1.2 "><p id="p1623064263217"><a name="p1623064263217"></a><a name="p1623064263217"></a>PUT /v2.1/{project_id}/os-security-groups/{security_group_id}</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.7.1.3 "><p id="p6994165671416"><a name="p6994165671416"></a><a name="p6994165671416"></a>ecs:securityGroups:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.099999999999998%" headers="mcps1.1.7.1.4 "><p id="p13482135418146"><a name="p13482135418146"></a><a name="p13482135418146"></a>vpc:securityGroups:get</p>
<p id="p237517554146"><a name="p237517554146"></a><a name="p237517554146"></a>vpc:securityGroups:update</p>
</td>
<td class="cellrowborder" valign="top" width="11.43%" headers="mcps1.1.7.1.5 "><p id="p1948713617712"><a name="p1948713617712"></a><a name="p1948713617712"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.84%" headers="mcps1.1.7.1.6 "><p id="p5487153612718"><a name="p5487153612718"></a><a name="p5487153612718"></a>×</p>
</td>
</tr>
<tr id="row511081915302"><td class="cellrowborder" valign="top" width="13.87%" headers="mcps1.1.7.1.1 "><p id="p4229144218510"><a name="p4229144218510"></a><a name="p4229144218510"></a>查询指定云服务器安全组列表(OpenStack原生)</p>
</td>
<td class="cellrowborder" valign="top" width="27.76%" headers="mcps1.1.7.1.2 "><p id="p56631353123214"><a name="p56631353123214"></a><a name="p56631353123214"></a>GET /v2.1/{project_id}/servers/{server_id}/os-security-groups</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.7.1.3 "><p id="p19959184131512"><a name="p19959184131512"></a><a name="p19959184131512"></a>ecs:securityGroups:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.099999999999998%" headers="mcps1.1.7.1.4 "><p id="p121968321520"><a name="p121968321520"></a><a name="p121968321520"></a>vpc:securityGroups:get</p>
</td>
<td class="cellrowborder" valign="top" width="11.43%" headers="mcps1.1.7.1.5 "><p id="p15926937674"><a name="p15926937674"></a><a name="p15926937674"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.84%" headers="mcps1.1.7.1.6 "><p id="p292617371472"><a name="p292617371472"></a><a name="p292617371472"></a>×</p>
</td>
</tr>
<tr id="row41101119143010"><td class="cellrowborder" valign="top" width="13.87%" headers="mcps1.1.7.1.1 "><p id="p142294421653"><a name="p142294421653"></a><a name="p142294421653"></a>添加安全组（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.76%" headers="mcps1.1.7.1.2 "><p id="p99431459183215"><a name="p99431459183215"></a><a name="p99431459183215"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.7.1.3 "><p id="p12212151661516"><a name="p12212151661516"></a><a name="p12212151661516"></a>ecs:securityGroups:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.099999999999998%" headers="mcps1.1.7.1.4 "><p id="p680191091517"><a name="p680191091517"></a><a name="p680191091517"></a>ecs:servers:get</p>
<p id="p2543151118158"><a name="p2543151118158"></a><a name="p2543151118158"></a>vpc:securityGroups:get</p>
<p id="p18302101217151"><a name="p18302101217151"></a><a name="p18302101217151"></a>vpc:securityGroups:create</p>
<p id="p14281113121517"><a name="p14281113121517"></a><a name="p14281113121517"></a>vpc:securityGroups:update</p>
<p id="p83501143156"><a name="p83501143156"></a><a name="p83501143156"></a>vpc:ports:get</p>
<p id="p1868151581517"><a name="p1868151581517"></a><a name="p1868151581517"></a>vpc:ports:update</p>
</td>
<td class="cellrowborder" valign="top" width="11.43%" headers="mcps1.1.7.1.5 "><p id="p5251203914712"><a name="p5251203914712"></a><a name="p5251203914712"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.84%" headers="mcps1.1.7.1.6 "><p id="p92511439578"><a name="p92511439578"></a><a name="p92511439578"></a>×</p>
</td>
</tr>
<tr id="row51102019153019"><td class="cellrowborder" valign="top" width="13.87%" headers="mcps1.1.7.1.1 "><p id="p132291642757"><a name="p132291642757"></a><a name="p132291642757"></a>移除安全组（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="27.76%" headers="mcps1.1.7.1.2 "><p id="p54371318143319"><a name="p54371318143319"></a><a name="p54371318143319"></a>POST /v2.1/{project_id}/servers/{server_id}/action</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.1.7.1.3 "><p id="p104767306159"><a name="p104767306159"></a><a name="p104767306159"></a>ecs:securityGroups:use</p>
</td>
<td class="cellrowborder" valign="top" width="18.099999999999998%" headers="mcps1.1.7.1.4 "><p id="p1992882351510"><a name="p1992882351510"></a><a name="p1992882351510"></a>ecs:servers:get</p>
<p id="p1622124111517"><a name="p1622124111517"></a><a name="p1622124111517"></a>vpc:securityGroups:get</p>
<p id="p1827517255152"><a name="p1827517255152"></a><a name="p1827517255152"></a>vpc:securityGroups:delete</p>
<p id="p134085269151"><a name="p134085269151"></a><a name="p134085269151"></a>vpc:securityGroups:update</p>
<p id="p825722720154"><a name="p825722720154"></a><a name="p825722720154"></a>vpc:ports:get</p>
<p id="p040532810157"><a name="p040532810157"></a><a name="p040532810157"></a>vpc:ports:update</p>
</td>
<td class="cellrowborder" valign="top" width="11.43%" headers="mcps1.1.7.1.5 "><p id="p1420517411778"><a name="p1420517411778"></a><a name="p1420517411778"></a>√</p>
</td>
<td class="cellrowborder" valign="top" width="8.84%" headers="mcps1.1.7.1.6 "><p id="p1420512411172"><a name="p1420512411172"></a><a name="p1420512411172"></a>×</p>
</td>
</tr>
</tbody>
</table>

