# 弹性云服务器支持的操作系统监控指标（安装Agent）<a name="ecs_03_1003"></a>

## 功能说明<a name="section12784212213"></a>

通过在弹性云服务器中安装Agent插件，可以为用户提供服务器的系统级、主动式、细颗粒度监控服务。本节定义了弹性云服务器上报云监控的操作系统监控指标。

操作系统监控目前支持的监控指标有：CPU相关监控项、CPU负载类相关监控项、内存相关监控项、磁盘相关监控项、磁盘I/O相关监控项、文件系统类相关监控项、网卡类相关监控项、NTP类相关监控项、TCP连接数类相关监控、GPU相关监控项、NPU相关监控项。

安装Agent后，对于不同的操作系统、不同的弹性云服务器类型，您可以查看不同类型的操作系统监控指标。指标采集周期是1分钟。

## 命名空间<a name="section24282572112133"></a>

AGT.ECS

## 操作系统监控指标：CPU<a name="section47952021926"></a>

**表 1**  CPU相关监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table7594115620353"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row95951556133512"><th class="cellrowborder" valign="top" width="12.751275127512752%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p19741153185914"><a name="zh-cn_topic_0084814075_p19741153185914"></a><a name="zh-cn_topic_0084814075_p19741153185914"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.5014501450145%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1255413283615"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1255413283615"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1255413283615"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="33.513351335133514%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105546320367"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105546320367"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105546320367"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="13.991399139913991%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_ecs_03_1002_p64622851222846"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_ecs_03_1002_p64622851222846"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_ecs_03_1002_p64622851222846"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.98109810981098%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1383633412472"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1383633412472"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1383633412472"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="14.261426142614262%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18780264718"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18780264718"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18780264718"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="row16202201820337"><td class="cellrowborder" valign="top" width="12.751275127512752%" headers="mcps1.2.7.1.1 "><p id="p32711419193316"><a name="p32711419193316"></a><a name="p32711419193316"></a>cpu_usage</p>
</td>
<td class="cellrowborder" valign="top" width="14.5014501450145%" headers="mcps1.2.7.1.2 "><p id="p122711819173313"><a name="p122711819173313"></a><a name="p122711819173313"></a>(Agent) CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="33.513351335133514%" headers="mcps1.2.7.1.3 "><p id="p1427121933317"><a name="p1427121933317"></a><a name="p1427121933317"></a>该指标用于统计测量对象当前CPU使用率。</p>
<p id="p1027120191337"><a name="p1027120191337"></a><a name="p1027120191337"></a>单位：百分比</p>
<a name="ul027111199334"></a><a name="ul027111199334"></a><ul id="ul027111199334"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出cpu使用率。用户可以通过top命令查看 %Cpu(s)值。</li><li>采集方式（Windows）：通过WindowsAPI GetSystemTimes获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.991399139913991%" headers="mcps1.2.7.1.4 "><p id="p1827141963319"><a name="p1827141963319"></a><a name="p1827141963319"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.98109810981098%" headers="mcps1.2.7.1.5 "><p id="p127281973319"><a name="p127281973319"></a><a name="p127281973319"></a><span id="text1983125020420"><a name="text1983125020420"></a><a name="text1983125020420"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.261426142614262%" headers="mcps1.2.7.1.6 "><p id="p10272121913316"><a name="p10272121913316"></a><a name="p10272121913316"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row8595175614350"><td class="cellrowborder" valign="top" width="12.751275127512752%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p19715195419502"><a name="zh-cn_topic_0084814075_p19715195419502"></a><a name="zh-cn_topic_0084814075_p19715195419502"></a>cpu_usage_idle</p>
</td>
<td class="cellrowborder" valign="top" width="14.5014501450145%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105451722015"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105451722015"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105451722015"></a>(Agent) CPU空闲时间占比</p>
</td>
<td class="cellrowborder" valign="top" width="33.513351335133514%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p65951856183515"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p65951856183515"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p65951856183515"></a>该指标用于统计测量对象当前CPU空闲时间占比。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1753993014112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1753993014112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1753993014112"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul7740114434813"></a><a name="zh-cn_topic_0084814075_ul7740114434813"></a><ul id="zh-cn_topic_0084814075_ul7740114434813"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出CPU空闲时间占比。</li><li>采集方式（Windows）：通过WindowsAPI GetSystemTimes获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.991399139913991%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p66362622114851"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p66362622114851"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p66362622114851"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.98109810981098%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8836734164720"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8836734164720"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8836734164720"></a><span id="text13631751962"><a name="text13631751962"></a><a name="text13631751962"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.261426142614262%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p162174963816"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p162174963816"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p162174963816"></a>1分钟</p>
</td>
</tr>
<tr id="row12203145116337"><td class="cellrowborder" valign="top" width="12.751275127512752%" headers="mcps1.2.7.1.1 "><p id="p55125273310"><a name="p55125273310"></a><a name="p55125273310"></a>cpu_usage_user</p>
</td>
<td class="cellrowborder" valign="top" width="14.5014501450145%" headers="mcps1.2.7.1.2 "><p id="p1951552163319"><a name="p1951552163319"></a><a name="p1951552163319"></a>(Agent) 用户空间CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="33.513351335133514%" headers="mcps1.2.7.1.3 "><p id="p105852183318"><a name="p105852183318"></a><a name="p105852183318"></a>该指标用于统计测量对象当前用户空间占用CPU使用率。</p>
<p id="p5535219335"><a name="p5535219335"></a><a name="p5535219335"></a>单位：百分比</p>
<a name="ul1451652183319"></a><a name="ul1451652183319"></a><ul id="ul1451652183319"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出cpu使用率。用户可以通过top命令查看 %Cpu(s) us值。</li><li>采集方式（Windows）：通过WindowsAPI GetSystemTimes获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.991399139913991%" headers="mcps1.2.7.1.4 "><p id="p0555218332"><a name="p0555218332"></a><a name="p0555218332"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.98109810981098%" headers="mcps1.2.7.1.5 "><p id="p36152183314"><a name="p36152183314"></a><a name="p36152183314"></a><span id="text10387175410620"><a name="text10387175410620"></a><a name="text10387175410620"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.261426142614262%" headers="mcps1.2.7.1.6 "><p id="p16252103318"><a name="p16252103318"></a><a name="p16252103318"></a>1分钟</p>
</td>
</tr>
<tr id="row82609618341"><td class="cellrowborder" valign="top" width="12.751275127512752%" headers="mcps1.2.7.1.1 "><p id="p71926719342"><a name="p71926719342"></a><a name="p71926719342"></a>cpu_usage_system</p>
</td>
<td class="cellrowborder" valign="top" width="14.5014501450145%" headers="mcps1.2.7.1.2 "><p id="p1619220763414"><a name="p1619220763414"></a><a name="p1619220763414"></a>(Agent) 内核空间CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="33.513351335133514%" headers="mcps1.2.7.1.3 "><p id="p61921474340"><a name="p61921474340"></a><a name="p61921474340"></a>该指标用于统计测量对象当前内核空间占用CPU使用率。</p>
<p id="p119267113420"><a name="p119267113420"></a><a name="p119267113420"></a>单位：百分比</p>
<a name="ul131921278344"></a><a name="ul131921278344"></a><ul id="ul131921278344"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出内核空间CPU使用率。用户可以通过top命令查看 %Cpu(s) sy值。</li><li>采集方式（Windows）：通过WindowsAPI GetSystemTimes获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.991399139913991%" headers="mcps1.2.7.1.4 "><p id="p919210711346"><a name="p919210711346"></a><a name="p919210711346"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.98109810981098%" headers="mcps1.2.7.1.5 "><p id="p1019310715343"><a name="p1019310715343"></a><a name="p1019310715343"></a><span id="text12802257867"><a name="text12802257867"></a><a name="text12802257867"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.261426142614262%" headers="mcps1.2.7.1.6 "><p id="p71938718342"><a name="p71938718342"></a><a name="p71938718342"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row923914003617"><td class="cellrowborder" valign="top" width="12.751275127512752%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p147151154185010"><a name="zh-cn_topic_0084814075_p147151154185010"></a><a name="zh-cn_topic_0084814075_p147151154185010"></a>cpu_usage_other</p>
</td>
<td class="cellrowborder" valign="top" width="14.5014501450145%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p54268533589"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p54268533589"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p54268533589"></a>(Agent) 其他CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="33.513351335133514%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9639820102610"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9639820102610"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9639820102610"></a>该指标用于统计测量对象其他占用CPU使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p585238104117"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p585238104117"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p585238104117"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul16241613135214"></a><a name="zh-cn_topic_0084814075_ul16241613135214"></a><ul id="zh-cn_topic_0084814075_ul16241613135214"><li>采集方式（Linux）：其他CPU使用率=1- 空闲CPU使用率（%）- 内核空间CPU使用率- 用户空间CPU使用率。</li><li>采集方式（Windows）：其他CPU使用率=1- 空闲CPU使用率（%）- 内核空间CPU使用率- 用户空间CPU使用率。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.991399139913991%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15426165314587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15426165314587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15426165314587"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.98109810981098%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1122010114534"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1122010114534"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1122010114534"></a><span id="text1016012011717"><a name="text1016012011717"></a><a name="text1016012011717"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.261426142614262%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p112201411534"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p112201411534"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p112201411534"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row5771145493710"><td class="cellrowborder" valign="top" width="12.751275127512752%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p671625425010"><a name="zh-cn_topic_0084814075_p671625425010"></a><a name="zh-cn_topic_0084814075_p671625425010"></a>cpu_usage_nice</p>
</td>
<td class="cellrowborder" valign="top" width="14.5014501450145%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18338192592712"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18338192592712"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18338192592712"></a>(Agent) Nice进程CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="33.513351335133514%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14357142313313"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14357142313313"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14357142313313"></a>该指标用于统计测量对象当前Nice进程CPU使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13802312422"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13802312422"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13802312422"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul31531140105416"></a><a name="zh-cn_topic_0084814075_ul31531140105416"></a><ul id="zh-cn_topic_0084814075_ul31531140105416"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出Nice进程CPU使用率。用户可以通过top命令查看 %Cpu(s) ni值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.991399139913991%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p49111420104116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p49111420104116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p49111420104116"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.98109810981098%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19489869535"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19489869535"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19489869535"></a><span id="text13300631573"><a name="text13300631573"></a><a name="text13300631573"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.261426142614262%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p134891645315"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p134891645315"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p134891645315"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1347919118387"><td class="cellrowborder" valign="top" width="12.751275127512752%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1171720549502"><a name="zh-cn_topic_0084814075_p1171720549502"></a><a name="zh-cn_topic_0084814075_p1171720549502"></a>cpu_usage_iowait</p>
</td>
<td class="cellrowborder" valign="top" width="14.5014501450145%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12309132815275"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12309132815275"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12309132815275"></a>(Agent) iowait状态占比</p>
</td>
<td class="cellrowborder" valign="top" width="33.513351335133514%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p5358182363312"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p5358182363312"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p5358182363312"></a>该指标用于统计测量对象当前iowait状态占用CPU的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13110915425"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13110915425"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13110915425"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul6110655175410"></a><a name="zh-cn_topic_0084814075_ul6110655175410"></a><ul id="zh-cn_topic_0084814075_ul6110655175410"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出iowait状态占比。用户可以通过top命令查看 %Cpu(s) wa值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.991399139913991%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35911215413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35911215413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35911215413"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.98109810981098%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p129676775315"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p129676775315"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p129676775315"></a><span id="text779713511717"><a name="text779713511717"></a><a name="text779713511717"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.261426142614262%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199671971537"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199671971537"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199671971537"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1585742117387"><td class="cellrowborder" valign="top" width="12.751275127512752%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p5717175415018"><a name="zh-cn_topic_0084814075_p5717175415018"></a><a name="zh-cn_topic_0084814075_p5717175415018"></a>cpu_usage_irq</p>
</td>
<td class="cellrowborder" valign="top" width="14.5014501450145%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p0789035152712"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p0789035152712"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p0789035152712"></a>(Agent) CPU中断时间占比</p>
</td>
<td class="cellrowborder" valign="top" width="33.513351335133514%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1358182311339"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1358182311339"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1358182311339"></a>该指标用于统计测量对象当前CPU处理中断用时占用CPU时间的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1847811754216"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1847811754216"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1847811754216"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul161211982552"></a><a name="zh-cn_topic_0084814075_ul161211982552"></a><ul id="zh-cn_topic_0084814075_ul161211982552"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出CPU中断时间占比。用户可以通过top命令查看 %Cpu(s) hi值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.991399139913991%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p185392264112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p185392264112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p185392264112"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.98109810981098%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p73370965316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p73370965316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p73370965316"></a><span id="text5703081276"><a name="text5703081276"></a><a name="text5703081276"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.261426142614262%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15337159155313"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15337159155313"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15337159155313"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row122701957103711"><td class="cellrowborder" valign="top" width="12.751275127512752%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p12742163205912"><a name="zh-cn_topic_0084814075_p12742163205912"></a><a name="zh-cn_topic_0084814075_p12742163205912"></a>cpu_usage_softirq</p>
</td>
<td class="cellrowborder" valign="top" width="14.5014501450145%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p103301332413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p103301332413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p103301332413"></a>(Agent) CPU软中断时间占比</p>
</td>
<td class="cellrowborder" valign="top" width="33.513351335133514%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p335819233334"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p335819233334"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p335819233334"></a>该指标用于统计测量对象当前CPU处理软中断时间占用CPU时间的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13161162444214"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13161162444214"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p13161162444214"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul1435116242555"></a><a name="zh-cn_topic_0084814075_ul1435116242555"></a><ul id="zh-cn_topic_0084814075_ul1435116242555"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出CPU软中断时间占比。用户可以通过top命令查看 %Cpu(s) si值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.991399139913991%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12645622184110"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12645622184110"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12645622184110"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.98109810981098%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1699416915530"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1699416915530"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1699416915530"></a><span id="text1568118106713"><a name="text1568118106713"></a><a name="text1568118106713"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.261426142614262%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p999416915313"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p999416915313"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p999416915313"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 操作系统监控指标：CPU负载<a name="section450012762919"></a>

**表 2**  CPU负载指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table059418341885"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row56003341289"><th class="cellrowborder" valign="top" width="12.839999999999998%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p236911231700"><a name="zh-cn_topic_0084814075_p236911231700"></a><a name="zh-cn_topic_0084814075_p236911231700"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.37%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11601634589"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11601634589"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11601634589"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="33.900000000000006%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46035341782"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46035341782"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46035341782"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="13.86%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p156041834186"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p156041834186"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p156041834186"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.68%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46051534285"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46051534285"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p46051534285"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="14.35%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p561016344817"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p561016344817"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p561016344817"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1761212343810"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1071885419506"><a name="zh-cn_topic_0084814075_p1071885419506"></a><a name="zh-cn_topic_0084814075_p1071885419506"></a>load_average1</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850194611018"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850194611018"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850194611018"></a>(Agent) 1分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="33.900000000000006%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7357107220"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7357107220"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7357107220"></a>该指标用于统计测量对象过去1分钟的CPU平均负载。</p>
<p id="zh-cn_topic_0084814075_p2297112311714"><a name="zh-cn_topic_0084814075_p2297112311714"></a><a name="zh-cn_topic_0084814075_p2297112311714"></a>采集方式（Linux）：通过/proc/loadavg中load1/逻辑CPU个数得到。用户可以通过top命令查看load1值。</p>
</td>
<td class="cellrowborder" valign="top" width="13.86%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198778139214"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198778139214"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198778139214"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.68%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13618634485"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13618634485"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13618634485"></a><span id="text28313141777"><a name="text28313141777"></a><a name="text28313141777"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.35%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9310913195413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9310913195413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9310913195413"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row46221234681"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p171811549508"><a name="zh-cn_topic_0084814075_p171811549508"></a><a name="zh-cn_topic_0084814075_p171811549508"></a>load_average5</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12509461401"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12509461401"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12509461401"></a>(Agent) 5分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="33.900000000000006%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p193579719219"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p193579719219"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p193579719219"></a>该指标用于统计测量对象过去5分钟的CPU平均负载。</p>
<p id="zh-cn_topic_0084814075_p1134824691718"><a name="zh-cn_topic_0084814075_p1134824691718"></a><a name="zh-cn_topic_0084814075_p1134824691718"></a>采集方式（Linux）：通过/proc/loadavg中load5/逻辑CPU个数得到。用户可以通过top命令查看load5值。</p>
</td>
<td class="cellrowborder" valign="top" width="13.86%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1387714135216"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1387714135216"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1387714135216"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.68%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p196291341812"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p196291341812"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p196291341812"></a><span id="text186173174716"><a name="text186173174716"></a><a name="text186173174716"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.35%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p344582715413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p344582715413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p344582715413"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row106321341682"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p19718125419505"><a name="zh-cn_topic_0084814075_p19718125419505"></a><a name="zh-cn_topic_0084814075_p19718125419505"></a>load_average15</p>
</td>
<td class="cellrowborder" valign="top" width="14.37%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850104612013"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850104612013"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1850104612013"></a>(Agent) 15分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="33.900000000000006%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p43571971429"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p43571971429"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p43571971429"></a>该指标用于统计测量对象过去15分钟的CPU平均负载。</p>
<p id="zh-cn_topic_0084814075_p540374831716"><a name="zh-cn_topic_0084814075_p540374831716"></a><a name="zh-cn_topic_0084814075_p540374831716"></a>采集方式（Linux）：通过/proc/loadavg中load15/逻辑CPU个数得到。用户可以通过top命令查看load15值。</p>
</td>
<td class="cellrowborder" valign="top" width="13.86%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p148771134213"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p148771134213"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p148771134213"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.68%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p663818341587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p663818341587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p663818341587"></a><span id="text9962101915710"><a name="text9962101915710"></a><a name="text9962101915710"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.35%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81142810545"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81142810545"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81142810545"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>Windows系统暂不支持CPU负载指标。

