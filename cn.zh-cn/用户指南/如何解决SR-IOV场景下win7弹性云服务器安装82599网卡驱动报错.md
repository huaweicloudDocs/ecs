# 如何解决SR-IOV场景下win7弹性云服务器安装82599网卡驱动报错？<a name="ZH-CN_TOPIC_0053287548"></a>

## 问题描述<a name="section395352320453"></a>

从Intel官网下载最新的20.4.1版本驱动包（下载地址：[https://downloadcenter.intel.com/search?keyword=Intel++Ethernet+Connections+CD](https://downloadcenter.intel.com/search?keyword=Intel++Ethernet+Connections+CD)），该版本驱动包在Windows7 64位SR-IOV直通弹性云服务器上安装时会提示“找不到英特尔适配器”错误。

## 原因分析<a name="section1422482320829"></a>

Intel 82599直通网卡在未安装驱动时被操作系统识别为以太网控制器设备，20.4.1版本驱动包在安装时未能正确识别出Intel网卡设备，导致程序报错。

## 处理方法<a name="section1276332720914"></a>

在20.4.1驱动包文件夹下运行Autorun.exe。安装驱动包前先给网卡安装驱动，使网卡被系统识别为Intel 82599 VF设备，安装驱动有两种方法。

-   方法1：通过版本更新方法安装驱动
    1.  从Intel官网下载18.6版本驱动包。
    2.  到18.6驱动包安装文件夹下运行Autorun.exe进行安装。
    3.  成功后到20.4.1版本驱动包文件夹下运行Autorun.exe更新驱动。

-   方法2：设备管理器手动安装驱动
    1.  打开Windows资源管理器，右键单击“计算机”，选择“管理”，打开“设备管理器”，在设备管理器中找到网卡，未安装驱动时，网卡位于“其他设备”一栏，名字为“以太网控制器”。
    2.  右键单击“以太网控制器”，选择“更新驱动程序软件”。
    3.  单击“浏览”，选择驱动包所在路径，单击“下一步”。
    4.  驱动安装成功后，可以在设备管理器的“网络适配器”一栏看到网卡。
    5.  单击“Autorun.exe”安装20.4.1版本一键安装驱动包。


