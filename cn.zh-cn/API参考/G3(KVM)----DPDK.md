# G3\(KVM\)  -- DPDK<a name="ZH-CN_TOPIC_0114104005"></a>

<a name="zh-cn_topic_0114079827_table58978167"></a>
<table><thead align="left"><tr id="zh-cn_topic_0114079827_row35162951"><th class="cellrowborder" valign="top" width="33%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0114079827_p29626789"><a name="zh-cn_topic_0114079827_p29626789"></a><a name="zh-cn_topic_0114079827_p29626789"></a>name</p>
</th>
<th class="cellrowborder" valign="top" width="22%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0114079827_p50959748"><a name="zh-cn_topic_0114079827_p50959748"></a><a name="zh-cn_topic_0114079827_p50959748"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="45%" id="mcps1.1.4.1.3"><p id="zh-cn_topic_0114079827_p34098956"><a name="zh-cn_topic_0114079827_p34098956"></a><a name="zh-cn_topic_0114079827_p34098956"></a>值</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0114079827_row10552036"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079827_p49408564"><a name="zh-cn_topic_0114079827_p49408564"></a><a name="zh-cn_topic_0114079827_p49408564"></a>hw:cpu_cores</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079827_p42670757"><a name="zh-cn_topic_0114079827_p42670757"></a><a name="zh-cn_topic_0114079827_p42670757"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079827_p33779294"><a name="zh-cn_topic_0114079827_p33779294"></a><a name="zh-cn_topic_0114079827_p33779294"></a>表示CPU核数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079827_row35578198"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079827_p63261775"><a name="zh-cn_topic_0114079827_p63261775"></a><a name="zh-cn_topic_0114079827_p63261775"></a>hw:cpu_policy</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079827_p23930149"><a name="zh-cn_topic_0114079827_p23930149"></a><a name="zh-cn_topic_0114079827_p23930149"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079827_p59293887"><a name="zh-cn_topic_0114079827_p59293887"></a><a name="zh-cn_topic_0114079827_p59293887"></a>表示cpu绑定策略</p>
<p id="zh-cn_topic_0114079827_p63882937"><a name="zh-cn_topic_0114079827_p63882937"></a><a name="zh-cn_topic_0114079827_p63882937"></a>取值：dedicated，表示绑核</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079827_row38075525"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079827_p64218721"><a name="zh-cn_topic_0114079827_p64218721"></a><a name="zh-cn_topic_0114079827_p64218721"></a>hw:cpu_sockets</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079827_p34333880"><a name="zh-cn_topic_0114079827_p34333880"></a><a name="zh-cn_topic_0114079827_p34333880"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079827_p29580916"><a name="zh-cn_topic_0114079827_p29580916"></a><a name="zh-cn_topic_0114079827_p29580916"></a>表示CPU插槽数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079827_row64901660"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079827_p22543082"><a name="zh-cn_topic_0114079827_p22543082"></a><a name="zh-cn_topic_0114079827_p22543082"></a>hw:cpu_thread_policy</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079827_p14050320"><a name="zh-cn_topic_0114079827_p14050320"></a><a name="zh-cn_topic_0114079827_p14050320"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079827_p64334135"><a name="zh-cn_topic_0114079827_p64334135"></a><a name="zh-cn_topic_0114079827_p64334135"></a>表示cpu超线程策略，仅当hw:cpu_policy=dedicated时生效</p>
<a name="ul45594585397"></a><a name="ul45594585397"></a><ul id="ul45594585397"><li>prefer：如果物理机支持超线程，那么同一个guest的vCPU将尽可能的被调度到相同的core上。</li><li>isolate：如果物理机支持超线程，那么同一个guest的vCPU将会被分到不同的core上，并且其他guest的vCPU不再允许调度到当前的core上。</li><li>require：主机必须有超线程，每个vCPU将被分配到线程兄弟节点上。</li></ul>
<p id="zh-cn_topic_0114079827_p48616614"><a name="zh-cn_topic_0114079827_p48616614"></a><a name="zh-cn_topic_0114079827_p48616614"></a>取值：require</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079827_row34896348"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079827_p8031928"><a name="zh-cn_topic_0114079827_p8031928"></a><a name="zh-cn_topic_0114079827_p8031928"></a>hw:cpu_threads</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079827_p46606392"><a name="zh-cn_topic_0114079827_p46606392"></a><a name="zh-cn_topic_0114079827_p46606392"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079827_p17021380"><a name="zh-cn_topic_0114079827_p17021380"></a><a name="zh-cn_topic_0114079827_p17021380"></a>表示CPU超线程数，sockets*cores*threads要等于vcpu个数</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079827_row18974699"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079827_p60555637"><a name="zh-cn_topic_0114079827_p60555637"></a><a name="zh-cn_topic_0114079827_p60555637"></a>pci_passthrough:alias</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079827_p6059584"><a name="zh-cn_topic_0114079827_p6059584"></a><a name="zh-cn_topic_0114079827_p6059584"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079827_p21064308"><a name="zh-cn_topic_0114079827_p21064308"></a><a name="zh-cn_topic_0114079827_p21064308"></a>指定PCI直通设备及数量</p>
<p id="zh-cn_topic_0114079827_p55361044"><a name="zh-cn_topic_0114079827_p55361044"></a><a name="zh-cn_topic_0114079827_p55361044"></a>格式：pci_type: count</p>
<p id="zh-cn_topic_0114079827_p28487351"><a name="zh-cn_topic_0114079827_p28487351"></a><a name="zh-cn_topic_0114079827_p28487351"></a>示例：nvidia-m60:1</p>
<p id="zh-cn_topic_0114079827_p55059575"><a name="zh-cn_topic_0114079827_p55059575"></a><a name="zh-cn_topic_0114079827_p55059575"></a>1. pci_type表示直通设备。</p>
<p id="zh-cn_topic_0114079827_p25774132"><a name="zh-cn_topic_0114079827_p25774132"></a><a name="zh-cn_topic_0114079827_p25774132"></a>2. count：guest配备的直通设备个数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079827_row30640599"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079827_p65969435"><a name="zh-cn_topic_0114079827_p65969435"></a><a name="zh-cn_topic_0114079827_p65969435"></a>quota:gpu</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079827_p41924012"><a name="zh-cn_topic_0114079827_p41924012"></a><a name="zh-cn_topic_0114079827_p41924012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079827_p40401777"><a name="zh-cn_topic_0114079827_p40401777"></a><a name="zh-cn_topic_0114079827_p40401777"></a>表示使用的GPU类型</p>
<p id="zh-cn_topic_0114079827_p28071674"><a name="zh-cn_topic_0114079827_p28071674"></a><a name="zh-cn_topic_0114079827_p28071674"></a>取值：nvidia-m60</p>
</td>
</tr>
<tr id="zh-cn_topic_0114079827_row51318482"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0114079827_p63156409"><a name="zh-cn_topic_0114079827_p63156409"></a><a name="zh-cn_topic_0114079827_p63156409"></a>quota:vif_max_rate</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0114079827_p15395467"><a name="zh-cn_topic_0114079827_p15395467"></a><a name="zh-cn_topic_0114079827_p15395467"></a>int</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0114079827_p39073330"><a name="zh-cn_topic_0114079827_p39073330"></a><a name="zh-cn_topic_0114079827_p39073330"></a>用于网络接口限速，单位Mbps</p>
</td>
</tr>
</tbody>
</table>

