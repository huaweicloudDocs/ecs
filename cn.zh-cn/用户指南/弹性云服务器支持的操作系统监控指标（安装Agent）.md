# 弹性云服务器支持的操作系统监控指标（安装Agent）<a name="ecs_03_1003"></a>

## 功能说明<a name="section12784212213"></a>

操作系统监控目前支持监控的监控指标有：CPU相关监控项、CPU负载类相关监控项、内存相关监控项、磁盘相关监控项、磁盘I/O相关监控项、文件系统类相关监控项、GPU相关监控项、网卡类相关监控项。

安装Agent后，您便可以查看弹性云服务器的操作系统监控指标。指标采集周期是1分钟。

## 操作系统监控指标说明<a name="section47952021926"></a>

对于不同的操作系统、不同的弹性云服务器类型，在安装Agent后均默认支持查看以下监控指标。

**表 1**  CPU相关监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table7594115620353"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row95951556133512"><th class="cellrowborder" valign="top" width="12.11%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p19741153185914"><a name="zh-cn_topic_0084814075_p19741153185914"></a><a name="zh-cn_topic_0084814075_p19741153185914"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="10.879999999999999%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1255413283615"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1255413283615"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1255413283615"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="42.620000000000005%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105546320367"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105546320367"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105546320367"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="8.4%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_ecs_03_1002_p64622851222846"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_ecs_03_1002_p64622851222846"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_ecs_03_1002_p64622851222846"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="8.3%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1383633412472"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1383633412472"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1383633412472"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="17.69%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18780264718"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18780264718"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18780264718"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row8595175614350"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p19715195419502"><a name="zh-cn_topic_0084814075_p19715195419502"></a><a name="zh-cn_topic_0084814075_p19715195419502"></a>cpu_usage_idle</p>
</td>
<td class="cellrowborder" valign="top" width="10.879999999999999%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105451722015"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105451722015"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105451722015"></a>（Agent）CPU空闲时间占比</p>
</td>
<td class="cellrowborder" valign="top" width="42.620000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p65951856183515"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p65951856183515"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p65951856183515"></a>该指标用于统计测量对象当前CPU空闲时间占比。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1753993014112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1753993014112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1753993014112"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul7740114434813"></a><a name="zh-cn_topic_0084814075_ul7740114434813"></a><ul id="zh-cn_topic_0084814075_ul7740114434813"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出CPU空闲时间占比。</li><li>采集方式（Windows）：用户可以通过top命令查看 %Cpu(s) id值。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p66362622114851"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p66362622114851"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p66362622114851"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.3%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8836734164720"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8836734164720"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8836734164720"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p162174963816"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p162174963816"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p162174963816"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row923914003617"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p147151154185010"><a name="zh-cn_topic_0084814075_p147151154185010"></a><a name="zh-cn_topic_0084814075_p147151154185010"></a>cpu_usage_other</p>
</td>
<td class="cellrowborder" valign="top" width="10.879999999999999%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p54268533589"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p54268533589"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p54268533589"></a>（Agent）其他CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="42.620000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9639820102610"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9639820102610"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9639820102610"></a>该指标用于统计测量对象其他占用CPU使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p585238104117"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p585238104117"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p585238104117"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul16241613135214"></a><a name="zh-cn_topic_0084814075_ul16241613135214"></a><ul id="zh-cn_topic_0084814075_ul16241613135214"><li>采集方式（Linux）：其他CPU使用率=1- 空闲CPU使用率（%）- 内核空间CPU使用率- 用户空间CPU使用率。</li><li>采集方式（Windows）：其他CPU使用率=1- 空闲CPU使用率（%）- 内核空间CPU使用率- 用户空间CPU使用率。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15426165314587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15426165314587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15426165314587"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.3%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1122010114534"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1122010114534"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1122010114534"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p112201411534"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p112201411534"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p112201411534"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1131810217360"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p87152544508"><a name="zh-cn_topic_0084814075_p87152544508"></a><a name="zh-cn_topic_0084814075_p87152544508"></a>cpu_usage_system</p>
</td>
<td class="cellrowborder" valign="top" width="10.879999999999999%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1542695395811"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1542695395811"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1542695395811"></a>（Agent）内核空间CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="42.620000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p155571638114119"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p155571638114119"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p155571638114119"></a>该指标用于统计测量对象当前内核空间占用CPU使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p169312431410"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p169312431410"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p169312431410"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul1247713472532"></a><a name="zh-cn_topic_0084814075_ul1247713472532"></a><ul id="zh-cn_topic_0084814075_ul1247713472532"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出内核空间CPU使用率。用户可以通过top命令查看 %Cpu(s) sy值。</li><li>采集方式（Windows）：通过WindowsAPI GetSystemTimes获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p342625305816"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p342625305816"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p342625305816"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.3%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1972422185320"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1972422185320"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1972422185320"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p57246216537"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p57246216537"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p57246216537"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1359545615355"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p187167549502"><a name="zh-cn_topic_0084814075_p187167549502"></a><a name="zh-cn_topic_0084814075_p187167549502"></a>cpu_usage_user</p>
</td>
<td class="cellrowborder" valign="top" width="10.879999999999999%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p66305567595"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p66305567595"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p66305567595"></a>（Agent）用户空间CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="42.620000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17595205633516"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17595205633516"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17595205633516"></a>该指标用于统计测量对象当前用户空间占用CPU使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2911184934116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2911184934116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2911184934116"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul6832185145410"></a><a name="zh-cn_topic_0084814075_ul6832185145410"></a><ul id="zh-cn_topic_0084814075_ul6832185145410"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出cpu使用率。用户可以通过top命令查看 %Cpu(s) us值。</li><li>采集方式（Windows）：通过WindowsAPI GetSystemTimes获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1663011568590"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1663011568590"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1663011568590"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.3%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p138729305317"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p138729305317"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p138729305317"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1687283175316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1687283175316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1687283175316"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row830162618574"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p371655465019"><a name="zh-cn_topic_0084814075_p371655465019"></a><a name="zh-cn_topic_0084814075_p371655465019"></a>cpu_usage</p>
</td>
<td class="cellrowborder" valign="top" width="10.879999999999999%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p092415835715"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p092415835715"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p092415835715"></a>（Agent）CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="42.620000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11924165815571"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11924165815571"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11924165815571"></a>该指标用于统计测量对象当前CPU使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199155719415"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199155719415"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199155719415"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul428752335411"></a><a name="zh-cn_topic_0084814075_ul428752335411"></a><ul id="zh-cn_topic_0084814075_ul428752335411"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出cpu使用率。用户可以通过top命令查看 %Cpu(s)值。</li><li>采集方式（Windows）：通过WindowsAPI GetSystemTimes获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8924205815579"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8924205815579"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8924205815579"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.3%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p142577565319"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p142577565319"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p142577565319"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p82577519535"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p82577519535"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p82577519535"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row5771145493710"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p671625425010"><a name="zh-cn_topic_0084814075_p671625425010"></a><a name="zh-cn_topic_0084814075_p671625425010"></a>cpu_usage_nice</p>
</td>
<td class="cellrowborder" valign="top" width="10.879999999999999%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18338192592712"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18338192592712"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18338192592712"></a>（Agent）Nice进程CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="42.620000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14357142313313"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14357142313313"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14357142313313"></a>该指标用于统计测量对象当前Nice进程CPU使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13802312422"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13802312422"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13802312422"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul31531140105416"></a><a name="zh-cn_topic_0084814075_ul31531140105416"></a><ul id="zh-cn_topic_0084814075_ul31531140105416"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出Nice进程CPU使用率。用户可以通过top命令查看 %Cpu(s) ni值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p49111420104116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p49111420104116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p49111420104116"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.3%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19489869535"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19489869535"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19489869535"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p134891645315"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p134891645315"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p134891645315"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1347919118387"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1171720549502"><a name="zh-cn_topic_0084814075_p1171720549502"></a><a name="zh-cn_topic_0084814075_p1171720549502"></a>cpu_usage_iowait</p>
</td>
<td class="cellrowborder" valign="top" width="10.879999999999999%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12309132815275"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12309132815275"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12309132815275"></a>（Agent）iowait状态占比</p>
</td>
<td class="cellrowborder" valign="top" width="42.620000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p5358182363312"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p5358182363312"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p5358182363312"></a>该指标用于统计测量对象当前iowait状态占用CPU的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13110915425"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13110915425"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13110915425"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul6110655175410"></a><a name="zh-cn_topic_0084814075_ul6110655175410"></a><ul id="zh-cn_topic_0084814075_ul6110655175410"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出iowait状态占比。用户可以通过top命令查看 %Cpu(s) wa值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35911215413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35911215413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35911215413"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.3%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p129676775315"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p129676775315"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p129676775315"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199671971537"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199671971537"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199671971537"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1585742117387"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p5717175415018"><a name="zh-cn_topic_0084814075_p5717175415018"></a><a name="zh-cn_topic_0084814075_p5717175415018"></a>cpu_usage_irq</p>
</td>
<td class="cellrowborder" valign="top" width="10.879999999999999%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p0789035152712"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p0789035152712"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p0789035152712"></a>（Agent）CPU中断时间占比</p>
</td>
<td class="cellrowborder" valign="top" width="42.620000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1358182311339"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1358182311339"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1358182311339"></a>该指标用于统计测量对象当前CPU处理中断用时占用CPU时间的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1847811754216"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1847811754216"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1847811754216"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul161211982552"></a><a name="zh-cn_topic_0084814075_ul161211982552"></a><ul id="zh-cn_topic_0084814075_ul161211982552"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出CPU中断时间占比。用户可以通过top命令查看 %Cpu(s) hi值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p185392264112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p185392264112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p185392264112"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.3%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p73370965316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p73370965316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p73370965316"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15337159155313"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15337159155313"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15337159155313"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row122701957103711"><td class="cellrowborder" valign="top" width="12.11%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p12742163205912"><a name="zh-cn_topic_0084814075_p12742163205912"></a><a name="zh-cn_topic_0084814075_p12742163205912"></a>cpu_usage_softirq</p>
</td>
<td class="cellrowborder" valign="top" width="10.879999999999999%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p103301332413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p103301332413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p103301332413"></a>（Agent）CPU软中断时间占比</p>
</td>
<td class="cellrowborder" valign="top" width="42.620000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p335819233334"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p335819233334"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p335819233334"></a>该指标用于统计测量对象当前CPU处理软中断时间占用CPU时间的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13161162444214"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13161162444214"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13161162444214"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul1435116242555"></a><a name="zh-cn_topic_0084814075_ul1435116242555"></a><ul id="zh-cn_topic_0084814075_ul1435116242555"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出CPU软中断时间占比。用户可以通过top命令查看 %Cpu(s) si值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.4%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12645622184110"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12645622184110"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12645622184110"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.3%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1699416915530"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1699416915530"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1699416915530"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p999416915313"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p999416915313"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p999416915313"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 2**  CPU负载指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table059418341885"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row56003341289"><th class="cellrowborder" valign="top" width="12.111211121112111%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p236911231700"><a name="zh-cn_topic_0084814075_p236911231700"></a><a name="zh-cn_topic_0084814075_p236911231700"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="10.64106410641064%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11601634589"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11601634589"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11601634589"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="42.9042904290429%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46035341782"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46035341782"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46035341782"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="8.430843084308432%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p156041834186"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p156041834186"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p156041834186"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="8.48084808480848%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46051534285"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46051534285"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46051534285"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="17.431743174317432%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p561016344817"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p561016344817"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p561016344817"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1761212343810"><td class="cellrowborder" valign="top" width="12.111211121112111%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1071885419506"><a name="zh-cn_topic_0084814075_p1071885419506"></a><a name="zh-cn_topic_0084814075_p1071885419506"></a>load_average1</p>
</td>
<td class="cellrowborder" valign="top" width="10.64106410641064%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850194611018"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850194611018"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850194611018"></a>（Agent） 1分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="42.9042904290429%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7357107220"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7357107220"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7357107220"></a>该指标用于统计测量对象过去1分钟的CPU平均负载。</p>
<p id="zh-cn_topic_0084814075_p2297112311714"><a name="zh-cn_topic_0084814075_p2297112311714"></a><a name="zh-cn_topic_0084814075_p2297112311714"></a>采集方式（Linux）：通过/proc/loadavg中load1/逻辑CPU个数得到。用户可以通过top命令查看load1值。</p>
</td>
<td class="cellrowborder" valign="top" width="8.430843084308432%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198778139214"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198778139214"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198778139214"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="8.48084808480848%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13618634485"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13618634485"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13618634485"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.431743174317432%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9310913195413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9310913195413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9310913195413"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row46221234681"><td class="cellrowborder" valign="top" width="12.111211121112111%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p171811549508"><a name="zh-cn_topic_0084814075_p171811549508"></a><a name="zh-cn_topic_0084814075_p171811549508"></a>load_average5</p>
</td>
<td class="cellrowborder" valign="top" width="10.64106410641064%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12509461401"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12509461401"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12509461401"></a>（Agent） 5分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="42.9042904290429%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p193579719219"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p193579719219"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p193579719219"></a>该指标用于统计测量对象过去5分钟的CPU平均负载。</p>
<p id="zh-cn_topic_0084814075_p1134824691718"><a name="zh-cn_topic_0084814075_p1134824691718"></a><a name="zh-cn_topic_0084814075_p1134824691718"></a>采集方式（Linux）：通过/proc/loadavg中load5/逻辑CPU个数得到。用户可以通过top命令查看load5值。</p>
</td>
<td class="cellrowborder" valign="top" width="8.430843084308432%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1387714135216"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1387714135216"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1387714135216"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="8.48084808480848%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p196291341812"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p196291341812"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p196291341812"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.431743174317432%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p344582715413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p344582715413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p344582715413"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row106321341682"><td class="cellrowborder" valign="top" width="12.111211121112111%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p19718125419505"><a name="zh-cn_topic_0084814075_p19718125419505"></a><a name="zh-cn_topic_0084814075_p19718125419505"></a>load_average15</p>
</td>
<td class="cellrowborder" valign="top" width="10.64106410641064%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850104612013"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850104612013"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850104612013"></a>（Agent） 15分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="42.9042904290429%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p43571971429"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p43571971429"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p43571971429"></a>该指标用于统计测量对象过去15分钟的CPU平均负载。</p>
<p id="zh-cn_topic_0084814075_p540374831716"><a name="zh-cn_topic_0084814075_p540374831716"></a><a name="zh-cn_topic_0084814075_p540374831716"></a>采集方式（Linux）：通过/proc/loadavg中load15/逻辑CPU个数得到。用户可以通过top命令查看load15值。</p>
</td>
<td class="cellrowborder" valign="top" width="8.430843084308432%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p148771134213"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p148771134213"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p148771134213"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="8.48084808480848%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p663818341587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p663818341587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p663818341587"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.431743174317432%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81142810545"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81142810545"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81142810545"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>Windows系统暂不支持CPU负载指标。

