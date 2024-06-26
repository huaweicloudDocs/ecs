# 远程登录Linux弹性云服务器（SSH密码方式）<a name="ZH-CN_TOPIC_0017955633"></a>

## 操作场景<a name="section193261132111117"></a>

本节操作介绍在Windows和Linux环境中使用SSH密码方式远程登录Linux云服务器的操作步骤。

## 前提条件<a name="section58260650112020"></a>

-   弹性云服务器状态为“运行中”。
-   弹性云服务器已经绑定弹性公网IP，绑定方式请参见[绑定弹性公网IP](绑定弹性公网IP.md)。

-   所在安全组入方向已开放22端口，配置方式请参见[配置安全组规则](配置安全组规则.md)。
-   使用的登录工具（如PuTTY）与待登录的弹性云服务器之间网络连通。例如，默认的22端口没有被防火墙屏蔽。

## 本地使用Windows操作系统<a name="section62068112020"></a>

如果本地主机为Windows操作系统，可以按照下面方式登录云服务器。

下面步骤以PuTTY为例。

1.  在以下路径中下载PuTTY和PuTTYgen。

    [https://www.chiark.greenend.org.uk/\~sgtatham/putty/latest.html](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)

2.  运行PuTTY。
3.  单击“Session”。
    1.  Host Name \(or IP address\)：输入云服务器的弹性公网IP。
    2.  Port：输入 22。
    3.  Connection Type：选择 SSH。
    4.  Saved Sessions：任务名称，在下一次使用putty时就可以单击保存的任务名称，即可打开远程连接。

        **图 1**  单击“Session”<a name="fig74247114018"></a>  
        ![](figures/单击-Session.png "单击-Session")

4.  单击“Window”，在“Translation”下的“Received data assumed to be in which character set:”选择“UTF-8”。
5.  单击“Open”。

    如果首次登录服务器，PuTTY会显示安全警告对话框，询问是否接受服务器的安全证书。单击“是”将证书保存到本地注册表中。

6.  建立到云服务器的SSH连接后，根据提示输入用户名和密码登录云服务器。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >如果是公共镜像（包括CoreOS），首次登录时，登录用户名、密码如下：
    >-   用户名：root
    >-   密码：购买云服务器时，您设置的密码
    >    若购买时云服务器未设置密码，请参考[在控制台重置弹性云服务器密码](在控制台重置弹性云服务器密码.md)进行设置。

## 本地使用Linux操作系统<a name="section20811823174313"></a>

如果本地主机为Linux操作系统，您可以在计算机的命令行中通过以下操作登录弹性云服务器。

1.  在您的linux计算机的命令行中执行如下命令，登录弹性云服务器。

    **ssh** _**xx.xx.xx.xx**_

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >xx.xx.xx.xx表示弹性云服务器绑定的弹性公网IP。

2.  根据界面提示信息，验证远程主机SSH指纹，并输入“yes”。

    ```
    The authenticity of host 'xx.xx.xx.xx (xx.xx.xx.xx)' can't be established.
    ECDSA key fingerprint is SHA256:rnKuzrUSYS03MCoaxxxxxxxxxxxxxxxxxxxxxxxxxxx.
    ECDSA key fingerprint is MD5:cf:64:5b:5e:74:30:xx:xx:xx:xx:xx:xx:xx:xx:xx:xx.
    Are you sure you want to continue connecting (yes/no)? yes                
    Warning: Permanently added 'xx.xx.xx.xx' (ECDSA) to the list of known hosts.
    ```

3.  根据界面提示，输入待登录的弹性云服务器的密码，完成登录操作。

    ```
    root@xx.xx.xx.xx's password: 
    
            Welcome to Huawei Cloud Service
    ```

## 相关链接<a name="section2826432183510"></a>

-   [忘记密码怎么办？](密码使用场景介绍.md)
-   [无法登录到Linux云服务器怎么办？](https://support.huaweicloud.com/ecs_faq/zh-cn_topic_0105127983.html)

