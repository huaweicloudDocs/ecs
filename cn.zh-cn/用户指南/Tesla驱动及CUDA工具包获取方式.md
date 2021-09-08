# Tesla驱动及CUDA工具包获取方式<a name="ZH-CN_TOPIC_0213874991"></a>

## 操作场景<a name="section11831857193910"></a>

使用GPU加速型云服务器时，需确保已安装Tesla驱动和CUDA工具包，否则无法实现计算加速功能。本节内容提供Tesla驱动及CUDA工具包下载地址，请根据实例的类型，选择具体的驱动版本。

Tesla驱动及CUDA工具包安装操作指导请参考[GPU加速型实例安装Tesla驱动及CUDA工具包](GPU加速型实例安装Tesla驱动及CUDA工具包.md)。

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
<tr id="row9941185313172"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p127655061810"><a name="p127655061810"></a><a name="p127655061810"></a>Pi2</p>
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

**表 2**  P2vs实例CUDA工具包下载地址

<a name="table15233533153010"></a>
<table><thead align="left"><tr id="row123343333014"><th class="cellrowborder" valign="top" width="12.530000000000003%" id="mcps1.2.6.1.1"><p id="p1023319330307"><a name="p1023319330307"></a><a name="p1023319330307"></a><strong id="b5233733163014"><a name="b5233733163014"></a><a name="b5233733163014"></a>实例</strong></p>
<p id="p16233183316304"><a name="p16233183316304"></a><a name="p16233183316304"></a><strong id="b1123363353015"><a name="b1123363353015"></a><a name="b1123363353015"></a>类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="16.900000000000006%" id="mcps1.2.6.1.2"><p id="p1233113318303"><a name="p1233113318303"></a><a name="p1233113318303"></a><strong id="b5233173333014"><a name="b5233173333014"></a><a name="b5233173333014"></a>操作系统</strong></p>
</th>
<th class="cellrowborder" valign="top" width="19.160000000000004%" id="mcps1.2.6.1.3"><p id="p16233133133015"><a name="p16233133133015"></a><a name="p16233133133015"></a><strong id="b823343318307"><a name="b823343318307"></a><a name="b823343318307"></a>CUDA版本</strong></p>
</th>
<th class="cellrowborder" valign="top" width="28.290000000000003%" id="mcps1.2.6.1.4"><p id="p13233113323016"><a name="p13233113323016"></a><a name="p13233113323016"></a><strong id="b20233153319305"><a name="b20233153319305"></a><a name="b20233153319305"></a>下载路径</strong></p>
</th>
<th class="cellrowborder" valign="top" width="23.12%" id="mcps1.2.6.1.5"><p id="p923303313301"><a name="p923303313301"></a><a name="p923303313301"></a><strong id="b12331533153011"><a name="b12331533153011"></a><a name="b12331533153011"></a>CPU架构</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row123463363014"><td class="cellrowborder" valign="top" width="12.530000000000003%" headers="mcps1.2.6.1.1 "><p id="p122341339305"><a name="p122341339305"></a><a name="p122341339305"></a>P2vs</p>
<p id="p32348332308"><a name="p32348332308"></a><a name="p32348332308"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" width="16.900000000000006%" headers="mcps1.2.6.1.2 "><p id="p19234033143020"><a name="p19234033143020"></a><a name="p19234033143020"></a>CentOS 7.5 64bit</p>
</td>
<td class="cellrowborder" valign="top" width="19.160000000000004%" headers="mcps1.2.6.1.3 "><p id="p1923418337308"><a name="p1923418337308"></a><a name="p1923418337308"></a>9.2/10.1</p>
<p id="p1123416339308"><a name="p1123416339308"></a><a name="p1123416339308"></a>内核版本不高于3.10.0-957.5.1.e17.x86_64时可以安装9.2版本的CUDA工具包。</p>
</td>
<td class="cellrowborder" rowspan="3" valign="top" width="28.290000000000003%" headers="mcps1.2.6.1.4 "><p id="p723443312301"><a name="p723443312301"></a><a name="p723443312301"></a>9.2版本：<a href="https://developer.nvidia.com/cuda-92-download-archive" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/cuda-92-download-archive</a></p>
<p id="p823423315307"><a name="p823423315307"></a><a name="p823423315307"></a></p>
<p id="p62341333103011"><a name="p62341333103011"></a><a name="p62341333103011"></a>10.1版本：</p>
<p id="p112341333173012"><a name="p112341333173012"></a><a name="p112341333173012"></a><a href="https://developer.nvidia.com/cuda-10.1-download-archive-base" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/cuda-10.1-download-archive-base</a></p>
</td>
<td class="cellrowborder" valign="top" width="23.12%" headers="mcps1.2.6.1.5 "><p id="p123416336301"><a name="p123416336301"></a><a name="p123416336301"></a>x86_64</p>
</td>
</tr>
<tr id="row123433316301"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p11234153314301"><a name="p11234153314301"></a><a name="p11234153314301"></a>P2vs</p>
<p id="p1323411332304"><a name="p1323411332304"></a><a name="p1323411332304"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p16234173312302"><a name="p16234173312302"></a><a name="p16234173312302"></a>Ubuntu 16.04 64bit</p>
<p id="p162342335301"><a name="p162342335301"></a><a name="p162342335301"></a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p12234173312306"><a name="p12234173312306"></a><a name="p12234173312306"></a>9.2/10.1</p>
<p id="p023403393011"><a name="p023403393011"></a><a name="p023403393011"></a>内核版本不高于4.4.0-141-generic时可以安装9.2版本的CUDA工具包。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p3234123315307"><a name="p3234123315307"></a><a name="p3234123315307"></a>x86_64</p>
</td>
</tr>
<tr id="row1234103318301"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p3234153312307"><a name="p3234153312307"></a><a name="p3234153312307"></a>P2vs</p>
<p id="p8234173312304"><a name="p8234173312304"></a><a name="p8234173312304"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p52341933163010"><a name="p52341933163010"></a><a name="p52341933163010"></a>Windows Server 2016 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1323403343011"><a name="p1323403343011"></a><a name="p1323403343011"></a>9.2/10.1</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p6234133319304"><a name="p6234133319304"></a><a name="p6234133319304"></a>x86_64</p>
</td>
</tr>
</tbody>
</table>