## 操作系统监控指标：内存<a name="section1531517713014"></a>

**表 3**  内存相关监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table181485064217"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row2081514503427"><th class="cellrowborder" valign="top" width="13.208679132086795%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p492517502010"><a name="zh-cn_topic_0084814075_p492517502010"></a><a name="zh-cn_topic_0084814075_p492517502010"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.198580141985802%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35662062433"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35662062433"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p35662062433"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="33.72662733726628%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125671366437"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125671366437"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125671366437"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="14.428557144285575%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1993419755115"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1993419755115"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1993419755115"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.318968103189684%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1993403575518"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1993403575518"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1993403575518"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="14.118588141185883%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p209051331165514"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p209051331165514"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p209051331165514"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row28151450174217"><td class="cellrowborder" valign="top" width="13.208679132086795%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p117181154185013"><a name="zh-cn_topic_0084814075_p117181154185013"></a><a name="zh-cn_topic_0084814075_p117181154185013"></a>mem_available</p>
</td>
<td class="cellrowborder" valign="top" width="14.198580141985802%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13426653115813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13426653115813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13426653115813"></a>(Agent) 可用内存</p>
</td>
<td class="cellrowborder" valign="top" width="33.72662733726628%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2659105264319"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2659105264319"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2659105264319"></a>该指标用于统计测量对象的可用内存。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p319812463425"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p319812463425"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p319812463425"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul178711134191"></a><a name="zh-cn_topic_0084814075_ul178711134191"></a><ul id="zh-cn_topic_0084814075_ul178711134191"><li>采集方式（Linux）：通过/proc/meminfo文件获取，<a name="ul246210229220"></a><a name="ul246210229220"></a><ul id="ul246210229220"><li>若/proc/meminfo中显示MemAvailable，则直接可得</li><li>若/proc/meminfo中不显示MemAvailable，则MemAvailable=MemFree+Buffers+Cached</li></ul>
</li><li>采集方式（Windows）：计算方法为（内存总量-已用内存量）。通过WindowsAPI GlobalMemoryStatusEx获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.428557144285575%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6815650164213"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6815650164213"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6815650164213"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="10.318968103189684%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1793493512550"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1793493512550"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1793493512550"></a><span id="text1217710231979"><a name="text1217710231979"></a><a name="text1217710231979"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.118588141185883%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2905183165513"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2905183165513"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2905183165513"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1881555015426"><td class="cellrowborder" valign="top" width="13.208679132086795%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p10719654105010"><a name="zh-cn_topic_0084814075_p10719654105010"></a><a name="zh-cn_topic_0084814075_p10719654105010"></a>mem_usedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="14.198580141985802%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7426953195818"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7426953195818"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7426953195818"></a>(Agent) 内存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="33.72662733726628%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p56603522431"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p56603522431"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p56603522431"></a>该指标用于统计测量对象的内存使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1271515216422"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1271515216422"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1271515216422"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul15740448151918"></a><a name="zh-cn_topic_0084814075_ul15740448151918"></a><ul id="zh-cn_topic_0084814075_ul15740448151918"><li>采集方式（Linux）：通过/proc/meminfo文件获取，(MemTotal-MemAvailable)/MemTotal<a name="ul2093415489228"></a><a name="ul2093415489228"></a><ul id="ul2093415489228"><li>若/proc/meminfo中显示MemAvailable，则MemUsedPercent=(MemTotal-MemAvailable)/MemTotal</li><li>若/proc/meminfo中不显示MemAvailable，则MemUsedPercent=(MemTotal-MemFree-Buffers-Cached)/MemTotal</li></ul>
</li><li>采集方式（Windows）：计算方法为（ 已用内存量/内存总量*100%）。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.428557144285575%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p168151550164215"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p168151550164215"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p168151550164215"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.318968103189684%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p20313183255619"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p20313183255619"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p20313183255619"></a><span id="text862052614718"><a name="text862052614718"></a><a name="text862052614718"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.118588141185883%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p53139328567"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p53139328567"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p53139328567"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row17755151194213"><td class="cellrowborder" valign="top" width="13.208679132086795%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p571975405014"><a name="zh-cn_topic_0084814075_p571975405014"></a><a name="zh-cn_topic_0084814075_p571975405014"></a>mem_free</p>
</td>
<td class="cellrowborder" valign="top" width="14.198580141985802%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13461198162815"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13461198162815"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13461198162815"></a>(Agent) 空闲内存量</p>
</td>
<td class="cellrowborder" valign="top" width="33.72662733726628%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p446198172813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p446198172813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p446198172813"></a>该指标用于统计测量对象的空闲内存量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3971074432"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3971074432"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3971074432"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul11951452161911"></a><a name="zh-cn_topic_0084814075_ul11951452161911"></a><ul id="zh-cn_topic_0084814075_ul11951452161911"><li>采集方式（Linux）：通过/proc/meminfo获取。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.428557144285575%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1646188112819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1646188112819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1646188112819"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="10.318968103189684%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4592183317560"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4592183317560"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4592183317560"></a><span id="text159787284713"><a name="text159787284713"></a><a name="text159787284713"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.118588141185883%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1559293395618"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1559293395618"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1559293395618"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row32411149194211"><td class="cellrowborder" valign="top" width="13.208679132086795%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p8719165419505"><a name="zh-cn_topic_0084814075_p8719165419505"></a><a name="zh-cn_topic_0084814075_p8719165419505"></a>mem_buffers</p>
</td>
<td class="cellrowborder" valign="top" width="14.198580141985802%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1097541222813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1097541222813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1097541222813"></a>(Agent) Buffers占用量</p>
</td>
<td class="cellrowborder" valign="top" width="33.72662733726628%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1491524514516"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1491524514516"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1491524514516"></a>该指标用于统计测量对象的Buffers内存量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1637141311439"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1637141311439"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1637141311439"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul1383115415196"></a><a name="zh-cn_topic_0084814075_ul1383115415196"></a><ul id="zh-cn_topic_0084814075_ul1383115415196"><li>采集方式（Linux）：通过/proc/meminfo获取。用户可以通过top命令查看 KiB Mem:buffers值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.428557144285575%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1975131212815"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1975131212815"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1975131212815"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="10.318968103189684%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188323414561"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188323414561"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188323414561"></a><span id="text988420311075"><a name="text988420311075"></a><a name="text988420311075"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.118588141185883%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10883183419560"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10883183419560"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10883183419560"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row148195464215"><td class="cellrowborder" valign="top" width="13.208679132086795%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p592575011019"><a name="zh-cn_topic_0084814075_p592575011019"></a><a name="zh-cn_topic_0084814075_p592575011019"></a>mem_cached</p>
</td>
<td class="cellrowborder" valign="top" width="14.198580141985802%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1996519532814"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1996519532814"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1996519532814"></a>(Agent) Cache占用量</p>
</td>
<td class="cellrowborder" valign="top" width="33.72662733726628%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15966946124515"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15966946124515"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15966946124515"></a>该指标用于统计测量对象Cache内存量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p411621174316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p411621174316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p411621174316"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul63235715193"></a><a name="zh-cn_topic_0084814075_ul63235715193"></a><ul id="zh-cn_topic_0084814075_ul63235715193"><li>采集方式（Linux）：通过/proc/meminfo获取。用户可以通过top命令查看 KiB Swap:cached Mem值。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.428557144285575%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p296519522819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p296519522819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p296519522819"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="10.318968103189684%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1614173512563"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1614173512563"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1614173512563"></a><span id="text141851342076"><a name="text141851342076"></a><a name="text141851342076"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.118588141185883%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1961433555618"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1961433555618"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1961433555618"></a>1分钟</p>
</td>
</tr>
<tr id="row19849142073113"><td class="cellrowborder" valign="top" width="13.208679132086795%" headers="mcps1.2.7.1.1 "><p id="p2084992083114"><a name="p2084992083114"></a><a name="p2084992083114"></a>total_open_files</p>
</td>
<td class="cellrowborder" valign="top" width="14.198580141985802%" headers="mcps1.2.7.1.2 "><p id="p8850132053110"><a name="p8850132053110"></a><a name="p8850132053110"></a>(Agent) 文件句柄总数</p>
</td>
<td class="cellrowborder" valign="top" width="33.72662733726628%" headers="mcps1.2.7.1.3 "><p id="p17850220153120"><a name="p17850220153120"></a><a name="p17850220153120"></a>该指标用于统计测量对象的所有进程使用的句柄总和。</p>
<p id="p1344044863415"><a name="p1344044863415"></a><a name="p1344044863415"></a>单位：个</p>
<a name="ul54402486347"></a><a name="ul54402486347"></a><ul id="ul54402486347"><li>采集方式（Linux）：通过/proc/{pid}/fd文件汇总所有进程使用的句柄数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.428557144285575%" headers="mcps1.2.7.1.4 "><p id="p207077814351"><a name="p207077814351"></a><a name="p207077814351"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.318968103189684%" headers="mcps1.2.7.1.5 "><p id="p18876142014717"><a name="p18876142014717"></a><a name="p18876142014717"></a><span id="text149563371872"><a name="text149563371872"></a><a name="text149563371872"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="14.118588141185883%" headers="mcps1.2.7.1.6 "><p id="p1070717843515"><a name="p1070717843515"></a><a name="p1070717843515"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 操作系统监控指标：磁盘<a name="section098622153112"></a>

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   目前仅支持物理磁盘指标的采集，不支持通过网络文件系统协议挂载的磁盘。
>-   会默认屏蔽docker相关的挂载点。挂载点前缀如下：
>    ```
>    /var/lib/docker;/mnt/paas/kubernetes;/var/lib/mesos
>    ```

**表 4**  磁盘相关监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table2050841310455"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row250917130458"><th class="cellrowborder" valign="top" width="13.099999999999998%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p126095471215"><a name="zh-cn_topic_0084814075_p126095471215"></a><a name="zh-cn_topic_0084814075_p126095471215"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.529999999999998%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13757487454"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13757487454"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13757487454"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="33.809999999999995%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p47794817458"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p47794817458"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p47794817458"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="14.179999999999998%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17186610175111"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17186610175111"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17186610175111"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.349999999999996%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81307820578"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81307820578"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p81307820578"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="14.029999999999998%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p21306815714"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p21306815714"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p21306815714"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row650913134455"><td class="cellrowborder" valign="top" width="13.099999999999998%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p10720854195015"><a name="zh-cn_topic_0084814075_p10720854195015"></a><a name="zh-cn_topic_0084814075_p10720854195015"></a>disk_free</p>
</td>
<td class="cellrowborder" valign="top" width="14.529999999999998%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11426145312588"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11426145312588"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11426145312588"></a>(Agent) 磁盘剩余存储量</p>
</td>
<td class="cellrowborder" valign="top" width="33.809999999999995%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p116982408478"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p116982408478"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p116982408478"></a>该指标用于统计测量对象磁盘的剩余存储空间。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p364185016435"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p364185016435"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p364185016435"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul1836810491232"></a><a name="zh-cn_topic_0084814075_ul1836810491232"></a><ul id="zh-cn_topic_0084814075_ul1836810491232"><li>采集方式（Linux）：执行df -h命令，查看Avail列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>采集方式（Windows）：使用WMI接口GetDiskFreeSpaceExW获取磁盘空间数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.179999999999998%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p194261653135820"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p194261653135820"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p194261653135820"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="10.349999999999996%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4938131119577"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4938131119577"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4938131119577"></a><span id="text102691642478"><a name="text102691642478"></a><a name="text102691642478"></a>云服务器</span> - 挂载点</p>
</td>
<td class="cellrowborder" valign="top" width="14.029999999999998%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1093851113572"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1093851113572"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1093851113572"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row75091135457"><td class="cellrowborder" valign="top" width="13.099999999999998%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p5721155418501"><a name="zh-cn_topic_0084814075_p5721155418501"></a><a name="zh-cn_topic_0084814075_p5721155418501"></a>disk_total</p>
</td>
<td class="cellrowborder" valign="top" width="14.529999999999998%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1775111613310"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1775111613310"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1775111613310"></a>(Agent) 磁盘存储总量</p>
</td>
<td class="cellrowborder" valign="top" width="33.809999999999995%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18426105319582"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18426105319582"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18426105319582"></a>该指标用于统计测量对象磁盘存储总量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3181456184316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3181456184316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3181456184316"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul22892410242"></a><a name="zh-cn_topic_0084814075_ul22892410242"></a><ul id="zh-cn_topic_0084814075_ul22892410242"><li>采集方式（Linux）：执行df -h命令，查看Size列数据。<p id="zh-cn_topic_0084814075_p5341629122612"><a name="zh-cn_topic_0084814075_p5341629122612"></a><a name="zh-cn_topic_0084814075_p5341629122612"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：使用WMI接口GetDiskFreeSpaceExW获取磁盘空间数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.179999999999998%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1057313810816"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1057313810816"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1057313810816"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="10.349999999999996%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p631511310574"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p631511310574"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p631511310574"></a><span id="text52607454717"><a name="text52607454717"></a><a name="text52607454717"></a>云服务器</span> - 挂载点</p>
</td>
<td class="cellrowborder" valign="top" width="14.029999999999998%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8315131319579"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8315131319579"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8315131319579"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row95094134450"><td class="cellrowborder" valign="top" width="13.099999999999998%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p19721165445019"><a name="zh-cn_topic_0084814075_p19721165445019"></a><a name="zh-cn_topic_0084814075_p19721165445019"></a>disk_used</p>
</td>
<td class="cellrowborder" valign="top" width="14.529999999999998%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p34202178311"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p34202178311"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p34202178311"></a>(Agent) 磁盘已用存量</p>
</td>
<td class="cellrowborder" valign="top" width="33.809999999999995%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p167462537593"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p167462537593"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p167462537593"></a>该指标用于统计测量对象磁盘的已用存储空间。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p25641849446"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p25641849446"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p25641849446"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul032356132415"></a><a name="zh-cn_topic_0084814075_ul032356132415"></a><ul id="zh-cn_topic_0084814075_ul032356132415"><li>采集方式（Linux）：执行df -h命令，查看Used列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>采集方式（Windows）：使用WMI接口GetDiskFreeSpaceExW获取磁盘空间数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.179999999999998%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13509440124615"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13509440124615"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13509440124615"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="10.349999999999996%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5014143578"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5014143578"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p5014143578"></a><span id="text1844610491575"><a name="text1844610491575"></a><a name="text1844610491575"></a>云服务器</span> - 挂载点</p>
</td>
<td class="cellrowborder" valign="top" width="14.029999999999998%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p160201485719"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p160201485719"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p160201485719"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1050951394510"><td class="cellrowborder" valign="top" width="13.099999999999998%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p572216546508"><a name="zh-cn_topic_0084814075_p572216546508"></a><a name="zh-cn_topic_0084814075_p572216546508"></a>disk_usedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="14.529999999999998%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105111318631"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105111318631"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105111318631"></a>(Agent) 磁盘使用率</p>
</td>
<td class="cellrowborder" valign="top" width="33.809999999999995%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p64261535585"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p64261535585"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p64261535585"></a>该指标用于统计测量对象磁盘使用率，以百分比为单位。计算方式为: 磁盘已用存储量/磁盘存储总量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14423171814449"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14423171814449"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14423171814449"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul098197247"></a><a name="zh-cn_topic_0084814075_ul098197247"></a><ul id="zh-cn_topic_0084814075_ul098197247"><li>采集方式（Linux）：通过计算Used/Size得出。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>采集方式（Windows）：使用WMI接口GetDiskFreeSpaceExW获取磁盘空间数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.179999999999998%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p94261253205813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p94261253205813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p94261253205813"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.349999999999996%" headers="mcps1.2.7.1.5 "><p id="p16126328102920"><a name="p16126328102920"></a><a name="p16126328102920"></a><span id="text18777652272"><a name="text18777652272"></a><a name="text18777652272"></a>云服务器</span> - 挂载点</p>
</td>
<td class="cellrowborder" valign="top" width="14.029999999999998%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3166191516578"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3166191516578"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3166191516578"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 操作系统监控指标：磁盘I/O<a name="section10529543193115"></a>

