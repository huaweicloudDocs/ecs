# 弹性云服务器支持的进程监控指标（安装Agent）<a name="ecs_03_1013"></a>

## 功能说明<a name="section12784212213"></a>

通过在弹性云服务器中安装Agent插件，可以对主机内的活跃进程进行监控，默认采集活跃进程消耗的CPU、内存，以及打开的文件数量等信息。

本节定义了弹性云服务器上报云监控的进程监控指标。

## 命名空间<a name="section24282572112133"></a>

AGT.ECS

## 进程监控指标说明<a name="section47952021926"></a>

对于不同的操作系统、不同的弹性云服务器类型，在安装Agent后均默认支持查看以下进程监控指标。

**表 1**  进程监控指标说明

<a name="zh-cn_topic_0084814075_table131966151727"></a>
<table><thead align="left"><tr id="zh-cn_topic_0084814075_row61979157214"><th class="cellrowborder" valign="top" width="13.71%" id="mcps1.2.7.1.1"><p id="zh-cn_topic_0084814075_p151971153212"><a name="zh-cn_topic_0084814075_p151971153212"></a><a name="zh-cn_topic_0084814075_p151971153212"></a>指标</p>
</th>
<th class="cellrowborder" valign="top" width="11.28%" id="mcps1.2.7.1.2"><p id="zh-cn_topic_0084814075_p18197615628"><a name="zh-cn_topic_0084814075_p18197615628"></a><a name="zh-cn_topic_0084814075_p18197615628"></a>指标名称</p>
</th>
<th class="cellrowborder" valign="top" width="35.120000000000005%" id="mcps1.2.7.1.3"><p id="zh-cn_topic_0084814075_p619717151526"><a name="zh-cn_topic_0084814075_p619717151526"></a><a name="zh-cn_topic_0084814075_p619717151526"></a>指标含义</p>
</th>
<th class="cellrowborder" valign="top" width="16.88%" id="mcps1.2.7.1.4"><p id="zh-cn_topic_0084814075_p419718157213"><a name="zh-cn_topic_0084814075_p419718157213"></a><a name="zh-cn_topic_0084814075_p419718157213"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="10.23%" id="mcps1.2.7.1.5"><p id="zh-cn_topic_0084814075_p111978155217"><a name="zh-cn_topic_0084814075_p111978155217"></a><a name="zh-cn_topic_0084814075_p111978155217"></a>测量对象（维度）</p>
</th>
<th class="cellrowborder" valign="top" width="12.78%" id="mcps1.2.7.1.6"><p id="zh-cn_topic_0084814075_p1519718153215"><a name="zh-cn_topic_0084814075_p1519718153215"></a><a name="zh-cn_topic_0084814075_p1519718153215"></a>监控周期（原始指标）</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0084814075_row5197015627"><td class="cellrowborder" valign="top" width="13.71%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p1546885210474"><a name="zh-cn_topic_0084814075_p1546885210474"></a><a name="zh-cn_topic_0084814075_p1546885210474"></a>proc_pHashId_cpu</p>
</td>
<td class="cellrowborder" valign="top" width="11.28%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p19146121813512"><a name="zh-cn_topic_0084814075_p19146121813512"></a><a name="zh-cn_topic_0084814075_p19146121813512"></a>CPU使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.120000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p072719521252"><a name="zh-cn_topic_0084814075_p072719521252"></a><a name="zh-cn_topic_0084814075_p072719521252"></a>进程消耗的CPU百分比，pHashId是（进程名+进程ID）的md5值。</p>
<p id="zh-cn_topic_0084814075_p127514570146"><a name="zh-cn_topic_0084814075_p127514570146"></a><a name="zh-cn_topic_0084814075_p127514570146"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul188031147670"></a><a name="zh-cn_topic_0084814075_ul188031147670"></a><ul id="zh-cn_topic_0084814075_ul188031147670"><li>采集方式（Linux）：通过计算/proc/pid/stat的变化得出。</li><li>采集方式（Windows）：通过Windows API GetProcessTimes获取进程CPU使用率。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p101988152216"><a name="zh-cn_topic_0084814075_p101988152216"></a><a name="zh-cn_topic_0084814075_p101988152216"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p819818151120"><a name="zh-cn_topic_0084814075_p819818151120"></a><a name="zh-cn_topic_0084814075_p819818151120"></a><span id="text1983125020420"><a name="text1983125020420"></a><a name="text1983125020420"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.78%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p1919819151127"><a name="zh-cn_topic_0084814075_p1919819151127"></a><a name="zh-cn_topic_0084814075_p1919819151127"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row122547189416"><td class="cellrowborder" valign="top" width="13.71%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p116763499474"><a name="zh-cn_topic_0084814075_p116763499474"></a><a name="zh-cn_topic_0084814075_p116763499474"></a>proc_pHashId_mem</p>
</td>
<td class="cellrowborder" valign="top" width="11.28%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p8724192617519"><a name="zh-cn_topic_0084814075_p8724192617519"></a><a name="zh-cn_topic_0084814075_p8724192617519"></a>内存使用率</p>
</td>
<td class="cellrowborder" valign="top" width="35.120000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p282220584518"><a name="zh-cn_topic_0084814075_p282220584518"></a><a name="zh-cn_topic_0084814075_p282220584518"></a>进程消耗的内存百分比，pHashId是（进程名+进程ID）的md5值。</p>
<p id="zh-cn_topic_0084814075_p97751859161412"><a name="zh-cn_topic_0084814075_p97751859161412"></a><a name="zh-cn_topic_0084814075_p97751859161412"></a>单位：百分比</p>
<a name="zh-cn_topic_0084814075_ul17380127818"></a><a name="zh-cn_topic_0084814075_ul17380127818"></a><ul id="zh-cn_topic_0084814075_ul17380127818"><li>采集方式（Linux）：<p id="zh-cn_topic_0084814075_p143075818819"><a name="zh-cn_topic_0084814075_p143075818819"></a><a name="zh-cn_topic_0084814075_p143075818819"></a>RSS*PAGESIZE/MemTotal</p>
<p id="zh-cn_topic_0084814075_p1343018589820"><a name="zh-cn_topic_0084814075_p1343018589820"></a><a name="zh-cn_topic_0084814075_p1343018589820"></a>RSS: 通过获取/proc/pid/statm第二列得到</p>
<p id="zh-cn_topic_0084814075_p1143011589815"><a name="zh-cn_topic_0084814075_p1143011589815"></a><a name="zh-cn_topic_0084814075_p1143011589815"></a>PAGESIZE: 通过命令getconf PAGESIZE获取</p>
<p id="zh-cn_topic_0084814075_p184302584813"><a name="zh-cn_topic_0084814075_p184302584813"></a><a name="zh-cn_topic_0084814075_p184302584813"></a>MemTotal：通过/proc/meminfo获取</p>
</li><li>采集方式（Windows）：使用Windows  API procGlobalMemoryStatusEx获取内存总量，通过GetProcessMemoryInfo获取内存已使用量，计算两者比值得到内存使用率。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p122558181345"><a name="zh-cn_topic_0084814075_p122558181345"></a><a name="zh-cn_topic_0084814075_p122558181345"></a>0-100%</p>
</td>
<td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p125518181647"><a name="zh-cn_topic_0084814075_p125518181647"></a><a name="zh-cn_topic_0084814075_p125518181647"></a><span id="text111021424121218"><a name="text111021424121218"></a><a name="text111021424121218"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.78%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p2255181818412"><a name="zh-cn_topic_0084814075_p2255181818412"></a><a name="zh-cn_topic_0084814075_p2255181818412"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row134801141742"><td class="cellrowborder" valign="top" width="13.71%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p16108144124710"><a name="zh-cn_topic_0084814075_p16108144124710"></a><a name="zh-cn_topic_0084814075_p16108144124710"></a>proc_pHashId_file</p>
</td>
<td class="cellrowborder" valign="top" width="11.28%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p135156347514"><a name="zh-cn_topic_0084814075_p135156347514"></a><a name="zh-cn_topic_0084814075_p135156347514"></a>打开文件数</p>
</td>
<td class="cellrowborder" valign="top" width="35.120000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p6494154211513"><a name="zh-cn_topic_0084814075_p6494154211513"></a><a name="zh-cn_topic_0084814075_p6494154211513"></a>进程打开文件数，pHashId是（进程名+进程ID）的md5值。</p>
<a name="zh-cn_topic_0084814075_ul1567503084"></a><a name="zh-cn_topic_0084814075_ul1567503084"></a><ul id="zh-cn_topic_0084814075_ul1567503084"><li>采集方式（Linux）：通过执行ls -l /proc/pid/fd 可以查看数量。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p194801914147"><a name="zh-cn_topic_0084814075_p194801914147"></a><a name="zh-cn_topic_0084814075_p194801914147"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p1248011141749"><a name="zh-cn_topic_0084814075_p1248011141749"></a><a name="zh-cn_topic_0084814075_p1248011141749"></a><span id="text177779274123"><a name="text177779274123"></a><a name="text177779274123"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.78%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p9480141419415"><a name="zh-cn_topic_0084814075_p9480141419415"></a><a name="zh-cn_topic_0084814075_p9480141419415"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row104062369319"><td class="cellrowborder" valign="top" width="13.71%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p106651442103712"><a name="zh-cn_topic_0084814075_p106651442103712"></a><a name="zh-cn_topic_0084814075_p106651442103712"></a>proc_running_count</p>
</td>
<td class="cellrowborder" valign="top" width="11.28%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p6740185510386"><a name="zh-cn_topic_0084814075_p6740185510386"></a><a name="zh-cn_topic_0084814075_p6740185510386"></a>(Agent) 运行中进程数</p>
</td>
<td class="cellrowborder" valign="top" width="35.120000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p072111023915"><a name="zh-cn_topic_0084814075_p072111023915"></a><a name="zh-cn_topic_0084814075_p072111023915"></a>该指标用于统计测量对象处于运行状态的进程数。</p>
<a name="zh-cn_topic_0084814075_ul4970742815"></a><a name="zh-cn_topic_0084814075_ul4970742815"></a><ul id="zh-cn_topic_0084814075_ul4970742815"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p134061536931"><a name="zh-cn_topic_0084814075_p134061536931"></a><a name="zh-cn_topic_0084814075_p134061536931"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p94061361331"><a name="zh-cn_topic_0084814075_p94061361331"></a><a name="zh-cn_topic_0084814075_p94061361331"></a><span id="text17432029151211"><a name="text17432029151211"></a><a name="text17432029151211"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.78%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p174062360316"><a name="zh-cn_topic_0084814075_p174062360316"></a><a name="zh-cn_topic_0084814075_p174062360316"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row162083416319"><td class="cellrowborder" valign="top" width="13.71%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p106651042113715"><a name="zh-cn_topic_0084814075_p106651042113715"></a><a name="zh-cn_topic_0084814075_p106651042113715"></a>proc_idle_count</p>
</td>
<td class="cellrowborder" valign="top" width="11.28%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p3740125514380"><a name="zh-cn_topic_0084814075_p3740125514380"></a><a name="zh-cn_topic_0084814075_p3740125514380"></a>(Agent) 空闲进程数</p>
</td>
<td class="cellrowborder" valign="top" width="35.120000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p872120113911"><a name="zh-cn_topic_0084814075_p872120113911"></a><a name="zh-cn_topic_0084814075_p872120113911"></a>该指标用于统计测量对象处于空闲状态的进程数。</p>
<a name="zh-cn_topic_0084814075_ul5222137680"></a><a name="zh-cn_topic_0084814075_ul5222137680"></a><ul id="zh-cn_topic_0084814075_ul5222137680"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p11621934838"><a name="zh-cn_topic_0084814075_p11621934838"></a><a name="zh-cn_topic_0084814075_p11621934838"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p662133414311"><a name="zh-cn_topic_0084814075_p662133414311"></a><a name="zh-cn_topic_0084814075_p662133414311"></a><span id="text1394703131218"><a name="text1394703131218"></a><a name="text1394703131218"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.78%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p36212343319"><a name="zh-cn_topic_0084814075_p36212343319"></a><a name="zh-cn_topic_0084814075_p36212343319"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row11531321333"><td class="cellrowborder" valign="top" width="13.71%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p66651142143710"><a name="zh-cn_topic_0084814075_p66651142143710"></a><a name="zh-cn_topic_0084814075_p66651142143710"></a>proc_zombie_count</p>
</td>
<td class="cellrowborder" valign="top" width="11.28%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p274010553387"><a name="zh-cn_topic_0084814075_p274010553387"></a><a name="zh-cn_topic_0084814075_p274010553387"></a>(Agent) 僵死进程数</p>
</td>
<td class="cellrowborder" valign="top" width="35.120000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p07216015392"><a name="zh-cn_topic_0084814075_p07216015392"></a><a name="zh-cn_topic_0084814075_p07216015392"></a>该指标用于统计测量对象处于僵死状态的进程数。</p>
<a name="zh-cn_topic_0084814075_ul18587962817"></a><a name="zh-cn_topic_0084814075_ul18587962817"></a><ul id="zh-cn_topic_0084814075_ul18587962817"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p185423216318"><a name="zh-cn_topic_0084814075_p185423216318"></a><a name="zh-cn_topic_0084814075_p185423216318"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p105423214314"><a name="zh-cn_topic_0084814075_p105423214314"></a><a name="zh-cn_topic_0084814075_p105423214314"></a><span id="text1689234101214"><a name="text1689234101214"></a><a name="text1689234101214"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.78%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p15414324316"><a name="zh-cn_topic_0084814075_p15414324316"></a><a name="zh-cn_topic_0084814075_p15414324316"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row202201298317"><td class="cellrowborder" valign="top" width="13.71%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p116651042143719"><a name="zh-cn_topic_0084814075_p116651042143719"></a><a name="zh-cn_topic_0084814075_p116651042143719"></a>proc_blocked_count</p>
</td>
<td class="cellrowborder" valign="top" width="11.28%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p2740755103817"><a name="zh-cn_topic_0084814075_p2740755103817"></a><a name="zh-cn_topic_0084814075_p2740755103817"></a>(Agent) 阻塞进程数</p>
</td>
<td class="cellrowborder" valign="top" width="35.120000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p1972120103917"><a name="zh-cn_topic_0084814075_p1972120103917"></a><a name="zh-cn_topic_0084814075_p1972120103917"></a>该指标用于统计测量对象被阻塞的进程数。</p>
<a name="zh-cn_topic_0084814075_ul097288687"></a><a name="zh-cn_topic_0084814075_ul097288687"></a><ul id="zh-cn_topic_0084814075_ul097288687"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p13220102911317"><a name="zh-cn_topic_0084814075_p13220102911317"></a><a name="zh-cn_topic_0084814075_p13220102911317"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p8220192918316"><a name="zh-cn_topic_0084814075_p8220192918316"></a><a name="zh-cn_topic_0084814075_p8220192918316"></a><span id="text11229336121217"><a name="text11229336121217"></a><a name="text11229336121217"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.78%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p19220122914310"><a name="zh-cn_topic_0084814075_p19220122914310"></a><a name="zh-cn_topic_0084814075_p19220122914310"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row1578216251831"><td class="cellrowborder" valign="top" width="13.71%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p12666542163710"><a name="zh-cn_topic_0084814075_p12666542163710"></a><a name="zh-cn_topic_0084814075_p12666542163710"></a>proc_sleeping_count</p>
</td>
<td class="cellrowborder" valign="top" width="11.28%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p1741105513811"><a name="zh-cn_topic_0084814075_p1741105513811"></a><a name="zh-cn_topic_0084814075_p1741105513811"></a>(Agent) 睡眠进程数</p>
</td>
<td class="cellrowborder" valign="top" width="35.120000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p17215017397"><a name="zh-cn_topic_0084814075_p17215017397"></a><a name="zh-cn_topic_0084814075_p17215017397"></a>该指标用于统计测量对象处于睡眠状态的进程数。</p>
<a name="zh-cn_topic_0084814075_ul456914117813"></a><a name="zh-cn_topic_0084814075_ul456914117813"></a><ul id="zh-cn_topic_0084814075_ul456914117813"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：暂不支持。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p18783102510317"><a name="zh-cn_topic_0084814075_p18783102510317"></a><a name="zh-cn_topic_0084814075_p18783102510317"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p15783182510318"><a name="zh-cn_topic_0084814075_p15783182510318"></a><a name="zh-cn_topic_0084814075_p15783182510318"></a><span id="text1984717397124"><a name="text1984717397124"></a><a name="text1984717397124"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.78%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p18783225630"><a name="zh-cn_topic_0084814075_p18783225630"></a><a name="zh-cn_topic_0084814075_p18783225630"></a>1分钟</p>
</td>
</tr>
<tr id="zh-cn_topic_0084814075_row81989151821"><td class="cellrowborder" valign="top" width="13.71%" headers="mcps1.2.7.1.1 "><p id="zh-cn_topic_0084814075_p18666134223719"><a name="zh-cn_topic_0084814075_p18666134223719"></a><a name="zh-cn_topic_0084814075_p18666134223719"></a>proc_total_count</p>
</td>
<td class="cellrowborder" valign="top" width="11.28%" headers="mcps1.2.7.1.2 "><p id="zh-cn_topic_0084814075_p137416556389"><a name="zh-cn_topic_0084814075_p137416556389"></a><a name="zh-cn_topic_0084814075_p137416556389"></a>(Agent) 系统进程数</p>
</td>
<td class="cellrowborder" valign="top" width="35.120000000000005%" headers="mcps1.2.7.1.3 "><p id="zh-cn_topic_0084814075_p157213019397"><a name="zh-cn_topic_0084814075_p157213019397"></a><a name="zh-cn_topic_0084814075_p157213019397"></a>该指标用于统计测量对象的总进程数。</p>
<a name="zh-cn_topic_0084814075_ul582615139815"></a><a name="zh-cn_topic_0084814075_ul582615139815"></a><ul id="zh-cn_topic_0084814075_ul582615139815"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：通过psapi.dll系统进程状态支持模块得到进程总数。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.7.1.4 "><p id="zh-cn_topic_0084814075_p5199161514219"><a name="zh-cn_topic_0084814075_p5199161514219"></a><a name="zh-cn_topic_0084814075_p5199161514219"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.7.1.5 "><p id="zh-cn_topic_0084814075_p2199111519210"><a name="zh-cn_topic_0084814075_p2199111519210"></a><a name="zh-cn_topic_0084814075_p2199111519210"></a><span id="text1971425121"><a name="text1971425121"></a><a name="text1971425121"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="12.78%" headers="mcps1.2.7.1.6 "><p id="zh-cn_topic_0084814075_p419917154212"><a name="zh-cn_topic_0084814075_p419917154212"></a><a name="zh-cn_topic_0084814075_p419917154212"></a>1分钟</p>
</td>
</tr>
<tr id="row5654161815453"><td class="cellrowborder" valign="top" width="13.71%" headers="mcps1.2.7.1.1 "><p id="p1365591815459"><a name="p1365591815459"></a><a name="p1365591815459"></a>proc_specified_count</p>
</td>
<td class="cellrowborder" valign="top" width="11.28%" headers="mcps1.2.7.1.2 "><p id="p76551918104514"><a name="p76551918104514"></a><a name="p76551918104514"></a>(Agent) 指定进程数</p>
</td>
<td class="cellrowborder" valign="top" width="35.120000000000005%" headers="mcps1.2.7.1.3 "><p id="p1065501817454"><a name="p1065501817454"></a><a name="p1065501817454"></a>该指标用于统计测量对象指定的进程数。</p>
<a name="ul568845714455"></a><a name="ul568845714455"></a><ul id="ul568845714455"><li>采集方式（Linux）：通过统计 /proc/pid/status 中Status值获取每个进程的状态，进而统计各个状态进程总数。</li><li>采集方式（Windows）：通过psapi.dll系统进程状态支持模块得到进程总数。</li></ul>
</td>
<td class="cellrowborder" valign="top" width="16.88%" headers="mcps1.2.7.1.4 "><p id="p1565511854515"><a name="p1565511854515"></a><a name="p1565511854515"></a>≥0</p>
</td>
<td class="cellrowborder" valign="top" width="10.23%" headers="mcps1.2.7.1.5 "><a name="ul5985322104918"></a><a name="ul5985322104918"></a><ul id="ul5985322104918"><li><span id="text35141744131211"><a name="text35141744131211"></a><a name="text35141744131211"></a>云服务器</span></li><li><span id="text743713463123"><a name="text743713463123"></a><a name="text743713463123"></a>云服务器</span> - 进程</li></ul>
</td>
<td class="cellrowborder" valign="top" width="12.78%" headers="mcps1.2.7.1.6 "><p id="p1665519188454"><a name="p1665519188454"></a><a name="p1665519188454"></a>1分钟</p>
</td>
</tr>
</tbody>
</table>

