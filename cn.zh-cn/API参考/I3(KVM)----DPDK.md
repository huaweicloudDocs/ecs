# I3\(KVM\) -- DPDK<a name="ZH-CN_TOPIC_0114104003"></a>

1.  

    <a name="table829318795010"></a>
    <table><thead align="left"><tr id="row14293167115011"><th class="cellrowborder" valign="top" width="33%" id="mcps1.1.4.1.1"><p id="p142931672509"><a name="p142931672509"></a><a name="p142931672509"></a>name</p>
    </th>
    <th class="cellrowborder" valign="top" width="19%" id="mcps1.1.4.1.2"><p id="p16293676500"><a name="p16293676500"></a><a name="p16293676500"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="48%" id="mcps1.1.4.1.3"><p id="p10293187195012"><a name="p10293187195012"></a><a name="p10293187195012"></a>值</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1029311785015"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="p172937712501"><a name="p172937712501"></a><a name="p172937712501"></a>resource_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.4.1.2 "><p id="p192935711508"><a name="p192935711508"></a><a name="p192935711508"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.4.1.3 "><p id="p142931276500"><a name="p142931276500"></a><a name="p142931276500"></a>系统参数</p>
    </td>
    </tr>
    <tr id="row829307175016"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="p52935755012"><a name="p52935755012"></a><a name="p52935755012"></a>ecs:performancetype</p>
    </td>
    <td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.4.1.2 "><p id="p17293177195016"><a name="p17293177195016"></a><a name="p17293177195016"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.4.1.3 "><p id="p102936712501"><a name="p102936712501"></a><a name="p102936712501"></a>flavor分类，用于console，flavor的产品类别归属（常驻配置）</p>
    <p id="p14293574508"><a name="p14293574508"></a><a name="p14293574508"></a>取值：highio</p>
    </td>
    </tr>
    <tr id="row16293277508"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="p1129316745011"><a name="p1129316745011"></a><a name="p1129316745011"></a>ecs:virtualization_env_types</p>
    </td>
    <td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.4.1.2 "><p id="p82933713509"><a name="p82933713509"></a><a name="p82933713509"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.4.1.3 "><p id="p9293775503"><a name="p9293775503"></a><a name="p9293775503"></a>用于console，表示虚拟化类型</p>
    <p id="p22935714505"><a name="p22935714505"></a><a name="p22935714505"></a>取值：CloudCompute</p>
    </td>
    </tr>
    <tr id="row1929377105019"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="p12293147205017"><a name="p12293147205017"></a><a name="p12293147205017"></a>hw:mem_page_size</p>
    </td>
    <td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.4.1.2 "><p id="p6293117155014"><a name="p6293117155014"></a><a name="p6293117155014"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.4.1.3 "><p id="p2293974503"><a name="p2293974503"></a><a name="p2293974503"></a>系统参数</p>
    </td>
    </tr>
    <tr id="row162932078504"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.1.4.1.1 "><p id="p1029397185013"><a name="p1029397185013"></a><a name="p1029397185013"></a>quota:nvme_ssd</p>
    </td>
    <td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.4.1.2 "><p id="p229310705012"><a name="p229310705012"></a><a name="p229310705012"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48%" headers="mcps1.1.4.1.3 "><p id="p1229377195011"><a name="p1229377195011"></a><a name="p1229377195011"></a>表示使用nvme ssd硬盘</p>
    <p id="p122939795016"><a name="p122939795016"></a><a name="p122939795016"></a>格式：disk_type:spec:count:size:safe_format</p>
    <p id="p102931876503"><a name="p102931876503"></a><a name="p102931876503"></a>示例：1.6T:large:2:1600:True</p>
    <a name="ol1928522255019"></a><a name="ol1928522255019"></a><ol id="ol1928522255019"><li>disk_type表示主机上配备的nvme ssd的单卡容量大小，1.6T/3.2T。</li><li>spec：large表示大规格，small表示小规格。</li><li>count：guest配备的nvme ssd卡个数，大规格：1/2/4/7，小规格：2。</li><li>size：guest使用的盘的容量大小。在大规格情况下，此项即为host单卡大小，在小规格情况下，此项为1/4规格或者1/2规格，单位为GB。host单卡3.2T：大规格3200，小规格800/1600；host单卡1.6T：大规格1600，小规格400/800。</li><li>safe_format：删除弹性云服务器时是否进行安全格式化操作，True/False。</li></ol>
    </td>
    </tr>
    </tbody>
    </table>