**表 5**  磁盘I/O相关监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table35183543283"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row953775472814"><th class="cellrowborder" valign="top" width="13.118688131186884%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p1175211451217"><a name="zh-cn_topic_0084814075_p1175211451217"></a><a name="zh-cn_topic_0084814075_p1175211451217"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.518548145185484%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p45421054192813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p45421054192813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p45421054192813"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.13658634136587%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18546175412289"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18546175412289"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18546175412289"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="13.708629137086294%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1549175452814"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1549175452814"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1549175452814"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.508949105089494%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1175214128581"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1175214128581"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1175214128581"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="14.008599140085995%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1475220121587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1475220121587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1475220121587"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row13734554112815"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p117251254185016"><a name="zh-cn_topic_0084814075_p117251254185016"></a><a name="zh-cn_topic_0084814075_p117251254185016"></a>disk_agt_read_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15737185472818"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15737185472818"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15737185472818"></a>(Agent) 磁盘读速率</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p20741205422814"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p20741205422814"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p20741205422814"></a>该指标用于统计每秒从测量对象读出数据量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p782163415446"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p782163415446"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p782163415446"></a>单位：Byte/s</p>
<a name="zh-cn_topic_0084814075_ul91083169316"></a><a name="zh-cn_topic_0084814075_ul91083169316"></a><ul id="zh-cn_topic_0084814075_ul91083169316"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p9613124165112"><a name="zh-cn_topic_0084814075_p9613124165112"></a><a name="zh-cn_topic_0084814075_p9613124165112"></a>通过计算采集周期内/proc/diskstats中对应设备第六列数据的变化得出磁盘读速率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188071658143519"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188071658143519"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188071658143519"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：<a name="zh-cn_topic_0084814075_ul159131398347"></a><a name="zh-cn_topic_0084814075_ul159131398347"></a><ul id="zh-cn_topic_0084814075_ul159131398347"><li>使用WMI中Win32_PerfFormattedData_PerfDisk_LogicalDisk对象获取磁盘I/O数据。</li><li>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>高CPU情况下存在获取超时的现象，会导致无法获取监控数据。</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p974485419280"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p974485419280"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p974485419280"></a>≥ 0 Byte/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul489983411339"></a><a name="ul489983411339"></a><ul id="ul489983411339"><li><span id="text4635056773"><a name="text4635056773"></a><a name="text4635056773"></a>云服务器</span> - 磁盘</li><li><span id="text17455100387"><a name="text17455100387"></a><a name="text17455100387"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p147521812115810"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p147521812115810"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p147521812115810"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row47721654152813"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p197258544505"><a name="zh-cn_topic_0084814075_p197258544505"></a><a name="zh-cn_topic_0084814075_p197258544505"></a>disk_agt_read_requests_rate</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p677775412818"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p677775412818"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p677775412818"></a>(Agent) 磁盘读操作速率</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p107805542289"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p107805542289"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p107805542289"></a>该指标用于统计每秒从测量对象读取数据的请求次数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1044113915445"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1044113915445"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1044113915445"></a>单位：请求/秒</p>
<a name="zh-cn_topic_0084814075_ul499512533117"></a><a name="zh-cn_topic_0084814075_ul499512533117"></a><ul id="zh-cn_topic_0084814075_ul499512533117"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p838794495115"><a name="zh-cn_topic_0084814075_p838794495115"></a><a name="zh-cn_topic_0084814075_p838794495115"></a>通过计算采集周期内/proc/diskstats中对应设备第四列数据的变化得出磁盘读操作速率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9794308367"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9794308367"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9794308367"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：<a name="zh-cn_topic_0084814075_ul1079485110345"></a><a name="zh-cn_topic_0084814075_ul1079485110345"></a><ul id="zh-cn_topic_0084814075_ul1079485110345"><li>使用WMI中Win32_PerfFormattedData_PerfDisk_LogicalDisk对象获取磁盘I/O数据。</li><li>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>高CPU情况下存在获取超时的现象，会导致无法获取监控数据。</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1778413542289"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1778413542289"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1778413542289"></a>≥ 0 请求/秒</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul103161140193313"></a><a name="ul103161140193313"></a><ul id="ul103161140193313"><li><span id="text968714313810"><a name="text968714313810"></a><a name="text968714313810"></a>云服务器</span> - 磁盘</li><li><span id="text2212964814"><a name="text2212964814"></a><a name="text2212964814"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1852618177589"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1852618177589"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1852618177589"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row10814954112817"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p14726854145017"><a name="zh-cn_topic_0084814075_p14726854145017"></a><a name="zh-cn_topic_0084814075_p14726854145017"></a>disk_agt_write_bytes_rate</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17817554182816"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17817554182816"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17817554182816"></a>(Agent) 磁盘写速率</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2822195462819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2822195462819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2822195462819"></a>该指标用于统计每秒写到测量对象的数据量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1935811508444"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1935811508444"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1935811508444"></a>单位：Byte/s</p>
<a name="zh-cn_topic_0084814075_ul14619526183113"></a><a name="zh-cn_topic_0084814075_ul14619526183113"></a><ul id="zh-cn_topic_0084814075_ul14619526183113"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p4595144810511"><a name="zh-cn_topic_0084814075_p4595144810511"></a><a name="zh-cn_topic_0084814075_p4595144810511"></a>通过计算采集周期内/proc/diskstats中对应设备第十列数据的变化得出磁盘写速率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p26213763615"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p26213763615"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p26213763615"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：<a name="zh-cn_topic_0084814075_ul13419557193415"></a><a name="zh-cn_topic_0084814075_ul13419557193415"></a><ul id="zh-cn_topic_0084814075_ul13419557193415"><li>使用WMI中Win32_PerfFormattedData_PerfDisk_LogicalDisk对象获取磁盘I/O数据。</li><li>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>高CPU情况下存在获取超时的现象，会导致无法获取监控数据。</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p118255544285"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p118255544285"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p118255544285"></a>≥ 0 Byte/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul767464313335"></a><a name="ul767464313335"></a><ul id="ul767464313335"><li><span id="text153739916819"><a name="text153739916819"></a><a name="text153739916819"></a>云服务器</span> - 磁盘</li><li><span id="text323091217818"><a name="text323091217818"></a><a name="text323091217818"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1248714187586"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1248714187586"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1248714187586"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1285235420281"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p15726195413502"><a name="zh-cn_topic_0084814075_p15726195413502"></a><a name="zh-cn_topic_0084814075_p15726195413502"></a>disk_agt_write_requests_rate</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p985616542281"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p985616542281"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p985616542281"></a>(Agent) 磁盘写操作速率</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3859105420283"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3859105420283"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3859105420283"></a>该指标用于统计每秒向测量对象写数据的请求次数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8945842145517"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8945842145517"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8945842145517"></a>单位：请求/秒</p>
<a name="zh-cn_topic_0084814075_ul83511528173115"></a><a name="zh-cn_topic_0084814075_ul83511528173115"></a><ul id="zh-cn_topic_0084814075_ul83511528173115"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p1054795119518"><a name="zh-cn_topic_0084814075_p1054795119518"></a><a name="zh-cn_topic_0084814075_p1054795119518"></a>通过计算采集周期内/proc/diskstats中对应设备第八列数据的变化得出磁盘写操作速率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2413945123613"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2413945123613"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2413945123613"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：<a name="zh-cn_topic_0084814075_ul109514211357"></a><a name="zh-cn_topic_0084814075_ul109514211357"></a><ul id="zh-cn_topic_0084814075_ul109514211357"><li>使用WMI中Win32_PerfFormattedData_PerfDisk_LogicalDisk对象获取磁盘I/O数据。</li><li>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>高CPU情况下存在获取超时的现象，会导致无法获取监控数据。</li></ul>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6863125414286"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6863125414286"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6863125414286"></a>≥ 0 请求/秒</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul10413476339"></a><a name="ul10413476339"></a><ul id="ul10413476339"><li><span id="text10568201512811"><a name="text10568201512811"></a><a name="text10568201512811"></a>云服务器</span> - 磁盘</li><li><span id="text13541816812"><a name="text13541816812"></a><a name="text13541816812"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p31371420205819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p31371420205819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p31371420205819"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row3526538307"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p3727135416503"><a name="zh-cn_topic_0084814075_p3727135416503"></a><a name="zh-cn_topic_0084814075_p3727135416503"></a>disk_readTime</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1888124844819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1888124844819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1888124844819"></a>(Agent) 读操作平均耗时</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15890164812481"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15890164812481"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p15890164812481"></a>该指标用于统计测量对象磁盘读操作平均耗时。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3665195675519"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3665195675519"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3665195675519"></a>单位：ms/Count</p>
<a name="zh-cn_topic_0084814075_ul102521430153119"></a><a name="zh-cn_topic_0084814075_ul102521430153119"></a><ul id="zh-cn_topic_0084814075_ul102521430153119"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p17419165475115"><a name="zh-cn_topic_0084814075_p17419165475115"></a><a name="zh-cn_topic_0084814075_p17419165475115"></a>通过计算采集周期内/proc/diskstats中对应设备第七列数据的变化得出磁盘读操作平均耗时。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9405754103611"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9405754103611"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9405754103611"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p761943410503"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p761943410503"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p761943410503"></a>≥ 0 ms/Count</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul1366417535339"></a><a name="ul1366417535339"></a><ul id="ul1366417535339"><li><span id="text721013213811"><a name="text721013213811"></a><a name="text721013213811"></a>云服务器</span> - 磁盘</li><li><span id="text1540016231681"><a name="text1540016231681"></a><a name="text1540016231681"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p172182118586"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p172182118586"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p172182118586"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1271463304"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p672711548501"><a name="zh-cn_topic_0084814075_p672711548501"></a><a name="zh-cn_topic_0084814075_p672711548501"></a>disk_writeTime</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p48901848154819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p48901848154819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p48901848154819"></a>(Agent) 写操作平均耗时</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2890104810484"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2890104810484"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2890104810484"></a>该指标用于统计测量对象磁盘写操作平均耗时。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p169767319562"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p169767319562"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p169767319562"></a>单位：ms/Count</p>
<a name="zh-cn_topic_0084814075_ul48044353318"></a><a name="zh-cn_topic_0084814075_ul48044353318"></a><ul id="zh-cn_topic_0084814075_ul48044353318"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p1851410568512"><a name="zh-cn_topic_0084814075_p1851410568512"></a><a name="zh-cn_topic_0084814075_p1851410568512"></a>通过计算采集周期内/proc/diskstats中对应设备第十一列数据的变化得出磁盘写操作平均耗时。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p148401021372"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p148401021372"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p148401021372"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p166190349509"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p166190349509"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p166190349509"></a>≥ 0 ms/Count</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul14275185714336"></a><a name="ul14275185714336"></a><ul id="ul14275185714336"><li><span id="text196874259811"><a name="text196874259811"></a><a name="text196874259811"></a>云服务器</span> - 磁盘</li><li><span id="text1177242714811"><a name="text1177242714811"></a><a name="text1177242714811"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4736922145813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4736922145813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4736922145813"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row87124813010"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p57524451528"><a name="zh-cn_topic_0084814075_p57524451528"></a><a name="zh-cn_topic_0084814075_p57524451528"></a>disk_ioUtils</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198904485488"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198904485488"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198904485488"></a>(Agent) 磁盘I/O使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6204818503"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6204818503"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6204818503"></a>该指标用于统计测量对象磁盘I/O使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15507131035617"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15507131035617"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15507131035617"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul125541937123112"></a><a name="zh-cn_topic_0084814075_ul125541937123112"></a><ul id="zh-cn_topic_0084814075_ul125541937123112"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p186291818135219"><a name="zh-cn_topic_0084814075_p186291818135219"></a><a name="zh-cn_topic_0084814075_p186291818135219"></a>通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化得出磁盘I/O使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p477581114379"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p477581114379"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p477581114379"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1761915344507"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1761915344507"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1761915344507"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul19122059133318"></a><a name="ul19122059133318"></a><ul id="ul19122059133318"><li><span id="text1831110331684"><a name="text1831110331684"></a><a name="text1831110331684"></a>云服务器</span> - 磁盘</li><li><span id="text107790351087"><a name="text107790351087"></a><a name="text107790351087"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1645517259587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1645517259587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1645517259587"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row1430742210414"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1872235410504"><a name="zh-cn_topic_0084814075_p1872235410504"></a><a name="zh-cn_topic_0084814075_p1872235410504"></a>disk_queue_length</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1222693718413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1222693718413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1222693718413"></a>(Agent) 平均队列长度</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52311737154114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52311737154114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52311737154114"></a>该指标用于统计指定时间段内，平均等待完成的读取或写入操作请求的数量</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823173704120"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823173704120"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823173704120"></a>单位：个</p>
<a name="zh-cn_topic_0084814075_ul1178004023114"></a><a name="zh-cn_topic_0084814075_ul1178004023114"></a><ul id="zh-cn_topic_0084814075_ul1178004023114"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p776352085214"><a name="zh-cn_topic_0084814075_p776352085214"></a><a name="zh-cn_topic_0084814075_p776352085214"></a>通过计算采集周期内/proc/diskstats中对应设备第十四列数据的变化得出磁盘平均队列长度。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p813441910376"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p813441910376"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p813441910376"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823618378417"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823618378417"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p823618378417"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul14547154173417"></a><a name="ul14547154173417"></a><ul id="ul14547154173417"><li><span id="text135883381687"><a name="text135883381687"></a><a name="text135883381687"></a>云服务器</span> - 磁盘</li><li><span id="text41956411883"><a name="text41956411883"></a><a name="text41956411883"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p121721127145817"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p121721127145817"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p121721127145817"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row599132484116"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p14723175455019"><a name="zh-cn_topic_0084814075_p14723175455019"></a><a name="zh-cn_topic_0084814075_p14723175455019"></a>disk_write_bytes_per_operation</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6262173714416"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6262173714416"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6262173714416"></a>(Agent) 平均写操作大小</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p122701037104116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p122701037104116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p122701037104116"></a>该指标用于统计指定时间段内，平均每个写I/O操作传输的字节数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p627315376415"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p627315376415"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p627315376415"></a>单位：Byte/op</p>
<a name="zh-cn_topic_0084814075_ul1734274483111"></a><a name="zh-cn_topic_0084814075_ul1734274483111"></a><ul id="zh-cn_topic_0084814075_ul1734274483111"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p1222162495215"><a name="zh-cn_topic_0084814075_p1222162495215"></a><a name="zh-cn_topic_0084814075_p1222162495215"></a>通过计算采集周期内/proc/diskstats中对应设备第十列数据的变化与第八列数据的变化相除得出磁盘平均写操作大小。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p347420279373"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p347420279373"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p347420279373"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p527813774116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p527813774116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p527813774116"></a>≥ 0 Byte/op</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul2093173340"></a><a name="ul2093173340"></a><ul id="ul2093173340"><li><span id="text107269451887"><a name="text107269451887"></a><a name="text107269451887"></a>云服务器</span> - 磁盘</li><li><span id="text138518481484"><a name="text138518481484"></a><a name="text138518481484"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2024152885820"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2024152885820"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2024152885820"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row1475812710414"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p15723254175018"><a name="zh-cn_topic_0084814075_p15723254175018"></a><a name="zh-cn_topic_0084814075_p15723254175018"></a>disk_read_bytes_per_operation</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6301237144116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6301237144116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6301237144116"></a>(Agent) 平均读操作大小</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p63051537174111"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p63051537174111"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p63051537174111"></a>该指标用于统计指定时间段内，平均每个读I/O操作传输的字节数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11308203711410"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11308203711410"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11308203711410"></a>单位：Byte/op</p>
<a name="zh-cn_topic_0084814075_ul118664451315"></a><a name="zh-cn_topic_0084814075_ul118664451315"></a><ul id="zh-cn_topic_0084814075_ul118664451315"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p1421517295528"><a name="zh-cn_topic_0084814075_p1421517295528"></a><a name="zh-cn_topic_0084814075_p1421517295528"></a>通过计算采集周期内/proc/diskstats中对应设备第六列数据的变化与第四列数据的变化相除得出磁盘平均读操作大小。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p474673323716"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p474673323716"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p474673323716"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p231512379414"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p231512379414"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p231512379414"></a>≥ 0 Byte/op</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul657219918343"></a><a name="ul657219918343"></a><ul id="ul657219918343"><li><span id="text198845013813"><a name="text198845013813"></a><a name="text198845013813"></a>云服务器</span> - 磁盘</li><li><span id="text811012561782"><a name="text811012561782"></a><a name="text811012561782"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9109123075819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9109123075819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9109123075819"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row65193615419"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p147526451428"><a name="zh-cn_topic_0084814075_p147526451428"></a><a name="zh-cn_topic_0084814075_p147526451428"></a>disk_io_svctm</p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4336537134110"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4336537134110"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4336537134110"></a>(Agent) 平均I/O服务时长</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p43443375417"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p43443375417"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p43443375417"></a>该指标用于统计指定时间段内，平均每个读或写I/O的操作时长。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p434793715415"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p434793715415"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p434793715415"></a>单位：ms/op</p>
<a name="zh-cn_topic_0084814075_ul734610486318"></a><a name="zh-cn_topic_0084814075_ul734610486318"></a><ul id="zh-cn_topic_0084814075_ul734610486318"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p1813763215528"><a name="zh-cn_topic_0084814075_p1813763215528"></a><a name="zh-cn_topic_0084814075_p1813763215528"></a>通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化与第四列数据和第八列数据和的变化相除得出磁盘平均I/O时长。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1687154263712"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1687154263712"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1687154263712"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p235163718419"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p235163718419"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p235163718419"></a>≥ 0 ms/op</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><a name="ul1738121203410"></a><a name="ul1738121203410"></a><ul id="ul1738121203410"><li><span id="text12661711913"><a name="text12661711913"></a><a name="text12661711913"></a>云服务器</span> - 磁盘</li><li><span id="text1678073990"><a name="text1678073990"></a><a name="text1678073990"></a>云服务器</span> - 挂载点</li></ul>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9904203116583"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9904203116583"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p9904203116583"></a>1分钟</p>
</td>
</tr>
<tr id="row11792121320589"><td class="cellrowborder" valign="top" width="13.118688131186884%" headers="mcps1.2.7.1.1 "><p id="p16161312175117"><a name="p16161312175117"></a><a name="p16161312175117"></a>disk_device_used_percent</p>
<p id="p1861671219512"><a name="p1861671219512"></a><a name="p1861671219512"></a></p>
</td>
<td class="cellrowborder" valign="top" width="14.518548145185484%" headers="mcps1.2.7.1.2 "><p id="p1161712128517"><a name="p1161712128517"></a><a name="p1161712128517"></a>块设备使用率</p>
</td>
<td class="cellrowborder" valign="top" width="34.13658634136587%" headers="mcps1.2.7.1.3 "><p id="p8617191215116"><a name="p8617191215116"></a><a name="p8617191215116"></a>该指标用于统计测量对象物理磁盘使用率，以百分比为单位。计算方式为: 所有已挂载磁盘分区已用存储量/磁盘存储总量。</p>
<a name="ul361761225114"></a><a name="ul361761225114"></a><ul id="ul361761225114"><li>采集方式（Linux）：通过汇总每个挂载点的磁盘使用量，在通过磁盘扇区大小和扇区数量计算出磁盘总大小，计算出整体磁盘使用率</li><li>（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.708629137086294%" headers="mcps1.2.7.1.4 "><p id="p379317135582"><a name="p379317135582"></a><a name="p379317135582"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.508949105089494%" headers="mcps1.2.7.1.5 "><p id="p1342573410210"><a name="p1342573410210"></a><a name="p1342573410210"></a><span id="text74737571305"><a name="text74737571305"></a><a name="text74737571305"></a>云服务器</span> - 磁盘</p>
</td>
<td class="cellrowborder" valign="top" width="14.008599140085995%" headers="mcps1.2.7.1.6 "><p id="p37937136584"><a name="p37937136584"></a><a name="p37937136584"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 操作系统监控指标：文件系统<a name="section33521124193212"></a>