**表 3**  P2s实例CUDA工具包下载地址

<a name="table189141151993"></a>
<table><thead align="left"><tr id="row179141857910"><th class="cellrowborder" valign="top" width="12.540000000000004%" id="mcps1.2.6.1.1"><p id="p179141153911"><a name="p179141153911"></a><a name="p179141153911"></a><strong id="b69144516914"><a name="b69144516914"></a><a name="b69144516914"></a>实例</strong></p>
<p id="p39141058910"><a name="p39141058910"></a><a name="p39141058910"></a><strong id="b19914950913"><a name="b19914950913"></a><a name="b19914950913"></a>类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="16.89%" id="mcps1.2.6.1.2"><p id="p7914175996"><a name="p7914175996"></a><a name="p7914175996"></a><strong id="b129141451899"><a name="b129141451899"></a><a name="b129141451899"></a>操作系统</strong></p>
</th>
<th class="cellrowborder" valign="top" width="19.160000000000004%" id="mcps1.2.6.1.3"><p id="p191418515920"><a name="p191418515920"></a><a name="p191418515920"></a><strong id="b14914175298"><a name="b14914175298"></a><a name="b14914175298"></a>CUDA版本</strong></p>
</th>
<th class="cellrowborder" valign="top" width="28.290000000000003%" id="mcps1.2.6.1.4"><p id="p791475298"><a name="p791475298"></a><a name="p791475298"></a><strong id="b14914652912"><a name="b14914652912"></a><a name="b14914652912"></a>下载路径</strong></p>
</th>
<th class="cellrowborder" valign="top" width="23.12%" id="mcps1.2.6.1.5"><p id="p119140518910"><a name="p119140518910"></a><a name="p119140518910"></a><strong id="b29141451910"><a name="b29141451910"></a><a name="b29141451910"></a>CPU架构</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row4914135592"><td class="cellrowborder" valign="top" width="12.540000000000004%" headers="mcps1.2.6.1.1 "><p id="p149141451991"><a name="p149141451991"></a><a name="p149141451991"></a>P2s</p>
<p id="p1991475394"><a name="p1991475394"></a><a name="p1991475394"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" width="16.89%" headers="mcps1.2.6.1.2 "><p id="p09141058912"><a name="p09141058912"></a><a name="p09141058912"></a>CentOS 7.4 64bit</p>
</td>
<td class="cellrowborder" valign="top" width="19.160000000000004%" headers="mcps1.2.6.1.3 "><p id="p591435391"><a name="p591435391"></a><a name="p591435391"></a>9.2及以上版本</p>
<p id="p791414513913"><a name="p791414513913"></a><a name="p791414513913"></a>内核版本不高于3.10.0-957.5.1.e17.x86_64时可以安装9.2版本的CUDA工具包。</p>
</td>
<td class="cellrowborder" rowspan="4" valign="top" width="28.290000000000003%" headers="mcps1.2.6.1.4 "><p id="p1263594710916"><a name="p1263594710916"></a><a name="p1263594710916"></a>请按需选择对应的CUDA版本</p>
<p id="p38408142911"><a name="p38408142911"></a><a name="p38408142911"></a><a href="https://developer.nvidia.com/cuda-downloads" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/cuda-downloads</a></p>
</td>
<td class="cellrowborder" valign="top" width="23.12%" headers="mcps1.2.6.1.5 "><p id="p1491514516919"><a name="p1491514516919"></a><a name="p1491514516919"></a>x86_64</p>
</td>
</tr>
<tr id="row491515520914"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p10915115094"><a name="p10915115094"></a><a name="p10915115094"></a>P2s</p>
<p id="p49151156919"><a name="p49151156919"></a><a name="p49151156919"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1291510519916"><a name="p1291510519916"></a><a name="p1291510519916"></a>Ubuntu 16.04 64bit</p>
<p id="p169151951393"><a name="p169151951393"></a><a name="p169151951393"></a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p209158516913"><a name="p209158516913"></a><a name="p209158516913"></a>9.2及以上版本</p>
<p id="p9915456913"><a name="p9915456913"></a><a name="p9915456913"></a>内核版本不高于4.4.0-141-generic时可以安装9.2版本的CUDA工具包。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p19915145793"><a name="p19915145793"></a><a name="p19915145793"></a>x86_64</p>
</td>
</tr>
<tr id="row39152058919"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p29151158913"><a name="p29151158913"></a><a name="p29151158913"></a>P2s</p>
<p id="p791545196"><a name="p791545196"></a><a name="p791545196"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p8915359910"><a name="p8915359910"></a><a name="p8915359910"></a>Windows Server 2016 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p3915175493"><a name="p3915175493"></a><a name="p3915175493"></a>9.2及以上版本</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p5915351597"><a name="p5915351597"></a><a name="p5915351597"></a>x86_64</p>
</td>
</tr>
<tr id="row18915451694"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p9915145099"><a name="p9915145099"></a><a name="p9915145099"></a>P2s</p>
<p id="p179151551194"><a name="p179151551194"></a><a name="p179151551194"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p17915251915"><a name="p17915251915"></a><a name="p17915251915"></a>Windows Server 2012 R2 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p89151251596"><a name="p89151251596"></a><a name="p89151251596"></a>9.2及以上版本</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p39151511912"><a name="p39151511912"></a><a name="p39151511912"></a>x86_64</p>
</td>
</tr>
</tbody>
</table>