**表 3**  内存相关监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table181485064217"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row2081514503427"><th class="cellrowborder" valign="top" width="11.53%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p492517502010"><a name="zh-cn_topic_0084814075_p492517502010"></a><a name="zh-cn_topic_0084814075_p492517502010"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="13.62%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35662062433"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35662062433"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35662062433"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="41.32%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125671366437"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125671366437"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125671366437"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="9.030000000000001%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1993419755115"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1993419755115"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1993419755115"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="8.110000000000001%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1993403575518"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1993403575518"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1993403575518"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.39%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p209051331165514"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p209051331165514"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p209051331165514"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row28151450174217"><td class="cellrowborder" valign="top" width="11.53%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p117181154185013"><a name="zh-cn_topic_0084814075_p117181154185013"></a><a name="zh-cn_topic_0084814075_p117181154185013"></a>mem_available</p>
</td>
<td class="cellrowborder" valign="top" width="13.62%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13426653115813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13426653115813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13426653115813"></a>（Agent）可用内存</p>
</td>
<td class="cellrowborder" valign="top" width="41.32%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2659105264319"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2659105264319"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2659105264319"></a>该指标用于统计测量对象的可用内存。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p319812463425"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p319812463425"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p319812463425"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul178711134191"></a><a name="zh-cn_topic_0084814075_ul178711134191"></a><ul id="zh-cn_topic_0084814075_ul178711134191"><li>采集方式（Linux）：通过/proc/meminfo得到MemAvailable;若/proc/meminfo中不显示MemAvailable，则MemAvailable=MemFree+Buffers+Cached</li><li>采集方式（Windows）：计算方法为（内存总量-已用内存量）。通过WindowsAPI GlobalMemoryStatusEx获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.030000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6815650164213"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6815650164213"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6815650164213"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="8.110000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1793493512550"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1793493512550"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1793493512550"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.39%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2905183165513"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2905183165513"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2905183165513"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1881555015426"><td class="cellrowborder" valign="top" width="11.53%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p10719654105010"><a name="zh-cn_topic_0084814075_p10719654105010"></a><a name="zh-cn_topic_0084814075_p10719654105010"></a>mem_usedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="13.62%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7426953195818"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7426953195818"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7426953195818"></a>（Agent）内存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="41.32%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p56603522431"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p56603522431"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p56603522431"></a>该指标用于统计测量对象的内存使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1271515216422"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1271515216422"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1271515216422"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul15740448151918"></a><a name="zh-cn_topic_0084814075_ul15740448151918"></a><ul id="zh-cn_topic_0084814075_ul15740448151918"><li>采集方式（Linux）：通过/proc/meminfo文件获取,(MemTotal-MemAvailable)/MemTotal</li><li>采集方式（Windows）：计算方法为（ 已用内存量/内存总量*100%）。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.030000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p168151550164215"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p168151550164215"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p168151550164215"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.110000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p20313183255619"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p20313183255619"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p20313183255619"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.39%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p53139328567"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p53139328567"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p53139328567"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row17755151194213"><td class="cellrowborder" valign="top" width="11.53%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p571975405014"><a name="zh-cn_topic_0084814075_p571975405014"></a><a name="zh-cn_topic_0084814075_p571975405014"></a>mem_free</p>
</td>
<td class="cellrowborder" valign="top" width="13.62%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13461198162815"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13461198162815"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13461198162815"></a>（Agent）空闲内存量</p>
</td>
<td class="cellrowborder" valign="top" width="41.32%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p446198172813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p446198172813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p446198172813"></a>该指标用于统计测量对象的空闲内存量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3971074432"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3971074432"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3971074432"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul11951452161911"></a><a name="zh-cn_topic_0084814075_ul11951452161911"></a><ul id="zh-cn_topic_0084814075_ul11951452161911"><li>采集方式（Linux）：通过/proc/meminfo获取。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.030000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1646188112819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1646188112819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1646188112819"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="8.110000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4592183317560"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4592183317560"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4592183317560"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.39%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1559293395618"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1559293395618"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1559293395618"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row32411149194211"><td class="cellrowborder" valign="top" width="11.53%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p8719165419505"><a name="zh-cn_topic_0084814075_p8719165419505"></a><a name="zh-cn_topic_0084814075_p8719165419505"></a>mem_buffers</p>
</td>
<td class="cellrowborder" valign="top" width="13.62%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1097541222813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1097541222813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1097541222813"></a>（Agent）Buffers占用量</p>
</td>
<td class="cellrowborder" valign="top" width="41.32%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1491524514516"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1491524514516"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1491524514516"></a>该指标用于统计测量对象的Buffers内存量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1637141311439"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1637141311439"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1637141311439"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul1383115415196"></a><a name="zh-cn_topic_0084814075_ul1383115415196"></a><ul id="zh-cn_topic_0084814075_ul1383115415196"><li>采集方式（Linux）：通过/proc/meminfo获取。用户可以通过top命令查看 KiB Mem:buffers值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.030000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1975131212815"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1975131212815"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1975131212815"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="8.110000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188323414561"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188323414561"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188323414561"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.39%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10883183419560"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10883183419560"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10883183419560"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row148195464215"><td class="cellrowborder" valign="top" width="11.53%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p592575011019"><a name="zh-cn_topic_0084814075_p592575011019"></a><a name="zh-cn_topic_0084814075_p592575011019"></a>mem_cached</p>
</td>
<td class="cellrowborder" valign="top" width="13.62%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1996519532814"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1996519532814"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1996519532814"></a>（Agent）Cache占用量</p>
</td>
<td class="cellrowborder" valign="top" width="41.32%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15966946124515"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15966946124515"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15966946124515"></a>该指标用于统计测量对象Cache内存量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p411621174316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p411621174316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p411621174316"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul63235715193"></a><a name="zh-cn_topic_0084814075_ul63235715193"></a><ul id="zh-cn_topic_0084814075_ul63235715193"><li>采集方式（Linux）：通过/proc/meminfo获取。用户可以通过top命令查看 KiB Swap:cached Mem值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.030000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p296519522819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p296519522819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p296519522819"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="8.110000000000001%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1614173512563"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1614173512563"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1614173512563"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.39%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1961433555618"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1961433555618"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1961433555618"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 4**  磁盘相关监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table2050841310455"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row250917130458"><th class="cellrowborder" valign="top" width="11.991199119911991%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p126095471215"><a name="zh-cn_topic_0084814075_p126095471215"></a><a name="zh-cn_topic_0084814075_p126095471215"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="12.55125512551255%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13757487454"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13757487454"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13757487454"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="42.12421242124212%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p47794817458"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p47794817458"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p47794817458"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="8.73087308730873%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17186610175111"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17186610175111"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17186610175111"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="8.3008300830083%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81307820578"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81307820578"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81307820578"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.301630163016302%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p21306815714"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p21306815714"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p21306815714"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row650913134455"><td class="cellrowborder" valign="top" width="11.991199119911991%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p10720854195015"><a name="zh-cn_topic_0084814075_p10720854195015"></a><a name="zh-cn_topic_0084814075_p10720854195015"></a>mountPointPrefix_disk_free</p>
</td>
<td class="cellrowborder" valign="top" width="12.55125512551255%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11426145312588"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11426145312588"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11426145312588"></a>（Agent）磁盘剩余存储量</p>
</td>
<td class="cellrowborder" valign="top" width="42.12421242124212%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p116982408478"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p116982408478"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p116982408478"></a>该指标用于统计测量对象磁盘的剩余存储空间。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p364185016435"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p364185016435"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p364185016435"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul1836810491232"></a><a name="zh-cn_topic_0084814075_ul1836810491232"></a><ul id="zh-cn_topic_0084814075_ul1836810491232"><li>采集方式（Linux）：执行df -h命令，查看Avail列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>采集方式（Windows）：使用WMI接口GetDiskFreeSpaceExW获取磁盘空间数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.73087308730873%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p194261653135820"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p194261653135820"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p194261653135820"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="8.3008300830083%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4938131119577"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4938131119577"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4938131119577"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.301630163016302%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1093851113572"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1093851113572"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1093851113572"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row75091135457"><td class="cellrowborder" valign="top" width="11.991199119911991%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p5721155418501"><a name="zh-cn_topic_0084814075_p5721155418501"></a><a name="zh-cn_topic_0084814075_p5721155418501"></a>mountPointPrefix_disk_total</p>
</td>
<td class="cellrowborder" valign="top" width="12.55125512551255%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1775111613310"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1775111613310"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1775111613310"></a>（Agent）磁盘存储总量</p>
</td>
<td class="cellrowborder" valign="top" width="42.12421242124212%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18426105319582"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18426105319582"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18426105319582"></a>该指标用于统计测量对象磁盘存储总量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3181456184316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3181456184316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3181456184316"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul22892410242"></a><a name="zh-cn_topic_0084814075_ul22892410242"></a><ul id="zh-cn_topic_0084814075_ul22892410242"><li>采集方式（Linux）：执行df -h命令，查看Size列数据。<p id="zh-cn_topic_0084814075_p5341629122612"><a name="zh-cn_topic_0084814075_p5341629122612"></a><a name="zh-cn_topic_0084814075_p5341629122612"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：使用WMI接口GetDiskFreeSpaceExW获取磁盘空间数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.73087308730873%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1057313810816"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1057313810816"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1057313810816"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="8.3008300830083%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p631511310574"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p631511310574"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p631511310574"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.301630163016302%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8315131319579"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8315131319579"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8315131319579"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row95094134450"><td class="cellrowborder" valign="top" width="11.991199119911991%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p19721165445019"><a name="zh-cn_topic_0084814075_p19721165445019"></a><a name="zh-cn_topic_0084814075_p19721165445019"></a>mountPointPrefix_disk_used</p>
</td>
<td class="cellrowborder" valign="top" width="12.55125512551255%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p34202178311"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p34202178311"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p34202178311"></a>（Agent）磁盘已用存量</p>
</td>
<td class="cellrowborder" valign="top" width="42.12421242124212%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p167462537593"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p167462537593"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p167462537593"></a>该指标用于统计测量对象磁盘的已用存储空间。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p25641849446"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p25641849446"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p25641849446"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul032356132415"></a><a name="zh-cn_topic_0084814075_ul032356132415"></a><ul id="zh-cn_topic_0084814075_ul032356132415"><li>采集方式（Linux）：执行df -h命令，查看Used列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>采集方式（Windows）：使用WMI接口GetDiskFreeSpaceExW获取磁盘空间数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.73087308730873%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13509440124615"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13509440124615"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13509440124615"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="8.3008300830083%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5014143578"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5014143578"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5014143578"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.301630163016302%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p160201485719"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p160201485719"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p160201485719"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1050951394510"><td class="cellrowborder" valign="top" width="11.991199119911991%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p572216546508"><a name="zh-cn_topic_0084814075_p572216546508"></a><a name="zh-cn_topic_0084814075_p572216546508"></a>mountPointPrefix_disk_usedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="12.55125512551255%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105111318631"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105111318631"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105111318631"></a>（Agent）磁盘使用率</p>
</td>
<td class="cellrowborder" valign="top" width="42.12421242124212%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p64261535585"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p64261535585"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p64261535585"></a>该指标用于统计测量对象磁盘使用率，以百分比为单位。计算方式为: 磁盘已用存储量/磁盘存储总量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14423171814449"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14423171814449"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14423171814449"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul098197247"></a><a name="zh-cn_topic_0084814075_ul098197247"></a><ul id="zh-cn_topic_0084814075_ul098197247"><li>采集方式（Linux）：通过计算Used/Size得出。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>采集方式（Windows）：使用WMI接口GetDiskFreeSpaceExW获取磁盘空间数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.73087308730873%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p94261253205813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p94261253205813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p94261253205813"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.3008300830083%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p16166715155711"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p16166715155711"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p16166715155711"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.301630163016302%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3166191516578"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3166191516578"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3166191516578"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 5**  磁盘I/O相关监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table35183543283"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row953775472814"><th class="cellrowborder" valign="top" width="11.64%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p1175211451217"><a name="zh-cn_topic_0084814075_p1175211451217"></a><a name="zh-cn_topic_0084814075_p1175211451217"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="12.94%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p45421054192813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p45421054192813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p45421054192813"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="42.39%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18546175412289"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18546175412289"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18546175412289"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="8.64%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1549175452814"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1549175452814"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1549175452814"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="7.86%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1175214128581"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1175214128581"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1175214128581"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="16.53%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1475220121587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1475220121587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1475220121587"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row13734554112815"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p117251254185016"><a name="zh-cn_topic_0084814075_p117251254185016"></a><a name="zh-cn_topic_0084814075_p117251254185016"></a>mountPointPrefix_disk_agt_read_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15737185472818"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15737185472818"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15737185472818"></a>（Agent）磁盘读速率</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p20741205422814"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p20741205422814"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p20741205422814"></a>该指标用于统计每秒从测量对象读出数据量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p782163415446"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p782163415446"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p782163415446"></a>单位：byte/s</p>
<a name="zh-cn_topic_0084814075_ul91083169316"></a><a name="zh-cn_topic_0084814075_ul91083169316"></a><ul id="zh-cn_topic_0084814075_ul91083169316"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p9613124165112"><a name="zh-cn_topic_0084814075_p9613124165112"></a><a name="zh-cn_topic_0084814075_p9613124165112"></a>通过计算采集周期内/proc/diskstats中对应设备第六列数据的变化得出磁盘读速率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188071658143519"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188071658143519"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188071658143519"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：<a name="zh-cn_topic_0084814075_ul159131398347"></a><a name="zh-cn_topic_0084814075_ul159131398347"></a><ul id="zh-cn_topic_0084814075_ul159131398347"><li>使用WMI中Win32_PerfFormattedData_PerfDisk_LogicalDisk对象获取磁盘I/O数据。</li><li>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>高CPU情况下存在获取超时的现象，会导致无法获取监控数据。</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p974485419280"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p974485419280"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p974485419280"></a>≥ 0 bytes/s</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2752612105816"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2752612105816"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2752612105816"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p147521812115810"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p147521812115810"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p147521812115810"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row47721654152813"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p197258544505"><a name="zh-cn_topic_0084814075_p197258544505"></a><a name="zh-cn_topic_0084814075_p197258544505"></a>mountPointPrefix_disk_agt_read_requests_rate</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p677775412818"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p677775412818"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p677775412818"></a>（Agent）磁盘读操作速率</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p107805542289"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p107805542289"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p107805542289"></a>该指标用于统计每秒从测量对象读取数据的请求次数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1044113915445"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1044113915445"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1044113915445"></a>单位：请求/秒</p>
<a name="zh-cn_topic_0084814075_ul499512533117"></a><a name="zh-cn_topic_0084814075_ul499512533117"></a><ul id="zh-cn_topic_0084814075_ul499512533117"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p838794495115"><a name="zh-cn_topic_0084814075_p838794495115"></a><a name="zh-cn_topic_0084814075_p838794495115"></a>通过计算采集周期内/proc/diskstats中对应设备第四列数据的变化得出磁盘读操作速率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9794308367"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9794308367"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9794308367"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：<a name="zh-cn_topic_0084814075_ul1079485110345"></a><a name="zh-cn_topic_0084814075_ul1079485110345"></a><ul id="zh-cn_topic_0084814075_ul1079485110345"><li>使用WMI中Win32_PerfFormattedData_PerfDisk_LogicalDisk对象获取磁盘I/O数据。</li><li>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>高CPU情况下存在获取超时的现象，会导致无法获取监控数据。</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1778413542289"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1778413542289"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1778413542289"></a>≥ 0 Requests/s</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p952613171583"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p952613171583"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p952613171583"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1852618177589"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1852618177589"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1852618177589"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row10814954112817"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p14726854145017"><a name="zh-cn_topic_0084814075_p14726854145017"></a><a name="zh-cn_topic_0084814075_p14726854145017"></a>mountPointPrefix_disk_agt_write_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17817554182816"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17817554182816"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17817554182816"></a>（Agent）磁盘写速率</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2822195462819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2822195462819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2822195462819"></a>该指标用于统计每秒写到测量对象的数据量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1935811508444"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1935811508444"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1935811508444"></a>单位：byte/s</p>
<a name="zh-cn_topic_0084814075_ul14619526183113"></a><a name="zh-cn_topic_0084814075_ul14619526183113"></a><ul id="zh-cn_topic_0084814075_ul14619526183113"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p4595144810511"><a name="zh-cn_topic_0084814075_p4595144810511"></a><a name="zh-cn_topic_0084814075_p4595144810511"></a>通过计算采集周期内/proc/diskstats中对应设备第十列数据的变化得出磁盘写速率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p26213763615"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p26213763615"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p26213763615"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：<a name="zh-cn_topic_0084814075_ul13419557193415"></a><a name="zh-cn_topic_0084814075_ul13419557193415"></a><ul id="zh-cn_topic_0084814075_ul13419557193415"><li>使用WMI中Win32_PerfFormattedData_PerfDisk_LogicalDisk对象获取磁盘I/O数据。</li><li>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>高CPU情况下存在获取超时的现象，会导致无法获取监控数据。</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p118255544285"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p118255544285"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p118255544285"></a>≥ 0 bytes/s</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p7487618135810"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p7487618135810"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p7487618135810"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1248714187586"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1248714187586"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1248714187586"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1285235420281"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p15726195413502"><a name="zh-cn_topic_0084814075_p15726195413502"></a><a name="zh-cn_topic_0084814075_p15726195413502"></a>mountPointPrefix_disk_agt_write_requests_rate</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p985616542281"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p985616542281"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p985616542281"></a>（Agent）磁盘写操作速率</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3859105420283"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3859105420283"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3859105420283"></a>该指标用于统计每秒向测量对象写数据的请求次数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8945842145517"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8945842145517"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8945842145517"></a>单位：请求/秒</p>
<a name="zh-cn_topic_0084814075_ul83511528173115"></a><a name="zh-cn_topic_0084814075_ul83511528173115"></a><ul id="zh-cn_topic_0084814075_ul83511528173115"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p1054795119518"><a name="zh-cn_topic_0084814075_p1054795119518"></a><a name="zh-cn_topic_0084814075_p1054795119518"></a>通过计算采集周期内/proc/diskstats中对应设备第八列数据的变化得出磁盘写操作速率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2413945123613"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2413945123613"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2413945123613"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：<a name="zh-cn_topic_0084814075_ul109514211357"></a><a name="zh-cn_topic_0084814075_ul109514211357"></a><ul id="zh-cn_topic_0084814075_ul109514211357"><li>使用WMI中Win32_PerfFormattedData_PerfDisk_LogicalDisk对象获取磁盘I/O数据。</li><li>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>高CPU情况下存在获取超时的现象，会导致无法获取监控数据。</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6863125414286"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6863125414286"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6863125414286"></a>≥ 0 Requests/s</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p121371320125819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p121371320125819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p121371320125819"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p31371420205819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p31371420205819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p31371420205819"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row3526538307"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p3727135416503"><a name="zh-cn_topic_0084814075_p3727135416503"></a><a name="zh-cn_topic_0084814075_p3727135416503"></a>disk_readTime</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1888124844819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1888124844819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1888124844819"></a>（Agent）读操作平均耗时</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15890164812481"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15890164812481"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15890164812481"></a>该指标用于统计测量对象磁盘读操作平均耗时。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3665195675519"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3665195675519"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3665195675519"></a>单位：ms/count</p>
<a name="zh-cn_topic_0084814075_ul102521430153119"></a><a name="zh-cn_topic_0084814075_ul102521430153119"></a><ul id="zh-cn_topic_0084814075_ul102521430153119"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p17419165475115"><a name="zh-cn_topic_0084814075_p17419165475115"></a><a name="zh-cn_topic_0084814075_p17419165475115"></a>通过计算采集周期内/proc/diskstats中对应设备第七列数据的变化得出磁盘读操作平均耗时。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9405754103611"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9405754103611"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9405754103611"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p761943410503"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p761943410503"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p761943410503"></a>≥ 0 ms/count</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p147211621135814"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p147211621135814"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p147211621135814"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p172182118586"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p172182118586"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p172182118586"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1271463304"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p672711548501"><a name="zh-cn_topic_0084814075_p672711548501"></a><a name="zh-cn_topic_0084814075_p672711548501"></a>disk_writeTime</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p48901848154819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p48901848154819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p48901848154819"></a>（Agent）写操作平均耗时</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2890104810484"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2890104810484"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2890104810484"></a>该指标用于统计测量对象磁盘写操作平均耗时。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p169767319562"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p169767319562"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p169767319562"></a>单位：ms/count</p>
<a name="zh-cn_topic_0084814075_ul48044353318"></a><a name="zh-cn_topic_0084814075_ul48044353318"></a><ul id="zh-cn_topic_0084814075_ul48044353318"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p1851410568512"><a name="zh-cn_topic_0084814075_p1851410568512"></a><a name="zh-cn_topic_0084814075_p1851410568512"></a>通过计算采集周期内/proc/diskstats中对应设备第十一列数据的变化得出磁盘写操作平均耗时。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p148401021372"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p148401021372"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p148401021372"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p166190349509"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p166190349509"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p166190349509"></a>≥ 0 ms/count</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1173672219581"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1173672219581"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1173672219581"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4736922145813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4736922145813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4736922145813"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row87124813010"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p57524451528"><a name="zh-cn_topic_0084814075_p57524451528"></a><a name="zh-cn_topic_0084814075_p57524451528"></a>disk_ioUtils</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198904485488"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198904485488"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198904485488"></a>（Agent）磁盘I/O使用率</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6204818503"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6204818503"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6204818503"></a>该指标用于统计测量对象磁盘I/O使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15507131035617"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15507131035617"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15507131035617"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul125541937123112"></a><a name="zh-cn_topic_0084814075_ul125541937123112"></a><ul id="zh-cn_topic_0084814075_ul125541937123112"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p186291818135219"><a name="zh-cn_topic_0084814075_p186291818135219"></a><a name="zh-cn_topic_0084814075_p186291818135219"></a>通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化得出磁盘I/O使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p477581114379"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p477581114379"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p477581114379"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1761915344507"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1761915344507"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1761915344507"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p745512515589"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p745512515589"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p745512515589"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1645517259587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1645517259587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1645517259587"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row1430742210414"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1872235410504"><a name="zh-cn_topic_0084814075_p1872235410504"></a><a name="zh-cn_topic_0084814075_p1872235410504"></a>disk_queue_length</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1222693718413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1222693718413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1222693718413"></a>（Agent）平均队列长度</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52311737154114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52311737154114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52311737154114"></a>该指标用于统计指定时间段内，平均等待完成的读取或写入操作请求的数量</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823173704120"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823173704120"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823173704120"></a>单位：个</p>
<a name="zh-cn_topic_0084814075_ul1178004023114"></a><a name="zh-cn_topic_0084814075_ul1178004023114"></a><ul id="zh-cn_topic_0084814075_ul1178004023114"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p776352085214"><a name="zh-cn_topic_0084814075_p776352085214"></a><a name="zh-cn_topic_0084814075_p776352085214"></a>通过计算采集周期内/proc/diskstats中对应设备第十四列数据的变化得出磁盘平均队列长度。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p813441910376"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p813441910376"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p813441910376"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823618378417"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823618378417"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823618378417"></a>≥ 0 Counts</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p151723273587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p151723273587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p151723273587"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p121721127145817"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p121721127145817"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p121721127145817"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row599132484116"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p14723175455019"><a name="zh-cn_topic_0084814075_p14723175455019"></a><a name="zh-cn_topic_0084814075_p14723175455019"></a>disk_write_bytes_per_operation</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6262173714416"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6262173714416"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6262173714416"></a>（Agent）平均写操作大小</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p122701037104116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p122701037104116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p122701037104116"></a>该指标用于统计指定时间段内，平均每个写I/O操作传输的字节数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p627315376415"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p627315376415"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p627315376415"></a>单位：byte/op</p>
<a name="zh-cn_topic_0084814075_ul1734274483111"></a><a name="zh-cn_topic_0084814075_ul1734274483111"></a><ul id="zh-cn_topic_0084814075_ul1734274483111"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p1222162495215"><a name="zh-cn_topic_0084814075_p1222162495215"></a><a name="zh-cn_topic_0084814075_p1222162495215"></a>通过计算采集周期内/proc/diskstats中对应设备第十列数据的变化与第八列数据的变化相除得出磁盘平均写操作大小。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p347420279373"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p347420279373"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p347420279373"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p527813774116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p527813774116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p527813774116"></a>≥ 0 ms/op</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p172414288587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p172414288587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p172414288587"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2024152885820"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2024152885820"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2024152885820"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row1475812710414"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p15723254175018"><a name="zh-cn_topic_0084814075_p15723254175018"></a><a name="zh-cn_topic_0084814075_p15723254175018"></a>disk_read_bytes_per_operation</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6301237144116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6301237144116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6301237144116"></a>（Agent）平均读操作大小</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p63051537174111"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p63051537174111"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p63051537174111"></a>该指标用于统计指定时间段内，平均每个读I/O操作传输的字节数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11308203711410"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11308203711410"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11308203711410"></a>单位：byte/op</p>
<a name="zh-cn_topic_0084814075_ul118664451315"></a><a name="zh-cn_topic_0084814075_ul118664451315"></a><ul id="zh-cn_topic_0084814075_ul118664451315"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p1421517295528"><a name="zh-cn_topic_0084814075_p1421517295528"></a><a name="zh-cn_topic_0084814075_p1421517295528"></a>通过计算采集周期内/proc/diskstats中对应设备第六列数据的变化与第四列数据的变化相除得出磁盘平均读操作大小。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p474673323716"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p474673323716"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p474673323716"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p231512379414"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p231512379414"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p231512379414"></a>≥ 0 KB/op</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5109113016584"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5109113016584"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5109113016584"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9109123075819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9109123075819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9109123075819"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row65193615419"><td class="cellrowborder" valign="top" width="11.64%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p147526451428"><a name="zh-cn_topic_0084814075_p147526451428"></a><a name="zh-cn_topic_0084814075_p147526451428"></a>disk_io_svctm</p>
</td>
<td class="cellrowborder" valign="top" width="12.94%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4336537134110"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4336537134110"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4336537134110"></a>（Agent）平均I/O服务时长</p>
</td>
<td class="cellrowborder" valign="top" width="42.39%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p43443375417"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p43443375417"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p43443375417"></a>该指标用于统计指定时间段内，平均每个读或写I/O的操作时长。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p434793715415"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p434793715415"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p434793715415"></a>单位：ms/op</p>
<a name="zh-cn_topic_0084814075_ul734610486318"></a><a name="zh-cn_topic_0084814075_ul734610486318"></a><ul id="zh-cn_topic_0084814075_ul734610486318"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p1813763215528"><a name="zh-cn_topic_0084814075_p1813763215528"></a><a name="zh-cn_topic_0084814075_p1813763215528"></a>通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化与第四列数据和第八列数据和的变化相除得出磁盘平均I/O时长。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1687154263712"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1687154263712"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1687154263712"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.64%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p235163718419"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p235163718419"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p235163718419"></a>≥ 0 ms/op</p>
</td>
<td class="cellrowborder" valign="top" width="7.86%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1090416312588"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1090416312588"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1090416312588"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="16.53%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9904203116583"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9904203116583"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9904203116583"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 6**  文件系统类监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_table296913551343"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row49905557345"><th class="cellrowborder" valign="top" width="11.41%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p2030317411858"><a name="zh-cn_topic_0084814075_p2030317411858"></a><a name="zh-cn_topic_0084814075_p2030317411858"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="15.93%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2994055123412"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2994055123412"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2994055123412"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="39.51%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1599916553345"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1599916553345"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1599916553345"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="8.14%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p93135623412"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p93135623412"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p93135623412"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="9.07%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1679482712"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1679482712"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1679482712"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="15.939999999999998%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1794324119"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1794324119"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1794324119"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row7330851124119"><td class="cellrowborder" valign="top" width="11.41%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p830413411251"><a name="zh-cn_topic_0084814075_p830413411251"></a><a name="zh-cn_topic_0084814075_p830413411251"></a>disk_fs_rwstate</p>
</td>
<td class="cellrowborder" valign="top" width="15.93%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p84715811419"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p84715811419"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p84715811419"></a>（Agent）文件系统读写状态</p>
</td>
<td class="cellrowborder" valign="top" width="39.51%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p9639112920367"><a name="zh-cn_topic_0084814075_p9639112920367"></a><a name="zh-cn_topic_0084814075_p9639112920367"></a>该指标用于统计测量对象挂载文件系统的读写状态。状态分为：可读写（0）/只读（1）。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19501958164115"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19501958164115"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19501958164115"></a>采集方式（Linux）：通过读取/proc/mounts中第四列文件系统挂载参数获得。</p>
</td>
<td class="cellrowborder" valign="top" width="8.14%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p05585817414"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p05585817414"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p05585817414"></a>0,1</p>
</td>
<td class="cellrowborder" valign="top" width="9.07%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p57951125117"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p57951125117"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p57951125117"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="15.939999999999998%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1879516218114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1879516218114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1879516218114"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row4161756163419"><td class="cellrowborder" valign="top" width="11.41%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p117245547501"><a name="zh-cn_topic_0084814075_p117245547501"></a><a name="zh-cn_topic_0084814075_p117245547501"></a>disk_inodesTotal</p>
</td>
<td class="cellrowborder" valign="top" width="15.93%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a3cf28f4ba8c34be683cf7c28eb36028e"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a3cf28f4ba8c34be683cf7c28eb36028e"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a3cf28f4ba8c34be683cf7c28eb36028e"></a>（Agent）inode空间大小</p>
</td>
<td class="cellrowborder" valign="top" width="39.51%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p13973112183711"><a name="zh-cn_topic_0084814075_p13973112183711"></a><a name="zh-cn_topic_0084814075_p13973112183711"></a>该指标用于统计测量对象当前磁盘的inode空间量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6853181323"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6853181323"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6853181323"></a>采集方式（Linux）：执行df -i命令，查看Inodes列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</td>
<td class="cellrowborder" valign="top" width="8.14%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a667a6062f5434cb381b861e3a52526f8"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a667a6062f5434cb381b861e3a52526f8"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a667a6062f5434cb381b861e3a52526f8"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="9.07%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1110310615110"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1110310615110"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1110310615110"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="15.939999999999998%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14103961213"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14103961213"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14103961213"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row7421756203419"><td class="cellrowborder" valign="top" width="11.41%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p187241854115013"><a name="zh-cn_topic_0084814075_p187241854115013"></a><a name="zh-cn_topic_0084814075_p187241854115013"></a>disk_inodesUsed</p>
</td>
<td class="cellrowborder" valign="top" width="15.93%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ada107ec63c5e48fc872d433a6d6431fa"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ada107ec63c5e48fc872d433a6d6431fa"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ada107ec63c5e48fc872d433a6d6431fa"></a>（Agent）inode已使用空间</p>
</td>
<td class="cellrowborder" valign="top" width="39.51%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a964a48c0ba3c4f3cbeff333aa5dd7d6f"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a964a48c0ba3c4f3cbeff333aa5dd7d6f"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a964a48c0ba3c4f3cbeff333aa5dd7d6f"></a>该指标用于统计测量对象当前磁盘已使用的inode空间量。</p>
<p id="zh-cn_topic_0084814075_p31351624203716"><a name="zh-cn_topic_0084814075_p31351624203716"></a><a name="zh-cn_topic_0084814075_p31351624203716"></a>采集方式（Linux）：执行df -i命令，查看IUsed列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</td>
<td class="cellrowborder" valign="top" width="8.14%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ac21f06dacf11428da8ad15257903cc2f"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ac21f06dacf11428da8ad15257903cc2f"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ac21f06dacf11428da8ad15257903cc2f"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="9.07%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p78495617112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p78495617112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p78495617112"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="15.939999999999998%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p884926418"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p884926418"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p884926418"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row1362175683411"><td class="cellrowborder" valign="top" width="11.41%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1730419411353"><a name="zh-cn_topic_0084814075_p1730419411353"></a><a name="zh-cn_topic_0084814075_p1730419411353"></a>disk_inodesUsedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="15.93%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_aecb1139b3e694480b09dcb590ce395ed"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_aecb1139b3e694480b09dcb590ce395ed"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_aecb1139b3e694480b09dcb590ce395ed"></a>（Agent）inode已使用占比</p>
</td>
<td class="cellrowborder" valign="top" width="39.51%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_af7d7bf90b33c4ab8a734dca22a9b0803"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_af7d7bf90b33c4ab8a734dca22a9b0803"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_af7d7bf90b33c4ab8a734dca22a9b0803"></a>该指标用于统计测量对象当前磁盘已使用的inode占比。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p626484910565"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p626484910565"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p626484910565"></a>单位：百分比</p>
<p id="zh-cn_topic_0084814075_p1791822633712"><a name="zh-cn_topic_0084814075_p1791822633712"></a><a name="zh-cn_topic_0084814075_p1791822633712"></a>采集方式（Linux）：执行df -i命令，查看IUse%列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</td>
<td class="cellrowborder" valign="top" width="8.14%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a976d888f07a94317952cbd3259ba9a2d"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a976d888f07a94317952cbd3259ba9a2d"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a976d888f07a94317952cbd3259ba9a2d"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="9.07%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1549127915"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1549127915"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1549127915"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="15.939999999999998%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11491117710"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11491117710"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11491117710"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>Windows系统暂不支持文件系统类监控指标。