**表 6**  文件系统类监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_table296913551343"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row49905557345"><th class="cellrowborder" valign="top" width="12.97%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p2030317411858"><a name="zh-cn_topic_0084814075_p2030317411858"></a><a name="zh-cn_topic_0084814075_p2030317411858"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.66%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2994055123412"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2994055123412"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p2994055123412"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.28%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1599916553345"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1599916553345"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1599916553345"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="13.700000000000001%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p93135623412"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p93135623412"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p93135623412"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.639999999999999%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1679482712"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1679482712"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1679482712"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="13.750000000000002%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1794324119"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1794324119"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1794324119"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row7330851124119"><td class="cellrowborder" valign="top" width="12.97%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p830413411251"><a name="zh-cn_topic_0084814075_p830413411251"></a><a name="zh-cn_topic_0084814075_p830413411251"></a>disk_fs_rwstate</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p84715811419"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p84715811419"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p84715811419"></a>(Agent) 文件系统读写状态</p>
</td>
<td class="cellrowborder" valign="top" width="34.28%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p9639112920367"><a name="zh-cn_topic_0084814075_p9639112920367"></a><a name="zh-cn_topic_0084814075_p9639112920367"></a>该指标用于统计测量对象挂载文件系统的读写状态。状态分为：可读写（0）/只读（1）。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19501958164115"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19501958164115"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19501958164115"></a>采集方式（Linux）：通过读取/proc/mounts中第四列文件系统挂载参数获得。</p>
</td>
<td class="cellrowborder" valign="top" width="13.700000000000001%" headers="mcps1.2.7.1.4 "><a name="ul1799812422371"></a><a name="ul1799812422371"></a><ul id="ul1799812422371"><li>0：可读写</li><li>1：只读</li></ul>
</td>
<td class="cellrowborder" valign="top" width="10.639999999999999%" headers="mcps1.2.7.1.5 "><p id="p12358515366"><a name="p12358515366"></a><a name="p12358515366"></a><span id="text6321174916"><a name="text6321174916"></a><a name="text6321174916"></a>云服务器</span> - 挂载点</p>
</td>
<td class="cellrowborder" valign="top" width="13.750000000000002%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1879516218114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1879516218114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1879516218114"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row4161756163419"><td class="cellrowborder" valign="top" width="12.97%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p117245547501"><a name="zh-cn_topic_0084814075_p117245547501"></a><a name="zh-cn_topic_0084814075_p117245547501"></a>disk_inodesTotal</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a3cf28f4ba8c34be683cf7c28eb36028e"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a3cf28f4ba8c34be683cf7c28eb36028e"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a3cf28f4ba8c34be683cf7c28eb36028e"></a>(Agent) inode空间大小</p>
</td>
<td class="cellrowborder" valign="top" width="34.28%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p13973112183711"><a name="zh-cn_topic_0084814075_p13973112183711"></a><a name="zh-cn_topic_0084814075_p13973112183711"></a>该指标用于统计测量对象当前磁盘的inode空间量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6853181323"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6853181323"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p6853181323"></a>采集方式（Linux）：执行df -i命令，查看Inodes列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</td>
<td class="cellrowborder" valign="top" width="13.700000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a667a6062f5434cb381b861e3a52526f8"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a667a6062f5434cb381b861e3a52526f8"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a667a6062f5434cb381b861e3a52526f8"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.639999999999999%" headers="mcps1.2.7.1.5 "><p id="p198152983613"><a name="p198152983613"></a><a name="p198152983613"></a><span id="text69821198914"><a name="text69821198914"></a><a name="text69821198914"></a>云服务器</span> - 挂载点</p>
</td>
<td class="cellrowborder" valign="top" width="13.750000000000002%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14103961213"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14103961213"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14103961213"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row7421756203419"><td class="cellrowborder" valign="top" width="12.97%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p187241854115013"><a name="zh-cn_topic_0084814075_p187241854115013"></a><a name="zh-cn_topic_0084814075_p187241854115013"></a>disk_inodesUsed</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ada107ec63c5e48fc872d433a6d6431fa"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ada107ec63c5e48fc872d433a6d6431fa"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ada107ec63c5e48fc872d433a6d6431fa"></a>(Agent) inode已使用空间</p>
</td>
<td class="cellrowborder" valign="top" width="34.28%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a964a48c0ba3c4f3cbeff333aa5dd7d6f"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a964a48c0ba3c4f3cbeff333aa5dd7d6f"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a964a48c0ba3c4f3cbeff333aa5dd7d6f"></a>该指标用于统计测量对象当前磁盘已使用的inode空间量。</p>
<p id="zh-cn_topic_0084814075_p31351624203716"><a name="zh-cn_topic_0084814075_p31351624203716"></a><a name="zh-cn_topic_0084814075_p31351624203716"></a>采集方式（Linux）：执行df -i命令，查看IUsed列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</td>
<td class="cellrowborder" valign="top" width="13.700000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ac21f06dacf11428da8ad15257903cc2f"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ac21f06dacf11428da8ad15257903cc2f"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_ac21f06dacf11428da8ad15257903cc2f"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.639999999999999%" headers="mcps1.2.7.1.5 "><p id="p21506128367"><a name="p21506128367"></a><a name="p21506128367"></a><span id="text14178313191"><a name="text14178313191"></a><a name="text14178313191"></a>云服务器</span> - 挂载点</p>
</td>
<td class="cellrowborder" valign="top" width="13.750000000000002%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p884926418"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p884926418"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p884926418"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row1362175683411"><td class="cellrowborder" valign="top" width="12.97%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1730419411353"><a name="zh-cn_topic_0084814075_p1730419411353"></a><a name="zh-cn_topic_0084814075_p1730419411353"></a>disk_inodesUsedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_aecb1139b3e694480b09dcb590ce395ed"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_aecb1139b3e694480b09dcb590ce395ed"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_aecb1139b3e694480b09dcb590ce395ed"></a>(Agent) inode已使用占比</p>
</td>
<td class="cellrowborder" valign="top" width="34.28%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_af7d7bf90b33c4ab8a734dca22a9b0803"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_af7d7bf90b33c4ab8a734dca22a9b0803"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_af7d7bf90b33c4ab8a734dca22a9b0803"></a>该指标用于统计测量对象当前磁盘已使用的inode占比。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p626484910565"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p626484910565"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p626484910565"></a>单位：百分比</p>
<p id="zh-cn_topic_0084814075_p1791822633712"><a name="zh-cn_topic_0084814075_p1791822633712"></a><a name="zh-cn_topic_0084814075_p1791822633712"></a>采集方式（Linux）：执行df -i命令，查看IUse%列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</td>
<td class="cellrowborder" valign="top" width="13.700000000000001%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a976d888f07a94317952cbd3259ba9a2d"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a976d888f07a94317952cbd3259ba9a2d"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a976d888f07a94317952cbd3259ba9a2d"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.639999999999999%" headers="mcps1.2.7.1.5 "><p id="p9949141419362"><a name="p9949141419362"></a><a name="p9949141419362"></a><span id="text1032071517915"><a name="text1032071517915"></a><a name="text1032071517915"></a>云服务器</span> - 挂载点</p>
</td>
<td class="cellrowborder" valign="top" width="13.750000000000002%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11491117710"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11491117710"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11491117710"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>Windows系统暂不支持文件系统类监控指标。

## 操作系统监控指标：网卡<a name="section1766510514324"></a>

**表 7**  网卡相关监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table925754617116"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row15262846141118"><th class="cellrowborder" valign="top" width="13.11868813118688%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p171851310486"><a name="zh-cn_topic_0084814075_p171851310486"></a><a name="zh-cn_topic_0084814075_p171851310486"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.48855114488551%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1326424661114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1326424661114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1326424661114"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.6065393460654%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p192660460118"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p192660460118"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p192660460118"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="13.338666133386662%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p526712460111"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p526712460111"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p526712460111"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.68893110688931%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p326235015116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p326235015116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p326235015116"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="13.758624137586242%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p926219501611"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p926219501611"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p926219501611"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row52701046191115"><td class="cellrowborder" valign="top" width="13.11868813118688%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p191851310883"><a name="zh-cn_topic_0084814075_p191851310883"></a><a name="zh-cn_topic_0084814075_p191851310883"></a>net_bitRecv</p>
</td>
<td class="cellrowborder" valign="top" width="14.48855114488551%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p112711946161117"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p112711946161117"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p112711946161117"></a>(Agent) 出网带宽</p>
</td>
<td class="cellrowborder" valign="top" width="34.6065393460654%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p12729154165011"><a name="zh-cn_topic_0084814075_p12729154165011"></a><a name="zh-cn_topic_0084814075_p12729154165011"></a>该指标用于统计测量对象网卡每秒发送的比特数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12195165575819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12195165575819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12195165575819"></a>单位：bit/s</p>
<a name="zh-cn_topic_0084814075_ul7241184533819"></a><a name="zh-cn_topic_0084814075_ul7241184533819"></a><ul id="zh-cn_topic_0084814075_ul7241184533819"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.338666133386662%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p42762467110"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p42762467110"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p42762467110"></a>≥ 0 bit/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.68893110688931%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p62621850618"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p62621850618"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p62621850618"></a><span id="text114080191392"><a name="text114080191392"></a><a name="text114080191392"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.758624137586242%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p42627501114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p42627501114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p42627501114"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row4280144612117"><td class="cellrowborder" valign="top" width="13.11868813118688%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p21850108820"><a name="zh-cn_topic_0084814075_p21850108820"></a><a name="zh-cn_topic_0084814075_p21850108820"></a>net_bitSent</p>
</td>
<td class="cellrowborder" valign="top" width="14.48855114488551%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2281174621114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2281174621114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2281174621114"></a>(Agent) 入网带宽</p>
</td>
<td class="cellrowborder" valign="top" width="34.6065393460654%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p117291054185012"><a name="zh-cn_topic_0084814075_p117291054185012"></a><a name="zh-cn_topic_0084814075_p117291054185012"></a>该指标用于统计测量对象网卡每秒接收的比特数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p119005035917"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p119005035917"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p119005035917"></a>单位：bit/s</p>
<a name="zh-cn_topic_0084814075_ul15438713143910"></a><a name="zh-cn_topic_0084814075_ul15438713143910"></a><ul id="zh-cn_topic_0084814075_ul15438713143910"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.338666133386662%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p351716217142"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p351716217142"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p351716217142"></a>≥ 0 bit/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.68893110688931%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p35151601923"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p35151601923"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p35151601923"></a><span id="text936182115911"><a name="text936182115911"></a><a name="text936182115911"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.758624137586242%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10515200127"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10515200127"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10515200127"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1328934621110"><td class="cellrowborder" valign="top" width="13.11868813118688%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p318511101687"><a name="zh-cn_topic_0084814075_p318511101687"></a><a name="zh-cn_topic_0084814075_p318511101687"></a>net_packetRecv</p>
</td>
<td class="cellrowborder" valign="top" width="14.48855114488551%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14290124641113"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14290124641113"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14290124641113"></a>(Agent) 网卡包接收速率</p>
</td>
<td class="cellrowborder" valign="top" width="34.6065393460654%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4292134691112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4292134691112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4292134691112"></a>该指标用于统计测量对象网卡每秒接收的数据包数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1251716155915"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1251716155915"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1251716155915"></a>单位：Counts/s</p>
<a name="zh-cn_topic_0084814075_ul117291816103919"></a><a name="zh-cn_topic_0084814075_ul117291816103919"></a><ul id="zh-cn_topic_0084814075_ul117291816103919"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.338666133386662%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4297104616118"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4297104616118"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4297104616118"></a>≥ 0 Counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.68893110688931%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p021851828"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p021851828"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p021851828"></a><span id="text9879142219911"><a name="text9879142219911"></a><a name="text9879142219911"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.758624137586242%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p92186113215"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p92186113215"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p92186113215"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row0298154621113"><td class="cellrowborder" valign="top" width="13.11868813118688%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p673055425015"><a name="zh-cn_topic_0084814075_p673055425015"></a><a name="zh-cn_topic_0084814075_p673055425015"></a>net_packetSent</p>
</td>
<td class="cellrowborder" valign="top" width="14.48855114488551%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p829924613116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p829924613116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p829924613116"></a>(Agent) 网卡包发送速率</p>
</td>
<td class="cellrowborder" valign="top" width="34.6065393460654%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13300194619118"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13300194619118"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13300194619118"></a>该指标用于统计测量对象网卡每秒发送的数据包数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1365112114592"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1365112114592"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1365112114592"></a>单位：Counts/s</p>
<a name="zh-cn_topic_0084814075_ul6600141843917"></a><a name="zh-cn_topic_0084814075_ul6600141843917"></a><ul id="zh-cn_topic_0084814075_ul6600141843917"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.338666133386662%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p030515462112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p030515462112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p030515462112"></a>≥ 0 Counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.68893110688931%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18966811226"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18966811226"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18966811226"></a><span id="text112225262915"><a name="text112225262915"></a><a name="text112225262915"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.758624137586242%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10966315218"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10966315218"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10966315218"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1513145363017"><td class="cellrowborder" valign="top" width="13.11868813118688%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p273015414504"><a name="zh-cn_topic_0084814075_p273015414504"></a><a name="zh-cn_topic_0084814075_p273015414504"></a>net_errin</p>
</td>
<td class="cellrowborder" valign="top" width="14.48855114488551%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p73131027132512"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p73131027132512"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p73131027132512"></a>(Agent) 接收误包率</p>
</td>
<td class="cellrowborder" valign="top" width="34.6065393460654%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9313172719250"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9313172719250"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p9313172719250"></a>该指标用于统计测量对象网卡每秒接收的错误数据包数量占所接收的数据包的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188355280597"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188355280597"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p188355280597"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul83991822163915"></a><a name="zh-cn_topic_0084814075_ul83991822163915"></a><ul id="zh-cn_topic_0084814075_ul83991822163915"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.338666133386662%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3369579281"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3369579281"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p3369579281"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.68893110688931%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1669318212218"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1669318212218"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1669318212218"></a><span id="text8557112819910"><a name="text8557112819910"></a><a name="text8557112819910"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.758624137586242%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19693821220"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19693821220"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p19693821220"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1950851143011"><td class="cellrowborder" valign="top" width="13.11868813118688%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p5731125414508"><a name="zh-cn_topic_0084814075_p5731125414508"></a><a name="zh-cn_topic_0084814075_p5731125414508"></a>net_errout</p>
</td>
<td class="cellrowborder" valign="top" width="14.48855114488551%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p155501224102512"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p155501224102512"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p155501224102512"></a>(Agent) 发送误包率</p>
</td>
<td class="cellrowborder" valign="top" width="34.6065393460654%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1563924505919"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1563924505919"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1563924505919"></a>该指标用于统计测量对象网卡每秒发送的错误数据包数量占所发送的数据包的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125501924112513"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125501924112513"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p125501924112513"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul861123718398"></a><a name="zh-cn_topic_0084814075_ul861123718398"></a><ul id="zh-cn_topic_0084814075_ul861123718398"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.338666133386662%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204221754161213"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204221754161213"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204221754161213"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.68893110688931%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12801931621"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12801931621"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12801931621"></a><span id="text163666323914"><a name="text163666323914"></a><a name="text163666323914"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.758624137586242%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p88021311217"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p88021311217"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p88021311217"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row134221248529"><td class="cellrowborder" valign="top" width="13.11868813118688%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p97311654145016"><a name="zh-cn_topic_0084814075_p97311654145016"></a><a name="zh-cn_topic_0084814075_p97311654145016"></a>net_dropin</p>
</td>
<td class="cellrowborder" valign="top" width="14.48855114488551%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1216444673017"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1216444673017"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1216444673017"></a>(Agent) 接收丢包率</p>
</td>
<td class="cellrowborder" valign="top" width="34.6065393460654%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p216474618302"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p216474618302"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p216474618302"></a>该指标用于统计测量对象网卡每秒接收并已丢弃的数据包数量占所接收的数据包的比率</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p58891549205917"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p58891549205917"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p58891549205917"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul14377393390"></a><a name="zh-cn_topic_0084814075_ul14377393390"></a><ul id="zh-cn_topic_0084814075_ul14377393390"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.338666133386662%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10992115701213"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10992115701213"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10992115701213"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.68893110688931%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p176841041427"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p176841041427"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p176841041427"></a><span id="text19722163519915"><a name="text19722163519915"></a><a name="text19722163519915"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.758624137586242%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p968454322"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p968454322"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p968454322"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row115851812525"><td class="cellrowborder" valign="top" width="13.11868813118688%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p47311654105013"><a name="zh-cn_topic_0084814075_p47311654105013"></a><a name="zh-cn_topic_0084814075_p47311654105013"></a>net_dropout</p>
</td>
<td class="cellrowborder" valign="top" width="14.48855114488551%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p16466149153017"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p16466149153017"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p16466149153017"></a>(Agent) 发送丢包率</p>
</td>
<td class="cellrowborder" valign="top" width="34.6065393460654%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3266135619131"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3266135619131"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3266135619131"></a>该指标用于统计测量对象网卡每秒发送并已丢弃的数据包数量占所发送的数据包的比率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1097754165914"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1097754165914"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1097754165914"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul1133016418390"></a><a name="zh-cn_topic_0084814075_ul1133016418390"></a><ul id="zh-cn_topic_0084814075_ul1133016418390"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.338666133386662%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p139272012134"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p139272012134"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p139272012134"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.68893110688931%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4279951221"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4279951221"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4279951221"></a><span id="text1161103918917"><a name="text1161103918917"></a><a name="text1161103918917"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.758624137586242%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p427914519217"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p427914519217"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p427914519217"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 操作系统监控指标：NTP<a name="section12290615193311"></a>

