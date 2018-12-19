# P1\(KVM\)   -- DPDK<a name="ZH-CN_TOPIC_0114104006"></a>

<a name="zh-cn_topic_0114079828_table31939521"></a>
<table><thead align="left"><tr id="zh-cn_topic_0114079828_row22445387"><th class="cellrowborder" valign="top" width="33.333333333333336%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0114079828_p6137036"><a name="zh-cn_topic_0114079828_p6137036"></a><a name="zh-cn_topic_0114079828_p6137036"></a>name</p>
</th>
<th class="cellrowborder" valign="top" width="22.222222222222225%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0114079828_p27337939"><a name="zh-cn_topic_0114079828_p27337939"></a><a name="zh-cn_topic_0114079828_p27337939"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.44444444444445%" id="mcps1.1.4.1.3"><p id="zh-cn_topic_0114079828_p66889413"><a name="zh-cn_topic_0114079828_p66889413"></a><a name="zh-cn_topic_0114079828_p66889413"></a>值</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0114079828_row49333388"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079828_p36581520"><a name="zh-cn_topic_0114079828_p36581520"></a><a name="zh-cn_topic_0114079828_p36581520"></a>hw:cpu_cores</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079828_p10313144"><a name="zh-cn_topic_0114079828_p10313144"></a><a name="zh-cn_topic_0114079828_p10313144"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079828_p30058349"><a name="zh-cn_topic_0114079828_p30058349"></a><a name="zh-cn_topic_0114079828_p30058349"></a>表示CPU核数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079828_row2089687"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079828_p35046986"><a name="zh-cn_topic_0114079828_p35046986"></a><a name="zh-cn_topic_0114079828_p35046986"></a>hw:cpu_policy</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079828_p20233597"><a name="zh-cn_topic_0114079828_p20233597"></a><a name="zh-cn_topic_0114079828_p20233597"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079828_p28308632"><a name="zh-cn_topic_0114079828_p28308632"></a><a name="zh-cn_topic_0114079828_p28308632"></a>表示cpu绑定策略</p>
<p id="zh-cn_topic_0114079828_p53451100"><a name="zh-cn_topic_0114079828_p53451100"></a><a name="zh-cn_topic_0114079828_p53451100"></a>取值：dedicated，表示绑核</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079828_row11297860"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079828_p42711464"><a name="zh-cn_topic_0114079828_p42711464"></a><a name="zh-cn_topic_0114079828_p42711464"></a>hw:cpu_sockets</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079828_p37076589"><a name="zh-cn_topic_0114079828_p37076589"></a><a name="zh-cn_topic_0114079828_p37076589"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079828_p50413755"><a name="zh-cn_topic_0114079828_p50413755"></a><a name="zh-cn_topic_0114079828_p50413755"></a>表示CPU插槽数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079828_row51070612"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079828_p43078913"><a name="zh-cn_topic_0114079828_p43078913"></a><a name="zh-cn_topic_0114079828_p43078913"></a>hw:cpu_thread_policy</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079828_p66839947"><a name="zh-cn_topic_0114079828_p66839947"></a><a name="zh-cn_topic_0114079828_p66839947"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079828_p45326617"><a name="zh-cn_topic_0114079828_p45326617"></a><a name="zh-cn_topic_0114079828_p45326617"></a>表示cpu超线程策略，仅当hw:cpu_policy=dedicated时生效</p>
<a name="ul16198132113527"></a><a name="ul16198132113527"></a><ul id="ul16198132113527"><li>prefer：如果物理机支持超线程，那么同一个guest的vCPU将尽可能的被调度到相同的core上。</li><li>isolate：如果物理机支持超线程，那么同一个guest的vCPU将会被分到不同的core上，并且其他guest的vCPU不再允许调度到当前的core上。</li><li>require：主机必须有超线程，每个vCPU将被分配到线程兄弟节点上。</li></ul>
<p id="zh-cn_topic_0114079828_p28561251"><a name="zh-cn_topic_0114079828_p28561251"></a><a name="zh-cn_topic_0114079828_p28561251"></a>取值：require</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079828_row55724670"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079828_p17404391"><a name="zh-cn_topic_0114079828_p17404391"></a><a name="zh-cn_topic_0114079828_p17404391"></a>hw:cpu_threads</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079828_p469528"><a name="zh-cn_topic_0114079828_p469528"></a><a name="zh-cn_topic_0114079828_p469528"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079828_p38031802"><a name="zh-cn_topic_0114079828_p38031802"></a><a name="zh-cn_topic_0114079828_p38031802"></a>表示CPU超线程数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079828_row6741900"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079828_p9223066"><a name="zh-cn_topic_0114079828_p9223066"></a><a name="zh-cn_topic_0114079828_p9223066"></a>p2p_direct:alias</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079828_p8870892"><a name="zh-cn_topic_0114079828_p8870892"></a><a name="zh-cn_topic_0114079828_p8870892"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079828_p47453675"><a name="zh-cn_topic_0114079828_p47453675"></a><a name="zh-cn_topic_0114079828_p47453675"></a>表示支持p2p direct的设备</p>
<p id="zh-cn_topic_0114079828_p24429894"><a name="zh-cn_topic_0114079828_p24429894"></a><a name="zh-cn_topic_0114079828_p24429894"></a>取值：nvidia-p100</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079828_row18542462"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079828_p25544462"><a name="zh-cn_topic_0114079828_p25544462"></a><a name="zh-cn_topic_0114079828_p25544462"></a>pci_passthrough:alias</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079828_p55835522"><a name="zh-cn_topic_0114079828_p55835522"></a><a name="zh-cn_topic_0114079828_p55835522"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079828_p26383427"><a name="zh-cn_topic_0114079828_p26383427"></a><a name="zh-cn_topic_0114079828_p26383427"></a>指定PCI直通设备及数量</p>
<p id="zh-cn_topic_0114079828_p36124251"><a name="zh-cn_topic_0114079828_p36124251"></a><a name="zh-cn_topic_0114079828_p36124251"></a>格式：pci_type: count</p>
<p id="zh-cn_topic_0114079828_p56682808"><a name="zh-cn_topic_0114079828_p56682808"></a><a name="zh-cn_topic_0114079828_p56682808"></a>示例：nvidia-p100:1</p>
<p id="zh-cn_topic_0114079828_p40383225"><a name="zh-cn_topic_0114079828_p40383225"></a><a name="zh-cn_topic_0114079828_p40383225"></a>1. pci_type：表示直通设备。</p>
<p id="zh-cn_topic_0114079828_p27904713"><a name="zh-cn_topic_0114079828_p27904713"></a><a name="zh-cn_topic_0114079828_p27904713"></a>2. count：guest配备的直通设备个数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079828_row49815832"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079828_p8550624"><a name="zh-cn_topic_0114079828_p8550624"></a><a name="zh-cn_topic_0114079828_p8550624"></a>quota:gpu</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079828_p21511928"><a name="zh-cn_topic_0114079828_p21511928"></a><a name="zh-cn_topic_0114079828_p21511928"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079828_p64744584"><a name="zh-cn_topic_0114079828_p64744584"></a><a name="zh-cn_topic_0114079828_p64744584"></a>表示使用的GPU类型</p>
<p id="zh-cn_topic_0114079828_p45830349"><a name="zh-cn_topic_0114079828_p45830349"></a><a name="zh-cn_topic_0114079828_p45830349"></a>取值：nvidia-p100</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079828_row9819961"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079828_p57219378"><a name="zh-cn_topic_0114079828_p57219378"></a><a name="zh-cn_topic_0114079828_p57219378"></a>quota:nvme_ssd</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079828_p4258076"><a name="zh-cn_topic_0114079828_p4258076"></a><a name="zh-cn_topic_0114079828_p4258076"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079828_p9359903"><a name="zh-cn_topic_0114079828_p9359903"></a><a name="zh-cn_topic_0114079828_p9359903"></a>表示使用nvme ssd硬盘</p>
<p id="zh-cn_topic_0114079828_p17130265"><a name="zh-cn_topic_0114079828_p17130265"></a><a name="zh-cn_topic_0114079828_p17130265"></a>格式：disk_type:spec:count:size:safe_format</p>
<p id="zh-cn_topic_0114079828_p19954658"><a name="zh-cn_topic_0114079828_p19954658"></a><a name="zh-cn_topic_0114079828_p19954658"></a>示例：800G:large:1:800:True</p>
<a name="ol083484913524"></a><a name="ol083484913524"></a><ol id="ol083484913524"><li>disk_type表示主机上配备的nvme ssd的单卡容量大小。</li><li>spec：large表示大规格，small表示小规格。</li><li>count：guest配备的nvme ssd卡个数。</li><li>size：guest使用的盘的容量大小。在大规格情况下，此项即为host单卡大小，在小规格情况下，此为1/4规格或者1/2规格，单位为GB。</li><li>safe_format：删除弹性云服务器时是否进行安全格式化操作，True/False。</li></ol>
</td>
</tr>
<tr id="zh-cn_topic_0114079828_row46570941"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079828_p14149906"><a name="zh-cn_topic_0114079828_p14149906"></a><a name="zh-cn_topic_0114079828_p14149906"></a>quota:vif_max_rate</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079828_p5291760"><a name="zh-cn_topic_0114079828_p5291760"></a><a name="zh-cn_topic_0114079828_p5291760"></a>int</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079828_p25979390"><a name="zh-cn_topic_0114079828_p25979390"></a><a name="zh-cn_topic_0114079828_p25979390"></a>用于网络接口限速，单位Mbps</p>
</td>
</tr>
</tbody>
</table>

