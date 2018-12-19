# 重置Windows弹性云服务器的密码<a name="ZH-CN_TOPIC_0021426802"></a>

## 前提条件<a name="section1344819634213"></a>

-   准备一台Linux操作系统的临时弹性云服务器，建议操作系统为Ubuntu14.04以上版本，且该临时弹性云服务器与待重置密码的弹性云服务器位于同一个可用区。
-   临时弹性云服务器已经绑定弹性公网IP，并配置系统apt-get源。
-   通过下面的方法，在临时弹性云服务器中安装ntfs-3g和chntpw软件包。

    方法一：

    执行以下命令，安装ntfs-3g和chntpw软件包。

    **sudo apt-get install ntfs-3g chntpw**

    方法二：

    根据临时弹性云服务器的操作系统版本，下载对应版本的ntfs-3g和chntpw软件包进行安装，详细的安装与使用指导，请参见[NTFS官网资料](http://www.tuxera.com/community/open-source-ntfs-3g/)和[chntpw官网资料](http://www.chntpw.com/reset-windows-7-admin-password-with-ubuntu/)。

    ntfs-3g获取地址：[www.tuxera.com/community/open-source-ntfs-3g/](http://www.tuxera.com/community/open-source-ntfs-3g/)。

    chntpw获取地址：[https://pkgs.org/download/chntpw](https://pkgs.org/download/chntpw)。


## 操作步骤<a name="section1052621215437"></a>

1.  关闭原弹性云服务器，卸载系统盘，并将其挂载至临时弹性云服务器上。
    1.  登录管理控制台。
    2.  选择“计算 \> 弹性云服务器”。
    3.  原Windows弹性云服务器关机，并进入其详情页，选择“云硬盘”页签。

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >原Windows弹性云服务器关机时，请勿执行强制关机操作，否则可能引起重置密码操作失败。  

    4.  <a name="li49674320202157"></a>单击系统盘所在行的“卸载”，卸载系统盘。
    5.  展开临时弹性云服务器的详情页，并选择“云硬盘”页签。
    6.  <a name="li32570973202157"></a>单击“挂载磁盘”，在“挂载磁盘”对话框中，选择[1.d](#li49674320202157)中卸载的系统盘，并将其挂载到临时弹性云服务器上。

2.  远程登录临时弹性云服务器，挂载磁盘。
    1.  <a name="li20334892202157"></a>执行以下命令，查看卸载的系统盘在临时弹性云服务器上的目录。

        **fdisk -l**

    2.  执行以下命令，将卸载的系统盘的文件系统挂载到临时弹性云服务器上。

        **mount -t ntfs-3g /dev/**_[2.a](#li20334892202157)__**的查询结果**_ **/mnt/**

        例如，[2.a](#li20334892202157)的查询结果为“xvde2”：

        **mount -t ntfs-3g /dev/xvde2 /mnt/**


3.  修改密码，并清除原始密码。
    1.  执行以下命令，备份SAM文件。

        **cp /mnt/Windows/System32/config/SAM /mnt/Windows/System32/config/SAM.bak**

    2.  执行以下命令，修改指定用户密码。

        **chntpw -u** **Administrator /mnt/Windows/System32/config/SAM**

    3.  按照系统提示，依次输入“1”、“q”和“y”，按“Enter”。

        系统包含如下回显信息时，表示密码清除成功。

        ```
        Select: [q] > 1
        Password cleared!
        
        Hives that have changed:
        #Name
        0<SAM>
        Write hive files? (y/n) [n] : y
        0<SAM> - OK
        ```


4.  关闭临时弹性云服务器，卸载原弹性云服务器的系统盘，并将其挂载回原弹性云服务器。
    1.  临时弹性云服务器关机，并进入详情页，选择“云硬盘”页签。
    2.  <a name="li46368402202157"></a>单击“卸载”，卸载[1.f](#li32570973202157)中临时挂载的数据盘。
    3.  展开原Windows弹性云服务器的详情页，选择“云硬盘”页签。
    4.  单击“挂载磁盘”，在“挂载磁盘”对话框中，选择[4.b](#li46368402202157)中卸载的数据盘，并选择挂载点为“/dev/sda”。

5.  开启原Windows弹性云服务器，设置新密码。
    1.  单击“开机”，开启原Windows弹性云服务器，待状态为“运行中”后，单击“操作”列下的“远程登录”。
    2.  单击“开始”菜单，在搜索框中输入“CMD”，按“Enter”。
    3.  执行以下命令，修改用户密码，新密码必须符合[表1](使用场景介绍.md#zh-cn_topic_0021426802_table4381109318958)。

        **net user** **Administrator** _**新密码**_