**表 8**  NTP类监控指标说明

<a name="table15802173323719"></a>
<table><thead align="left"><tr id="row9803103393712"><th class="cellrowborder" valign="top" width="13.11868813118688%" id="mcps1.2.7.1.1"><p id="p280373353710"><a name="p280373353710"></a><a name="p280373353710"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.638536146385361%" id="mcps1.2.7.1.2"><p id="p188031033173716"><a name="p188031033173716"></a><a name="p188031033173716"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="34.8965103489651%" id="mcps1.2.7.1.3"><p id="p980313311375"><a name="p980313311375"></a><a name="p980313311375"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="12.818718128187182%" id="mcps1.2.7.1.4"><p id="p12803123353715"><a name="p12803123353715"></a><a name="p12803123353715"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.70892910708929%" id="mcps1.2.7.1.5"><p id="p1380393314375"><a name="p1380393314375"></a><a name="p1380393314375"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="13.818618138186181%" id="mcps1.2.7.1.6"><p id="p19803833193715"><a name="p19803833193715"></a><a name="p19803833193715"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="row128043331371"><td class="cellrowborder" valign="top" width="13.11868813118688%" headers="mcps1.2.7.1.1 "><p id="p18448751101416"><a name="p18448751101416"></a><a name="p18448751101416"></a>ntp_offset</p>
</td>
<td class="cellrowborder" valign="top" width="14.638536146385361%" headers="mcps1.2.7.1.2 "><p id="p102120911511"><a name="p102120911511"></a><a name="p102120911511"></a>(Agent) NTP偏移量</p>
</td>
<td class="cellrowborder" valign="top" width="34.8965103489651%" headers="mcps1.2.7.1.3 "><p id="p8804183310375"><a name="p8804183310375"></a><a name="p8804183310375"></a>该指标用于统计测量对象当前NTP偏移量。</p>
<p id="p580413334374"><a name="p580413334374"></a><a name="p580413334374"></a>单位：ms</p>
<p id="p18041733183713"><a name="p18041733183713"></a><a name="p18041733183713"></a>采集方式（Linux）：执行chronyc sources -v命令，获取偏移量。</p>
</td>
<td class="cellrowborder" valign="top" width="12.818718128187182%" headers="mcps1.2.7.1.4 "><p id="p11804133319373"><a name="p11804133319373"></a><a name="p11804133319373"></a>≥ 0 ms</p>
</td>
<td class="cellrowborder" valign="top" width="10.70892910708929%" headers="mcps1.2.7.1.5 "><p id="p280414333374"><a name="p280414333374"></a><a name="p280414333374"></a><span id="text1129334314912"><a name="text1129334314912"></a><a name="text1129334314912"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.818618138186181%" headers="mcps1.2.7.1.6 "><p id="p1880416337379"><a name="p1880416337379"></a><a name="p1880416337379"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 操作系统监控指标：TCP<a name="section13448184811331"></a>

**表 9**  TCP类监控指标说明

<a name="table1190118812389"></a>
<table><thead align="left"><tr id="row1902118143819"><th class="cellrowborder" valign="top" width="12.89%" id="mcps1.2.7.1.1"><p id="p15902287386"><a name="p15902287386"></a><a name="p15902287386"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.740000000000004%" id="mcps1.2.7.1.2"><p id="p390317811385"><a name="p390317811385"></a><a name="p390317811385"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="35.53000000000001%" id="mcps1.2.7.1.3"><p id="p7903138123811"><a name="p7903138123811"></a><a name="p7903138123811"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="12.24%" id="mcps1.2.7.1.4"><p id="p29035816388"><a name="p29035816388"></a><a name="p29035816388"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.660000000000002%" id="mcps1.2.7.1.5"><p id="p190419853816"><a name="p190419853816"></a><a name="p190419853816"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="13.940000000000003%" id="mcps1.2.7.1.6"><p id="p6904684388"><a name="p6904684388"></a><a name="p6904684388"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="row9904987389"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p6904108123816"><a name="p6904108123816"></a><a name="p6904108123816"></a>net_tcp_total</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p18904118183819"><a name="p18904118183819"></a><a name="p18904118183819"></a>(Agent) TCP TOTAL</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p590411883819"><a name="p590411883819"></a><a name="p590411883819"></a>该指标用于统计测量对象所有状态的TCP连接数总和。</p>
<p id="p59051683381"><a name="p59051683381"></a><a name="p59051683381"></a>单位：Count</p>
<a name="ul11594115714262"></a><a name="ul11594115714262"></a><ul id="ul11594115714262"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p79056811387"><a name="p79056811387"></a><a name="p79056811387"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p19051843810"><a name="p19051843810"></a><a name="p19051843810"></a><span id="text21687455910"><a name="text21687455910"></a><a name="text21687455910"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p89051586382"><a name="p89051586382"></a><a name="p89051586382"></a>1分钟</p>
</td>
</tr>
<tr id="row6519828181715"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p105193288178"><a name="p105193288178"></a><a name="p105193288178"></a>net_tcp_established</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p1452042881713"><a name="p1452042881713"></a><a name="p1452042881713"></a>(Agent) TCP ESTABLISHED</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p115206283179"><a name="p115206283179"></a><a name="p115206283179"></a>该指标用于统计测量对象处于ESTABLISHED状态的TCP连接数量。</p>
<p id="p6440104013246"><a name="p6440104013246"></a><a name="p6440104013246"></a>单位：Count</p>
<a name="ul47962144278"></a><a name="ul47962144278"></a><ul id="ul47962144278"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p391013569236"><a name="p391013569236"></a><a name="p391013569236"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p9910115616236"><a name="p9910115616236"></a><a name="p9910115616236"></a><span id="text799514815913"><a name="text799514815913"></a><a name="text799514815913"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p89108564230"><a name="p89108564230"></a><a name="p89108564230"></a>1分钟</p>
</td>
</tr>
<tr id="row5520528151715"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p55201828111712"><a name="p55201828111712"></a><a name="p55201828111712"></a>net_tcp_sys_sent</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p105201928121718"><a name="p105201928121718"></a><a name="p105201928121718"></a>(Agent) TCP SYS_SENT</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p1452062861716"><a name="p1452062861716"></a><a name="p1452062861716"></a>该指标用于统计测量对象处于请求连接状态的TCP连接数量。</p>
<p id="p637334314244"><a name="p637334314244"></a><a name="p637334314244"></a>单位：Count</p>
<a name="ul20289418162714"></a><a name="ul20289418162714"></a><ul id="ul20289418162714"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p344552518248"><a name="p344552518248"></a><a name="p344552518248"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p7446182515240"><a name="p7446182515240"></a><a name="p7446182515240"></a><span id="text5448151190"><a name="text5448151190"></a><a name="text5448151190"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p144616253243"><a name="p144616253243"></a><a name="p144616253243"></a>1分钟</p>
</td>
</tr>
<tr id="row175219281171"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p1152119287171"><a name="p1152119287171"></a><a name="p1152119287171"></a>net_tcp_sys_recv</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p552172810179"><a name="p552172810179"></a><a name="p552172810179"></a>(Agent) TCP SYS_RECV</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p12521152812172"><a name="p12521152812172"></a><a name="p12521152812172"></a>该指标用于统计测量对象服务器端收到的请求连接的TCP数量。</p>
<p id="p8490124618244"><a name="p8490124618244"></a><a name="p8490124618244"></a>单位：Count</p>
<a name="ul138061121162713"></a><a name="ul138061121162713"></a><ul id="ul138061121162713"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p1468627122416"><a name="p1468627122416"></a><a name="p1468627122416"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p164691627132416"><a name="p164691627132416"></a><a name="p164691627132416"></a><span id="text5569581912"><a name="text5569581912"></a><a name="text5569581912"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p13469202710246"><a name="p13469202710246"></a><a name="p13469202710246"></a>1分钟</p>
</td>
</tr>
<tr id="row9521152817174"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p8521142891718"><a name="p8521142891718"></a><a name="p8521142891718"></a>net_tcp_fin_wait1</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p13521122815175"><a name="p13521122815175"></a><a name="p13521122815175"></a>(Agent) TCP FIN_WAIT1</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p1452202861710"><a name="p1452202861710"></a><a name="p1452202861710"></a>该指标用于统计测量对象客户端主动关闭且没有收到服务端ACK的TCP连接数量。</p>
<p id="p7754174816241"><a name="p7754174816241"></a><a name="p7754174816241"></a>单位：Count</p>
<a name="ul11545202562718"></a><a name="ul11545202562718"></a><ul id="ul11545202562718"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p623832802416"><a name="p623832802416"></a><a name="p623832802416"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p1923812812245"><a name="p1923812812245"></a><a name="p1923812812245"></a><span id="text137302001018"><a name="text137302001018"></a><a name="text137302001018"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p6238328202419"><a name="p6238328202419"></a><a name="p6238328202419"></a>1分钟</p>
</td>
</tr>
<tr id="row625513224170"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p18256192213178"><a name="p18256192213178"></a><a name="p18256192213178"></a>net_tcp_fin_wait2</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p0256922191714"><a name="p0256922191714"></a><a name="p0256922191714"></a>(Agent) TCP FIN_WAIT2</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p8256222201717"><a name="p8256222201717"></a><a name="p8256222201717"></a>该指标用于统计测量对象处于FIN_WAIT2状态的TCP连接数量。</p>
<p id="p1413205111247"><a name="p1413205111247"></a><a name="p1413205111247"></a>单位：Count</p>
<a name="ul107553214276"></a><a name="ul107553214276"></a><ul id="ul107553214276"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p385762818243"><a name="p385762818243"></a><a name="p385762818243"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p285719283242"><a name="p285719283242"></a><a name="p285719283242"></a><span id="text183801845108"><a name="text183801845108"></a><a name="text183801845108"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p1185717280241"><a name="p1185717280241"></a><a name="p1185717280241"></a>1分钟</p>
</td>
</tr>
<tr id="row176431172716"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0000001531134066_p7769124765414"><a name="zh-cn_topic_0000001531134066_p7769124765414"></a><a name="zh-cn_topic_0000001531134066_p7769124765414"></a>net_tcp_time_wait</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0000001531134066_p1376910476547"><a name="zh-cn_topic_0000001531134066_p1376910476547"></a><a name="zh-cn_topic_0000001531134066_p1376910476547"></a>(Agent) TCP TIME_WAIT</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0000001531134066_p5769114795417"><a name="zh-cn_topic_0000001531134066_p5769114795417"></a><a name="zh-cn_topic_0000001531134066_p5769114795417"></a>该指标用于统计测量对象处于TIME_WAIT状态的TCP连接数量。</p>
<p id="p104177342710"><a name="p104177342710"></a><a name="p104177342710"></a>单位：Count</p>
<a name="zh-cn_topic_0000001531134066_ul9453193313156"></a><a name="zh-cn_topic_0000001531134066_ul9453193313156"></a><ul id="zh-cn_topic_0000001531134066_ul9453193313156"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p15635113711714"><a name="p15635113711714"></a><a name="p15635113711714"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p1635133719711"><a name="p1635133719711"></a><a name="p1635133719711"></a><span id="text363515379715"><a name="text363515379715"></a><a name="text363515379715"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p263511374716"><a name="p263511374716"></a><a name="p263511374716"></a>1分钟</p>
</td>
</tr>
<tr id="row22561622101712"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p132566224174"><a name="p132566224174"></a><a name="p132566224174"></a>net_tcp_close</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p1325602212175"><a name="p1325602212175"></a><a name="p1325602212175"></a>(Agent) TCP CLOSE</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p13256102261712"><a name="p13256102261712"></a><a name="p13256102261712"></a>该指标用于统计测量对象关闭的或未打开的TCP连接数量。</p>
<p id="p821715413246"><a name="p821715413246"></a><a name="p821715413246"></a>单位：Count</p>
<a name="ul1646683511271"></a><a name="ul1646683511271"></a><ul id="ul1646683511271"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p12637129102415"><a name="p12637129102415"></a><a name="p12637129102415"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p7637329102413"><a name="p7637329102413"></a><a name="p7637329102413"></a><span id="text108169614100"><a name="text108169614100"></a><a name="text108169614100"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p176371529192411"><a name="p176371529192411"></a><a name="p176371529192411"></a>1分钟</p>
</td>
</tr>
<tr id="row12213454777"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0000001531134066_p476994710544"><a name="zh-cn_topic_0000001531134066_p476994710544"></a><a name="zh-cn_topic_0000001531134066_p476994710544"></a>net_tcp_close_wait</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0000001531134066_p3769154711548"><a name="zh-cn_topic_0000001531134066_p3769154711548"></a><a name="zh-cn_topic_0000001531134066_p3769154711548"></a>(Agent) TCP CLOSE_WAIT</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0000001531134066_p1876964720547"><a name="zh-cn_topic_0000001531134066_p1876964720547"></a><a name="zh-cn_topic_0000001531134066_p1876964720547"></a>该指标用于统计测量对象处于CLOSE_WAIT状态的TCP连接数量。</p>
<p id="p7367201889"><a name="p7367201889"></a><a name="p7367201889"></a>单位：Count</p>
<a name="zh-cn_topic_0000001531134066_ul7273192771517"></a><a name="zh-cn_topic_0000001531134066_ul7273192771517"></a><ul id="zh-cn_topic_0000001531134066_ul7273192771517"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p103611239814"><a name="p103611239814"></a><a name="p103611239814"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p73616231811"><a name="p73616231811"></a><a name="p73616231811"></a><span id="text536112231782"><a name="text536112231782"></a><a name="text536112231782"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p236252310813"><a name="p236252310813"></a><a name="p236252310813"></a>1分钟</p>
</td>
</tr>
<tr id="row136373771716"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p836323719173"><a name="p836323719173"></a><a name="p836323719173"></a>net_tcp_last_ack</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p83631937141710"><a name="p83631937141710"></a><a name="p83631937141710"></a>(Agent) TCP LAST_ACK</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p23631137201719"><a name="p23631137201719"></a><a name="p23631137201719"></a>该指标用于统计测量对象被动关闭等待ACK报文的TCP连接数量。</p>
<p id="p621112576243"><a name="p621112576243"></a><a name="p621112576243"></a>单位：Count</p>
<a name="ul522133932712"></a><a name="ul522133932712"></a><ul id="ul522133932712"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p4408030112411"><a name="p4408030112411"></a><a name="p4408030112411"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p1940819301247"><a name="p1940819301247"></a><a name="p1940819301247"></a><span id="text10401310171016"><a name="text10401310171016"></a><a name="text10401310171016"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p04089308247"><a name="p04089308247"></a><a name="p04089308247"></a>1分钟</p>
</td>
</tr>
<tr id="row17364237191713"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p5364103717178"><a name="p5364103717178"></a><a name="p5364103717178"></a>net_tcp_listen</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p1136413715177"><a name="p1136413715177"></a><a name="p1136413715177"></a>(Agent) TCP LISTEN</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p3364037161720"><a name="p3364037161720"></a><a name="p3364037161720"></a>该指标用于统计测量对象处于LISTEN状态的TCP连接数量。</p>
<p id="p61619020258"><a name="p61619020258"></a><a name="p61619020258"></a>单位：Count</p>
<a name="ul91571543182716"></a><a name="ul91571543182716"></a><ul id="ul91571543182716"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p111671314249"><a name="p111671314249"></a><a name="p111671314249"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p1216715318244"><a name="p1216715318244"></a><a name="p1216715318244"></a><span id="text12515181320104"><a name="text12515181320104"></a><a name="text12515181320104"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p1167131152417"><a name="p1167131152417"></a><a name="p1167131152417"></a>1分钟</p>
</td>
</tr>
<tr id="row390528183811"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p9679163592011"><a name="p9679163592011"></a><a name="p9679163592011"></a>net_tcp_closing</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p17912195741914"><a name="p17912195741914"></a><a name="p17912195741914"></a>(Agent) TCP CLOSING</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p1906983388"><a name="p1906983388"></a><a name="p1906983388"></a>该指标用于统计测量对象处于服务端和客户端同时主动关闭状态的TCP连接数量。</p>
<p id="p3906982388"><a name="p3906982388"></a><a name="p3906982388"></a>单位：Count</p>
<a name="ul1168984813270"></a><a name="ul1168984813270"></a><ul id="ul1168984813270"><li>采集方式（Linux）：通过/proc/net/tcp文件获取到所有状态的TCP连接，再统计每个状态的连接数量。</li><li>采集方式（Windows）：通过WindowsAPI GetTcpTable2获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p590611817386"><a name="p590611817386"></a><a name="p590611817386"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p1790615818388"><a name="p1790615818388"></a><a name="p1790615818388"></a><span id="text3100171711014"><a name="text3100171711014"></a><a name="text3100171711014"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p13906584387"><a name="p13906584387"></a><a name="p13906584387"></a>1分钟</p>
</td>
</tr>
<tr id="row790628103820"><td class="cellrowborder" valign="top" width="12.89%" headers="mcps1.2.7.1.1 "><p id="p152151562018"><a name="p152151562018"></a><a name="p152151562018"></a>net_tcp_retrans</p>
</td>
<td class="cellrowborder" valign="top" width="14.740000000000004%" headers="mcps1.2.7.1.2 "><p id="p2090713816386"><a name="p2090713816386"></a><a name="p2090713816386"></a>(Agent) TCP重传率</p>
</td>
<td class="cellrowborder" valign="top" width="35.53000000000001%" headers="mcps1.2.7.1.3 "><p id="p129074812386"><a name="p129074812386"></a><a name="p129074812386"></a>该指标用于统计测量对象重新发送的报文数与总发送的报文数之间的比值。</p>
<p id="p49074810383"><a name="p49074810383"></a><a name="p49074810383"></a>单位：百分比</p>
<a name="ul201294012288"></a><a name="ul201294012288"></a><ul id="ul201294012288"><li>采集方式（Linux）：通过从/proc/net/snmp文件中获取对应的数据，计算采集周期内发送包数和重传包数的比值得出。</li><li>采集方式（Windows）：重传率通过WindowsAPI GetTcpStatistics获取</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.7.1.4 "><p id="p990711817385"><a name="p990711817385"></a><a name="p990711817385"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.660000000000002%" headers="mcps1.2.7.1.5 "><p id="p29071989383"><a name="p29071989383"></a><a name="p29071989383"></a><span id="text1355591991013"><a name="text1355591991013"></a><a name="text1355591991013"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="13.940000000000003%" headers="mcps1.2.7.1.6 "><p id="p4907188153812"><a name="p4907188153812"></a><a name="p4907188153812"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 操作系统监控指标：GPU<a name="section282013415343"></a>