**表 7**  网卡相关监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table925754617116"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row15262846141118"><th class="cellrowborder" valign="top" width="12.57%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p171851310486"><a name="zh-cn_topic_0084814075_p171851310486"></a><a name="zh-cn_topic_0084814075_p171851310486"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="12.18%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1326424661114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1326424661114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1326424661114"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="42.94%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p192660460118"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p192660460118"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p192660460118"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="9.22%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p526712460111"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p526712460111"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p526712460111"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.2%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p326235015116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p326235015116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p326235015116"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="12.889999999999999%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p926219501611"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p926219501611"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p926219501611"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row52701046191115"><td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p191851310883"><a name="zh-cn_topic_0084814075_p191851310883"></a><a name="zh-cn_topic_0084814075_p191851310883"></a>net_bitRecv</p>
</td>
<td class="cellrowborder" valign="top" width="12.18%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p112711946161117"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p112711946161117"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p112711946161117"></a>（Agent）出网带宽</p>
</td>
<td class="cellrowborder" valign="top" width="42.94%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p12729154165011"><a name="zh-cn_topic_0084814075_p12729154165011"></a><a name="zh-cn_topic_0084814075_p12729154165011"></a>该指标用于统计测量对象网卡每秒发送的比特数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12195165575819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12195165575819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12195165575819"></a>单位：bit/s</p>
<a name="zh-cn_topic_0084814075_ul7241184533819"></a><a name="zh-cn_topic_0084814075_ul7241184533819"></a><ul id="zh-cn_topic_0084814075_ul7241184533819"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.22%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p42762467110"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p42762467110"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p42762467110"></a>≥ 0 bits/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p62621850618"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p62621850618"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p62621850618"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.889999999999999%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p42627501114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p42627501114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p42627501114"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row4280144612117"><td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p21850108820"><a name="zh-cn_topic_0084814075_p21850108820"></a><a name="zh-cn_topic_0084814075_p21850108820"></a>net_bitSent</p>
</td>
<td class="cellrowborder" valign="top" width="12.18%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2281174621114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2281174621114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2281174621114"></a>（Agent）入网带宽</p>
</td>
<td class="cellrowborder" valign="top" width="42.94%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p117291054185012"><a name="zh-cn_topic_0084814075_p117291054185012"></a><a name="zh-cn_topic_0084814075_p117291054185012"></a>该指标用于统计测量对象网卡每秒接收的比特数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p119005035917"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p119005035917"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p119005035917"></a>单位：bit/s</p>
<a name="zh-cn_topic_0084814075_ul15438713143910"></a><a name="zh-cn_topic_0084814075_ul15438713143910"></a><ul id="zh-cn_topic_0084814075_ul15438713143910"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.22%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p351716217142"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p351716217142"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p351716217142"></a>≥ 0 bits/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p35151601923"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p35151601923"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p35151601923"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.889999999999999%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10515200127"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10515200127"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10515200127"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1328934621110"><td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p318511101687"><a name="zh-cn_topic_0084814075_p318511101687"></a><a name="zh-cn_topic_0084814075_p318511101687"></a>net_packetRecv</p>
</td>
<td class="cellrowborder" valign="top" width="12.18%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14290124641113"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14290124641113"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14290124641113"></a>（Agent）网卡包接收速率</p>
</td>
<td class="cellrowborder" valign="top" width="42.94%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4292134691112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4292134691112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4292134691112"></a>该指标用于统计测量对象网卡每秒接收的数据包数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1251716155915"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1251716155915"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1251716155915"></a>单位：Count/s</p>
<a name="zh-cn_topic_0084814075_ul117291816103919"></a><a name="zh-cn_topic_0084814075_ul117291816103919"></a><ul id="zh-cn_topic_0084814075_ul117291816103919"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.22%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4297104616118"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4297104616118"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4297104616118"></a>≥ 0 counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p021851828"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p021851828"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p021851828"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.889999999999999%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p92186113215"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p92186113215"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p92186113215"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row0298154621113"><td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p673055425015"><a name="zh-cn_topic_0084814075_p673055425015"></a><a name="zh-cn_topic_0084814075_p673055425015"></a>net_packetSent</p>
</td>
<td class="cellrowborder" valign="top" width="12.18%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p829924613116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p829924613116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p829924613116"></a>（Agent）网卡包发送速率</p>
</td>
<td class="cellrowborder" valign="top" width="42.94%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13300194619118"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13300194619118"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13300194619118"></a>该指标用于统计测量对象网卡每秒发送的数据包数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1365112114592"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1365112114592"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1365112114592"></a>单位：Count/s</p>
<a name="zh-cn_topic_0084814075_ul6600141843917"></a><a name="zh-cn_topic_0084814075_ul6600141843917"></a><ul id="zh-cn_topic_0084814075_ul6600141843917"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.22%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p030515462112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p030515462112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p030515462112"></a>≥ 0 counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18966811226"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18966811226"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18966811226"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.889999999999999%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10966315218"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10966315218"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10966315218"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1513145363017"><td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p273015414504"><a name="zh-cn_topic_0084814075_p273015414504"></a><a name="zh-cn_topic_0084814075_p273015414504"></a>net_errin</p>
</td>
<td class="cellrowborder" valign="top" width="12.18%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p73131027132512"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p73131027132512"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p73131027132512"></a>（Agent）接收误包率</p>
</td>
<td class="cellrowborder" valign="top" width="42.94%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9313172719250"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9313172719250"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9313172719250"></a>该指标用于统计测量对象网卡每秒接收的错误数据包数量占所接收的数据包的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188355280597"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188355280597"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188355280597"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul83991822163915"></a><a name="zh-cn_topic_0084814075_ul83991822163915"></a><ul id="zh-cn_topic_0084814075_ul83991822163915"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.22%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3369579281"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3369579281"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3369579281"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1669318212218"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1669318212218"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1669318212218"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.889999999999999%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19693821220"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19693821220"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19693821220"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1950851143011"><td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p5731125414508"><a name="zh-cn_topic_0084814075_p5731125414508"></a><a name="zh-cn_topic_0084814075_p5731125414508"></a>net_errout</p>
</td>
<td class="cellrowborder" valign="top" width="12.18%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p155501224102512"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p155501224102512"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p155501224102512"></a>（Agent）发送误包率</p>
</td>
<td class="cellrowborder" valign="top" width="42.94%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1563924505919"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1563924505919"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1563924505919"></a>该指标用于统计测量对象网卡每秒发送的错误数据包数量占所发送的数据包的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125501924112513"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125501924112513"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125501924112513"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul861123718398"></a><a name="zh-cn_topic_0084814075_ul861123718398"></a><ul id="zh-cn_topic_0084814075_ul861123718398"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.22%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204221754161213"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204221754161213"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204221754161213"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12801931621"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12801931621"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12801931621"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.889999999999999%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p88021311217"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p88021311217"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p88021311217"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row134221248529"><td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p97311654145016"><a name="zh-cn_topic_0084814075_p97311654145016"></a><a name="zh-cn_topic_0084814075_p97311654145016"></a>net_dropin</p>
</td>
<td class="cellrowborder" valign="top" width="12.18%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1216444673017"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1216444673017"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1216444673017"></a>（Agent）接收丢包率</p>
</td>
<td class="cellrowborder" valign="top" width="42.94%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p216474618302"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p216474618302"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p216474618302"></a>该指标用于统计测量对象网卡每秒接收并已丢弃的数据包数量占所接收的数据包的比率</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p58891549205917"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p58891549205917"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p58891549205917"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul14377393390"></a><a name="zh-cn_topic_0084814075_ul14377393390"></a><ul id="zh-cn_topic_0084814075_ul14377393390"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.22%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10992115701213"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10992115701213"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10992115701213"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p176841041427"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p176841041427"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p176841041427"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.889999999999999%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p968454322"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p968454322"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p968454322"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row115851812525"><td class="cellrowborder" valign="top" width="12.57%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p47311654105013"><a name="zh-cn_topic_0084814075_p47311654105013"></a><a name="zh-cn_topic_0084814075_p47311654105013"></a>net_dropout</p>
</td>
<td class="cellrowborder" valign="top" width="12.18%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p16466149153017"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p16466149153017"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p16466149153017"></a>（Agent）发送丢包率</p>
</td>
<td class="cellrowborder" valign="top" width="42.94%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3266135619131"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3266135619131"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3266135619131"></a>该指标用于统计测量对象网卡每秒发送并已丢弃的数据包数量占所发送的数据包的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1097754165914"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1097754165914"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1097754165914"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul1133016418390"></a><a name="zh-cn_topic_0084814075_ul1133016418390"></a><ul id="zh-cn_topic_0084814075_ul1133016418390"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="9.22%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p139272012134"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p139272012134"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p139272012134"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4279951221"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4279951221"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4279951221"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.889999999999999%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p427914519217"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p427914519217"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p427914519217"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 8**  进程类监控指标说明

