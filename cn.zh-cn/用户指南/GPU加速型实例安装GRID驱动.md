# GPU加速型实例安装GRID驱动<a name="ZH-CN_TOPIC_0149610914"></a>

## 操作场景<a name="section18938132731610"></a>

GPU加速型实例如需使用OpenGL/DirectX/Vulcan等图形加速能力则需要安装GRID驱动并自行购买和配置使用GRID License。此外，GRID驱动配合vDWS类型License，也支持CUDA，用来满足既需要计算加速也需要图形加速的场景。

-   使用公共镜像创建的图形加速型（G系列）实例默认已安装特定版本的GRID驱动，但GRID License需自行购买和配置使用。
-   使用私有镜像创建的GPU加速型实例，则需要安装GRID驱动并自行购买和配置使用GRID License。

本节操作介绍如何安装GRID驱动，购买或者申请GRID License，以及如何配置License服务器。

安装GRID驱动操作步骤：

1.  [购买GRID License](#section1130184214229)
2.  [下载GRID驱动及License软件包](#section91244318407)
3.  [部署和配置License Server](#section19229135113439)
4.  [安装GRID驱动并配置License](#section17545653184812)

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   使用公共镜像创建的图形加速型（G系列）实例默认已安装特定版本的GRID驱动，但GRID License需自行购买和配置使用，请提前确认云服务器是否已经预装或者预装版本是否符合需求。
>-   NVIDIA支持用户申请90天试用版License。
>-   不同规格的GPU实例介绍和应用场景请参见[GPU加速型](https://support.huaweicloud.com/productdesc-ecs/ecs_01_0045.html)。

## 购买GRID License<a name="section1130184214229"></a>

-   购买License

    如果需要正式版本License，请联系NVIDIA或者所在国家/地区的NVIDIA代理商。

-   申请试用版License。

    打开[NVIDIA官方网站](https://www.nvidia.com/object/nvidia-enterprise-account.html)，填写相关信息。

    注册账号和申请试用版License的注意事项请参见[NVIDIA官方帮助页](https://nvid.nvidia.com/NvidiaUtilities/#/needHelp)。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >试用版License的使用方法和正式版本的License一致，可以保留试用版账号激活正式版本的License，无需重新注册。试用版License有限期限为90天，账号过期将无法使用，请尽快购买正式版本。

    **图 1**  申请试用版License<a name="fig45088922717"></a>  
    ![](figures/申请试用版License.png "申请试用版License")


## 下载GRID驱动及License软件包<a name="section91244318407"></a>

1.  请根据[表1](#table188851534175019)对应操作系统下载驱动安装包。

    了解更多GRID驱动信息请参考[NVIDIA vGPU驱动](https://docs.nvidia.com/grid/index.html)。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >GPU直通型实例：根据需求选择GRID驱动版本。
    >GPU虚拟化型实例：请严格按照下表选择合适的驱动版本下载使用。

    **表 1**  GPU实例类型支持的GRID驱动版本

    <a name="table188851534175019"></a>
    <table><thead align="left"><tr id="row38821334115015"><th class="cellrowborder" valign="top" width="10.601060106010602%" id="mcps1.2.6.1.1"><p id="p11882134205019"><a name="p11882134205019"></a><a name="p11882134205019"></a>实例类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.09160916091609%" id="mcps1.2.6.1.2"><p id="p15882113415507"><a name="p15882113415507"></a><a name="p15882113415507"></a>GPU挂载方式</p>
    </th>
    <th class="cellrowborder" valign="top" width="38.84388438843885%" id="mcps1.2.6.1.3"><p id="p68821634185016"><a name="p68821634185016"></a><a name="p68821634185016"></a>操作系统</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.352335233523352%" id="mcps1.2.6.1.4"><p id="p188821634185016"><a name="p188821634185016"></a><a name="p188821634185016"></a>驱动版本</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.111111111111112%" id="mcps1.2.6.1.5"><p id="p148822034135011"><a name="p148822034135011"></a><a name="p148822034135011"></a>CPU架构</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1088383418500"><td class="cellrowborder" valign="top" width="10.601060106010602%" headers="mcps1.2.6.1.1 "><p id="p988213340507"><a name="p988213340507"></a><a name="p988213340507"></a>G5</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.09160916091609%" headers="mcps1.2.6.1.2 "><p id="p5882133411506"><a name="p5882133411506"></a><a name="p5882133411506"></a>GPU虚拟化型实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.84388438843885%" headers="mcps1.2.6.1.3 "><a name="ul288211347506"></a><a name="ul288211347506"></a><ul id="ul288211347506"><li>Windows Server 2016 Standard 64bit</li><li>Windows Server 2012 R2 Standard 64bit</li><li>CentOS 7.5 64bit</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="23.352335233523352%" headers="mcps1.2.6.1.4 "><p id="p1788253412506"><a name="p1788253412506"></a><a name="p1788253412506"></a>GRID 7.1: NVIDIA vGPU for Linux KVM</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.111111111111112%" headers="mcps1.2.6.1.5 "><p id="p888233485010"><a name="p888233485010"></a><a name="p888233485010"></a>x86_64</p>
    </td>
    </tr>
    <tr id="row8883143415018"><td class="cellrowborder" valign="top" width="10.601060106010602%" headers="mcps1.2.6.1.1 "><p id="p1088343415016"><a name="p1088343415016"></a><a name="p1088343415016"></a>G3</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.09160916091609%" headers="mcps1.2.6.1.2 "><p id="p1688363495015"><a name="p1688363495015"></a><a name="p1688363495015"></a>GPU直通型实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.84388438843885%" headers="mcps1.2.6.1.3 "><a name="ul4883534185016"></a><a name="ul4883534185016"></a><ul id="ul4883534185016"><li>Windows Server 2012 R2 Standard 64bit</li><li>Windows Server 2008 R2 Enterprise SP1 64bit</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="23.352335233523352%" headers="mcps1.2.6.1.4 "><p id="p17883203435012"><a name="p17883203435012"></a><a name="p17883203435012"></a>按需选择版本</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.111111111111112%" headers="mcps1.2.6.1.5 "><p id="p2883434145012"><a name="p2883434145012"></a><a name="p2883434145012"></a>x86_64</p>
    </td>
    </tr>
    <tr id="row1688333425020"><td class="cellrowborder" valign="top" width="10.601060106010602%" headers="mcps1.2.6.1.1 "><p id="p5883234135012"><a name="p5883234135012"></a><a name="p5883234135012"></a>G1</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.09160916091609%" headers="mcps1.2.6.1.2 "><p id="p1788343411505"><a name="p1788343411505"></a><a name="p1788343411505"></a>GPU虚拟化型实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.84388438843885%" headers="mcps1.2.6.1.3 "><a name="ul6883434145013"></a><a name="ul6883434145013"></a><ul id="ul6883434145013"><li>Windows Server 2012 R2 Standard 64bit</li><li>Windows Server 2008 R2 Enterprise SP1 64bit</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="23.352335233523352%" headers="mcps1.2.6.1.4 "><p id="p13883534125016"><a name="p13883534125016"></a><a name="p13883534125016"></a>vGPU 4.1：GRID for UVP</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.111111111111112%" headers="mcps1.2.6.1.5 "><p id="p1788318343509"><a name="p1788318343509"></a><a name="p1788318343509"></a>x86_64</p>
    </td>
    </tr>
    <tr id="row18841534145013"><td class="cellrowborder" valign="top" width="10.601060106010602%" headers="mcps1.2.6.1.1 "><p id="p15883133418509"><a name="p15883133418509"></a><a name="p15883133418509"></a>P2vs</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.09160916091609%" headers="mcps1.2.6.1.2 "><p id="p1988318348507"><a name="p1988318348507"></a><a name="p1988318348507"></a>GPU直通型实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.84388438843885%" headers="mcps1.2.6.1.3 "><a name="ul1188310348506"></a><a name="ul1188310348506"></a><ul id="ul1188310348506"><li>Windows Server 2016 Standard 64bit</li><li>Ubuntu Server 16.04 64bit</li><li>CentOS 7.5 64bit</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="23.352335233523352%" headers="mcps1.2.6.1.4 "><p id="p98841134115015"><a name="p98841134115015"></a><a name="p98841134115015"></a>按需选择版本</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.111111111111112%" headers="mcps1.2.6.1.5 "><p id="p588413341503"><a name="p588413341503"></a><a name="p588413341503"></a>x86_64</p>
    </td>
    </tr>
    <tr id="row188463416506"><td class="cellrowborder" valign="top" width="10.601060106010602%" headers="mcps1.2.6.1.1 "><p id="p88847349507"><a name="p88847349507"></a><a name="p88847349507"></a>P2v</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.09160916091609%" headers="mcps1.2.6.1.2 "><p id="p78841634205014"><a name="p78841634205014"></a><a name="p78841634205014"></a>GPU直通型实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.84388438843885%" headers="mcps1.2.6.1.3 "><a name="ul188843346508"></a><a name="ul188843346508"></a><ul id="ul188843346508"><li>Windows Server 2016 Standard 64bit</li><li>Windows Server 2012 R2 Standard 64bit</li><li>Ubuntu Server 16.04 64bit</li><li>CentOS 7.4 64bit</li><li>EulerOS 2.2 64bit</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="23.352335233523352%" headers="mcps1.2.6.1.4 "><p id="p788420344509"><a name="p788420344509"></a><a name="p788420344509"></a>按需选择版本</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.111111111111112%" headers="mcps1.2.6.1.5 "><p id="p688413475015"><a name="p688413475015"></a><a name="p688413475015"></a>x86_64</p>
    </td>
    </tr>
    <tr id="row1088563415507"><td class="cellrowborder" valign="top" width="10.601060106010602%" headers="mcps1.2.6.1.1 "><p id="p168841734135014"><a name="p168841734135014"></a><a name="p168841734135014"></a>P1</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.09160916091609%" headers="mcps1.2.6.1.2 "><p id="p19884113418507"><a name="p19884113418507"></a><a name="p19884113418507"></a>GPU直通型实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.84388438843885%" headers="mcps1.2.6.1.3 "><a name="ul1888563455018"></a><a name="ul1888563455018"></a><ul id="ul1888563455018"><li>Windows Server 2012 R2 Standard 64bit</li><li>Debian 8.0 64bit</li><li>Ubuntu Server 16.04 64bit</li><li>CentOS 7.3 64bit</li><li>EulerOS 2.2 64bit</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="23.352335233523352%" headers="mcps1.2.6.1.4 "><p id="p48856342502"><a name="p48856342502"></a><a name="p48856342502"></a>按需选择版本</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.111111111111112%" headers="mcps1.2.6.1.5 "><p id="p15885203475011"><a name="p15885203475011"></a><a name="p15885203475011"></a>x86_64</p>
    </td>
    </tr>
    <tr id="row1885134185018"><td class="cellrowborder" valign="top" width="10.601060106010602%" headers="mcps1.2.6.1.1 "><p id="p288510344504"><a name="p288510344504"></a><a name="p288510344504"></a>Pi2</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.09160916091609%" headers="mcps1.2.6.1.2 "><p id="p148857346506"><a name="p148857346506"></a><a name="p148857346506"></a>GPU直通型实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.84388438843885%" headers="mcps1.2.6.1.3 "><a name="ul488523475014"></a><a name="ul488523475014"></a><ul id="ul488523475014"><li>Windows Server 2016 Standard 64bit</li><li>Ubuntu Server 16.04 64bit</li><li>CentOS 7.5 64bit</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="23.352335233523352%" headers="mcps1.2.6.1.4 "><p id="p1488593415507"><a name="p1488593415507"></a><a name="p1488593415507"></a>按需选择版本</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.111111111111112%" headers="mcps1.2.6.1.5 "><p id="p11885934165013"><a name="p11885934165013"></a><a name="p11885934165013"></a>x86_64</p>
    </td>
    </tr>
    <tr id="row48851834205018"><td class="cellrowborder" valign="top" width="10.601060106010602%" headers="mcps1.2.6.1.1 "><p id="p888523416502"><a name="p888523416502"></a><a name="p888523416502"></a>Pi1</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.09160916091609%" headers="mcps1.2.6.1.2 "><p id="p16885113414509"><a name="p16885113414509"></a><a name="p16885113414509"></a>GPU直通型实例</p>
    </td>
    <td class="cellrowborder" valign="top" width="38.84388438843885%" headers="mcps1.2.6.1.3 "><a name="ul108851734175018"></a><a name="ul108851734175018"></a><ul id="ul108851734175018"><li>Ubuntu Server 16.04 64bit</li><li>Ubuntu Server 14.04 64bit</li><li>CentOS 7.3 64bit</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="23.352335233523352%" headers="mcps1.2.6.1.4 "><p id="p198851134145013"><a name="p198851134145013"></a><a name="p198851134145013"></a>按需选择版本</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.111111111111112%" headers="mcps1.2.6.1.5 "><p id="p888510346508"><a name="p888510346508"></a><a name="p888510346508"></a>x86_64</p>
    </td>
    </tr>
    </tbody>
    </table>

2.  注册成功后，登录[NVIDIA官网](https://nvid.nvidia.com/dashboard/)，填写账户信息。
3.  判断是否为首次注册使用NVIDIA。
    1.  是，执行[4](#li1859773663819)。
    2.  否，执行[6](#li0791101412396)。

4.  <a name="li1859773663819"></a>在注册NVIDIA用户成功的邮件中，查询PAK，如[图2](#fig133361216153817)所示。

    **图 2**  注册PAK<a name="fig133361216153817"></a>  
    ![](figures/注册PAK.png "注册PAK")

5.  将[4](#li1859773663819)中查找的PAK填写在“Redeem Product Activation Keys”页面 ，并单击“Redeem”。

    **图 3**  Redeem Product Activation Keys<a name="fig16617143616380"></a>  
    ![](figures/Redeem-Product-Activation-Keys.png "Redeem-Product-Activation-Keys")

6.  <a name="li0791101412396"></a>输入“用户名”和“密码”，并单击“登录”。

    **图 4**  登录NVIDIA官网<a name="fig1367291114395"></a>  
    ![](figures/登录NVIDIA官网.png "登录NVIDIA官网")

7.  根据界面提示，进入NVIDIA门户网站，并选择“Software & Services \> Product Information”。

    **图 5**  Product Information<a name="fig028419910169"></a>  
    ![](figures/Product-Information.png "Product-Information")

8.  选择“Archived Versions”页签。
9.  对照[表1](#table188851534175019)选择相应版本的GRID驱动下载。
10. 解压缩GRID驱动包，并选择和弹性云服务器操作系统匹配的驱动进行安装。
11. 在“Product Download”页面，单击“2019.05 License Manager for Linux”，下载License软件包。

    **图 6**  选择Product Information<a name="fig13215124318392"></a>  
    ![](figures/选择Product-Information.png "选择Product-Information")


## 部署和配置License Server<a name="section19229135113439"></a>

我们以CentOS 7.5操作系统的云服务器为例演示部署和配置License Server。

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   云服务器规格不小于2vCPU，内存不小于4GB。
>-   请提前记录云服务器MAC地址。
>-   如用作生产用途，建议采用高可用模式部署，主备高可用模式部署License Server 请参考[NVIDIA官方License Server高可用部署文档](https://docs.nvidia.com/grid/ls/2019.05/grid-license-server-user-guide/index.html#license-server-high-availability)。

1.  配置网络：
    -   如使用VPC网络访问License Server：请确保License Server和使用GRID驱动的GPU加速型实例处在同一个VPC子网内。
    -   如使用公网IP访问License Server：请配置License Server所在的安全组，增加入方向规则：TCP 7070和TCP 8080。


1.  安装License Server。

    具体过程请参考[NVIDIA官方License Server安装文档](https://docs.nvidia.com/grid/ls/latest/grid-license-server-user-guide/index.html#installing-nvidia-grid-license-server)。

2.  获取License文件
    1.  新建页签，登录NVIDIA网站[http://nvid.nvidia.com/dashboard/](http://nvid.nvidia.com/dashboard/)，选择“Register License Server”。

        **图 7**  选择Register License Server<a name="fig1319854518598"></a>  
        ![](figures/选择Register-License-Server.png "选择Register-License-Server")

    2.  在MAC address栏里填入License服务器的MAC地址（MAC地址不能带“:”），单击“Create”。主备部署的情况需要把主备服务器的MAC地址都填入表格中。

        **图 8**  填写License的MAC地址<a name="fig1311314141015"></a>  
        ![](figures/填写License的MAC地址.png "填写License的MAC地址")

    3.  在View Server页面，单击“Map Add-Ons”。

        **图 9**  Map Add-Ons<a name="fig14172558038"></a>  
        ![](figures/Map-Add-Ons.png "Map-Add-Ons")

    4.  在Map Add-Ons页面，Qty to Add填入分配的数量，并单击“Map Add-Ons”。

        **图 10**  填写Qty to Add<a name="fig885115301363"></a>  
        ![](figures/填写Qty-to-Add.png "填写Qty-to-Add")

    5.  下载license文件

        **图 11**  下载license文件<a name="fig19995314613"></a>  
        ![](figures/下载license文件.png "下载license文件")

3.  在Web浏览器中，根据安装时配置的管理页面链接，访问License Server管理界面的主页。

    默认访问链接为：http://_弹性公网IP地址_:8080/licserver。

4.  单击“License Server \> License Management”，使用License服务器配置菜单导入，并单击“Upload”上传许可证\*.bin文件，完成License Server的配置。

    **图 12**  Qty to Add<a name="fig101141159980"></a>  
    ![](figures/Qty-to-Add.png "Qty-to-Add")


## 安装GRID驱动并配置License<a name="section17545653184812"></a>

1.  以Windows操作系统GPU加速型实例为例，选择合适版本的GRID驱动进行安装。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >微软的远程登录协议不支持使用GPU的3D硬件加速能力，如需使用请安装VNC/PCoIP/NICE DCV等第三方桌面协议软件，并通过相应客户端连接GPU实例，使用GPU图形图像加速能力。

2.  使用第三方桌面协议连接后，在Windows控制面板中打开NVIDIA控制面板 。
3.  在一级许可证服务器中填入部署的License server的IP和端口，并点击应用。当出现“您的系统已获GRID vGPU许可”则代表安装GRID驱动成功，并且可以在License Server管理控制台Licensed Clients中看到已安装GRID驱动并使用了License的GPU实例的MAC地址。

    **图 13**  License Server管理控制台<a name="fig7104162713349"></a>  
    ![](figures/License-Server管理控制台.png "License-Server管理控制台")


