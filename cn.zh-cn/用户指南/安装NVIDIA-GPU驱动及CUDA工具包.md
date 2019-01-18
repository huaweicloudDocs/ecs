# 安装NVIDIA GPU驱动及CUDA工具包<a name="ZH-CN_TOPIC_0149470468"></a>

## 操作场景<a name="section20948151111013"></a>

使用P1型、P2v型、Pi1型弹性云服务器时，需确保云服务器已安装GPU驱动和CUDA工具包，否则无法实现计算加速功能。

## 前提条件<a name="section148811241191114"></a>

1.  已绑定弹性公网IP。
2.  云服务器未安装GPU驱动以及CUDA工具包。

>![](public_sys-resources/icon-note.gif) **说明：**   
>从NVIDIA官网下载安装CUDA工具包后，会自动将对应GPU驱动安装，无需再单独安装GPU驱动  

## CUDA工具包下载地址<a name="section16533957201716"></a>

**表 1**  CUDA工具包下载地址

<a name="table1925059201814"></a>
<table><tbody><tr id="row1823381018183"><td class="cellrowborder" rowspan="2" valign="top"><p id="p42331710131810"><a name="p42331710131810"></a><a name="p42331710131810"></a><strong id="b132332010191813"><a name="b132332010191813"></a><a name="b132332010191813"></a>实例</strong></p>
<p id="p923318107185"><a name="p923318107185"></a><a name="p923318107185"></a><strong id="b523310105184"><a name="b523310105184"></a><a name="b523310105184"></a>类型</strong></p>
</td>
<td class="cellrowborder" rowspan="2" valign="top"><p id="p423371018187"><a name="p423371018187"></a><a name="p423371018187"></a><strong id="b32336108188"><a name="b32336108188"></a><a name="b32336108188"></a>操作系统</strong></p>
</td>
<td class="cellrowborder" rowspan="2" valign="top"><p id="p11233310161819"><a name="p11233310161819"></a><a name="p11233310161819"></a><strong id="b18233191012188"><a name="b18233191012188"></a><a name="b18233191012188"></a>CUDA版本</strong></p>
</td>
<td class="cellrowborder" rowspan="2" valign="top"><p id="p13233131021814"><a name="p13233131021814"></a><a name="p13233131021814"></a><strong id="b182330103182"><a name="b182330103182"></a><a name="b182330103182"></a>下载路径</strong></p>
</td>
<td class="cellrowborder" colspan="5" valign="top"><p id="p1523301081815"><a name="p1523301081815"></a><a name="p1523301081815"></a><strong id="b19233151061818"><a name="b19233151061818"></a><a name="b19233151061818"></a>索引项</strong></p>
</td>
</tr>
<tr id="row18234171011816"><td class="cellrowborder" valign="top"><p id="p1023414107181"><a name="p1023414107181"></a><a name="p1023414107181"></a><strong id="b1523461012188"><a name="b1523461012188"></a><a name="b1523461012188"></a>Operating</strong></p>
<p id="p18234151061820"><a name="p18234151061820"></a><a name="p18234151061820"></a><strong id="b72345105183"><a name="b72345105183"></a><a name="b72345105183"></a>System</strong></p>
</td>
<td class="cellrowborder" valign="top"><p id="p223401061810"><a name="p223401061810"></a><a name="p223401061810"></a><strong id="b16234111016185"><a name="b16234111016185"></a><a name="b16234111016185"></a>Architecture</strong></p>
</td>
<td class="cellrowborder" valign="top"><p id="p523421071815"><a name="p523421071815"></a><a name="p523421071815"></a><strong id="b1223419100185"><a name="b1223419100185"></a><a name="b1223419100185"></a>Distribution</strong></p>
</td>
<td class="cellrowborder" valign="top"><p id="p9234910161810"><a name="p9234910161810"></a><a name="p9234910161810"></a><strong id="b92341010161820"><a name="b92341010161820"></a><a name="b92341010161820"></a>Version</strong></p>
</td>
<td class="cellrowborder" valign="top"><p id="p1923413106186"><a name="p1923413106186"></a><a name="p1923413106186"></a><strong id="b3234131019186"><a name="b3234131019186"></a><a name="b3234131019186"></a>Installer</strong></p>
<p id="p123421041811"><a name="p123421041811"></a><a name="p123421041811"></a><strong id="b19234181013184"><a name="b19234181013184"></a><a name="b19234181013184"></a>Type</strong></p>
</td>
</tr>
<tr id="row102341510181817"><td class="cellrowborder" rowspan="4" valign="top" width="6.270627062706271%"><p id="p1234010111816"><a name="p1234010111816"></a><a name="p1234010111816"></a>P2v</p>
<p id="p42349108182"><a name="p42349108182"></a><a name="p42349108182"></a>(V100)</p>
</td>
<td class="cellrowborder" valign="top" width="11.101110111011101%"><p id="p192341110131820"><a name="p192341110131820"></a><a name="p192341110131820"></a>CentOS 7.4 64bit</p>
</td>
<td class="cellrowborder" rowspan="4" valign="top" width="9.21092109210921%"><p id="p1923431041818"><a name="p1923431041818"></a><a name="p1923431041818"></a>9.2</p>
</td>
<td class="cellrowborder" rowspan="4" valign="top" width="21.56215621562156%"><p id="p19234310151814"><a name="p19234310151814"></a><a name="p19234310151814"></a>https://developer.nvidia.com/cuda-92-download-archive</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p17234010121812"><a name="p17234010121812"></a><a name="p17234010121812"></a>Linux</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p1234171015187"><a name="p1234171015187"></a><a name="p1234171015187"></a>x86_64</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p19234101013187"><a name="p19234101013187"></a><a name="p19234101013187"></a>CentOS</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p323418102185"><a name="p323418102185"></a><a name="p323418102185"></a>7</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p1023481091815"><a name="p1023481091815"></a><a name="p1023481091815"></a>rpm(local)</p>
</td>
</tr>
<tr id="row4234910171815"><td class="cellrowborder" valign="top"><p id="p192342010101812"><a name="p192342010101812"></a><a name="p192342010101812"></a>Ubuntu 16.04 64bit</p>
</td>
<td class="cellrowborder" valign="top"><p id="p4235171012181"><a name="p4235171012181"></a><a name="p4235171012181"></a>Linux</p>
</td>
<td class="cellrowborder" valign="top"><p id="p9235410171815"><a name="p9235410171815"></a><a name="p9235410171815"></a>x86_64</p>
</td>
<td class="cellrowborder" valign="top"><p id="p123581014183"><a name="p123581014183"></a><a name="p123581014183"></a>Ubuntu</p>
</td>
<td class="cellrowborder" valign="top"><p id="p723518103184"><a name="p723518103184"></a><a name="p723518103184"></a>16.04</p>
</td>
<td class="cellrowborder" valign="top"><p id="p14235171091819"><a name="p14235171091819"></a><a name="p14235171091819"></a>deb(local)</p>
</td>
</tr>
<tr id="row423561031812"><td class="cellrowborder" valign="top"><p id="p102359104187"><a name="p102359104187"></a><a name="p102359104187"></a>Windows Server 2016 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1223581041820"><a name="p1223581041820"></a><a name="p1223581041820"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top"><p id="p52355101181"><a name="p52355101181"></a><a name="p52355101181"></a>x86_64</p>
</td>
<td class="cellrowborder" valign="top"><p id="p15235510171810"><a name="p15235510171810"></a><a name="p15235510171810"></a>-</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1235710101818"><a name="p1235710101818"></a><a name="p1235710101818"></a>Server 2016</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1023513106181"><a name="p1023513106181"></a><a name="p1023513106181"></a>exe(local)</p>
</td>
</tr>
<tr id="row1923521018188"><td class="cellrowborder" valign="top"><p id="p102351110191814"><a name="p102351110191814"></a><a name="p102351110191814"></a>Windows Server 2012 R2 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top"><p id="p2235121001819"><a name="p2235121001819"></a><a name="p2235121001819"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top"><p id="p12351010121813"><a name="p12351010121813"></a><a name="p12351010121813"></a>x86_64</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1323561061820"><a name="p1323561061820"></a><a name="p1323561061820"></a>-</p>
</td>
<td class="cellrowborder" valign="top"><p id="p723501021810"><a name="p723501021810"></a><a name="p723501021810"></a>Server 2012 R2</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1823521018185"><a name="p1823521018185"></a><a name="p1823521018185"></a>exe(local)</p>
</td>
</tr>
<tr id="row11235510131813"><td class="cellrowborder" rowspan="3" valign="top" width="6.270627062706271%"><p id="p22358104183"><a name="p22358104183"></a><a name="p22358104183"></a>P1</p>
<p id="p11235101013181"><a name="p11235101013181"></a><a name="p11235101013181"></a>(P100)</p>
</td>
<td class="cellrowborder" valign="top" width="11.101110111011101%"><p id="p22351110161817"><a name="p22351110161817"></a><a name="p22351110161817"></a>CentOS 7.3 64bit</p>
</td>
<td class="cellrowborder" rowspan="3" valign="top" width="9.21092109210921%"><p id="p11235151021818"><a name="p11235151021818"></a><a name="p11235151021818"></a>9</p>
</td>
<td class="cellrowborder" rowspan="3" valign="top" width="21.56215621562156%"><p id="p10235151031815"><a name="p10235151031815"></a><a name="p10235151031815"></a>https://developer.nvidia.com/cuda-90-download-archive</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p10235171012186"><a name="p10235171012186"></a><a name="p10235171012186"></a>Linux</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p72351210101819"><a name="p72351210101819"></a><a name="p72351210101819"></a>x86_64</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p122367104188"><a name="p122367104188"></a><a name="p122367104188"></a>CentOS</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p52362010181818"><a name="p52362010181818"></a><a name="p52362010181818"></a>7</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p0236131001817"><a name="p0236131001817"></a><a name="p0236131001817"></a>rpm(local)</p>
</td>
</tr>
<tr id="row13236141001819"><td class="cellrowborder" valign="top"><p id="p52361010161815"><a name="p52361010161815"></a><a name="p52361010161815"></a>Ubuntu 16.04 64bit</p>
</td>
<td class="cellrowborder" valign="top"><p id="p9236510131810"><a name="p9236510131810"></a><a name="p9236510131810"></a>Linux</p>
</td>
<td class="cellrowborder" valign="top"><p id="p92361110111812"><a name="p92361110111812"></a><a name="p92361110111812"></a>x86_64</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1236111018189"><a name="p1236111018189"></a><a name="p1236111018189"></a>Ubuntu</p>
</td>
<td class="cellrowborder" valign="top"><p id="p18236161041813"><a name="p18236161041813"></a><a name="p18236161041813"></a>16.04</p>
</td>
<td class="cellrowborder" valign="top"><p id="p18236131012181"><a name="p18236131012181"></a><a name="p18236131012181"></a>deb(local)</p>
</td>
</tr>
<tr id="row14236111091815"><td class="cellrowborder" valign="top"><p id="p18236201010185"><a name="p18236201010185"></a><a name="p18236201010185"></a>Windows Server 2012 R2 Standard 64bit</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1236101019183"><a name="p1236101019183"></a><a name="p1236101019183"></a>Windows</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1123621021813"><a name="p1123621021813"></a><a name="p1123621021813"></a>x86_64</p>
</td>
<td class="cellrowborder" valign="top"><p id="p112361310141815"><a name="p112361310141815"></a><a name="p112361310141815"></a>-</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1236181081811"><a name="p1236181081811"></a><a name="p1236181081811"></a>Server 2012 R2</p>
</td>
<td class="cellrowborder" valign="top"><p id="p7236171020184"><a name="p7236171020184"></a><a name="p7236171020184"></a>exe(local)</p>
</td>
</tr>
<tr id="row2236181031812"><td class="cellrowborder" rowspan="2" valign="top" width="6.270627062706271%"><p id="p13236410181818"><a name="p13236410181818"></a><a name="p13236410181818"></a>Pi1</p>
<p id="p152361310111812"><a name="p152361310111812"></a><a name="p152361310111812"></a>(P4)</p>
</td>
<td class="cellrowborder" valign="top" width="11.101110111011101%"><p id="p72361910171813"><a name="p72361910171813"></a><a name="p72361910171813"></a>CentOS 7.3 64bit</p>
</td>
<td class="cellrowborder" rowspan="2" valign="top" width="9.21092109210921%"><p id="p142365104184"><a name="p142365104184"></a><a name="p142365104184"></a>9</p>
</td>
<td class="cellrowborder" rowspan="2" valign="top" width="21.56215621562156%"><p id="p4236201011817"><a name="p4236201011817"></a><a name="p4236201011817"></a>https://developer.nvidia.com/cuda-90-download-archive</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p132365103183"><a name="p132365103183"></a><a name="p132365103183"></a>Linux</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p3236010131812"><a name="p3236010131812"></a><a name="p3236010131812"></a>x86_64</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p122364104185"><a name="p122364104185"></a><a name="p122364104185"></a>CentOS</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p1123621013188"><a name="p1123621013188"></a><a name="p1123621013188"></a>7</p>
</td>
<td class="cellrowborder" valign="top" width="10.371037103710371%"><p id="p1523671020180"><a name="p1523671020180"></a><a name="p1523671020180"></a>rpm(local)</p>
</td>
</tr>
<tr id="row18237111091810"><td class="cellrowborder" valign="top"><p id="p19237201061810"><a name="p19237201061810"></a><a name="p19237201061810"></a>Ubuntu 16.04 64bit</p>
</td>
<td class="cellrowborder" valign="top"><p id="p22377102188"><a name="p22377102188"></a><a name="p22377102188"></a>Linux</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1723716105187"><a name="p1723716105187"></a><a name="p1723716105187"></a>x86_64</p>
</td>
<td class="cellrowborder" valign="top"><p id="p122371810161813"><a name="p122371810161813"></a><a name="p122371810161813"></a>Ubuntu</p>
</td>
<td class="cellrowborder" valign="top"><p id="p12237191021820"><a name="p12237191021820"></a><a name="p12237191021820"></a>16.04</p>
</td>
<td class="cellrowborder" valign="top"><p id="p1323791018187"><a name="p1323791018187"></a><a name="p1323791018187"></a>deb(local)</p>
</td>
</tr>
</tbody>
</table>