## 维度<a name="section36963297112133"></a>

<a name="table41237041112133"></a>
<table><thead align="left"><tr id="row28021974112133"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.1.4.1.1"><p id="p9189163971113"><a name="p9189163971113"></a><a name="p9189163971113"></a>维度</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.1.4.1.2"><p id="p55187441112133"><a name="p55187441112133"></a><a name="p55187441112133"></a>Key</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.1.4.1.3"><p id="p40997749112133"><a name="p40997749112133"></a><a name="p40997749112133"></a>Value</p>
</th>
</tr>
</thead>
<tbody><tr id="row32483336112133"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.1 "><p id="p8821155612914"><a name="p8821155612914"></a><a name="p8821155612914"></a><span id="text631414559129"><a name="text631414559129"></a><a name="text631414559129"></a>云服务器</span></p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.2 "><p id="p13904597112133"><a name="p13904597112133"></a><a name="p13904597112133"></a>instance_id</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.3 "><p id="p52530562112133"><a name="p52530562112133"></a><a name="p52530562112133"></a><span id="text173241214361"><a name="text173241214361"></a><a name="text173241214361"></a>云服务器</span>ID。</p>
</td>
</tr>
<tr id="row1273932910106"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.1 "><p id="p1031111110102"><a name="p1031111110102"></a><a name="p1031111110102"></a><span id="text12148258151214"><a name="text12148258151214"></a><a name="text12148258151214"></a>云服务器</span> - 进程</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.2 "><p id="p17739182961016"><a name="p17739182961016"></a><a name="p17739182961016"></a>proc</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.3 "><p id="p9532152615102"><a name="p9532152615102"></a><a name="p9532152615102"></a><span id="text18340142814103"><a name="text18340142814103"></a><a name="text18340142814103"></a>云服务器</span>的进程。</p>
<p id="p53231813996"><a name="p53231813996"></a><a name="p53231813996"></a>该取值可通过云监控服务的“<a href="https://support.huaweicloud.com/api-ces/ListAgentDimensionInfo.html" target="_blank" rel="noopener noreferrer">查询主机监控维度指标信息</a>”获取。</p>
</td>
</tr>
</tbody>
</table>