**表 4**  P2v实例CUDA工具包下载地址

<a name="table1568017042711"></a>
<table><thead align="left"><tr id="row156808014275"><th class="cellrowborder" valign="top" width="12.530000000000003%" id="mcps1.2.6.1.1"><p id="p1268060192714"><a name="p1268060192714"></a><a name="p1268060192714"></a><strong id="b126813072715"><a name="b126813072715"></a><a name="b126813072715"></a>实例</strong></p>
<p id="p1768110192710"><a name="p1768110192710"></a><a name="p1768110192710"></a><strong id="b5681140172713"><a name="b5681140172713"></a><a name="b5681140172713"></a>类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="17.000000000000004%" id="mcps1.2.6.1.2"><p id="p10681208276"><a name="p10681208276"></a><a name="p10681208276"></a><strong id="b56814012719"><a name="b56814012719"></a><a name="b56814012719"></a>操作系统</strong></p>
</th>
<th class="cellrowborder" valign="top" width="19.060000000000002%" id="mcps1.2.6.1.3"><p id="p2068130112711"><a name="p2068130112711"></a><a name="p2068130112711"></a><strong id="b14681507272"><a name="b14681507272"></a><a name="b14681507272"></a>CUDA版本</strong></p>
</th>
<th class="cellrowborder" valign="top" width="28.290000000000003%" id="mcps1.2.6.1.4"><p id="p5681301272"><a name="p5681301272"></a><a name="p5681301272"></a><strong id="b16681170112716"><a name="b16681170112716"></a><a name="b16681170112716"></a>下载路径</strong></p>
</th>
<th class="cellrowborder" valign="top" width="23.12%" id="mcps1.2.6.1.5"><p id="p668115013273"><a name="p668115013273"></a><a name="p668115013273"></a><strong id="b20681160142710"><a name="b20681160142710"></a><a name="b20681160142710"></a>CPU架构</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row9681305277"><td class="cellrowborder" valign="top" width="12.530000000000003%" headers="mcps1.2.6.1.1 "><p id="p193381141288"><a name="p193381141288"></a><a name="p193381141288"></a>P2v</p>
<p id="p11338111420282"><a name="p11338111420282"></a><a name="p11338111420282"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" width="17.000000000000004%" headers="mcps1.2.6.1.2 "><p id="p524971716290"><a name="p524971716290"></a><a name="p524971716290"></a>CentOS 7.7 64bit</p>
</td>
<td class="cellrowborder" valign="top" width="19.060000000000002%" headers="mcps1.2.6.1.3 "><p id="p1468112011275"><a name="p1468112011275"></a><a name="p1468112011275"></a>9.2/10.1</p>
<p id="p14912682331"><a name="p14912682331"></a><a name="p14912682331"></a>内核版本不高于3.10.0-957.5.1.e17.x86_64时可以安装9.2版本的CUDA工具包。</p>
</td>
<td class="cellrowborder" rowspan="6" valign="top" width="28.290000000000003%" headers="mcps1.2.6.1.4 "><p id="p16732131003213"><a name="p16732131003213"></a><a name="p16732131003213"></a>9.2版本：<a href="https://developer.nvidia.com/cuda-92-download-archive" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/cuda-92-download-archive</a></p>
<p id="p8732191063214"><a name="p8732191063214"></a><a name="p8732191063214"></a></p>
<p id="p473211063217"><a name="p473211063217"></a><a name="p473211063217"></a>10.1版本：</p>
<p id="p117321110123212"><a name="p117321110123212"></a><a name="p117321110123212"></a><a href="https://developer.nvidia.com/cuda-10.1-download-archive-base" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/cuda-10.1-download-archive-base</a></p>
<p id="p4650101312237"><a name="p4650101312237"></a><a name="p4650101312237"></a></p>
</td>
<td class="cellrowborder" valign="top" width="23.12%" headers="mcps1.2.6.1.5 "><p id="p2681200142714"><a name="p2681200142714"></a><a name="p2681200142714"></a>x86_64</p>
</td>
</tr>
<tr id="row57457541274"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p10222812102813"><a name="p10222812102813"></a><a name="p10222812102813"></a>P2v</p>
<p id="p42221112152817"><a name="p42221112152817"></a><a name="p42221112152817"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p8249101718293"><a name="p8249101718293"></a><a name="p8249101718293"></a>EulerOS 2.5 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1746205419275"><a name="p1746205419275"></a><a name="p1746205419275"></a>9.2</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p174612544273"><a name="p174612544273"></a><a name="p174612544273"></a>x86_64</p>
</td>
</tr>
<tr id="row1781505172819"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p039911562810"><a name="p039911562810"></a><a name="p039911562810"></a>P2v</p>
<p id="p18399815202811"><a name="p18399815202811"></a><a name="p18399815202811"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p0250181719294"><a name="p0250181719294"></a><a name="p0250181719294"></a>Ubuntu 16.04 64bit</p>
<p id="p19250917112920"><a name="p19250917112920"></a><a name="p19250917112920"></a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p128153512286"><a name="p128153512286"></a><a name="p128153512286"></a>9.2/10.1</p>
<p id="p841162753314"><a name="p841162753314"></a><a name="p841162753314"></a>内核版本不高于4.4.0-141-generic时可以安装9.2版本的CUDA工具包。</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1381555132812"><a name="p1381555132812"></a><a name="p1381555132812"></a>x86_64</p>
</td>
</tr>
<tr id="row17457310202310"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p69283143231"><a name="p69283143231"></a><a name="p69283143231"></a>P2v</p>
<p id="p159281147232"><a name="p159281147232"></a><a name="p159281147232"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p18928161413231"><a name="p18928161413231"></a><a name="p18928161413231"></a>Windows Server 2019 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p1392881410233"><a name="p1392881410233"></a><a name="p1392881410233"></a>9.2/10.1</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p29281114192319"><a name="p29281114192319"></a><a name="p29281114192319"></a>x86_64</p>
</td>
</tr>
<tr id="row19371337288"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p11475716112817"><a name="p11475716112817"></a><a name="p11475716112817"></a>P2v</p>
<p id="p0475181615287"><a name="p0475181615287"></a><a name="p0475181615287"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p2250141712298"><a name="p2250141712298"></a><a name="p2250141712298"></a>Windows Server 2016 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p23813332812"><a name="p23813332812"></a><a name="p23813332812"></a>9.2/10.1</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p193816311284"><a name="p193816311284"></a><a name="p193816311284"></a>x86_64</p>
</td>
</tr>
<tr id="row33813162818"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p03881317172812"><a name="p03881317172812"></a><a name="p03881317172812"></a>P2v</p>
<p id="p73881817102817"><a name="p73881817102817"></a><a name="p73881817102817"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p182501177297"><a name="p182501177297"></a><a name="p182501177297"></a>Windows Server 2012 R2 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p163843152816"><a name="p163843152816"></a><a name="p163843152816"></a>9.2/10.1</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p15386317283"><a name="p15386317283"></a><a name="p15386317283"></a>x86_64</p>
</td>
</tr>
</tbody>
</table>