**表 10**  GPU类监控指标说明

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table760319497509"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row860364919508"><th class="cellrowborder" valign="top" width="12.839999999999998%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p32277610918"><a name="zh-cn_topic_0084814075_p32277610918"></a><a name="zh-cn_topic_0084814075_p32277610918"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.680000000000001%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14302112714513"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14302112714513"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14302112714513"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="35.61%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p33041727195112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p33041727195112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p33041727195112"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="12.31%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1430742725119"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1430742725119"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1430742725119"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.91%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52072618319"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52072618319"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p52072618319"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="13.65%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p620726332"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p620726332"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p620726332"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="row746982084018"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p047052074016"><a name="p047052074016"></a><a name="p047052074016"></a>gpu_status</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p14470152019409"><a name="p14470152019409"></a><a name="p14470152019409"></a>gpu健康状态</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p1790545312405"><a name="p1790545312405"></a><a name="p1790545312405"></a>该指标用于统计虚拟机上GPU健康状态，是一个综合指标。</p>
<p id="p1328210459435"><a name="p1328210459435"></a><a name="p1328210459435"></a>该指标无单位。</p>
<a name="ul3933536132120"></a><a name="ul3933536132120"></a><ul id="ul3933536132120"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><a name="ul71981855184210"></a><a name="ul71981855184210"></a><ul id="ul71981855184210"><li>0：代表健康</li><li>1：代表亚健康</li><li>2：代表故障</li></ul>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul159221818184112"></a><a name="ul159221818184112"></a><ul id="ul159221818184112"><li><span id="text20708923101011"><a name="text20708923101011"></a><a name="text20708923101011"></a>云服务器</span></li><li><span id="text207862254109"><a name="text207862254109"></a><a name="text207862254109"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p127452874211"><a name="p127452874211"></a><a name="p127452874211"></a>1分钟</p>
</td>
</tr>
<tr id="row13470102024017"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p11470192084013"><a name="p11470192084013"></a><a name="p11470192084013"></a>gpu_usage_encoder</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p105491340144017"><a name="p105491340144017"></a><a name="p105491340144017"></a>编码使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p1490545394013"><a name="p1490545394013"></a><a name="p1490545394013"></a>该指标用于统计该GPU的编码能力使用率。</p>
<p id="p970515244320"><a name="p970515244320"></a><a name="p970515244320"></a>单位：百分比</p>
<a name="ul118046496229"></a><a name="ul118046496229"></a><ul id="ul118046496229"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p4471162024014"><a name="p4471162024014"></a><a name="p4471162024014"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul4253925164118"></a><a name="ul4253925164118"></a><ul id="ul4253925164118"><li><span id="text82502287107"><a name="text82502287107"></a><a name="text82502287107"></a>云服务器</span></li><li><span id="text827793117106"><a name="text827793117106"></a><a name="text827793117106"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p105058106426"><a name="p105058106426"></a><a name="p105058106426"></a>1分钟</p>
</td>
</tr>
<tr id="row1347118205404"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p8471112054017"><a name="p8471112054017"></a><a name="p8471112054017"></a>gpu_usage_decoder</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p185491240184018"><a name="p185491240184018"></a><a name="p185491240184018"></a>解码使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p590515319400"><a name="p590515319400"></a><a name="p590515319400"></a>该指标用于统计该GPU的解码能力使用率。</p>
<p id="p19170956174316"><a name="p19170956174316"></a><a name="p19170956174316"></a>单位：百分比</p>
<a name="ul1528833932413"></a><a name="ul1528833932413"></a><ul id="ul1528833932413"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p16471162013409"><a name="p16471162013409"></a><a name="p16471162013409"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul129509272419"></a><a name="ul129509272419"></a><ul id="ul129509272419"><li><span id="text168821034131013"><a name="text168821034131013"></a><a name="text168821034131013"></a>云服务器</span></li><li><span id="text34971737141015"><a name="text34971737141015"></a><a name="text34971737141015"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p277841554218"><a name="p277841554218"></a><a name="p277841554218"></a>1分钟</p>
</td>
</tr>
<tr id="row547182044019"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p747216205408"><a name="p747216205408"></a><a name="p747216205408"></a>gpu_volatile_correctable</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p14549840194014"><a name="p14549840194014"></a><a name="p14549840194014"></a>可纠正ECC错误数量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p1990615539406"><a name="p1990615539406"></a><a name="p1990615539406"></a>该指标用于统计该GPU重置以来可纠正的ECC错误数量，每次重置后归0。</p>
<p id="p1311519313444"><a name="p1311519313444"></a><a name="p1311519313444"></a>单位：个。</p>
<a name="ul1824512444246"></a><a name="ul1824512444246"></a><ul id="ul1824512444246"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p1472182010406"><a name="p1472182010406"></a><a name="p1472182010406"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul16519143184111"></a><a name="ul16519143184111"></a><ul id="ul16519143184111"><li><span id="text17530164013104"><a name="text17530164013104"></a><a name="text17530164013104"></a>云服务器</span></li><li><span id="text665014423102"><a name="text665014423102"></a><a name="text665014423102"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p14710101624211"><a name="p14710101624211"></a><a name="p14710101624211"></a>1分钟</p>
</td>
</tr>
<tr id="row947202012407"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p154721820154011"><a name="p154721820154011"></a><a name="p154721820154011"></a>gpu_volatile_uncorrectable</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p18549240174019"><a name="p18549240174019"></a><a name="p18549240174019"></a>不可纠正ECC错误数量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p10906253144011"><a name="p10906253144011"></a><a name="p10906253144011"></a>该指标用于统计该GPU重置以来不可纠正的ECC错误数量，每次重置后归0。</p>
<p id="p19626810174413"><a name="p19626810174413"></a><a name="p19626810174413"></a>单位：个</p>
<a name="ul1499314792416"></a><a name="ul1499314792416"></a><ul id="ul1499314792416"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p8473220154012"><a name="p8473220154012"></a><a name="p8473220154012"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul15215183620414"></a><a name="ul15215183620414"></a><ul id="ul15215183620414"><li><span id="text1495194418103"><a name="text1495194418103"></a><a name="text1495194418103"></a>云服务器</span></li><li><span id="text137694951020"><a name="text137694951020"></a><a name="text137694951020"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p761271794213"><a name="p761271794213"></a><a name="p761271794213"></a>1分钟</p>
</td>
</tr>
<tr id="row947312017403"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p547332044012"><a name="p547332044012"></a><a name="p547332044012"></a>gpu_aggregate_correctable</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p15549174084015"><a name="p15549174084015"></a><a name="p15549174084015"></a>累计可纠正ECC错误数量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p16906205374014"><a name="p16906205374014"></a><a name="p16906205374014"></a>该指标用于统计该GPU累计的可纠正ECC错误数量。</p>
<p id="p13440131354414"><a name="p13440131354414"></a><a name="p13440131354414"></a>单位：个</p>
<a name="ul17370452132412"></a><a name="ul17370452132412"></a><ul id="ul17370452132412"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p04736208408"><a name="p04736208408"></a><a name="p04736208408"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul2104839124118"></a><a name="ul2104839124118"></a><ul id="ul2104839124118"><li><span id="text14806165113104"><a name="text14806165113104"></a><a name="text14806165113104"></a>云服务器</span></li><li><span id="text19141254101013"><a name="text19141254101013"></a><a name="text19141254101013"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p844914189422"><a name="p844914189422"></a><a name="p844914189422"></a>1分钟</p>
</td>
</tr>
<tr id="row67221014194019"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p1472219148407"><a name="p1472219148407"></a><a name="p1472219148407"></a>gpu_aggregate_uncorrectable</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p15491740184014"><a name="p15491740184014"></a><a name="p15491740184014"></a>累计不可纠正ECC错误数量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p490619536400"><a name="p490619536400"></a><a name="p490619536400"></a>该指标用于统计该GPU累计的不可纠正ECC错误数量。</p>
<p id="p37291515144416"><a name="p37291515144416"></a><a name="p37291515144416"></a>单位：个</p>
<a name="ul9835955112415"></a><a name="ul9835955112415"></a><ul id="ul9835955112415"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p8722414134012"><a name="p8722414134012"></a><a name="p8722414134012"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul14451743114120"></a><a name="ul14451743114120"></a><ul id="ul14451743114120"><li><span id="text1867118564102"><a name="text1867118564102"></a><a name="text1867118564102"></a>云服务器</span></li><li><span id="text366712081115"><a name="text366712081115"></a><a name="text366712081115"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p1746561974210"><a name="p1746561974210"></a><a name="p1746561974210"></a>1分钟</p>
</td>
</tr>
<tr id="row1572271464010"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p472215145409"><a name="p472215145409"></a><a name="p472215145409"></a>gpu_retired_page_single_bit</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p12550194011402"><a name="p12550194011402"></a><a name="p12550194011402"></a>retired page single bit错误数量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p490665320403"><a name="p490665320403"></a><a name="p490665320403"></a>该指标用于统计该GPU当前卡隔离的单比特页的数量。</p>
<p id="p16986218174416"><a name="p16986218174416"></a><a name="p16986218174416"></a>单位：个</p>
<a name="ul716716210254"></a><a name="ul716716210254"></a><ul id="ul716716210254"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p1972317145409"><a name="p1972317145409"></a><a name="p1972317145409"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul77101746134116"></a><a name="ul77101746134116"></a><ul id="ul77101746134116"><li><span id="text9397144131118"><a name="text9397144131118"></a><a name="text9397144131118"></a>云服务器</span></li><li><span id="text133991165112"><a name="text133991165112"></a><a name="text133991165112"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p14290102017424"><a name="p14290102017424"></a><a name="p14290102017424"></a>1分钟</p>
</td>
</tr>
<tr id="row572318141401"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p187236142406"><a name="p187236142406"></a><a name="p187236142406"></a>gpu_retired_page_double_bit</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p1755024018401"><a name="p1755024018401"></a><a name="p1755024018401"></a>retired page double bit错误数量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p1390612534408"><a name="p1390612534408"></a><a name="p1390612534408"></a>该指标用于统计该GPU当前卡隔离的双比特页的数量。</p>
<p id="p147615218446"><a name="p147615218446"></a><a name="p147615218446"></a>单位：个</p>
<a name="ul1273417511255"></a><a name="ul1273417511255"></a><ul id="ul1273417511255"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p27232014134014"><a name="p27232014134014"></a><a name="p27232014134014"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul10281154934112"></a><a name="ul10281154934112"></a><ul id="ul10281154934112"><li><span id="text1912729111114"><a name="text1912729111114"></a><a name="text1912729111114"></a>云服务器</span></li><li><span id="text04541811141116"><a name="text04541811141116"></a><a name="text04541811141116"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p263172318423"><a name="p263172318423"></a><a name="p263172318423"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1160494935017"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p2736145405012"><a name="zh-cn_topic_0084814075_p2736145405012"></a><a name="zh-cn_topic_0084814075_p2736145405012"></a>gpu_performance_state</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17121531516"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17121531516"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p17121531516"></a>(Agent) 性能状态</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p1773094122317"><a name="zh-cn_topic_0084814075_p1773094122317"></a><a name="zh-cn_topic_0084814075_p1773094122317"></a>该指标用于统计测量对象当前的GPU性能状态。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p57121353125118"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p57121353125118"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p57121353125118"></a>该指标无单位。</p>
<a name="ul1053353619254"></a><a name="ul1053353619254"></a><ul id="ul1053353619254"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1296192392"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1296192392"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1296192392"></a>P0-P15、P32，</p>
<a name="ul111151237134320"></a><a name="ul111151237134320"></a><ul id="ul111151237134320"><li>P0：表示最大性能状态</li><li>P15：表示最小性能状态</li><li>P32：表示状态未知</li></ul>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul7767155612230"></a><a name="ul7767155612230"></a><ul id="ul7767155612230"><li><span id="text12767195614239"><a name="text12767195614239"></a><a name="text12767195614239"></a>云服务器</span></li><li><span id="text576720564238"><a name="text576720564238"></a><a name="text576720564238"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1220811616315"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1220811616315"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1220811616315"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row7604114955016"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p15253828135214"><a name="zh-cn_topic_0084814075_p15253828135214"></a><a name="zh-cn_topic_0084814075_p15253828135214"></a>gpu_usage_mem</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p371205316513"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p371205316513"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p371205316513"></a>(Agent) 显存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1712453175111"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1712453175111"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1712453175111"></a>该指标用于统计测量对象当前的显存使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p834992019534"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p834992019534"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p834992019534"></a>单位：百分比</p>
<a name="ul335262712258"></a><a name="ul335262712258"></a><ul id="ul335262712258"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18712195314515"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18712195314515"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p18712195314515"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul6883856182310"></a><a name="ul6883856182310"></a><ul id="ul6883856182310"><li><span id="text14883115615231"><a name="text14883115615231"></a><a name="text14883115615231"></a>云服务器</span></li><li><span id="text14883185615232"><a name="text14883185615232"></a><a name="text14883185615232"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p7533165316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p7533165316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p7533165316"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row1860417492507"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p8255028185219"><a name="zh-cn_topic_0084814075_p8255028185219"></a><a name="zh-cn_topic_0084814075_p8255028185219"></a>gpu_usage_gpu</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p165351440103411"><a name="p165351440103411"></a><a name="p165351440103411"></a>(Agent) GPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1971315538511"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1971315538511"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1971315538511"></a>该指标用于统计测量对象当前的GPU使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204891126115312"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204891126115312"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p204891126115312"></a>单位：百分比</p>
<a name="ul6496164052517"></a><a name="ul6496164052517"></a><ul id="ul6496164052517"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1223616464528"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1223616464528"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1223616464528"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul396805602314"></a><a name="ul396805602314"></a><ul id="ul396805602314"><li><span id="text996745602314"><a name="text996745602314"></a><a name="text996745602314"></a>云服务器</span></li><li><span id="text1096813564232"><a name="text1096813564232"></a><a name="text1096813564232"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p478591611316"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p478591611316"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p478591611316"></a>1分钟</p>
</td>
</tr>
<tr id="row724624116115"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p10247154119117"><a name="p10247154119117"></a><a name="p10247154119117"></a>gpu_free_mem</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p18247154117111"><a name="p18247154117111"></a><a name="p18247154117111"></a>GPU显存剩余量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p18996134214477"><a name="p18996134214477"></a><a name="p18996134214477"></a>该指标用于统计测量对象当前的GPU显存剩余量。</p>
<p id="p9247174121116"><a name="p9247174121116"></a><a name="p9247174121116"></a>单位：MB</p>
<a name="ul9742112672318"></a><a name="ul9742112672318"></a><ul id="ul9742112672318"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p12247194181113"><a name="p12247194181113"></a><a name="p12247194181113"></a>≥ 0 MB</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul558157182312"></a><a name="ul558157182312"></a><ul id="ul558157182312"><li><span id="text17576578235"><a name="text17576578235"></a><a name="text17576578235"></a>云服务器</span></li><li><span id="text1757135717233"><a name="text1757135717233"></a><a name="text1757135717233"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p208133416428"><a name="p208133416428"></a><a name="p208133416428"></a>1分钟</p>
</td>
</tr>
<tr id="row4247124181118"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p324774111110"><a name="p324774111110"></a><a name="p324774111110"></a>gpu_graphics_clocks</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p0247204119118"><a name="p0247204119118"></a><a name="p0247204119118"></a>GPU显卡时钟频率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p760611118492"><a name="p760611118492"></a><a name="p760611118492"></a>该指标用于统计测量对象当前的GPU显卡（着色器）时钟频率。</p>
<p id="p1779417467157"><a name="p1779417467157"></a><a name="p1779417467157"></a>单位：MHz</p>
<a name="ul681320298238"></a><a name="ul681320298238"></a><ul id="ul681320298238"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p82478417110"><a name="p82478417110"></a><a name="p82478417110"></a>≥ 0 MHz</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul1214619577231"></a><a name="ul1214619577231"></a><ul id="ul1214619577231"><li><span id="text2145257102319"><a name="text2145257102319"></a><a name="text2145257102319"></a>云服务器</span></li><li><span id="text18146145710238"><a name="text18146145710238"></a><a name="text18146145710238"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p47715357422"><a name="p47715357422"></a><a name="p47715357422"></a>1分钟</p>
</td>
</tr>
<tr id="row62489418116"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p202482041121117"><a name="p202482041121117"></a><a name="p202482041121117"></a>gpu_mem_clocks</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p19248541111120"><a name="p19248541111120"></a><a name="p19248541111120"></a>GPU内存时钟频率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p598152211494"><a name="p598152211494"></a><a name="p598152211494"></a>该指标用于统计测量对象当前的GPU内存时钟频率。</p>
<p id="p9248541181120"><a name="p9248541181120"></a><a name="p9248541181120"></a>单位：MHz</p>
<a name="ul18701432152315"></a><a name="ul18701432152315"></a><ul id="ul18701432152315"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p8248124112111"><a name="p8248124112111"></a><a name="p8248124112111"></a>≥ 0 MHz</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul18233145792314"></a><a name="ul18233145792314"></a><ul id="ul18233145792314"><li><span id="text1023285772316"><a name="text1023285772316"></a><a name="text1023285772316"></a>云服务器</span></li><li><span id="text9232115702316"><a name="text9232115702316"></a><a name="text9232115702316"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p1226119364421"><a name="p1226119364421"></a><a name="p1226119364421"></a>1分钟</p>
</td>
</tr>
<tr id="row5248134115118"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p724874191118"><a name="p724874191118"></a><a name="p724874191118"></a>gpu_power_draw</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p1824874161110"><a name="p1824874161110"></a><a name="p1824874161110"></a>GPU功率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p186587348492"><a name="p186587348492"></a><a name="p186587348492"></a>该指标用于统计测量对象当前的GPU功率。</p>
<p id="p13248104117115"><a name="p13248104117115"></a><a name="p13248104117115"></a>单位：W</p>
<a name="ul69618372234"></a><a name="ul69618372234"></a><ul id="ul69618372234"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p324884161113"><a name="p324884161113"></a><a name="p324884161113"></a>NA</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul18321657182310"></a><a name="ul18321657182310"></a><ul id="ul18321657182310"><li><span id="text153216570239"><a name="text153216570239"></a><a name="text153216570239"></a>云服务器</span></li><li><span id="text13321357122315"><a name="text13321357122315"></a><a name="text13321357122315"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p19539103718420"><a name="p19539103718420"></a><a name="p19539103718420"></a>1分钟</p>
</td>
</tr>
<tr id="row172481411112"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p13249174131120"><a name="p13249174131120"></a><a name="p13249174131120"></a>gpu_rx_throughput_pci</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p7249194119118"><a name="p7249194119118"></a><a name="p7249194119118"></a>GPU PCI入方向带宽</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p16574648174914"><a name="p16574648174914"></a><a name="p16574648174914"></a>该指标用于统计测量对象当前的GPU PCI入方向带宽。</p>
<p id="p1124910416116"><a name="p1124910416116"></a><a name="p1124910416116"></a>单位：MByte/s</p>
<a name="ul1583953972315"></a><a name="ul1583953972315"></a><ul id="ul1583953972315"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p1249114114118"><a name="p1249114114118"></a><a name="p1249114114118"></a>≥ 0 MByte/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul18406657132319"></a><a name="ul18406657132319"></a><ul id="ul18406657132319"><li><span id="text040615578234"><a name="text040615578234"></a><a name="text040615578234"></a>云服务器</span></li><li><span id="text134061057142317"><a name="text134061057142317"></a><a name="text134061057142317"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p14995193944219"><a name="p14995193944219"></a><a name="p14995193944219"></a>1分钟</p>
</td>
</tr>
<tr id="row224934141110"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p202496417113"><a name="p202496417113"></a><a name="p202496417113"></a>gpu_sm_clocks</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p1124914111117"><a name="p1124914111117"></a><a name="p1124914111117"></a>GPU流式处理器时钟频率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p147031724506"><a name="p147031724506"></a><a name="p147031724506"></a>该指标用于统计测量对象当前的GPU流式处理器时钟频率。</p>
<p id="p17405161411201"><a name="p17405161411201"></a><a name="p17405161411201"></a>单位：MHz</p>
<a name="ul6933154212315"></a><a name="ul6933154212315"></a><ul id="ul6933154212315"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p13249104121120"><a name="p13249104121120"></a><a name="p13249104121120"></a>≥ 0 MHz</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul18492125752318"></a><a name="ul18492125752318"></a><ul id="ul18492125752318"><li><span id="text17492145712313"><a name="text17492145712313"></a><a name="text17492145712313"></a>云服务器</span></li><li><span id="text1849217574236"><a name="text1849217574236"></a><a name="text1849217574236"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p79144114214"><a name="p79144114214"></a><a name="p79144114214"></a>1分钟</p>
</td>
</tr>
<tr id="row64581327121110"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p19458927181112"><a name="p19458927181112"></a><a name="p19458927181112"></a>gpu_temperature</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p13458327101113"><a name="p13458327101113"></a><a name="p13458327101113"></a>GPU温度</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p270171612507"><a name="p270171612507"></a><a name="p270171612507"></a>该指标用于统计测量对象当前的GPU温度。</p>
<p id="p14458142781115"><a name="p14458142781115"></a><a name="p14458142781115"></a>单位：℃</p>
<a name="ul771044515231"></a><a name="ul771044515231"></a><ul id="ul771044515231"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p1645818279117"><a name="p1645818279117"></a><a name="p1645818279117"></a>≥ 0 ℃</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul185811657112315"></a><a name="ul185811657112315"></a><ul id="ul185811657112315"><li><span id="text13580195717231"><a name="text13580195717231"></a><a name="text13580195717231"></a>云服务器</span></li><li><span id="text1758165742317"><a name="text1758165742317"></a><a name="text1758165742317"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p110915422428"><a name="p110915422428"></a><a name="p110915422428"></a>1分钟</p>
</td>
</tr>
<tr id="row7458102711114"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p4458122741113"><a name="p4458122741113"></a><a name="p4458122741113"></a>gpu_tx_throughput_pci</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p14458827181117"><a name="p14458827181117"></a><a name="p14458827181117"></a>GPU PCI出方向带宽</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p1425517294509"><a name="p1425517294509"></a><a name="p1425517294509"></a>该指标用于统计测量对象当前的GPU PCI出方向带宽。</p>
<p id="p11459182711118"><a name="p11459182711118"></a><a name="p11459182711118"></a>单位：MByte/s</p>
<a name="ul09311485234"></a><a name="ul09311485234"></a><ul id="ul09311485234"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p94666337447"><a name="p94666337447"></a><a name="p94666337447"></a>≥ 0 MByte/s</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul14672155710232"></a><a name="ul14672155710232"></a><ul id="ul14672155710232"><li><span id="text2067215712315"><a name="text2067215712315"></a><a name="text2067215712315"></a>云服务器</span></li><li><span id="text567225782314"><a name="text567225782314"></a><a name="text567225782314"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p4136154314210"><a name="p4136154314210"></a><a name="p4136154314210"></a>1分钟</p>
</td>
</tr>
<tr id="row1745922781119"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p7459162761112"><a name="p7459162761112"></a><a name="p7459162761112"></a>gpu_used_mem</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p12459127191112"><a name="p12459127191112"></a><a name="p12459127191112"></a>GPU显存使用量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p145271542145018"><a name="p145271542145018"></a><a name="p145271542145018"></a>该指标用于统计测量对象当前的GPU显存使用量。</p>
<p id="p13459192751115"><a name="p13459192751115"></a><a name="p13459192751115"></a>单位：MB</p>
<a name="ul91819522231"></a><a name="ul91819522231"></a><ul id="ul91819522231"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p104591427121115"><a name="p104591427121115"></a><a name="p104591427121115"></a>≥ 0 MB</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul1375715577232"></a><a name="ul1375715577232"></a><ul id="ul1375715577232"><li><span id="text7757657112314"><a name="text7757657112314"></a><a name="text7757657112314"></a>云服务器</span></li><li><span id="text7757185732314"><a name="text7757185732314"></a><a name="text7757185732314"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p196114454423"><a name="p196114454423"></a><a name="p196114454423"></a>1分钟</p>
</td>
</tr>
<tr id="row10724269117"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p117242612117"><a name="p117242612117"></a><a name="p117242612117"></a>gpu_video_clocks</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p1572420619110"><a name="p1572420619110"></a><a name="p1572420619110"></a>GPU视频时钟频率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p1744265615015"><a name="p1744265615015"></a><a name="p1744265615015"></a>该指标用于统计测量对象当前的GPU视频（包含编解码）时钟频率。</p>
<p id="p197241765111"><a name="p197241765111"></a><a name="p197241765111"></a>单位：MHz</p>
<a name="ul3668105492317"></a><a name="ul3668105492317"></a><ul id="ul3668105492317"><li>采集方式（Linux）：通过调用GPU卡的libnvidia-ml.so.1库文件获取。</li><li>采集方式（Windows）：通过调用GPU卡的nvml.dll库获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p272419601114"><a name="p272419601114"></a><a name="p272419601114"></a>≥ 0 MHz</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul6847757102313"></a><a name="ul6847757102313"></a><ul id="ul6847757102313"><li><span id="text138471557102311"><a name="text138471557102311"></a><a name="text138471557102311"></a>云服务器</span></li><li><span id="text14847155717232"><a name="text14847155717232"></a><a name="text14847155717232"></a>云服务器</span> - GPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p1599544524218"><a name="p1599544524218"></a><a name="p1599544524218"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 操作系统监控指标：NPU<a name="section1903193212814"></a>

