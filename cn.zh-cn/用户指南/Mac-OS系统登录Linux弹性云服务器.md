# Mac OS系统登录Linux弹性云服务器<a name="ecs_03_0194"></a>

## 操作场景<a name="section4777132715121"></a>

本节为您介绍如何在Mac OS系统主机上登录Linux云服务器。

## 前提条件<a name="section796403214133"></a>

-   云服务器状态为“运行中”。
-   已获取Linux云服务器用户名和密码。忘记密码请参考[在控制台重置弹性云服务器密码](在控制台重置弹性云服务器密码.md)重置密码。
-   弹性云服务器已经绑定弹性公网IP，绑定方式请参见[绑定弹性公网IP](绑定弹性公网IP.md)。

-   所在安全组入方向已开放3389端口，配置方式请参见[配置安全组规则](配置安全组规则.md)。

## 操作步骤<a name="section13366111713156"></a>

您可以通过Mac OS系统自带的终端（Terminal）登录Linux云服务器。

-   SSH密码方式
    1.  打开系统自带的终端（Terminal），执行以下命令，登录云服务器。

        **ssh** _**用户名**_**@_弹性公网IP_**

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >如果是公共镜像（包括CoreOS），用户名为“root”。


-   SSH密钥方式
    1.  打开系统自带的终端（Terminal），执行以下命令，变更权限。下面步骤以私钥文件是kp-123.pem为例进行介绍。

        **chmod 400 /_path_/kp-123.pem**

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >上述命令的path为密钥文件的存放路径。

    2.  执行以下命令，登录云服务器。

        **ssh -i** **/_path_/kp-123.pem** _**用户名**_**@_弹性公网IP_**

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >-   如果是“CoreOS”的公共镜像，用户名为“core”。
        >-   如果是“非CoreOS”的公共镜像，用户名为“root”。



## 后续处理<a name="section51158488121525"></a>

-   以SSH密钥方式登录弹性云服务器后，可以通过设置密码（执行**passwd**命令），后续使用VNC方式登录Linux弹性云服务器。

