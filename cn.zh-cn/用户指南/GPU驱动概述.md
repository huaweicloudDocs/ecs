# GPU驱动概述<a name="ZH-CN_TOPIC_0234802636"></a>

## GPU驱动概述<a name="section134733278713"></a>

在使用GPU加速型实例前，请确保实例已安装GPU驱动以获得相应的GPU加速能力。

GPU加速型实例支持两种类型的驱动：GRID驱动和Tesla驱动。

-   如果需要使用OpenGL/DirectX/Vulcan等图形加速能力，则需要安装GRID驱动并自行购买和配置使用GRID License。此外，GRID驱动配合vDWS类型License，也支持CUDA，用来满足既需要计算加速也需要图形加速的场景。
    -   使用公共镜像创建的图形加速型（G系列）实例默认已安装特定版本的GRID驱动，但GRID License需自行购买和配置使用，请提前确认GPU加速型实例是否已经预装或者预装版本是否符合需求。
    -   使用私有镜像创建的GPU加速型实例，如需安装GRID驱动请参考[GPU加速型实例安装GRID驱动](GPU加速型实例安装GRID驱动.md)。

-   如果需要实现计算加速能力，则需要安装Tesla驱动。
    -   使用公共镜像创建的计算加速型（P系列）实例默认已安装特定版本的Tesla驱动。
    -   使用私有镜像创建的GPU加速型实例，如需安装Tesla驱动请参考[GPU加速型实例安装Tesla驱动及CUDA工具包](GPU加速型实例安装Tesla驱动及CUDA工具包.md)。


**表 1**  GPU驱动支持的加速能力

<a name="table8917107174212"></a>
<table><thead align="left"><tr id="row991219704215"><th class="cellrowborder" valign="top" width="14.421442144214422%" id="mcps1.2.9.1.1"><p id="p39120764214"><a name="p39120764214"></a><a name="p39120764214"></a>驱动类型</p>
</th>
<th class="cellrowborder" valign="top" width="8.260826082608261%" id="mcps1.2.9.1.2"><p id="p139122774218"><a name="p139122774218"></a><a name="p139122774218"></a>License</p>
</th>
<th class="cellrowborder" valign="top" width="7.100710071007101%" id="mcps1.2.9.1.3"><p id="p99125713426"><a name="p99125713426"></a><a name="p99125713426"></a>CUDA</p>
</th>
<th class="cellrowborder" valign="top" width="9.170917091709173%" id="mcps1.2.9.1.4"><p id="p209123714425"><a name="p209123714425"></a><a name="p209123714425"></a>OpenGL</p>
</th>
<th class="cellrowborder" valign="top" width="7.640764076407641%" id="mcps1.2.9.1.5"><p id="p091214714427"><a name="p091214714427"></a><a name="p091214714427"></a>DirectX</p>
</th>
<th class="cellrowborder" valign="top" width="10.201020102010201%" id="mcps1.2.9.1.6"><p id="p691216704210"><a name="p691216704210"></a><a name="p691216704210"></a>Vulcan</p>
</th>
<th class="cellrowborder" valign="top" width="23.332333233323336%" id="mcps1.2.9.1.7"><p id="p179123724213"><a name="p179123724213"></a><a name="p179123724213"></a>典型应用场景</p>
</th>
<th class="cellrowborder" valign="top" width="19.87198719871987%" id="mcps1.2.9.1.8"><p id="p18178924144619"><a name="p18178924144619"></a><a name="p18178924144619"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1855995618596"><td class="cellrowborder" valign="top" width="14.421442144214422%" headers="mcps1.2.9.1.1 "><p id="p1591447114213"><a name="p1591447114213"></a><a name="p1591447114213"></a>GRID驱动</p>
</td>
<td class="cellrowborder" valign="top" width="8.260826082608261%" headers="mcps1.2.9.1.2 "><p id="p14915207134210"><a name="p14915207134210"></a><a name="p14915207134210"></a>需要</p>
</td>
<td class="cellrowborder" valign="top" width="7.100710071007101%" headers="mcps1.2.9.1.3 "><p id="p16915273428"><a name="p16915273428"></a><a name="p16915273428"></a>支持</p>
</td>
<td class="cellrowborder" valign="top" width="9.170917091709173%" headers="mcps1.2.9.1.4 "><p id="p119161479424"><a name="p119161479424"></a><a name="p119161479424"></a>支持</p>
</td>
<td class="cellrowborder" valign="top" width="7.640764076407641%" headers="mcps1.2.9.1.5 "><p id="p6917177104211"><a name="p6917177104211"></a><a name="p6917177104211"></a>支持</p>
</td>
<td class="cellrowborder" valign="top" width="10.201020102010201%" headers="mcps1.2.9.1.6 "><p id="p4917207154214"><a name="p4917207154214"></a><a name="p4917207154214"></a>支持</p>
</td>
<td class="cellrowborder" valign="top" width="23.332333233323336%" headers="mcps1.2.9.1.7 "><p id="p189178715422"><a name="p189178715422"></a><a name="p189178715422"></a>3D渲染、图形工作站、游戏加速</p>
</td>
<td class="cellrowborder" valign="top" width="19.87198719871987%" headers="mcps1.2.9.1.8 "><p id="p197573180464"><a name="p197573180464"></a><a name="p197573180464"></a>付费使用，需要购买License，满足图形图像类应用加速用途。</p>
</td>
</tr>
<tr id="row14531647215"><td class="cellrowborder" valign="top" width="14.421442144214422%" headers="mcps1.2.9.1.1 "><p id="p1391214714214"><a name="p1391214714214"></a><a name="p1391214714214"></a>Tesla驱动</p>
</td>
<td class="cellrowborder" valign="top" width="8.260826082608261%" headers="mcps1.2.9.1.2 "><p id="p13913971429"><a name="p13913971429"></a><a name="p13913971429"></a>不需要</p>
</td>
<td class="cellrowborder" valign="top" width="7.100710071007101%" headers="mcps1.2.9.1.3 "><p id="p10913197154217"><a name="p10913197154217"></a><a name="p10913197154217"></a>支持</p>
</td>
<td class="cellrowborder" valign="top" width="9.170917091709173%" headers="mcps1.2.9.1.4 "><p id="p89131972421"><a name="p89131972421"></a><a name="p89131972421"></a>不支持</p>
</td>
<td class="cellrowborder" valign="top" width="7.640764076407641%" headers="mcps1.2.9.1.5 "><p id="p129137715422"><a name="p129137715422"></a><a name="p129137715422"></a>不支持</p>
</td>
<td class="cellrowborder" valign="top" width="10.201020102010201%" headers="mcps1.2.9.1.6 "><p id="p79138712422"><a name="p79138712422"></a><a name="p79138712422"></a>不支持</p>
</td>
<td class="cellrowborder" valign="top" width="23.332333233323336%" headers="mcps1.2.9.1.7 "><p id="p99135734212"><a name="p99135734212"></a><a name="p99135734212"></a>科学计算、深度学习训练和推理</p>
</td>
<td class="cellrowborder" valign="top" width="19.87198719871987%" headers="mcps1.2.9.1.8 "><p id="p137571518174618"><a name="p137571518174618"></a><a name="p137571518174618"></a>通常搭配使用NVIDIA CUDA SDK，可免费下载使用，满足通用计算类应用加速用途。</p>
</td>
</tr>
</tbody>
</table>