**表 11**  NPU类监控指标说明

<a name="table843191416295"></a>
<table><thead align="left"><tr id="row154321714192917"><th class="cellrowborder" valign="top" width="12.839999999999998%" id="mcps1.2.7.1.1"><p id="p143291416299"><a name="p143291416299"></a><a name="p143291416299"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="14.680000000000001%" id="mcps1.2.7.1.2"><p id="p3432101419296"><a name="p3432101419296"></a><a name="p3432101419296"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="35.61%" id="mcps1.2.7.1.3"><p id="p4432114152910"><a name="p4432114152910"></a><a name="p4432114152910"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="12.31%" id="mcps1.2.7.1.4"><p id="p194331714162920"><a name="p194331714162920"></a><a name="p194331714162920"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.91%" id="mcps1.2.7.1.5"><p id="p1443391442913"><a name="p1443391442913"></a><a name="p1443391442913"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="13.65%" id="mcps1.2.7.1.6"><p id="p643313148293"><a name="p643313148293"></a><a name="p643313148293"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="row243351412913"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p6652132023215"><a name="p6652132023215"></a><a name="p6652132023215"></a>npu_device_health</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p12652142013323"><a name="p12652142013323"></a><a name="p12652142013323"></a>NPU健康状况</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p7652620143214"><a name="p7652620143214"></a><a name="p7652620143214"></a>该指标用于统计虚拟机上NPU卡的健康状态，是一个综合指标。</p>
<p id="p1565212013212"><a name="p1565212013212"></a><a name="p1565212013212"></a>该指标无单位。</p>
<p id="p13664101215339"><a name="p13664101215339"></a><a name="p13664101215339"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><a name="ul1434121415293"></a><a name="ul1434121415293"></a><ul id="ul1434121415293"><li>0：代表健康</li><li>1：代表存在一般告警</li><li>2：代表存在重要告警</li><li>3：代表存在紧急告警</li></ul>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul93018122242"></a><a name="ul93018122242"></a><ul id="ul93018122242"><li><span id="text7331719249"><a name="text7331719249"></a><a name="text7331719249"></a>云服务器</span></li><li><span id="text1143416144292"><a name="text1143416144292"></a><a name="text1143416144292"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p18435131442914"><a name="p18435131442914"></a><a name="p18435131442914"></a>1分钟</p>
</td>
</tr>
<tr id="row54351114102919"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p765272010325"><a name="p765272010325"></a><a name="p765272010325"></a>npu_util_rate_mem</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p16652520203219"><a name="p16652520203219"></a><a name="p16652520203219"></a>NPU显存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p126521020113214"><a name="p126521020113214"></a><a name="p126521020113214"></a>该指标用于统计该NPU的编码能力使用率。</p>
<p id="p36525207326"><a name="p36525207326"></a><a name="p36525207326"></a>单位：百分比</p>
<p id="p193801515143313"><a name="p193801515143313"></a><a name="p193801515143313"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p84351914202917"><a name="p84351914202917"></a><a name="p84351914202917"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul19990202742420"></a><a name="ul19990202742420"></a><ul id="ul19990202742420"><li><span id="text1399012782410"><a name="text1399012782410"></a><a name="text1399012782410"></a>云服务器</span></li><li><span id="text499032715245"><a name="text499032715245"></a><a name="text499032715245"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p7436151413297"><a name="p7436151413297"></a><a name="p7436151413297"></a>1分钟</p>
</td>
</tr>
<tr id="row1436141416296"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p56538203325"><a name="p56538203325"></a><a name="p56538203325"></a>npu_util_rate_ai_core</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p565316206326"><a name="p565316206326"></a><a name="p565316206326"></a>NPU卡AI核心使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p16531820163213"><a name="p16531820163213"></a><a name="p16531820163213"></a>该指标用于统计该NPU的AI核心使用率。</p>
<p id="p146531920193214"><a name="p146531920193214"></a><a name="p146531920193214"></a>单位：百分比</p>
<p id="p33411187339"><a name="p33411187339"></a><a name="p33411187339"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p3437151462912"><a name="p3437151462912"></a><a name="p3437151462912"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul11106132812416"></a><a name="ul11106132812416"></a><ul id="ul11106132812416"><li><span id="text13105028162414"><a name="text13105028162414"></a><a name="text13105028162414"></a>云服务器</span></li><li><span id="text11058280244"><a name="text11058280244"></a><a name="text11058280244"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p5438214122918"><a name="p5438214122918"></a><a name="p5438214122918"></a>1分钟</p>
</td>
</tr>
<tr id="row2025121712314"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p1165362073217"><a name="p1165362073217"></a><a name="p1165362073217"></a>npu_util_rate_ai_cpu</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p17653720193215"><a name="p17653720193215"></a><a name="p17653720193215"></a>NPU卡AI CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p16653920103218"><a name="p16653920103218"></a><a name="p16653920103218"></a>该指标用于统计该NPU的AI CPU的使用率。</p>
<p id="p16653102014329"><a name="p16653102014329"></a><a name="p16653102014329"></a>单位：百分比。</p>
<p id="p2910192010339"><a name="p2910192010339"></a><a name="p2910192010339"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p7252101714312"><a name="p7252101714312"></a><a name="p7252101714312"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul1119652819245"></a><a name="ul1119652819245"></a><ul id="ul1119652819245"><li><span id="text2196122852416"><a name="text2196122852416"></a><a name="text2196122852416"></a>云服务器</span></li><li><span id="text1219613289244"><a name="text1219613289244"></a><a name="text1219613289244"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p89569863713"><a name="p89569863713"></a><a name="p89569863713"></a>1分钟</p>
</td>
</tr>
<tr id="row1185019192313"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p196541320123215"><a name="p196541320123215"></a><a name="p196541320123215"></a>npu_util_rate_ctrl_cpu</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p86541201328"><a name="p86541201328"></a><a name="p86541201328"></a>NPU控制CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p196542020103217"><a name="p196542020103217"></a><a name="p196542020103217"></a>该指标用于统计该NPU的控制CPU的使用率。</p>
<p id="p6654220163216"><a name="p6654220163216"></a><a name="p6654220163216"></a>单位：百分比。</p>
<p id="p4365224133318"><a name="p4365224133318"></a><a name="p4365224133318"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p185061917318"><a name="p185061917318"></a><a name="p185061917318"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul1528682862415"></a><a name="ul1528682862415"></a><ul id="ul1528682862415"><li><span id="text142851628112420"><a name="text142851628112420"></a><a name="text142851628112420"></a>云服务器</span></li><li><span id="text928618286243"><a name="text928618286243"></a><a name="text928618286243"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p9432963718"><a name="p9432963718"></a><a name="p9432963718"></a>1分钟</p>
</td>
</tr>
<tr id="row11586132612314"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p66542201322"><a name="p66542201322"></a><a name="p66542201322"></a>npu_util_rate_mem_bandwidth</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p18654112083219"><a name="p18654112083219"></a><a name="p18654112083219"></a>NPU显存带宽使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p065462083220"><a name="p065462083220"></a><a name="p065462083220"></a>该指标用于统计该NPU的显存的带宽使用率。</p>
<p id="p3654152011326"><a name="p3654152011326"></a><a name="p3654152011326"></a>单位：百分比。</p>
<p id="p573482810337"><a name="p573482810337"></a><a name="p573482810337"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p1558712613110"><a name="p1558712613110"></a><a name="p1558712613110"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul8377162842415"></a><a name="ul8377162842415"></a><ul id="ul8377162842415"><li><span id="text133773284247"><a name="text133773284247"></a><a name="text133773284247"></a>云服务器</span></li><li><span id="text1637752832415"><a name="text1637752832415"></a><a name="text1637752832415"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p712849113712"><a name="p712849113712"></a><a name="p712849113712"></a>1分钟</p>
</td>
</tr>
<tr id="row15872026133114"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p6655192043217"><a name="p6655192043217"></a><a name="p6655192043217"></a>npu_freq_mem</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p96551020103213"><a name="p96551020103213"></a><a name="p96551020103213"></a>NPU显存频率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p14655120193216"><a name="p14655120193216"></a><a name="p14655120193216"></a>该指标用于统计该NPU的显存的时钟频率。</p>
<p id="p11655120183210"><a name="p11655120183210"></a><a name="p11655120183210"></a>单位：兆赫兹（MHz）。</p>
<p id="p369631163314"><a name="p369631163314"></a><a name="p369631163314"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p165872264316"><a name="p165872264316"></a><a name="p165872264316"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul94748285243"></a><a name="ul94748285243"></a><ul id="ul94748285243"><li><span id="text347312285249"><a name="text347312285249"></a><a name="text347312285249"></a>云服务器</span></li><li><span id="text1347482822420"><a name="text1347482822420"></a><a name="text1347482822420"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p32142912377"><a name="p32142912377"></a><a name="p32142912377"></a>1分钟</p>
</td>
</tr>
<tr id="row1115194513118"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p96551620163210"><a name="p96551620163210"></a><a name="p96551620163210"></a>npu_freq_ai_core</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p1865510207328"><a name="p1865510207328"></a><a name="p1865510207328"></a>NPU卡AI核心频率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p6655112019320"><a name="p6655112019320"></a><a name="p6655112019320"></a>该指标用于统计该NPU AI核心的时钟频率。</p>
<p id="p1365512083217"><a name="p1365512083217"></a><a name="p1365512083217"></a>单位：兆赫兹（MHz）。</p>
<p id="p2195234143319"><a name="p2195234143319"></a><a name="p2195234143319"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p81674518313"><a name="p81674518313"></a><a name="p81674518313"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul4567122810240"></a><a name="ul4567122810240"></a><ul id="ul4567122810240"><li><span id="text85673281249"><a name="text85673281249"></a><a name="text85673281249"></a>云服务器</span></li><li><span id="text656742812245"><a name="text656742812245"></a><a name="text656742812245"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p16296109153718"><a name="p16296109153718"></a><a name="p16296109153718"></a>1分钟</p>
</td>
</tr>
<tr id="row51634514317"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p465615205329"><a name="p465615205329"></a><a name="p465615205329"></a>npu_usage_mem</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p19656112010328"><a name="p19656112010328"></a><a name="p19656112010328"></a>NPU显存使用量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p1565672083211"><a name="p1565672083211"></a><a name="p1565672083211"></a>该指标用于统计该NPU 显存的使用量。</p>
<p id="p865682033212"><a name="p865682033212"></a><a name="p865682033212"></a>单位：兆Byte（MB）。</p>
<p id="p10415113713336"><a name="p10415113713336"></a><a name="p10415113713336"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p1916145173114"><a name="p1916145173114"></a><a name="p1916145173114"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul4662142816246"></a><a name="ul4662142816246"></a><ul id="ul4662142816246"><li><span id="text1266202815246"><a name="text1266202815246"></a><a name="text1266202815246"></a>云服务器</span></li><li><span id="text1866222815240"><a name="text1866222815240"></a><a name="text1866222815240"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p83791999374"><a name="p83791999374"></a><a name="p83791999374"></a>1分钟</p>
</td>
</tr>
<tr id="row1316345123118"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p06561420123219"><a name="p06561420123219"></a><a name="p06561420123219"></a>npu_sbe</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p15656102017326"><a name="p15656102017326"></a><a name="p15656102017326"></a>NPU单bit错误数量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p7656202043214"><a name="p7656202043214"></a><a name="p7656202043214"></a>该指标用于统计该NPU卡当前的单比特页错误的数量。</p>
<p id="p176561020163214"><a name="p176561020163214"></a><a name="p176561020163214"></a>单位：个</p>
<p id="p319664003313"><a name="p319664003313"></a><a name="p319664003313"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p71744511316"><a name="p71744511316"></a><a name="p71744511316"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul3759122816241"></a><a name="ul3759122816241"></a><ul id="ul3759122816241"><li><span id="text67593289244"><a name="text67593289244"></a><a name="text67593289244"></a>云服务器</span></li><li><span id="text975952872413"><a name="text975952872413"></a><a name="text975952872413"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p2458119133717"><a name="p2458119133717"></a><a name="p2458119133717"></a>1分钟</p>
</td>
</tr>
<tr id="row191716452313"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p106577207325"><a name="p106577207325"></a><a name="p106577207325"></a>npu_dbe</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p1565712207321"><a name="p1565712207321"></a><a name="p1565712207321"></a>NPU双bit错误数量</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p1665712020327"><a name="p1665712020327"></a><a name="p1665712020327"></a>该指标用于统计该NPU卡当前的多比特页错误的数量。</p>
<p id="p2065702083213"><a name="p2065702083213"></a><a name="p2065702083213"></a>单位：个</p>
<p id="p1541019431334"><a name="p1541019431334"></a><a name="p1541019431334"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p1417345113118"><a name="p1417345113118"></a><a name="p1417345113118"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul11850182872412"></a><a name="ul11850182872412"></a><ul id="ul11850182872412"><li><span id="text1185032812413"><a name="text1185032812413"></a><a name="text1185032812413"></a>云服务器</span></li><li><span id="text9850728162416"><a name="text9850728162416"></a><a name="text9850728162416"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p85471395379"><a name="p85471395379"></a><a name="p85471395379"></a>1分钟</p>
</td>
</tr>
<tr id="row7470205718312"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p765719202325"><a name="p765719202325"></a><a name="p765719202325"></a>npu_power</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p56571820183217"><a name="p56571820183217"></a><a name="p56571820183217"></a>NPU功率</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p106571920203218"><a name="p106571920203218"></a><a name="p106571920203218"></a>该指标用于统计该NPU卡的功率。其中，310卡仅支持显示额定功率，其余卡显示实际功率</p>
<p id="p1665732063214"><a name="p1665732063214"></a><a name="p1665732063214"></a>单位：瓦（W）</p>
<p id="p64051247113314"><a name="p64051247113314"></a><a name="p64051247113314"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p2471115753120"><a name="p2471115753120"></a><a name="p2471115753120"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul15941152816248"></a><a name="ul15941152816248"></a><ul id="ul15941152816248"><li><span id="text12941112810248"><a name="text12941112810248"></a><a name="text12941112810248"></a>云服务器</span></li><li><span id="text1294115281243"><a name="text1294115281243"></a><a name="text1294115281243"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p20629129113715"><a name="p20629129113715"></a><a name="p20629129113715"></a>1分钟</p>
</td>
</tr>
<tr id="row10471125783119"><td class="cellrowborder" valign="top" width="12.839999999999998%" headers="mcps1.2.7.1.1 "><p id="p13657620143214"><a name="p13657620143214"></a><a name="p13657620143214"></a>npu_temperature</p>
</td>
<td class="cellrowborder" valign="top" width="14.680000000000001%" headers="mcps1.2.7.1.2 "><p id="p18657112003217"><a name="p18657112003217"></a><a name="p18657112003217"></a>NPU温度</p>
</td>
<td class="cellrowborder" valign="top" width="35.61%" headers="mcps1.2.7.1.3 "><p id="p206571120123216"><a name="p206571120123216"></a><a name="p206571120123216"></a>该指标用于统计该NPU卡当前的温度</p>
<p id="p1365722043219"><a name="p1365722043219"></a><a name="p1365722043219"></a>单位：摄氏度（℃）</p>
<p id="p1010020502334"><a name="p1010020502334"></a><a name="p1010020502334"></a>采集方式（Linux）：通过调用NPU卡的libdcmi.so库文件获取。</p>
</td>
<td class="cellrowborder" valign="top" width="12.31%" headers="mcps1.2.7.1.4 "><p id="p9471175743111"><a name="p9471175743111"></a><a name="p9471175743111"></a>≥ 0</p>
</td>
<td class="cellrowborder" valign="top" width="10.91%" headers="mcps1.2.7.1.5 "><a name="ul5331329172413"></a><a name="ul5331329172413"></a><ul id="ul5331329172413"><li><span id="text1633162952416"><a name="text1633162952416"></a><a name="text1633162952416"></a>云服务器</span></li><li><span id="text1733162911245"><a name="text1733162911245"></a><a name="text1733162911245"></a>云服务器</span> - NPU</li></ul>
</td>
<td class="cellrowborder" valign="top" width="13.65%" headers="mcps1.2.7.1.6 "><p id="p177085919373"><a name="p177085919373"></a><a name="p177085919373"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>Windows系统暂不支持NPU类监控指标。