**表 5**  P1实例CUDA工具包下载地址

<a name="table10558744163515"></a>
<table><thead align="left"><tr id="row11558444123510"><th class="cellrowborder" valign="top" width="12.530000000000003%" id="mcps1.2.6.1.1"><p id="p12558194412351"><a name="p12558194412351"></a><a name="p12558194412351"></a><strong id="b355824463511"><a name="b355824463511"></a><a name="b355824463511"></a>实例</strong></p>
<p id="p3558544153516"><a name="p3558544153516"></a><a name="p3558544153516"></a><strong id="b1055804433520"><a name="b1055804433520"></a><a name="b1055804433520"></a>类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="16.900000000000006%" id="mcps1.2.6.1.2"><p id="p13559124453511"><a name="p13559124453511"></a><a name="p13559124453511"></a><strong id="b65597444358"><a name="b65597444358"></a><a name="b65597444358"></a>操作系统</strong></p>
</th>
<th class="cellrowborder" valign="top" width="15.230000000000002%" id="mcps1.2.6.1.3"><p id="p35591044143520"><a name="p35591044143520"></a><a name="p35591044143520"></a><strong id="b19559134453515"><a name="b19559134453515"></a><a name="b19559134453515"></a>CUDA版本</strong></p>
</th>
<th class="cellrowborder" valign="top" width="32.220000000000006%" id="mcps1.2.6.1.4"><p id="p14559244193519"><a name="p14559244193519"></a><a name="p14559244193519"></a><strong id="b1555915448353"><a name="b1555915448353"></a><a name="b1555915448353"></a>下载路径</strong></p>
</th>
<th class="cellrowborder" valign="top" width="23.12%" id="mcps1.2.6.1.5"><p id="p9559114493518"><a name="p9559114493518"></a><a name="p9559114493518"></a><strong id="b85591644183514"><a name="b85591644183514"></a><a name="b85591644183514"></a>CPU架构</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row17559844123515"><td class="cellrowborder" valign="top" width="12.530000000000003%" headers="mcps1.2.6.1.1 "><p id="p167751451103510"><a name="p167751451103510"></a><a name="p167751451103510"></a>P1</p>
<p id="p1677525103511"><a name="p1677525103511"></a><a name="p1677525103511"></a>(P100)</p>
</td>
<td class="cellrowborder" valign="top" width="16.900000000000006%" headers="mcps1.2.6.1.2 "><p id="p14910138153610"><a name="p14910138153610"></a><a name="p14910138153610"></a>CentOS 7.3 64bit</p>
</td>
<td class="cellrowborder" valign="top" width="15.230000000000002%" headers="mcps1.2.6.1.3 "><p id="p115591644203519"><a name="p115591644203519"></a><a name="p115591644203519"></a>9</p>
</td>
<td class="cellrowborder" rowspan="3" valign="top" width="32.220000000000006%" headers="mcps1.2.6.1.4 "><p id="p173767017378"><a name="p173767017378"></a><a name="p173767017378"></a><a href="https://developer.nvidia.com/cuda-90-download-archive" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/cuda-90-download-archive</a></p>
</td>
<td class="cellrowborder" valign="top" width="23.12%" headers="mcps1.2.6.1.5 "><p id="p1955934410359"><a name="p1955934410359"></a><a name="p1955934410359"></a>x86_64</p>
</td>
</tr>
<tr id="row19656202314361"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p2075731173712"><a name="p2075731173712"></a><a name="p2075731173712"></a>P1</p>
<p id="p137578116371"><a name="p137578116371"></a><a name="p137578116371"></a>(P100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p1591013893618"><a name="p1591013893618"></a><a name="p1591013893618"></a>Ubuntu 16.04 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p17656523163612"><a name="p17656523163612"></a><a name="p17656523163612"></a>9</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p14656162373614"><a name="p14656162373614"></a><a name="p14656162373614"></a>x86_64</p>
</td>
</tr>
<tr id="row17373122123614"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p19797121210375"><a name="p19797121210375"></a><a name="p19797121210375"></a>P1</p>
<p id="p37971412113710"><a name="p37971412113710"></a><a name="p37971412113710"></a>(P100)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p15910173812363"><a name="p15910173812363"></a><a name="p15910173812363"></a>Windows Server 2012 R2 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p133741121143610"><a name="p133741121143610"></a><a name="p133741121143610"></a>9</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p123741021103611"><a name="p123741021103611"></a><a name="p123741021103611"></a>x86_64</p>
</td>
</tr>
</tbody>
</table>

**表 6**  Pi2实例CUDA工具包下载地址

<a name="table2067594175114"></a>
<table><thead align="left"><tr id="row067511415518"><th class="cellrowborder" valign="top" width="12.530000000000003%" id="mcps1.2.6.1.1"><p id="p10675441165117"><a name="p10675441165117"></a><a name="p10675441165117"></a><strong id="b116751341165111"><a name="b116751341165111"></a><a name="b116751341165111"></a>实例</strong></p>
<p id="p867534114515"><a name="p867534114515"></a><a name="p867534114515"></a><strong id="b667513411512"><a name="b667513411512"></a><a name="b667513411512"></a>类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="16.990000000000002%" id="mcps1.2.6.1.2"><p id="p767564145113"><a name="p767564145113"></a><a name="p767564145113"></a><strong id="b1667594165111"><a name="b1667594165111"></a><a name="b1667594165111"></a>操作系统</strong></p>
</th>
<th class="cellrowborder" valign="top" width="15.140000000000004%" id="mcps1.2.6.1.3"><p id="p6675104115512"><a name="p6675104115512"></a><a name="p6675104115512"></a><strong id="b4675114111514"><a name="b4675114111514"></a><a name="b4675114111514"></a>CUDA版本</strong></p>
</th>
<th class="cellrowborder" valign="top" width="32.220000000000006%" id="mcps1.2.6.1.4"><p id="p167594112519"><a name="p167594112519"></a><a name="p167594112519"></a><strong id="b106751541145118"><a name="b106751541145118"></a><a name="b106751541145118"></a>下载路径</strong></p>
</th>
<th class="cellrowborder" valign="top" width="23.12%" id="mcps1.2.6.1.5"><p id="p156757416515"><a name="p156757416515"></a><a name="p156757416515"></a><strong id="b1767554135119"><a name="b1767554135119"></a><a name="b1767554135119"></a>CPU架构</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row367564155119"><td class="cellrowborder" valign="top" width="12.530000000000003%" headers="mcps1.2.6.1.1 "><p id="p967515413511"><a name="p967515413511"></a><a name="p967515413511"></a>Pi2</p>
<p id="p56755419514"><a name="p56755419514"></a><a name="p56755419514"></a>(T4)</p>
</td>
<td class="cellrowborder" valign="top" width="16.990000000000002%" headers="mcps1.2.6.1.2 "><p id="p156753415517"><a name="p156753415517"></a><a name="p156753415517"></a>CentOS 7.5 64bit</p>
</td>
<td class="cellrowborder" valign="top" width="15.140000000000004%" headers="mcps1.2.6.1.3 "><p id="p56751941145112"><a name="p56751941145112"></a><a name="p56751941145112"></a>10.1</p>
</td>
<td class="cellrowborder" rowspan="3" valign="top" width="32.220000000000006%" headers="mcps1.2.6.1.4 "><p id="p667504118517"><a name="p667504118517"></a><a name="p667504118517"></a><a href="https://developer.nvidia.com/cuda-10.1-download-archive-base" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/cuda-10.1-download-archive-base</a></p>
</td>
<td class="cellrowborder" valign="top" width="23.12%" headers="mcps1.2.6.1.5 "><p id="p13675144111518"><a name="p13675144111518"></a><a name="p13675144111518"></a>x86_64</p>
</td>
</tr>
<tr id="row867574155113"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p1067564111515"><a name="p1067564111515"></a><a name="p1067564111515"></a>Pi2</p>
<p id="p1267554114516"><a name="p1267554114516"></a><a name="p1267554114516"></a>(T4)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p2675204175118"><a name="p2675204175118"></a><a name="p2675204175118"></a>Ubuntu 16.04 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p15676194145112"><a name="p15676194145112"></a><a name="p15676194145112"></a>10.1</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p6676164165116"><a name="p6676164165116"></a><a name="p6676164165116"></a>x86_64</p>
</td>
</tr>
<tr id="row18676041195115"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p10676441135116"><a name="p10676441135116"></a><a name="p10676441135116"></a>Pi2</p>
<p id="p66760416513"><a name="p66760416513"></a><a name="p66760416513"></a>(T4)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p13676184113513"><a name="p13676184113513"></a><a name="p13676184113513"></a>Windows Server 2016 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p19676164175113"><a name="p19676164175113"></a><a name="p19676164175113"></a>10.1</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p8676134195111"><a name="p8676134195111"></a><a name="p8676134195111"></a>x86_64</p>
</td>
</tr>
</tbody>
</table>

**表 7**  Pi1实例CUDA工具包下载地址

<a name="table6355115314383"></a>
<table><thead align="left"><tr id="row9355125383813"><th class="cellrowborder" valign="top" width="12.48%" id="mcps1.2.6.1.1"><p id="p1535555363814"><a name="p1535555363814"></a><a name="p1535555363814"></a><strong id="b153551353133819"><a name="b153551353133819"></a><a name="b153551353133819"></a>实例</strong></p>
<p id="p835517539383"><a name="p835517539383"></a><a name="p835517539383"></a><strong id="b173551953163816"><a name="b173551953163816"></a><a name="b173551953163816"></a>类型</strong></p>
</th>
<th class="cellrowborder" valign="top" width="17.040000000000003%" id="mcps1.2.6.1.2"><p id="p16355115373819"><a name="p16355115373819"></a><a name="p16355115373819"></a><strong id="b6355175314388"><a name="b6355175314388"></a><a name="b6355175314388"></a>操作系统</strong></p>
</th>
<th class="cellrowborder" valign="top" width="15.140000000000004%" id="mcps1.2.6.1.3"><p id="p203561053133817"><a name="p203561053133817"></a><a name="p203561053133817"></a><strong id="b18356175314388"><a name="b18356175314388"></a><a name="b18356175314388"></a>CUDA版本</strong></p>
</th>
<th class="cellrowborder" valign="top" width="32.220000000000006%" id="mcps1.2.6.1.4"><p id="p33565536387"><a name="p33565536387"></a><a name="p33565536387"></a><strong id="b113561953163813"><a name="b113561953163813"></a><a name="b113561953163813"></a>下载路径</strong></p>
</th>
<th class="cellrowborder" valign="top" width="23.12%" id="mcps1.2.6.1.5"><p id="p1235655315386"><a name="p1235655315386"></a><a name="p1235655315386"></a><strong id="b1035695316388"><a name="b1035695316388"></a><a name="b1035695316388"></a>CPU架构</strong></p>
</th>
</tr>
</thead>
<tbody><tr id="row19356253123817"><td class="cellrowborder" valign="top" width="12.48%" headers="mcps1.2.6.1.1 "><p id="p819715611392"><a name="p819715611392"></a><a name="p819715611392"></a>Pi1</p>
<p id="p91971168396"><a name="p91971168396"></a><a name="p91971168396"></a>(P4)</p>
</td>
<td class="cellrowborder" valign="top" width="17.040000000000003%" headers="mcps1.2.6.1.2 "><p id="p14543113713918"><a name="p14543113713918"></a><a name="p14543113713918"></a>CentOS 7.3 64bit</p>
</td>
<td class="cellrowborder" valign="top" width="15.140000000000004%" headers="mcps1.2.6.1.3 "><p id="p1435635317381"><a name="p1435635317381"></a><a name="p1435635317381"></a>9</p>
</td>
<td class="cellrowborder" rowspan="2" valign="top" width="32.220000000000006%" headers="mcps1.2.6.1.4 "><p id="p0356185343820"><a name="p0356185343820"></a><a name="p0356185343820"></a><a href="https://developer.nvidia.com/cuda-90-download-archive" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/cuda-90-download-archive</a></p>
<p id="p9610627143918"><a name="p9610627143918"></a><a name="p9610627143918"></a></p>
</td>
<td class="cellrowborder" valign="top" width="23.12%" headers="mcps1.2.6.1.5 "><p id="p1835618536387"><a name="p1835618536387"></a><a name="p1835618536387"></a>x86_64</p>
</td>
</tr>
<tr id="row260922733913"><td class="cellrowborder" valign="top" headers="mcps1.2.6.1.1 "><p id="p5443531123917"><a name="p5443531123917"></a><a name="p5443531123917"></a>Pi1</p>
<p id="p54436312399"><a name="p54436312399"></a><a name="p54436312399"></a>(P4)</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.2 "><p id="p154393733915"><a name="p154393733915"></a><a name="p154393733915"></a>Ubuntu 16.04 64bit</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.3 "><p id="p6610327153916"><a name="p6610327153916"></a><a name="p6610327153916"></a>9</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.6.1.4 "><p id="p1610122713391"><a name="p1610122713391"></a><a name="p1610122713391"></a>x86_64</p>
</td>
</tr>
</tbody>
</table>

**表 8**  G6实例CUDA工具包下载地址

<a name="table69013507215"></a>
<table><tbody><tr id="row189115504216"><td class="cellrowborder" valign="top" width="17.141714171417142%"><p id="p7916500213"><a name="p7916500213"></a><a name="p7916500213"></a><strong id="b591155012212"><a name="b591155012212"></a><a name="b591155012212"></a>实例</strong></p>
<p id="p39110501824"><a name="p39110501824"></a><a name="p39110501824"></a><strong id="b59116501216"><a name="b59116501216"></a><a name="b59116501216"></a>类型</strong></p>
</td>
<td class="cellrowborder" valign="top" width="15.62156215621562%"><p id="p49116501213"><a name="p49116501213"></a><a name="p49116501213"></a><strong id="b139118504211"><a name="b139118504211"></a><a name="b139118504211"></a>操作系统</strong></p>
</td>
<td class="cellrowborder" valign="top" width="17.32173217321732%"><p id="p39115501229"><a name="p39115501229"></a><a name="p39115501229"></a><strong id="b169111509210"><a name="b169111509210"></a><a name="b169111509210"></a>CUDA版本</strong></p>
</td>
<td class="cellrowborder" valign="top" width="34.63346334633463%"><p id="p129165011216"><a name="p129165011216"></a><a name="p129165011216"></a><strong id="b169125017213"><a name="b169125017213"></a><a name="b169125017213"></a>下载路径</strong></p>
</td>
<td class="cellrowborder" valign="top" width="15.28152815281528%"><p id="p3911650728"><a name="p3911650728"></a><a name="p3911650728"></a><strong id="b0911509211"><a name="b0911509211"></a><a name="b0911509211"></a>CPU架构</strong></p>
</td>
</tr>
<tr id="row2911501214"><td class="cellrowborder" valign="top" width="17.141714171417142%"><p id="p1911650528"><a name="p1911650528"></a><a name="p1911650528"></a>G6</p>
<p id="p1586914541636"><a name="p1586914541636"></a><a name="p1586914541636"></a>(T4)</p>
</td>
<td class="cellrowborder" valign="top" width="15.62156215621562%"><p id="p189113501027"><a name="p189113501027"></a><a name="p189113501027"></a>Windows Server 2016 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top" width="17.32173217321732%"><p id="p1691750522"><a name="p1691750522"></a><a name="p1691750522"></a>10.1</p>
</td>
<td class="cellrowborder" valign="top" width="34.63346334633463%"><p id="p89118509212"><a name="p89118509212"></a><a name="p89118509212"></a><a href="https://developer.nvidia.com/cuda-10.1-download-archive-base" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/cuda-10.1-download-archive-base</a></p>
</td>
<td class="cellrowborder" valign="top" width="15.28152815281528%"><p id="p191115016212"><a name="p191115016212"></a><a name="p191115016212"></a>x86_64</p>
</td>
</tr>
</tbody>
</table>

**表 9**  G5实例CUDA工具包下载地址

<a name="table0205357153915"></a>
<table><tbody><tr id="row5801145717392"><td class="cellrowborder" valign="top" width="17.141714171417142%"><p id="p0801257123913"><a name="p0801257123913"></a><a name="p0801257123913"></a><strong id="b1080105711399"><a name="b1080105711399"></a><a name="b1080105711399"></a>实例</strong></p>
<p id="p68018578392"><a name="p68018578392"></a><a name="p68018578392"></a><strong id="b1080120577394"><a name="b1080120577394"></a><a name="b1080120577394"></a>类型</strong></p>
</td>
<td class="cellrowborder" valign="top" width="15.62156215621562%"><p id="p48011957163914"><a name="p48011957163914"></a><a name="p48011957163914"></a><strong id="b13801105723913"><a name="b13801105723913"></a><a name="b13801105723913"></a>操作系统</strong></p>
</td>
<td class="cellrowborder" valign="top" width="17.32173217321732%"><p id="p28011157173911"><a name="p28011157173911"></a><a name="p28011157173911"></a><strong id="b10801195716393"><a name="b10801195716393"></a><a name="b10801195716393"></a>CUDA版本</strong></p>
</td>
<td class="cellrowborder" valign="top" width="34.63346334633463%"><p id="p108012057193911"><a name="p108012057193911"></a><a name="p108012057193911"></a><strong id="b78011757123915"><a name="b78011757123915"></a><a name="b78011757123915"></a>下载路径</strong></p>
</td>
<td class="cellrowborder" valign="top" width="15.28152815281528%"><p id="p18801165718390"><a name="p18801165718390"></a><a name="p18801165718390"></a><strong id="b1735985491411"><a name="b1735985491411"></a><a name="b1735985491411"></a>CPU架构</strong></p>
</td>
</tr>
<tr id="row16814155714390"><td class="cellrowborder" rowspan="3" valign="top" width="17.141714171417142%"><p id="p381465712394"><a name="p381465712394"></a><a name="p381465712394"></a>G5.8xlarge.4</p>
<p id="p16814205743913"><a name="p16814205743913"></a><a name="p16814205743913"></a>(V100直通)</p>
</td>
<td class="cellrowborder" valign="top" width="15.62156215621562%"><p id="p5814195743910"><a name="p5814195743910"></a><a name="p5814195743910"></a>CentOS 7.5 64bit</p>
</td>
<td class="cellrowborder" rowspan="3" valign="top" width="17.32173217321732%"><p id="p1481425718395"><a name="p1481425718395"></a><a name="p1481425718395"></a>10.1</p>
</td>
<td class="cellrowborder" rowspan="3" valign="top" width="34.63346334633463%"><p id="p18814135743911"><a name="p18814135743911"></a><a name="p18814135743911"></a><a href="https://developer.nvidia.com/cuda-10.1-download-archive-base" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/cuda-10.1-download-archive-base</a></p>
</td>
<td class="cellrowborder" valign="top" width="15.28152815281528%"><p id="p481425713396"><a name="p481425713396"></a><a name="p481425713396"></a>x86_64</p>
</td>
</tr>
<tr id="row1981418574397"><td class="cellrowborder" valign="top"><p id="p208143578395"><a name="p208143578395"></a><a name="p208143578395"></a>Windows Server 2016 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top"><p id="p88148574393"><a name="p88148574393"></a><a name="p88148574393"></a>x86_64</p>
</td>
</tr>
<tr id="row581595763916"><td class="cellrowborder" valign="top"><p id="p68151957123917"><a name="p68151957123917"></a><a name="p68151957123917"></a>Windows Server 2012 R2 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top"><p id="p481525719396"><a name="p481525719396"></a><a name="p481525719396"></a>x86_64</p>
</td>
</tr>
</tbody>
</table>