## 安装CUDA工具包<a name="section16590173051016"></a>

1.  登录GPU弹性云服务器；

1.  在CUDA下载页面中，按照[表1](#table1925059201814)中的对应的索引项在页面中进行选择。

    以下操作以P2v实例使用Ubuntu 16.04 64bit安装CUDA 9.2为例

    **图 1**  选择CUDA版本<a name="fig562652218515"></a>  
    ![](figures/选择CUDA版本.jpg "选择CUDA版本")

2.  选择完成后，页面会自动呈现出Ubuntu 16.04 64bit对应的CUDA 9.2的下载地址按钮。

    **图 2**  下载CUDA<a name="fig15627111532512"></a>  
    ![](figures/下载CUDA.jpg "下载CUDA")

3.  下载CUDA工具包
    -   如果是windows虚拟机，直接点击Download按钮进行下载
    -   如果是linux虚拟机，浏览器中右键点击“复制链接地址”，然后在云服务器内部执行如下命令进行下载。

        **wget \[复制的链接地址\]**

        **图 3**  Linux云服务器下载CUDA<a name="fig14997193842510"></a>  
        ![](figures/Linux云服务器下载CUDA.jpg "Linux云服务器下载CUDA")


4.  待CUDA工具包下载完成后，按照NVIDIA官网安装指引进行安装
    -   如果是Windows虚拟机，双击打开exe文件，然后按照安装指引进行安装。
    -   如果是Linux虚拟机，按照如下图的NVIDIA官网的Installation Instructions进行安装。

        **图 4**  Linux云服务器安装CUDA<a name="fig729191813264"></a>  
        ![](figures/Linux云服务器安装CUDA.jpg "Linux云服务器安装CUDA")

        执行以下命令安装CUDA。

        **sudo dpkg -i cuda-repo-ubuntu1604-9-2-local\_9.2.148-1\_amd64.deb**

        **sudo apt-key add /var/cuda-repo-9-2/7fa2af80.pub**

        **sudo apt-get update**

        **sudo apt-get install cuda**

        **图 5**  安装CUDA回显01<a name="fig915411911720"></a>  
        ![](figures/安装CUDA回显01.jpg "安装CUDA回显01")

        **图 6**  安装CUDA回显02<a name="fig17971154341716"></a>  
        ![](figures/安装CUDA回显02.jpg "安装CUDA回显02")