## 维度<a name="section36963297112133"></a>

<a name="table41237041112133"></a>
<table><thead align="left"><tr id="row28021974112133"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.1.4.1.1"><p id="p55085261043"><a name="p55085261043"></a><a name="p55085261043"></a>维度</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.1.4.1.2"><p id="p55187441112133"><a name="p55187441112133"></a><a name="p55187441112133"></a>Key</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.1.4.1.3"><p id="p40997749112133"><a name="p40997749112133"></a><a name="p40997749112133"></a>Value</p>
</th>
</tr>
</thead>
<tbody><tr id="row32483336112133"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.1 "><p id="p205082261415"><a name="p205082261415"></a><a name="p205082261415"></a><span id="text458113671216"><a name="text458113671216"></a><a name="text458113671216"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.2 "><p id="p13904597112133"><a name="p13904597112133"></a><a name="p13904597112133"></a>instance_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.3 "><p id="p52530562112133"><a name="p52530562112133"></a><a name="p52530562112133"></a><span id="text173241214361"><a name="text173241214361"></a><a name="text173241214361"></a>云服务器</span>ID。</p>
</td>
</tr>
<tr id="row096485113561"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.1 "><p id="p165082261041"><a name="p165082261041"></a><a name="p165082261041"></a><span id="text2038351010129"><a name="text2038351010129"></a><a name="text2038351010129"></a>云服务器</span> - 磁盘</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.2 "><p id="p17739182961016"><a name="p17739182961016"></a><a name="p17739182961016"></a>disk</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.3 "><p id="p129648518563"><a name="p129648518563"></a><a name="p129648518563"></a><span id="text154800422570"><a name="text154800422570"></a><a name="text154800422570"></a>云服务器</span>磁盘。</p>
<p id="p5156135812581"><a name="p5156135812581"></a><a name="p5156135812581"></a>该取值可通过云监控服务的“<a href="https://support.huaweicloud.com/api-ces/ListAgentDimensionInfo.html" target="_blank" rel="noopener noreferrer">查询主机监控维度指标信息</a>”获取。</p>
</td>
</tr>
<tr id="row9729155418560"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.1 "><p id="p85095263419"><a name="p85095263419"></a><a name="p85095263419"></a><span id="text13931147123"><a name="text13931147123"></a><a name="text13931147123"></a>云服务器</span> - 挂载点</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.2 "><p id="p92984330104"><a name="p92984330104"></a><a name="p92984330104"></a>mount_point</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.3 "><p id="p1919713128158"><a name="p1919713128158"></a><a name="p1919713128158"></a><span id="text49341944145720"><a name="text49341944145720"></a><a name="text49341944145720"></a>云服务器</span>磁盘的挂载点。</p>
<p id="p76114286318"><a name="p76114286318"></a><a name="p76114286318"></a>该取值可通过云监控服务的“<a href="https://support.huaweicloud.com/api-ces/ListAgentDimensionInfo.html" target="_blank" rel="noopener noreferrer">查询主机监控维度指标信息</a>”获取。</p>
</td>
</tr>
<tr id="row131984579566"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.1 "><p id="p750913261748"><a name="p750913261748"></a><a name="p750913261748"></a><span id="text9137201714125"><a name="text9137201714125"></a><a name="text9137201714125"></a>云服务器</span> - GPU</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.2 "><p id="p46481736161013"><a name="p46481736161013"></a><a name="p46481736161013"></a>gpu</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.3 "><p id="p41981157125620"><a name="p41981157125620"></a><a name="p41981157125620"></a>GPU类型<span id="text0460175018577"><a name="text0460175018577"></a><a name="text0460175018577"></a>云服务器</span>中显卡。</p>
<p id="p53231813996"><a name="p53231813996"></a><a name="p53231813996"></a>该取值可通过云监控服务的“<a href="https://support.huaweicloud.com/api-ces/ListAgentDimensionInfo.html" target="_blank" rel="noopener noreferrer">查询主机监控维度指标信息</a>”获取。</p>
</td>
</tr>
<tr id="row9462151453814"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.1 "><p id="p1946319149384"><a name="p1946319149384"></a><a name="p1946319149384"></a><span id="text18973182312386"><a name="text18973182312386"></a><a name="text18973182312386"></a>云服务器</span> - NPU</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.2 "><p id="p164637145380"><a name="p164637145380"></a><a name="p164637145380"></a>npu</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.3 "><p id="p2899149142514"><a name="p2899149142514"></a><a name="p2899149142514"></a>NPU类型<span id="text1090089122515"><a name="text1090089122515"></a><a name="text1090089122515"></a>云服务器</span>中显卡。</p>
<p id="p139008918254"><a name="p139008918254"></a><a name="p139008918254"></a>该取值可通过云监控服务的“<a href="https://support.huaweicloud.com/api-ces/ListAgentDimensionInfo.html" target="_blank" rel="noopener noreferrer">查询主机监控维度指标信息</a>”获取。</p>
</td>
</tr>
</tbody>
</table>