<a name="zh-cn_topic_0084814075_table131966151727"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_row61979157214"><th class="cellrowborder" valign="top" width="12.908709129087088%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p151971153212"><a name="zh-cn_topic_0084814075_p151971153212"></a><a name="zh-cn_topic_0084814075_p151971153212"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="10.618938106189379%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_p18197615628"><a name="zh-cn_topic_0084814075_p18197615628"></a><a name="zh-cn_topic_0084814075_p18197615628"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="38.8961103889611%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_p619717151526"><a name="zh-cn_topic_0084814075_p619717151526"></a><a name="zh-cn_topic_0084814075_p619717151526"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="15.898410158984099%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_p419718157213"><a name="zh-cn_topic_0084814075_p419718157213"></a><a name="zh-cn_topic_0084814075_p419718157213"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="9.63903609639036%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_p111978155217"><a name="zh-cn_topic_0084814075_p111978155217"></a><a name="zh-cn_topic_0084814075_p111978155217"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="12.038796120387959%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_p1519718153215"><a name="zh-cn_topic_0084814075_p1519718153215"></a><a name="zh-cn_topic_0084814075_p1519718153215"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_row5197015627"><td class="cellrowborder" valign="top" width="12.908709129087088%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1546885210474"><a name="zh-cn_topic_0084814075_p1546885210474"></a><a name="zh-cn_topic_0084814075_p1546885210474"></a>proc_pHashId_cpu</p>
</td>
<td class="cellrowborder" valign="top" width="10.618938106189379%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p19146121813512"><a name="zh-cn_topic_0084814075_p19146121813512"></a><a name="zh-cn_topic_0084814075_p19146121813512"></a>进程CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p072719521252"><a name="zh-cn_topic_0084814075_p072719521252"></a><a name="zh-cn_topic_0084814075_p072719521252"></a>进程消耗的CPU百分比，pHashId是（进程名+进程ID）的md5值。</p>
<p id="zh-cn_topic_0084814075_p127514570146"><a name="zh-cn_topic_0084814075_p127514570146"></a><a name="zh-cn_topic_0084814075_p127514570146"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul188031147670"></a><a name="zh-cn_topic_0084814075_ul188031147670"></a><ul id="zh-cn_topic_0084814075_ul188031147670"><li>采集方式（Linux）：通过计算/proc/pid/stat的变化得出。</li><li>采集方式（Windows）：通过Windows API GetProcessTimes获取进程CPU使用率。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p101988152216"><a name="zh-cn_topic_0084814075_p101988152216"></a><a name="zh-cn_topic_0084814075_p101988152216"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p819818151120"><a name="zh-cn_topic_0084814075_p819818151120"></a><a name="zh-cn_topic_0084814075_p819818151120"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p1919819151127"><a name="zh-cn_topic_0084814075_p1919819151127"></a><a name="zh-cn_topic_0084814075_p1919819151127"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row122547189416"><td class="cellrowborder" valign="top" width="12.908709129087088%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p116763499474"><a name="zh-cn_topic_0084814075_p116763499474"></a><a name="zh-cn_topic_0084814075_p116763499474"></a>proc_pHashId_mem</p>
</td>
<td class="cellrowborder" valign="top" width="10.618938106189379%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p8724192617519"><a name="zh-cn_topic_0084814075_p8724192617519"></a><a name="zh-cn_topic_0084814075_p8724192617519"></a>进程内存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p282220584518"><a name="zh-cn_topic_0084814075_p282220584518"></a><a name="zh-cn_topic_0084814075_p282220584518"></a>进程消耗的内存百分比，pHashId是（进程名+进程ID）的md5值。</p>
<p id="zh-cn_topic_0084814075_p97751859161412"><a name="zh-cn_topic_0084814075_p97751859161412"></a><a name="zh-cn_topic_0084814075_p97751859161412"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul17380127818"></a><a name="zh-cn_topic_0084814075_ul17380127818"></a><ul id="zh-cn_topic_0084814075_ul17380127818"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p143075818819"><a name="zh-cn_topic_0084814075_p143075818819"></a><a name="zh-cn_topic_0084814075_p143075818819"></a>RSS*PAGESIZE/MemTotal</p>
<p id="zh-cn_topic_0084814075_p1343018589820"><a name="zh-cn_topic_0084814075_p1343018589820"></a><a name="zh-cn_topic_0084814075_p1343018589820"></a>RSS: 通过获取/proc/pid/statm第二列得到</p>
<p id="zh-cn_topic_0084814075_p1143011589815"><a name="zh-cn_topic_0084814075_p1143011589815"></a><a name="zh-cn_topic_0084814075_p1143011589815"></a>PAGESIZE: 通过命令getconf PAGESIZE获取</p>
<p id="zh-cn_topic_0084814075_p184302584813"><a name="zh-cn_topic_0084814075_p184302584813"></a><a name="zh-cn_topic_0084814075_p184302584813"></a>MemTotal：通过/proc/meminfo获取</p>
</li><li>采集方式（Windows）：使用Windows  API procGlobalMemoryStatusEx获取内存总量，通过GetProcessMemoryInfo获取内存已使用量，计算两者比值得到内存使用率。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p122558181345"><a name="zh-cn_topic_0084814075_p122558181345"></a><a name="zh-cn_topic_0084814075_p122558181345"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p125518181647"><a name="zh-cn_topic_0084814075_p125518181647"></a><a name="zh-cn_topic_0084814075_p125518181647"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p2255181818412"><a name="zh-cn_topic_0084814075_p2255181818412"></a><a name="zh-cn_topic_0084814075_p2255181818412"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row134801141742"><td class="cellrowborder" valign="top" width="12.908709129087088%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p16108144124710"><a name="zh-cn_topic_0084814075_p16108144124710"></a><a name="zh-cn_topic_0084814075_p16108144124710"></a>proc_pHashId_file</p>
</td>
<td class="cellrowborder" valign="top" width="10.618938106189379%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p135156347514"><a name="zh-cn_topic_0084814075_p135156347514"></a><a name="zh-cn_topic_0084814075_p135156347514"></a>进程打开文件数</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p6494154211513"><a name="zh-cn_topic_0084814075_p6494154211513"></a><a name="zh-cn_topic_0084814075_p6494154211513"></a>进程打开文件数，pHashId是（进程名+进程ID）的md5值。</p>
<a name="zh-cn_topic_0084814075_ul1567503084"></a><a name="zh-cn_topic_0084814075_ul1567503084"></a><ul id="zh-cn_topic_0084814075_ul1567503084"><li>采集方式（Linux）：通过执行ls -l /proc/pid/fd 可以查看数量。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p194801914147"><a name="zh-cn_topic_0084814075_p194801914147"></a><a name="zh-cn_topic_0084814075_p194801914147"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p1248011141749"><a name="zh-cn_topic_0084814075_p1248011141749"></a><a name="zh-cn_topic_0084814075_p1248011141749"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p9480141419415"><a name="zh-cn_topic_0084814075_p9480141419415"></a><a name="zh-cn_topic_0084814075_p9480141419415"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row104062369319"><td class="cellrowborder" valign="top" width="12.908709129087088%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p106651442103712"><a name="zh-cn_topic_0084814075_p106651442103712"></a><a name="zh-cn_topic_0084814075_p106651442103712"></a>proc_running_count</p>
</td>
<td class="cellrowborder" valign="top" width="10.618938106189379%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p6740185510386"><a name="zh-cn_topic_0084814075_p6740185510386"></a><a name="zh-cn_topic_0084814075_p6740185510386"></a>运行中进程数</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p072111023915"><a name="zh-cn_topic_0084814075_p072111023915"></a><a name="zh-cn_topic_0084814075_p072111023915"></a>该指标用于统计测量对象处于运行状态的进程数。</p>
<a name="zh-cn_topic_0084814075_ul4970742815"></a><a name="zh-cn_topic_0084814075_ul4970742815"></a><ul id="zh-cn_topic_0084814075_ul4970742815"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p134061536931"><a name="zh-cn_topic_0084814075_p134061536931"></a><a name="zh-cn_topic_0084814075_p134061536931"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p94061361331"><a name="zh-cn_topic_0084814075_p94061361331"></a><a name="zh-cn_topic_0084814075_p94061361331"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p174062360316"><a name="zh-cn_topic_0084814075_p174062360316"></a><a name="zh-cn_topic_0084814075_p174062360316"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row162083416319"><td class="cellrowborder" valign="top" width="12.908709129087088%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p106651042113715"><a name="zh-cn_topic_0084814075_p106651042113715"></a><a name="zh-cn_topic_0084814075_p106651042113715"></a>proc_idle_count</p>
</td>
<td class="cellrowborder" valign="top" width="10.618938106189379%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p3740125514380"><a name="zh-cn_topic_0084814075_p3740125514380"></a><a name="zh-cn_topic_0084814075_p3740125514380"></a>空闲进程数</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p872120113911"><a name="zh-cn_topic_0084814075_p872120113911"></a><a name="zh-cn_topic_0084814075_p872120113911"></a>该指标用于统计测量对象处于空闲状态的进程数。</p>
<a name="zh-cn_topic_0084814075_ul5222137680"></a><a name="zh-cn_topic_0084814075_ul5222137680"></a><ul id="zh-cn_topic_0084814075_ul5222137680"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p11621934838"><a name="zh-cn_topic_0084814075_p11621934838"></a><a name="zh-cn_topic_0084814075_p11621934838"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p662133414311"><a name="zh-cn_topic_0084814075_p662133414311"></a><a name="zh-cn_topic_0084814075_p662133414311"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p36212343319"><a name="zh-cn_topic_0084814075_p36212343319"></a><a name="zh-cn_topic_0084814075_p36212343319"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row11531321333"><td class="cellrowborder" valign="top" width="12.908709129087088%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p66651142143710"><a name="zh-cn_topic_0084814075_p66651142143710"></a><a name="zh-cn_topic_0084814075_p66651142143710"></a>proc_zombie_count</p>
</td>
<td class="cellrowborder" valign="top" width="10.618938106189379%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p274010553387"><a name="zh-cn_topic_0084814075_p274010553387"></a><a name="zh-cn_topic_0084814075_p274010553387"></a>僵死进程数</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p07216015392"><a name="zh-cn_topic_0084814075_p07216015392"></a><a name="zh-cn_topic_0084814075_p07216015392"></a>该指标用于统计测量对象处于僵死状态的进程数。</p>
<a name="zh-cn_topic_0084814075_ul18587962817"></a><a name="zh-cn_topic_0084814075_ul18587962817"></a><ul id="zh-cn_topic_0084814075_ul18587962817"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p185423216318"><a name="zh-cn_topic_0084814075_p185423216318"></a><a name="zh-cn_topic_0084814075_p185423216318"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p105423214314"><a name="zh-cn_topic_0084814075_p105423214314"></a><a name="zh-cn_topic_0084814075_p105423214314"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p15414324316"><a name="zh-cn_topic_0084814075_p15414324316"></a><a name="zh-cn_topic_0084814075_p15414324316"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row202201298317"><td class="cellrowborder" valign="top" width="12.908709129087088%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p116651042143719"><a name="zh-cn_topic_0084814075_p116651042143719"></a><a name="zh-cn_topic_0084814075_p116651042143719"></a>proc_blocked_count</p>
</td>
<td class="cellrowborder" valign="top" width="10.618938106189379%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p2740755103817"><a name="zh-cn_topic_0084814075_p2740755103817"></a><a name="zh-cn_topic_0084814075_p2740755103817"></a>阻塞进程数</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p1972120103917"><a name="zh-cn_topic_0084814075_p1972120103917"></a><a name="zh-cn_topic_0084814075_p1972120103917"></a>该指标用于统计测量对象被阻塞的进程数。</p>
<a name="zh-cn_topic_0084814075_ul097288687"></a><a name="zh-cn_topic_0084814075_ul097288687"></a><ul id="zh-cn_topic_0084814075_ul097288687"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p13220102911317"><a name="zh-cn_topic_0084814075_p13220102911317"></a><a name="zh-cn_topic_0084814075_p13220102911317"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p8220192918316"><a name="zh-cn_topic_0084814075_p8220192918316"></a><a name="zh-cn_topic_0084814075_p8220192918316"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p19220122914310"><a name="zh-cn_topic_0084814075_p19220122914310"></a><a name="zh-cn_topic_0084814075_p19220122914310"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row1578216251831"><td class="cellrowborder" valign="top" width="12.908709129087088%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p12666542163710"><a name="zh-cn_topic_0084814075_p12666542163710"></a><a name="zh-cn_topic_0084814075_p12666542163710"></a>proc_sleeping_count</p>
</td>
<td class="cellrowborder" valign="top" width="10.618938106189379%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p1741105513811"><a name="zh-cn_topic_0084814075_p1741105513811"></a><a name="zh-cn_topic_0084814075_p1741105513811"></a>睡眠进程数</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p17215017397"><a name="zh-cn_topic_0084814075_p17215017397"></a><a name="zh-cn_topic_0084814075_p17215017397"></a>该指标用于统计测量对象处于睡眠状态的进程数。</p>
<a name="zh-cn_topic_0084814075_ul456914117813"></a><a name="zh-cn_topic_0084814075_ul456914117813"></a><ul id="zh-cn_topic_0084814075_ul456914117813"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p18783102510317"><a name="zh-cn_topic_0084814075_p18783102510317"></a><a name="zh-cn_topic_0084814075_p18783102510317"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p15783182510318"><a name="zh-cn_topic_0084814075_p15783182510318"></a><a name="zh-cn_topic_0084814075_p15783182510318"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p18783225630"><a name="zh-cn_topic_0084814075_p18783225630"></a><a name="zh-cn_topic_0084814075_p18783225630"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row81989151821"><td class="cellrowborder" valign="top" width="12.908709129087088%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p18666134223719"><a name="zh-cn_topic_0084814075_p18666134223719"></a><a name="zh-cn_topic_0084814075_p18666134223719"></a>proc_total_count</p>
</td>
<td class="cellrowborder" valign="top" width="10.618938106189379%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p137416556389"><a name="zh-cn_topic_0084814075_p137416556389"></a><a name="zh-cn_topic_0084814075_p137416556389"></a>系统进程数</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p157213019397"><a name="zh-cn_topic_0084814075_p157213019397"></a><a name="zh-cn_topic_0084814075_p157213019397"></a>该指标用于统计测量对象的总进程数。</p>
<a name="zh-cn_topic_0084814075_ul582615139815"></a><a name="zh-cn_topic_0084814075_ul582615139815"></a><ul id="zh-cn_topic_0084814075_ul582615139815"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：通过psapi.dll系统进程状态支持模块得到进程总数。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p5199161514219"><a name="zh-cn_topic_0084814075_p5199161514219"></a><a name="zh-cn_topic_0084814075_p5199161514219"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p2199111519210"><a name="zh-cn_topic_0084814075_p2199111519210"></a><a name="zh-cn_topic_0084814075_p2199111519210"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p419917154212"><a name="zh-cn_topic_0084814075_p419917154212"></a><a name="zh-cn_topic_0084814075_p419917154212"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

