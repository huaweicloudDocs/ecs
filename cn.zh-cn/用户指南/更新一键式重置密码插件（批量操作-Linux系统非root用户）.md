# 更新一键式重置密码插件（批量操作-Linux系统非root用户）<a name="ecs_03_1010"></a>

## 操作场景<a name="zh-cn_topic_0000001238762193_ecs_03_0187_section18362920155819"></a>

当您需要对多台Linux系统的云服务器批量更新一键式重置密码插件时，可参考本文档操作。

## 前提条件<a name="zh-cn_topic_0000001238762193_section148505353295"></a>

-   登录已准备好的执行机，执行机需满足的条件请参见[约束与限制](#zh-cn_topic_0000001238762193_ecs_03_0187_section19369162055818)。
-   需要提前准备待批量安装插件的云服务器的IP地址、root用户的密码信息以及非root用户的密码信息。
-   执行机应该与待更新机器在同一VPC下。
-   在执行完步骤[7](#zh-cn_topic_0000001238762193_li1740314273362)之后可以解绑eip。

## 约束与限制<a name="zh-cn_topic_0000001238762193_ecs_03_0187_section19369162055818"></a>

-   需要选取一台操作系统为CentOS 7（公共镜像）且已绑定弹性公网IP的云服务器作为执行机，且与待批量安装插件的弹性云服务器之间网络需要互通。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >若已配置yum内部源，可不需要绑定弹性公网IP。

-   同一批执行机的非root用户的帐号名称必须相同。

## 操作步骤<a name="zh-cn_topic_0000001238762193_ecs_03_0187_section1837542012588"></a>

1.  执行以下命令，安装批量脚本运行所需要的依赖。

    **yum install ansible –y**

2.  请参考[获取并校验一键式重置密码插件完整性（Linux）](获取一键式重置密码插件.md#section15564103103311)，下载对应的一键式重置密码插件CloudResetPwdAgent.zip并完成完整性校验。

    安装一键式重置密码插件对插件的具体放置目录无特殊要求，请您自定义。

3.  执行以下命令，将批量操作脚本下载到root目录下。

    **curl  _URL_  \> \~/batch\_update\_log4j\_version\_for\_all\_user.py**

    其中，_URL_为批量操作的执行脚本。

    请根据云服务器所在区域选择脚本的下载地址：

    -   华北-北京一：[https://cn-north-1-cloud-reset-pwd.obs.cn-north-1.myhuaweicloud.com/linux/batch\_update\_resetpwd/batch\_update\_log4j\_version\_for\_all\_user.py](https://cn-north-1-cloud-reset-pwd.obs.cn-north-1.myhuaweicloud.com/linux/batch_update_resetpwd/batch_update_log4j_version_for_all_user.py)
    -   华北-北京四：[https://cn-north-4-cloud-reset-pwd.obs.cn-north-4.myhuaweicloud.com/linux/batch\_update\_resetpwd/batch\_update\_log4j\_version\_for\_all\_user.py](https://cn-north-4-cloud-reset-pwd.obs.cn-north-4.myhuaweicloud.com/linux/batch_update_resetpwd/batch_update_log4j_version_for_all_user.py)
    -   华东-上海二：[https://cn-east-2-cloud-reset-pwd.obs.cn-east-2.myhuaweicloud.com/linux/batch\_update\_resetpwd/batch\_update\_log4j\_version\_for\_all\_user.py](https://cn-east-2-cloud-reset-pwd.obs.cn-east-2.myhuaweicloud.com/linux/batch_update_resetpwd/batch_update_log4j_version_for_all_user.py)
    -   华南-广州：[https://cn-south-1-cloud-reset-pwd.obs.cn-south-1.myhuaweicloud.com/linux/batch\_update\_resetpwd/batch\_update\_log4j\_version\_for\_all\_user.py](https://cn-south-1-cloud-reset-pwd.obs.cn-south-1.myhuaweicloud.com/linux/batch_update_resetpwd/batch_update_log4j_version_for_all_user.py)
    -   中国-香港：[https://ap-southeast-1-cloud-reset-pwd.obs.ap-southeast-1.myhuaweicloud.com/linux/batch\_update\_resetpwd/batch\_update\_log4j\_version\_for\_all\_user.py](https://ap-southeast-1-cloud-reset-pwd.obs.ap-southeast-1.myhuaweicloud.com/linux/batch_update_resetpwd/batch_update_log4j_version_for_all_user.py)
    -   亚太-曼谷：[https://ap-southeast-2-cloud-reset-pwd.obs.ap-southeast-2.myhuaweicloud.com/linux/batch\_update\_resetpwd/batch\_update\_log4j\_version\_for\_all\_user.py](https://ap-southeast-2-cloud-reset-pwd.obs.ap-southeast-2.myhuaweicloud.com/linux/batch_update_resetpwd/batch_update_log4j_version_for_all_user.py)

4.  执行以下命令，将更新插件脚本下载到root目录下。

    **curl  _URL_  \> \~/update\_log4j\_version\_for\_resetpwdagent\_all\_user.sh**

    其中，_URL_为更新插件脚本的下载地址。

    请根据云服务器所在区域选择脚本的下载地址：

    -   华北-北京一：[https://cn-north-1-cloud-reset-pwd.obs.cn-north-1.myhuaweicloud.com/linux/batch\_update\_resetpwd/update\_log4j\_version\_for\_resetpwdagent\_all\_user.sh](https://cn-north-1-cloud-reset-pwd.obs.cn-north-1.myhuaweicloud.com/linux/batch_update_resetpwd/update_log4j_version_for_resetpwdagent_all_user.sh)
    -   华北-北京四：[https://cn-north-4-cloud-reset-pwd.obs.cn-north-4.myhuaweicloud.com/linux/batch\_update\_resetpwd/update\_log4j\_version\_for\_resetpwdagent\_all\_user.sh](https://cn-north-4-cloud-reset-pwd.obs.cn-north-4.myhuaweicloud.com/linux/batch_update_resetpwd/update_log4j_version_for_resetpwdagent_all_user.sh)
    -   华东-上海二：[https://cn-east-2-cloud-reset-pwd.obs.cn-east-2.myhuaweicloud.com/linux/batch\_update\_resetpwd/update\_log4j\_version\_for\_resetpwdagent\_all\_user.sh](https://cn-east-2-cloud-reset-pwd.obs.cn-east-2.myhuaweicloud.com/linux/batch_update_resetpwd/update_log4j_version_for_resetpwdagent_all_user.sh)
    -   华南-广州：[https://cn-south-1-cloud-reset-pwd.obs.cn-south-1.myhuaweicloud.com/linux/batch\_update\_resetpwd/update\_log4j\_version\_for\_resetpwdagent\_all\_user.sh](https://cn-south-1-cloud-reset-pwd.obs.cn-south-1.myhuaweicloud.com/linux/batch_update_resetpwd/update_log4j_version_for_resetpwdagent_all_user.sh)
    -   中国-香港：[https://ap-southeast-1-cloud-reset-pwd.obs.ap-southeast-1.myhuaweicloud.com/linux/batch\_update\_resetpwd/update\_log4j\_version\_for\_resetpwdagent\_all\_user.sh](https://ap-southeast-1-cloud-reset-pwd.obs.ap-southeast-1.myhuaweicloud.com/linux/batch_update_resetpwd/update_log4j_version_for_resetpwdagent_all_user.sh)
    -   亚太-曼谷：[https://ap-southeast-2-cloud-reset-pwd.obs.ap-southeast-2.myhuaweicloud.com/linux/batch\_update\_resetpwd/update\_log4j\_version\_for\_resetpwdagent\_all\_user.sh](https://ap-southeast-2-cloud-reset-pwd.obs.ap-southeast-2.myhuaweicloud.com/linux/batch_update_resetpwd/update_log4j_version_for_resetpwdagent_all_user.sh)

5.  <a name="zh-cn_topic_0000001238762193_li1740314273362"></a>检查如下脚本是否在root目录下：
    -   batch\_update\_log4j\_version\_for\_all\_user.py
    -   update\_log4j\_version\_for\_resetpwdagent\_all\_user.sh
    -   CloudResetPwdAgent.zip

6.  执行以下命令，新建并编辑host\_list.txt，按i进入编辑模式。

    **vi host\_list.txt**

    将需要自动安装驱动的云服务器的相关信息填写到host\_list.txt文件中。

    填写非root用户（以fspuser为例）的IP和密码，请严格按照“**IP,用户密码**”的格式填写，中间以英文逗号隔开。

    示例：

    ```
    [fspuser]
    192.168.1.10,'**********'
    192.168.1.11,'**********'
    ```

7.  执行以下命令，新建并编辑root\_pass.txt，按i进入编辑模式。

    **vi root\_pass.txt**

    将需要自动安装驱动的云服务器的root用户密码信息填写到root\_pass.txt文件中。

    填写root用户的IP和密码，请严格按照“**IP,用户密码**”的格式填写，中间以英文逗号隔开。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >root\_pass.txt文件中的IP请填写私有IP地址。

    示例：

    ```
    [root]
    192.168.1.10,'**********'
    192.168.1.11,'**********'
    ```

8.  运行批量执行操作脚本“batch\_update\_log4j\_version\_for\_all\_user.py”。

    **python batch\_update\_log4j\_version\_for\_all\_user.py**

    **图 1**  运行脚本<a name="zh-cn_topic_0000001238762193_fig2583720175813"></a>  
    ![](figures/运行脚本-29.png "运行脚本-29")

9.  执行如下命令，在“/root/logs/exec\_origin.log”的最后一行查看运行结果日志。

    **vim /root/logs/exec\_origin.log**

    若如[图2](#zh-cn_topic_0000001238762193_fig11117142718453)所示，则表示运行成功。

    **图 2**  运行成功<a name="zh-cn_topic_0000001238762193_fig11117142718453"></a>  
    ![](figures/运行成功-30.png "运行成功-30")


