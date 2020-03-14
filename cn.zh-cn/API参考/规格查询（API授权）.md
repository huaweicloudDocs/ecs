# 规格查询<a name="ZH-CN_TOPIC_0103071522"></a>

<a name="table12528123592919"></a>
<table><thead align="left"><tr id="row5528103512910"><th class="cellrowborder" valign="top" width="35.64356435643564%" id="mcps1.1.5.1.1"><p id="p3528935172915"><a name="p3528935172915"></a><a name="p3528935172915"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="23.762376237623762%" id="mcps1.1.5.1.2"><p id="p10605125713535"><a name="p10605125713535"></a><a name="p10605125713535"></a>API功能</p>
</th>
<th class="cellrowborder" valign="top" width="20.792079207920793%" id="mcps1.1.5.1.3"><p id="p19528153532917"><a name="p19528153532917"></a><a name="p19528153532917"></a>授权项</p>
</th>
<th class="cellrowborder" valign="top" width="19.801980198019802%" id="mcps1.1.5.1.4"><p id="p1726533114217"><a name="p1726533114217"></a><a name="p1726533114217"></a>授权项作用域</p>
</th>
</tr>
</thead>
<tbody><tr id="row1090113617259"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p8987111492511"><a name="p8987111492511"></a><a name="p8987111492511"></a>GET /v1/{project_id}/cloudservers/flavors</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.1.5.1.2 "><p id="p740144618428"><a name="p740144618428"></a><a name="p740144618428"></a>查询云服务器规格详情和扩展信息列表</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul2987171415255"></a><a name="ul2987171415255"></a><ul id="ul2987171415255"><li>ecs:cloudServerFlavors:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul93731813713"></a><a name="ul93731813713"></a><ul id="ul93731813713"><li>支持：</li></ul>
<p id="p33888131113"><a name="p33888131113"></a><a name="p33888131113"></a>项目(Project)</p>
<p id="p1338891314114"><a name="p1338891314114"></a><a name="p1338891314114"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row1750629135711"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p049813915572"><a name="p049813915572"></a><a name="p049813915572"></a>GET /v1/{project_id}/cloudservers/resize_flavors</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.1.5.1.2 "><p id="p104997917577"><a name="p104997917577"></a><a name="p104997917577"></a>查询云服务器规格变更支持列表</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul44991293574"></a><a name="ul44991293574"></a><ul id="ul44991293574"><li>ecs:cloudServers:list</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul174998913572"></a><a name="ul174998913572"></a><ul id="ul174998913572"><li>支持：</li></ul>
<p id="p154991692578"><a name="p154991692578"></a><a name="p154991692578"></a>项目(Project)</p>
<p id="p14499119185713"><a name="p14499119185713"></a><a name="p14499119185713"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
<tr id="row18168121715435"><td class="cellrowborder" valign="top" width="35.64356435643564%" headers="mcps1.1.5.1.1 "><p id="p99081131173310"><a name="p99081131173310"></a><a name="p99081131173310"></a>GET /v2.1/{project_id}/flavors/{flavors_id}/os-extra_specs</p>
</td>
<td class="cellrowborder" valign="top" width="23.762376237623762%" headers="mcps1.1.5.1.2 "><p id="p610062214316"><a name="p610062214316"></a><a name="p610062214316"></a>查询云服务器规格extra_specs的详情（OpenStack原生）</p>
</td>
<td class="cellrowborder" valign="top" width="20.792079207920793%" headers="mcps1.1.5.1.3 "><a name="ul71005222437"></a><a name="ul71005222437"></a><ul id="ul71005222437"><li>ecs:flavors:get</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.4 "><a name="ul11100132234316"></a><a name="ul11100132234316"></a><ul id="ul11100132234316"><li>支持：</li></ul>
<p id="p31007223436"><a name="p31007223436"></a><a name="p31007223436"></a>项目(Project)</p>
<p id="p41001622184319"><a name="p41001622184319"></a><a name="p41001622184319"></a></p>
<a name="ul1410052216433"></a><a name="ul1410052216433"></a><ul id="ul1410052216433"><li>不支持：</li></ul>
<p id="p410052254320"><a name="p410052254320"></a><a name="p410052254320"></a>企业项目(Enterprise Project)</p>
</td>
</tr>
</tbody>
</table>