**表 9**  GPU类监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table760319497509"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row860364919508"><th class="cellrowborder" valign="top" width="12.808719128087187%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p32277610918"><a name="zh-cn_topic_0084814075_p32277610918"></a><a name="zh-cn_topic_0084814075_p32277610918"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="10.71892810718928%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14302112714513"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14302112714513"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14302112714513"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="38.8961103889611%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p33041727195112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p33041727195112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p33041727195112"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="15.898410158984099%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1430742725119"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1430742725119"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1430742725119"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="9.63903609639036%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52072618319"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52072618319"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52072618319"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="12.038796120387959%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p620726332"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p620726332"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p620726332"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1160494935017"><td class="cellrowborder" valign="top" width="12.808719128087187%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p2736145405012"><a name="zh-cn_topic_0084814075_p2736145405012"></a><a name="zh-cn_topic_0084814075_p2736145405012"></a>slot0_gpu_performance_state</p>
</td>
<td class="cellrowborder" valign="top" width="10.71892810718928%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17121531516"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17121531516"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17121531516"></a>性能状态</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p1773094122317"><a name="zh-cn_topic_0084814075_p1773094122317"></a><a name="zh-cn_topic_0084814075_p1773094122317"></a>该指标用于统计测量对象当前的性能状态。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p57121353125118"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p57121353125118"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p57121353125118"></a>该指标无单位。</p>
<p id="zh-cn_topic_0084814075_p115941222144018"><a name="zh-cn_topic_0084814075_p115941222144018"></a><a name="zh-cn_topic_0084814075_p115941222144018"></a>采集方式（Linux）：执行nvidia-smi命令，查看Perf列数据。</p>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1296192392"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1296192392"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1296192392"></a>P0-P15、P32，</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p10891021195"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p10891021195"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p10891021195"></a>P0表示最大性能状态，P15表示最小性能状态，P32表示状态未知。</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p620786339"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p620786339"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p620786339"></a>GPU云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1220811616315"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1220811616315"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1220811616315"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row7604114955016"><td class="cellrowborder" valign="top" width="12.808719128087187%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p15253828135214"><a name="zh-cn_topic_0084814075_p15253828135214"></a><a name="zh-cn_topic_0084814075_p15253828135214"></a>slot0_gpu_usage_mem</p>
</td>
<td class="cellrowborder" valign="top" width="10.71892810718928%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p371205316513"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p371205316513"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p371205316513"></a>显存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1712453175111"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1712453175111"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1712453175111"></a>该指标用于统计测量对象当前的显存使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p834992019534"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p834992019534"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p834992019534"></a>单位：百分比</p>
<p id="zh-cn_topic_0084814075_p819023214401"><a name="zh-cn_topic_0084814075_p819023214401"></a><a name="zh-cn_topic_0084814075_p819023214401"></a>采集方式（Linux）：执行nvidia-smi命令，查看Memory-Usage列数据。</p>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18712195314515"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18712195314515"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18712195314515"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1053141612316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1053141612316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1053141612316"></a>GPU云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p7533165316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p7533165316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p7533165316"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1860417492507"><td class="cellrowborder" valign="top" width="12.808719128087187%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p8255028185219"><a name="zh-cn_topic_0084814075_p8255028185219"></a><a name="zh-cn_topic_0084814075_p8255028185219"></a>slot0_gpu_usage_gpu</p>
</td>
<td class="cellrowborder" valign="top" width="10.71892810718928%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p171385315110"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p171385315110"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p171385315110"></a>GPU利用率</p>
</td>
<td class="cellrowborder" valign="top" width="38.8961103889611%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1971315538511"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1971315538511"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1971315538511"></a>该指标用于统计测量对象当前的GPU利用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204891126115312"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204891126115312"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204891126115312"></a>单位：百分比</p>
<p id="zh-cn_topic_0084814075_p12770193419402"><a name="zh-cn_topic_0084814075_p12770193419402"></a><a name="zh-cn_topic_0084814075_p12770193419402"></a>采集方式（Linux）：执行nvidia-smi命令，查看GPU-Util列数据。</p>
</td>
<td class="cellrowborder" valign="top" width="15.898410158984099%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1223616464528"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1223616464528"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1223616464528"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="9.63903609639036%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5785121610312"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5785121610312"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5785121610312"></a>GPU云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="12.038796120387959%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p478591611316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p478591611316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p478591611316"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>Windows系统暂不支持GPU类监控指标。

## 维度<a name="section36963297112133"></a>

<a name="table41237041112133"></a>
<table><thead align="left"><tr id="row28021974112133"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="p55187441112133"><a name="p55187441112133"></a><a name="p55187441112133"></a>Key</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="p40997749112133"><a name="p40997749112133"></a><a name="p40997749112133"></a>Value</p>
</th>
</tr>
</thead>
<tbody><tr id="row32483336112133"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p13904597112133"><a name="p13904597112133"></a><a name="p13904597112133"></a>instance_id</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p52530562112133"><a name="p52530562112133"></a><a name="p52530562112133"></a><span id="text173241214361"><a name="text173241214361"></a><a name="text173241214361"></a>云服务器</span>ID</p>
</td>
</tr>
</tbody>
</table>

