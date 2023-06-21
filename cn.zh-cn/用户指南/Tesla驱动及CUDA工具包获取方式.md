# Tesla驱动及CUDA工具包获取方式<a name="ecs_03_0173"></a>

## 操作场景<a name="section11831857193910"></a>

使用GPU加速型云服务器时，需确保已安装Tesla驱动和CUDA工具包，否则无法实现计算加速功能。本节内容提供Tesla驱动及CUDA工具包下载地址，请根据实例的类型，选择具体的驱动版本。

Tesla驱动及CUDA工具包安装操作指导请参考[GPU加速型实例安装Tesla驱动及CUDA工具包](GPU加速型实例安装Tesla驱动及CUDA工具包.md)。

>![](public_sys-resources/icon-note.gif) **说明：** 
>当前已支持使用自动化脚本安装GPU驱动，建议优先使用自动安装方式，脚本获取以及安装指导请参考[（推荐）GPU加速型实例自动安装GPU驱动（Linux）](（推荐）GPU加速型实例自动安装GPU驱动（Linux）.md)和[（推荐）GPU加速型实例自动安装GPU驱动（Windows）](（推荐）GPU加速型实例自动安装GPU驱动（Windows）.md)。
>GPU虚拟化型实例，需要严格按照[表1](GPU加速型实例安装GRID驱动.md#table188851534175019)选择合适的驱动版本下载使用。

## Tesla驱动下载地址<a name="section28901217266"></a>

请单击[NVIDIA驱动下载](https://www.nvidia.com/Download/index.aspx?lang=en-us)，根据实例的类型，选择NVIDIA产品类型、产品系列和产品。

**表 1**  Tesla驱动产品类型对应关系

<a name="table394113539174"></a>
<table><thead align="left"><tr id="row1694195316175"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p47642020183"><a name="p47642020183"></a><a name="p47642020183"></a><strong id="b10871316141911"><a name="b10871316141911"></a><a name="b10871316141911"></a>实例类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="24.97%" id="mcps1.2.5.1.2"><p id="p77641406184"><a name="p77641406184"></a><a name="p77641406184"></a><strong id="b1687511163194"><a name="b1687511163194"></a><a name="b1687511163194"></a>产品类型（Product Type）</strong></p>
</th>
<th class="cellrowborder" valign="top" width="25.03%" id="mcps1.2.5.1.3"><p id="p876416010182"><a name="p876416010182"></a><a name="p876416010182"></a><strong id="b18881161621920"><a name="b18881161621920"></a><a name="b18881161621920"></a>产品系列（Product Series）</strong></p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p976440131814"><a name="p976440131814"></a><a name="p976440131814"></a><strong id="b488111617195"><a name="b488111617195"></a><a name="b488111617195"></a>产品（Product）</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row1922222222612"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p676415081817"><a name="p676415081817"></a><a name="p676415081817"></a>P2vs</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p127641908189"><a name="p127641908189"></a><a name="p127641908189"></a>Tesla</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p137642001186"><a name="p137642001186"></a><a name="p137642001186"></a>V-Series</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p20765100171810"><a name="p20765100171810"></a><a name="p20765100171810"></a>V100</p>
</td>
</tr>
<tr id="row921718111588"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p207571519811"><a name="p207571519811"></a><a name="p207571519811"></a>P2s</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p10757152816"><a name="p10757152816"></a><a name="p10757152816"></a>Tesla</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p076415789"><a name="p076415789"></a><a name="p076415789"></a>V-Series</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p107615151812"><a name="p107615151812"></a><a name="p107615151812"></a>V100</p>
</td>
</tr>
<tr id="row3941145391714"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p157646041817"><a name="p157646041817"></a><a name="p157646041817"></a>P2v</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p27644041812"><a name="p27644041812"></a><a name="p27644041812"></a>Tesla</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p107647091815"><a name="p107647091815"></a><a name="p107647091815"></a>V-Series</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p0764130121816"><a name="p0764130121816"></a><a name="p0764130121816"></a>V100</p>
</td>
</tr>
<tr id="row189411753181715"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p276419061816"><a name="p276419061816"></a><a name="p276419061816"></a>P1</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p5764120131815"><a name="p5764120131815"></a><a name="p5764120131815"></a>Tesla</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p167641303188"><a name="p167641303188"></a><a name="p167641303188"></a>P-Series</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p77641405181"><a name="p77641405181"></a><a name="p77641405181"></a>P100</p>
</td>
</tr>
<tr id="row9941185313172"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p36388214462"><a name="p36388214462"></a><a name="p36388214462"></a>Pi2</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p1676512015183"><a name="p1676512015183"></a><a name="p1676512015183"></a>Tesla</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p1765190191813"><a name="p1765190191813"></a><a name="p1765190191813"></a>T- Series</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1676580181812"><a name="p1676580181812"></a><a name="p1676580181812"></a>T4</p>
</td>
</tr>
<tr id="row14941653101720"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p107653071816"><a name="p107653071816"></a><a name="p107653071816"></a>Pi1</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p17656051813"><a name="p17656051813"></a><a name="p17656051813"></a>Tesla</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p3765100111812"><a name="p3765100111812"></a><a name="p3765100111812"></a>P-Series</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p076560141811"><a name="p076560141811"></a><a name="p076560141811"></a>P4</p>
</td>
</tr>
<tr id="row16833141214111"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p957118171219"><a name="p957118171219"></a><a name="p957118171219"></a>G6</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p10571817813"><a name="p10571817813"></a><a name="p10571817813"></a>Tesla</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p4571317715"><a name="p4571317715"></a><a name="p4571317715"></a>T- Series</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p145711117914"><a name="p145711117914"></a><a name="p145711117914"></a>T4</p>
</td>
</tr>
<tr id="row13941753161715"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p157656010183"><a name="p157656010183"></a><a name="p157656010183"></a>G5</p>
</td>
<td class="cellrowborder" valign="top" width="24.97%" headers="mcps1.2.5.1.2 "><p id="p13765404189"><a name="p13765404189"></a><a name="p13765404189"></a>Tesla</p>
</td>
<td class="cellrowborder" valign="top" width="25.03%" headers="mcps1.2.5.1.3 "><p id="p1576519051818"><a name="p1576519051818"></a><a name="p1576519051818"></a>V-Series</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p17650021818"><a name="p17650021818"></a><a name="p17650021818"></a>V100</p>
</td>
</tr>
</tbody>
</table>

## CUDA工具包下载地址<a name="section10203125783920"></a>

请从[CUDA软件包下载](https://developer.nvidia.com/cuda-toolkit-archive)获取CUDA软件包，您需要根据实例类型和驱动版本，选择对应的CUDA Toolkit软件包产品。

>![](public_sys-resources/icon-note.gif) **说明：** 
>驱动版本与CUDA Toolkit版本存在对应关系，如二者版本不匹配，可能导致驱动无法使用。
>版本对应关系，请参见[NVIDIA驱动下载](https://www.nvidia.com/Download/index.aspx?lang=en-us)。

下面以Tesla T4下载驱动软件包及CUDA Toolkit为例进行介绍。

1.  Tesla T4安装驱动软件包时，选择Linux操作系统，并指定CUDA Toolkit软件版本为11.6。

    **图 1**  指定CUDA Toolkit软件版本<a name="fig13391969382"></a>  
    ![](figures/指定CUDA-Toolkit软件版本.png "指定CUDA-Toolkit软件版本")

2.  下载CUDA软件包，需要选择CUDA Toolkit 11.6对应小版本。

    **图 2**  选择CUDA Toolkit对应版本<a name="fig55614344014"></a>  
    ![](figures/选择CUDA-Toolkit对应版本.png "选择CUDA-Toolkit对应版本")


