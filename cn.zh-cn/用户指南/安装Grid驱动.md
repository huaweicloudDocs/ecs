# 安装Grid驱动<a name="ZH-CN_TOPIC_0149610914"></a>

1.  请根据[表1](#table13692162018308)下载对应操作系统所需驱动的安装包。

    驱动下载地址：[http://www.nvidia.com/grid-eval](http://www.nvidia.com/grid-eval)

    **表 1**  GPU实例类型支持的vGPU/GRID驱动版本

    <a name="table13692162018308"></a>
    <table><thead align="left"><tr id="row2069215205305"><th class="cellrowborder" valign="top" width="22.43%" id="mcps1.2.3.1.1"><p id="p5692152019308"><a name="p5692152019308"></a><a name="p5692152019308"></a>实例类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="77.57%" id="mcps1.2.3.1.2"><p id="p6692720203012"><a name="p6692720203012"></a><a name="p6692720203012"></a>驱动版本</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row06922204302"><td class="cellrowborder" valign="top" width="22.43%" headers="mcps1.2.3.1.1 "><p id="p2692420143013"><a name="p2692420143013"></a><a name="p2692420143013"></a>G1</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.57%" headers="mcps1.2.3.1.2 "><p id="p169213208305"><a name="p169213208305"></a><a name="p169213208305"></a>vGPU 4.1：GRID for UVP</p>
    </td>
    </tr>
    <tr id="row15692102043010"><td class="cellrowborder" valign="top" width="22.43%" headers="mcps1.2.3.1.1 "><p id="p18692420113019"><a name="p18692420113019"></a><a name="p18692420113019"></a>G3</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.57%" headers="mcps1.2.3.1.2 "><p id="p1692152073018"><a name="p1692152073018"></a><a name="p1692152073018"></a>vGPU 4.1：GRID for UVP</p>
    </td>
    </tr>
    <tr id="row196927202303"><td class="cellrowborder" valign="top" width="22.43%" headers="mcps1.2.3.1.1 "><p id="p176923205308"><a name="p176923205308"></a><a name="p176923205308"></a>G5</p>
    </td>
    <td class="cellrowborder" valign="top" width="77.57%" headers="mcps1.2.3.1.2 "><p id="p156921206302"><a name="p156921206302"></a><a name="p156921206302"></a>vGPU 6.2：vGPU for Linux KVM</p>
    </td>
    </tr>
    </tbody>
    </table>

2.  判断是否为首次注册使用nvidia。
    1.  是，执行[3](#li1859773663819)。
    2.  否，执行[5](#li0791101412396)。

3.  <a name="li1859773663819"></a>在注册nvidia用户成功的邮件中，查询PAK，如[图1](#fig133361216153817)所示。

    **图 1**  注册PAK<a name="fig133361216153817"></a>  
    ![](figures/注册PAK.png "注册PAK")

4.  将[3](#li1859773663819)中查找的PAK填写在“Redeem Product Activation Keys”页面 ，并单击“Redeem”。

    **图 2**  Redeem Product Activation Keys<a name="fig16617143616380"></a>  
    ![](figures/Redeem-Product-Activation-Keys.png "Redeem-Product-Activation-Keys")

5.  <a name="li0791101412396"></a>输入“用户名”和“密码”，并单击“登录”。

    **图 3**  登录NVIDIA官网<a name="fig1367291114395"></a>  
    ![](figures/登录NVIDIA官网.png "登录NVIDIA官网")

6.  根据界面提示，进入NVIDIA门户网站，并选择“Software & Services \> Product Information”。

    **图 4**  选择Product Information<a name="fig028419910169"></a>  
    ![](figures/选择Product-Information.png "选择Product-Information")

7.  选择“Archived Versions”页签。
8.  对照[表1](#table13692162018308)选择相应版本的NVIDIA vGPU驱动下载。
9.  解压缩vGPU驱动包，并选择和云服务器操作系统匹配的驱动进行安装。

