# PI1\(KVM\) -- DPDK<a name="ZH-CN_TOPIC_0114104008"></a>

<a name="zh-cn_topic_0114079831_table40871974"></a>
<table><thead align="left"><tr id="zh-cn_topic_0114079831_row56089592"><th class="cellrowborder" valign="top" width="33%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0114079831_p46963092"><a name="zh-cn_topic_0114079831_p46963092"></a><a name="zh-cn_topic_0114079831_p46963092"></a>name</p>
</th>
<th class="cellrowborder" valign="top" width="23%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0114079831_p45914068"><a name="zh-cn_topic_0114079831_p45914068"></a><a name="zh-cn_topic_0114079831_p45914068"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="44%" id="mcps1.1.4.1.3"><p id="zh-cn_topic_0114079831_p28052000"><a name="zh-cn_topic_0114079831_p28052000"></a><a name="zh-cn_topic_0114079831_p28052000"></a>值</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0114079831_row57619553"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079831_p36672255"><a name="zh-cn_topic_0114079831_p36672255"></a><a name="zh-cn_topic_0114079831_p36672255"></a>hw:cpu_cores</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079831_p17662689"><a name="zh-cn_topic_0114079831_p17662689"></a><a name="zh-cn_topic_0114079831_p17662689"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079831_p21391728"><a name="zh-cn_topic_0114079831_p21391728"></a><a name="zh-cn_topic_0114079831_p21391728"></a>表示CPU核数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079831_row58307827"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079831_p25313584"><a name="zh-cn_topic_0114079831_p25313584"></a><a name="zh-cn_topic_0114079831_p25313584"></a>hw:cpu_policy</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079831_p37134413"><a name="zh-cn_topic_0114079831_p37134413"></a><a name="zh-cn_topic_0114079831_p37134413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079831_p55097458"><a name="zh-cn_topic_0114079831_p55097458"></a><a name="zh-cn_topic_0114079831_p55097458"></a>表示cpu绑定策略</p>
<p id="zh-cn_topic_0114079831_p26115080"><a name="zh-cn_topic_0114079831_p26115080"></a><a name="zh-cn_topic_0114079831_p26115080"></a>取值：dedicated，表示绑核</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079831_row33709128"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079831_p46084854"><a name="zh-cn_topic_0114079831_p46084854"></a><a name="zh-cn_topic_0114079831_p46084854"></a>hw:cpu_sockets</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079831_p41885733"><a name="zh-cn_topic_0114079831_p41885733"></a><a name="zh-cn_topic_0114079831_p41885733"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079831_p37301245"><a name="zh-cn_topic_0114079831_p37301245"></a><a name="zh-cn_topic_0114079831_p37301245"></a>表示CPU插槽数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079831_row166887"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079831_p13517902"><a name="zh-cn_topic_0114079831_p13517902"></a><a name="zh-cn_topic_0114079831_p13517902"></a>hw:cpu_thread_policy</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079831_p21208306"><a name="zh-cn_topic_0114079831_p21208306"></a><a name="zh-cn_topic_0114079831_p21208306"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079831_p40151226"><a name="zh-cn_topic_0114079831_p40151226"></a><a name="zh-cn_topic_0114079831_p40151226"></a>表示cpu超线程策略，仅当hw:cpu_policy=dedicated时生效</p>
<a name="ul5403154775414"></a><a name="ul5403154775414"></a><ul id="ul5403154775414"><li>prefer：如果物理机支持超线程，那么同一个guest的vCPU将尽可能的被调度到相同的core上。</li><li>isolate：如果物理机支持超线程，那么同一个guest的vCPU将会被分到不同的core上，并且其他guest的vCPU不再允许调度到当前的core上。</li><li>require：主机必须有超线程，每个vCPU将被分配到线程兄弟节点上。</li></ul>
<p id="zh-cn_topic_0114079831_p29906904"><a name="zh-cn_topic_0114079831_p29906904"></a><a name="zh-cn_topic_0114079831_p29906904"></a>取值：require</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079831_row726684"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079831_p58861423"><a name="zh-cn_topic_0114079831_p58861423"></a><a name="zh-cn_topic_0114079831_p58861423"></a>hw:cpu_threads</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079831_p3045930"><a name="zh-cn_topic_0114079831_p3045930"></a><a name="zh-cn_topic_0114079831_p3045930"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079831_p45393782"><a name="zh-cn_topic_0114079831_p45393782"></a><a name="zh-cn_topic_0114079831_p45393782"></a>表示CPU超线程数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079831_row5890858"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079831_p7397457"><a name="zh-cn_topic_0114079831_p7397457"></a><a name="zh-cn_topic_0114079831_p7397457"></a>pci_passthrough:alias</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079831_p62323165"><a name="zh-cn_topic_0114079831_p62323165"></a><a name="zh-cn_topic_0114079831_p62323165"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079831_p15011638"><a name="zh-cn_topic_0114079831_p15011638"></a><a name="zh-cn_topic_0114079831_p15011638"></a>指定PCI直通设备及数量</p>
<p id="zh-cn_topic_0114079831_p887019"><a name="zh-cn_topic_0114079831_p887019"></a><a name="zh-cn_topic_0114079831_p887019"></a>格式：pci_type: count</p>
<p id="zh-cn_topic_0114079831_p7983171"><a name="zh-cn_topic_0114079831_p7983171"></a><a name="zh-cn_topic_0114079831_p7983171"></a>示例：nvidia-p4:1</p>
<p id="zh-cn_topic_0114079831_p4739681"><a name="zh-cn_topic_0114079831_p4739681"></a><a name="zh-cn_topic_0114079831_p4739681"></a>1. pci_type表示直通设备；</p>
<p id="zh-cn_topic_0114079831_p42657133"><a name="zh-cn_topic_0114079831_p42657133"></a><a name="zh-cn_topic_0114079831_p42657133"></a>2. count：guest配备的直通设备个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079831_row48369880"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079831_p25646199"><a name="zh-cn_topic_0114079831_p25646199"></a><a name="zh-cn_topic_0114079831_p25646199"></a>quota:gpu</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079831_p64076263"><a name="zh-cn_topic_0114079831_p64076263"></a><a name="zh-cn_topic_0114079831_p64076263"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079831_p22794832"><a name="zh-cn_topic_0114079831_p22794832"></a><a name="zh-cn_topic_0114079831_p22794832"></a>表示使用的GPU类型</p>
<p id="zh-cn_topic_0114079831_p3826897"><a name="zh-cn_topic_0114079831_p3826897"></a><a name="zh-cn_topic_0114079831_p3826897"></a>取值：nvidia-p4</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079831_row34442073"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079831_p38344490"><a name="zh-cn_topic_0114079831_p38344490"></a><a name="zh-cn_topic_0114079831_p38344490"></a>quota:vif_max_rate</p>
</td>
<td class="cellrowborder" valign="top" width="23%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079831_p18895980"><a name="zh-cn_topic_0114079831_p18895980"></a><a name="zh-cn_topic_0114079831_p18895980"></a>int</p>
</td>
<td class="cellrowborder" valign="top" width="44%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079831_p54179398"><a name="zh-cn_topic_0114079831_p54179398"></a><a name="zh-cn_topic_0114079831_p54179398"></a>用于网络接口限速，单位Mbps</p>
</td>
</tr>
</tbody>
</table>

