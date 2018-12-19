# P2\(KVM\)   -- DPDK<a name="ZH-CN_TOPIC_0114104007"></a>

<a name="zh-cn_topic_0114079830_table43589530"></a>
<table><thead align="left"><tr id="zh-cn_topic_0114079830_row15575880"><th class="cellrowborder" valign="top" width="33.333333333333336%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0114079830_p53686747"><a name="zh-cn_topic_0114079830_p53686747"></a><a name="zh-cn_topic_0114079830_p53686747"></a>name</p>
</th>
<th class="cellrowborder" valign="top" width="22.222222222222225%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0114079830_p53659222"><a name="zh-cn_topic_0114079830_p53659222"></a><a name="zh-cn_topic_0114079830_p53659222"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="44.44444444444445%" id="mcps1.1.4.1.3"><p id="zh-cn_topic_0114079830_p51429730"><a name="zh-cn_topic_0114079830_p51429730"></a><a name="zh-cn_topic_0114079830_p51429730"></a>值</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0114079830_row5058598"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079830_p7093323"><a name="zh-cn_topic_0114079830_p7093323"></a><a name="zh-cn_topic_0114079830_p7093323"></a>hw:cpu_cores</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079830_p37688313"><a name="zh-cn_topic_0114079830_p37688313"></a><a name="zh-cn_topic_0114079830_p37688313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079830_p32854487"><a name="zh-cn_topic_0114079830_p32854487"></a><a name="zh-cn_topic_0114079830_p32854487"></a>表示CPU核数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079830_row27254927"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079830_p60165497"><a name="zh-cn_topic_0114079830_p60165497"></a><a name="zh-cn_topic_0114079830_p60165497"></a>hw:cpu_policy</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079830_p41567079"><a name="zh-cn_topic_0114079830_p41567079"></a><a name="zh-cn_topic_0114079830_p41567079"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079830_p11490242"><a name="zh-cn_topic_0114079830_p11490242"></a><a name="zh-cn_topic_0114079830_p11490242"></a>表示cpu绑定策略</p>
<p id="zh-cn_topic_0114079830_p36303315"><a name="zh-cn_topic_0114079830_p36303315"></a><a name="zh-cn_topic_0114079830_p36303315"></a>取值：dedicated，表示绑核</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079830_row58294385"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079830_p24224733"><a name="zh-cn_topic_0114079830_p24224733"></a><a name="zh-cn_topic_0114079830_p24224733"></a>hw:cpu_sockets</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079830_p16046317"><a name="zh-cn_topic_0114079830_p16046317"></a><a name="zh-cn_topic_0114079830_p16046317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079830_p24683273"><a name="zh-cn_topic_0114079830_p24683273"></a><a name="zh-cn_topic_0114079830_p24683273"></a>表示CPU插槽数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079830_row20822872"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079830_p8931058"><a name="zh-cn_topic_0114079830_p8931058"></a><a name="zh-cn_topic_0114079830_p8931058"></a>hw:cpu_thread_policy</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079830_p52327117"><a name="zh-cn_topic_0114079830_p52327117"></a><a name="zh-cn_topic_0114079830_p52327117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079830_p10638097"><a name="zh-cn_topic_0114079830_p10638097"></a><a name="zh-cn_topic_0114079830_p10638097"></a>表示cpu超线程策略，仅当hw:cpu_policy=dedicated时生效</p>
<a name="ul1837573925320"></a><a name="ul1837573925320"></a><ul id="ul1837573925320"><li>prefer：如果物理机支持超线程，那么同一个guest的vCPU将尽可能的被调度到相同的core上。</li><li>isolate：如果物理机支持超线程，那么同一个guest的vCPU将会被分到不同的core上，并且其他guest的vCPU不再允许调度到当前的core上。</li><li>require：主机必须有超线程，每个vCPU将被分配到线程兄弟节点上。</li></ul>
<p id="zh-cn_topic_0114079830_p3336177"><a name="zh-cn_topic_0114079830_p3336177"></a><a name="zh-cn_topic_0114079830_p3336177"></a>取值：require</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079830_row30025596"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079830_p16154192"><a name="zh-cn_topic_0114079830_p16154192"></a><a name="zh-cn_topic_0114079830_p16154192"></a>hw:cpu_threads</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079830_p33421169"><a name="zh-cn_topic_0114079830_p33421169"></a><a name="zh-cn_topic_0114079830_p33421169"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079830_p22760134"><a name="zh-cn_topic_0114079830_p22760134"></a><a name="zh-cn_topic_0114079830_p22760134"></a>表示CPU超线程数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079830_row3514615"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079830_p16248438"><a name="zh-cn_topic_0114079830_p16248438"></a><a name="zh-cn_topic_0114079830_p16248438"></a>p2p_direct:alias</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079830_p41055134"><a name="zh-cn_topic_0114079830_p41055134"></a><a name="zh-cn_topic_0114079830_p41055134"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079830_p37131542"><a name="zh-cn_topic_0114079830_p37131542"></a><a name="zh-cn_topic_0114079830_p37131542"></a>表示支持p2p direct的设备</p>
<p id="zh-cn_topic_0114079830_p65748423"><a name="zh-cn_topic_0114079830_p65748423"></a><a name="zh-cn_topic_0114079830_p65748423"></a>取值：nvidia-v100-pcie</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079830_row54864902"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079830_p14872087"><a name="zh-cn_topic_0114079830_p14872087"></a><a name="zh-cn_topic_0114079830_p14872087"></a>pci_passthrough:alias</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079830_p63788400"><a name="zh-cn_topic_0114079830_p63788400"></a><a name="zh-cn_topic_0114079830_p63788400"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079830_p66586810"><a name="zh-cn_topic_0114079830_p66586810"></a><a name="zh-cn_topic_0114079830_p66586810"></a>指定PCI直通设备及数量</p>
<p id="zh-cn_topic_0114079830_p62410385"><a name="zh-cn_topic_0114079830_p62410385"></a><a name="zh-cn_topic_0114079830_p62410385"></a>格式：pci_type: count</p>
<p id="zh-cn_topic_0114079830_p24822557"><a name="zh-cn_topic_0114079830_p24822557"></a><a name="zh-cn_topic_0114079830_p24822557"></a>示例：nvidia-v100-pcie:1</p>
<p id="zh-cn_topic_0114079830_p22076423"><a name="zh-cn_topic_0114079830_p22076423"></a><a name="zh-cn_topic_0114079830_p22076423"></a>1. pci_type表示直通设备；</p>
<p id="zh-cn_topic_0114079830_p64470080"><a name="zh-cn_topic_0114079830_p64470080"></a><a name="zh-cn_topic_0114079830_p64470080"></a>2. count：guest配备的直通设备个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079830_row43359809"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079830_p22483623"><a name="zh-cn_topic_0114079830_p22483623"></a><a name="zh-cn_topic_0114079830_p22483623"></a>quota:gpu</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079830_p9234211"><a name="zh-cn_topic_0114079830_p9234211"></a><a name="zh-cn_topic_0114079830_p9234211"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079830_p9773594"><a name="zh-cn_topic_0114079830_p9773594"></a><a name="zh-cn_topic_0114079830_p9773594"></a>表示使用的GPU类型</p>
<p id="zh-cn_topic_0114079830_p20853488"><a name="zh-cn_topic_0114079830_p20853488"></a><a name="zh-cn_topic_0114079830_p20853488"></a>取值：nvidia-v100-pcie</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079830_row53463670"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079830_p35590047"><a name="zh-cn_topic_0114079830_p35590047"></a><a name="zh-cn_topic_0114079830_p35590047"></a>quota:nvme_ssd</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079830_p64221564"><a name="zh-cn_topic_0114079830_p64221564"></a><a name="zh-cn_topic_0114079830_p64221564"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079830_p34564214"><a name="zh-cn_topic_0114079830_p34564214"></a><a name="zh-cn_topic_0114079830_p34564214"></a>表示使用nvme ssd硬盘</p>
<p id="zh-cn_topic_0114079830_p42642473"><a name="zh-cn_topic_0114079830_p42642473"></a><a name="zh-cn_topic_0114079830_p42642473"></a>格式：disk_type:spec:count:size:safe_format</p>
<p id="zh-cn_topic_0114079830_p48237940"><a name="zh-cn_topic_0114079830_p48237940"></a><a name="zh-cn_topic_0114079830_p48237940"></a>示例：800G:large:1:800:True</p>
<a name="ol0453659125312"></a><a name="ol0453659125312"></a><ol id="ol0453659125312"><li>disk_type表示主机上配备的nvme ssd的单卡容量大小。</li><li>spec：large表示大规格，small表示小规格。</li><li>count：guest配备的nvme ssd卡个数。</li><li>size：guest使用的盘的容量大小。在大规格情况下，此项即为host单卡大小，在小规格情况下，此为1/4规格或者1/2规格，单位为GB。</li><li>safe_format：删除弹性云服务器时是否进行安全格式化操作，True/False。</li></ol>
</td>
</tr>
<tr id="zh-cn_topic_0114079830_row33306906"><td class="cellrowborder" valign="top" width="33.333333333333336%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079830_p13504826"><a name="zh-cn_topic_0114079830_p13504826"></a><a name="zh-cn_topic_0114079830_p13504826"></a>quota:vif_max_rate</p>
</td>
<td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079830_p20149094"><a name="zh-cn_topic_0114079830_p20149094"></a><a name="zh-cn_topic_0114079830_p20149094"></a>int</p>
</td>
<td class="cellrowborder" valign="top" width="44.44444444444445%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079830_p21463943"><a name="zh-cn_topic_0114079830_p21463943"></a><a name="zh-cn_topic_0114079830_p21463943"></a>用于网络接口限速，单位Mbps</p>
</td>
</tr>
</tbody>
</table>

