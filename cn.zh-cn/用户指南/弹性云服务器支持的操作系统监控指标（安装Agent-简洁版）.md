# 弹性云服务器支持的操作系统监控指标（安装Agent，简洁版）<a name="ZH-CN_TOPIC_0215513361"></a>

## 功能说明<a name="section1480011141417"></a>

本节内容介绍弹性云服务器支持的操作系统监控指标。这些区域主机监控Agent采用最新版本的Agent，监控指标更为简洁。

当前支持如下区域：

“华东-上海一”、“华东-上海二”、“华北-北京一”、“华北-北京四”、“华南-广州”、“华南-深圳”、“西南-贵阳一”、“中国-香港”、“亚太-曼谷”、“亚太-新加坡”、“非洲-约翰内斯堡”。

安装Agent后，您便可以查看弹性云服务器的操作系统监控指标。指标采集周期是1分钟。

## 操作系统监控指标说明<a name="section1577017316411"></a>

**表 1**  操作系统监控支持的监控指标

<a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_table7594115620353"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_row95951556133512"><th class="cellrowborder" valign="top" width="12.110000000000003%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p19741153185914"><a name="zh-cn_topic_0084814075_p19741153185914"></a><a name="zh-cn_topic_0084814075_p19741153185914"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="12.750000000000004%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1255413283615"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1255413283615"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1255413283615"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="40.75000000000001%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105546320367"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105546320367"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105546320367"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="8.400000000000002%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_zh-cn_topic_0030911465_p64622851222846"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_zh-cn_topic_0030911465_p64622851222846"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_zh-cn_topic_0030911465_p64622851222846"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="8.300000000000002%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1383633412472"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1383633412472"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1383633412472"></a>测量对象</p>
</th>
<th class="cellrowborder" valign="top" width="17.69%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18780264718"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18780264718"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18780264718"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_row830162618574"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p371655465019"><a name="zh-cn_topic_0084814075_p371655465019"></a><a name="zh-cn_topic_0084814075_p371655465019"></a>cpu_usage</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p092415835715"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p092415835715"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p092415835715"></a>（Agent）CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11924165815571"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11924165815571"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11924165815571"></a>该指标用于统计测量对象当前CPU使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199155719415"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199155719415"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p199155719415"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul428752335411"></a><a name="zh-cn_topic_0084814075_ul428752335411"></a><ul id="zh-cn_topic_0084814075_ul428752335411"><li>采集方式（Linux）：通过计算采集周期内/proc/stat中的变化得出cpu使用率。用户可以通过top命令查看 %Cpu(s)值。</li><li>采集方式（Windows）：通过WindowsAPI GetSystemTimes获取。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8924205815579"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8924205815579"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p8924205815579"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p142577565319"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p142577565319"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p142577565319"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p82577519535"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p82577519535"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p82577519535"></a>1分钟</p>
</td>
</tr>
<tr id="row0712314639"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p171811549508"><a name="zh-cn_topic_0084814075_p171811549508"></a><a name="zh-cn_topic_0084814075_p171811549508"></a>load_average5</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12509461401"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12509461401"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p12509461401"></a>（Agent） 5分钟平均负载</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p193579719219"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p193579719219"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p193579719219"></a>该指标用于统计测量对象过去5分钟的CPU平均负载。</p>
<a name="ul81112552148"></a><a name="ul81112552148"></a><ul id="ul81112552148"><li>采集方式（Linux）：通过/proc/loadavg中load5/逻辑CPU个数得到。用户可以通过top命令查看load5值。</li><li>Windows系统暂不支持CPU负载指标。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1387714135216"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1387714135216"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1387714135216"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p196291341812"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p196291341812"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p196291341812"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p344582715413"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p344582715413"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p344582715413"></a>1分钟</p>
</td>
</tr>
<tr id="row1494141719318"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p10719654105010"><a name="zh-cn_topic_0084814075_p10719654105010"></a><a name="zh-cn_topic_0084814075_p10719654105010"></a>mem_usedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7426953195818"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7426953195818"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p7426953195818"></a>（Agent）内存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p56603522431"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p56603522431"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p56603522431"></a>该指标用于统计测量对象的内存使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1271515216422"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1271515216422"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1271515216422"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul15740448151918"></a><a name="zh-cn_topic_0084814075_ul15740448151918"></a><ul id="zh-cn_topic_0084814075_ul15740448151918"><li>采集方式（Linux）：通过/proc/meminfo文件获取,(MemTotal-MemAvailable)/MemTotal</li><li>采集方式（Windows）：计算方法为（ 已用内存量/内存总量*100%）。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p168151550164215"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p168151550164215"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p168151550164215"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p20313183255619"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p20313183255619"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p20313183255619"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p53139328567"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p53139328567"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p53139328567"></a>1分钟</p>
</td>
</tr>
<tr id="row1615092011317"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p10720854195015"><a name="zh-cn_topic_0084814075_p10720854195015"></a><a name="zh-cn_topic_0084814075_p10720854195015"></a>mountPointPrefix_disk_free</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11426145312588"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11426145312588"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p11426145312588"></a>（Agent）磁盘剩余存储量</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p116982408478"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p116982408478"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p116982408478"></a>该指标用于统计测量对象磁盘的剩余存储空间。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p364185016435"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p364185016435"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p364185016435"></a>单位：GB</p>
<a name="zh-cn_topic_0084814075_ul1836810491232"></a><a name="zh-cn_topic_0084814075_ul1836810491232"></a><ul id="zh-cn_topic_0084814075_ul1836810491232"><li>采集方式（Linux）：执行df -h命令，查看Avail列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>采集方式（Windows）：使用WMI接口GetDiskFreeSpaceExW获取磁盘空间数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p194261653135820"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p194261653135820"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p194261653135820"></a>≥0 GB</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4938131119577"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4938131119577"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p4938131119577"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1093851113572"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1093851113572"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1093851113572"></a>1分钟</p>
</td>
</tr>
<tr id="row1074412221533"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p572216546508"><a name="zh-cn_topic_0084814075_p572216546508"></a><a name="zh-cn_topic_0084814075_p572216546508"></a>mountPointPrefix_disk_usedPercent</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105111318631"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105111318631"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p105111318631"></a>（Agent）磁盘使用率</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p64261535585"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p64261535585"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p64261535585"></a>该指标用于统计测量对象磁盘使用率，以百分比为单位。计算方式为: 磁盘已用存储量/磁盘存储总量。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14423171814449"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14423171814449"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p14423171814449"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul098197247"></a><a name="zh-cn_topic_0084814075_ul098197247"></a><ul id="zh-cn_topic_0084814075_ul098197247"><li>采集方式（Linux）：通过计算Used/Size得出。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>采集方式（Windows）：使用WMI接口GetDiskFreeSpaceExW获取磁盘空间数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p94261253205813"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p94261253205813"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p94261253205813"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p16166715155711"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p16166715155711"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p16166715155711"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3166191516578"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3166191516578"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p3166191516578"></a>1分钟</p>
</td>
</tr>
<tr id="row1460621720610"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p57524451528"><a name="zh-cn_topic_0084814075_p57524451528"></a><a name="zh-cn_topic_0084814075_p57524451528"></a>mountPointPrefix_disk_ioUtils 和volumePrefix_disk_ioUtils</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198904485488"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198904485488"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p198904485488"></a>（Agent）磁盘I/O使用率</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6204818503"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6204818503"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p6204818503"></a>该指标用于统计测量对象磁盘I/O使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15507131035617"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15507131035617"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p15507131035617"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul125541937123112"></a><a name="zh-cn_topic_0084814075_ul125541937123112"></a><ul id="zh-cn_topic_0084814075_ul125541937123112"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p186291818135219"><a name="zh-cn_topic_0084814075_p186291818135219"></a><a name="zh-cn_topic_0084814075_p186291818135219"></a>通过计算采集周期内/proc/diskstats中对应设备第十三列数据的变化得出磁盘I/O使用率。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p477581114379"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p477581114379"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p477581114379"></a>挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</p>
</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1761915344507"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1761915344507"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p1761915344507"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p745512515589"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p745512515589"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p745512515589"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1645517259587"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1645517259587"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1645517259587"></a>1分钟</p>
</td>
</tr>
<tr id="row1992104573"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1730419411353"><a name="zh-cn_topic_0084814075_p1730419411353"></a><a name="zh-cn_topic_0084814075_p1730419411353"></a>mountPointPrefix_disk_inodesUsedPercen</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_aecb1139b3e694480b09dcb590ce395ed"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_aecb1139b3e694480b09dcb590ce395ed"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_aecb1139b3e694480b09dcb590ce395ed"></a>（Agent）inode已使用占比</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_af7d7bf90b33c4ab8a734dca22a9b0803"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_af7d7bf90b33c4ab8a734dca22a9b0803"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_af7d7bf90b33c4ab8a734dca22a9b0803"></a>该指标用于统计测量对象当前磁盘已使用的inode占比。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p626484910565"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p626484910565"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p626484910565"></a>单位：百分比</p>
<a name="ul185801230171510"></a><a name="ul185801230171510"></a><ul id="ul185801230171510"><li>采集方式（Linux）：执行df -i命令，查看IUse%列数据。挂载点前缀路径长度不能超过64个字符，必须以字母开头，只能包含0-9/a-z/A-Z/-/./~。</li><li>Windows系统暂不支持文件系统类监控指标。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a976d888f07a94317952cbd3259ba9a2d"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a976d888f07a94317952cbd3259ba9a2d"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_a976d888f07a94317952cbd3259ba9a2d"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1549127915"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1549127915"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1549127915"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11491117710"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11491117710"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p11491117710"></a>1分钟</p>
</td>
</tr>
<tr id="row15365203619712"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p21850108820"><a name="zh-cn_topic_0084814075_p21850108820"></a><a name="zh-cn_topic_0084814075_p21850108820"></a>net_bitSent</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2281174621114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2281174621114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p2281174621114"></a>（Agent）入网带宽</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p117291054185012"><a name="zh-cn_topic_0084814075_p117291054185012"></a><a name="zh-cn_topic_0084814075_p117291054185012"></a>该指标用于统计测量对象网卡每秒接收的比特数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p119005035917"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p119005035917"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p119005035917"></a>单位：bit/s</p>
<a name="zh-cn_topic_0084814075_ul15438713143910"></a><a name="zh-cn_topic_0084814075_ul15438713143910"></a><ul id="zh-cn_topic_0084814075_ul15438713143910"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p351716217142"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p351716217142"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p351716217142"></a>≥ 0 bits/s</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p35151601923"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p35151601923"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p35151601923"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10515200127"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10515200127"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10515200127"></a>1分钟</p>
</td>
</tr>
<tr id="row536512361678"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p191851310883"><a name="zh-cn_topic_0084814075_p191851310883"></a><a name="zh-cn_topic_0084814075_p191851310883"></a>net_bitRecv</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p112711946161117"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p112711946161117"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p112711946161117"></a>（Agent）出网带宽</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p12729154165011"><a name="zh-cn_topic_0084814075_p12729154165011"></a><a name="zh-cn_topic_0084814075_p12729154165011"></a>该指标用于统计测量对象网卡每秒发送的比特数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12195165575819"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12195165575819"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p12195165575819"></a>单位：bit/s</p>
<a name="zh-cn_topic_0084814075_ul7241184533819"></a><a name="zh-cn_topic_0084814075_ul7241184533819"></a><ul id="zh-cn_topic_0084814075_ul7241184533819"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p42762467110"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p42762467110"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p42762467110"></a>≥ 0 bits/s</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p62621850618"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p62621850618"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p62621850618"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p42627501114"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p42627501114"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p42627501114"></a>1分钟</p>
</td>
</tr>
<tr id="row34777139820"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p318511101687"><a name="zh-cn_topic_0084814075_p318511101687"></a><a name="zh-cn_topic_0084814075_p318511101687"></a>net_packetRecv</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14290124641113"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14290124641113"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p14290124641113"></a>（Agent）网卡包接收速率</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4292134691112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4292134691112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4292134691112"></a>该指标用于统计测量对象网卡每秒接收的数据包数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1251716155915"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1251716155915"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1251716155915"></a>单位：Count/s</p>
<a name="zh-cn_topic_0084814075_ul117291816103919"></a><a name="zh-cn_topic_0084814075_ul117291816103919"></a><ul id="zh-cn_topic_0084814075_ul117291816103919"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4297104616118"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4297104616118"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p4297104616118"></a>≥ 0 counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p021851828"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p021851828"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p021851828"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p92186113215"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p92186113215"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p92186113215"></a>1分钟</p>
</td>
</tr>
<tr id="row1047811131281"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p673055425015"><a name="zh-cn_topic_0084814075_p673055425015"></a><a name="zh-cn_topic_0084814075_p673055425015"></a>net_packetSent</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p829924613116"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p829924613116"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p829924613116"></a>（Agent）网卡包发送速率</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13300194619118"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13300194619118"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p13300194619118"></a>该指标用于统计测量对象网卡每秒发送的数据包数。</p>
<p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1365112114592"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1365112114592"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p1365112114592"></a>单位：Count/s</p>
<a name="zh-cn_topic_0084814075_ul6600141843917"></a><a name="zh-cn_topic_0084814075_ul6600141843917"></a><ul id="zh-cn_topic_0084814075_ul6600141843917"><li>采集方式（Linux）：通过计算采集周期内/proc/net/dev中的变化得出。</li><li>采集方式（Windows）：使用WMI中MibIfRow对象获取网络指标数据。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p030515462112"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p030515462112"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_zh-cn_topic_0083516942_p030515462112"></a>≥ 0 counts/s</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18966811226"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18966811226"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p18966811226"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10966315218"><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10966315218"></a><a name="zh-cn_topic_0084814075_zh-cn_topic_0084814075_p10966315218"></a>1分钟</p>
</td>
</tr>
<tr id="row163471212145920"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="p264114410219"><a name="p264114410219"></a><a name="p264114410219"></a>net_tcp_total</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="p0641124413217"><a name="p0641124413217"></a><a name="p0641124413217"></a>（Agent）所有状态的TCP连接数总和</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="p176415443212"><a name="p176415443212"></a><a name="p176415443212"></a>该指标用于统计测量对象网卡所有状态的TCP连接数总和。</p>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="p196411044192113"><a name="p196411044192113"></a><a name="p196411044192113"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="p1264216446211"><a name="p1264216446211"></a><a name="p1264216446211"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="p364218441211"><a name="p364218441211"></a><a name="p364218441211"></a>1分钟</p>
</td>
</tr>
<tr id="row23486128597"><td class="cellrowborder" valign="top" width="12.110000000000003%" headers="mcps1.2.7.1.1 "><p id="p16642444142111"><a name="p16642444142111"></a><a name="p16642444142111"></a>net_tcp_established</p>
</td>
<td class="cellrowborder" valign="top" width="12.750000000000004%" headers="mcps1.2.7.1.2 "><p id="p26425448210"><a name="p26425448210"></a><a name="p26425448210"></a>（Agent）处于ESTABLISHED状态的TCP连接数量</p>
</td>
<td class="cellrowborder" valign="top" width="40.75000000000001%" headers="mcps1.2.7.1.3 "><p id="p464214444219"><a name="p464214444219"></a><a name="p464214444219"></a>该指标用于统计测量对象网卡处于ESTABLISHED状态的TCP连接数量。</p>
</td>
<td class="cellrowborder" valign="top" width="8.400000000000002%" headers="mcps1.2.7.1.4 "><p id="p1764254413215"><a name="p1764254413215"></a><a name="p1764254413215"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="8.300000000000002%" headers="mcps1.2.7.1.5 "><p id="p8642844162114"><a name="p8642844162114"></a><a name="p8642844162114"></a>云服务器</p>
</td>
<td class="cellrowborder" valign="top" width="17.69%" headers="mcps1.2.7.1.6 "><p id="p46421244122113"><a name="p46421244122113"></a><a name="p46421244122113"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

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

