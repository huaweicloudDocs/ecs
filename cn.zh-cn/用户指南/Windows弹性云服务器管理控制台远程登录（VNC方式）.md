# Windows弹性云服务器管理控制台远程登录（VNC方式）<a name="ZH-CN_TOPIC_0027290684"></a>

## 操作场景<a name="section72402524547"></a>

本节为您介绍如何通过控制台提供的远程登录功能（即VNC方式）登录到弹性云服务器上。

## 前提条件<a name="section1641012498356"></a>

如果您的弹性云服务器是采用密钥方式鉴权，请在登录前先使用密钥文件解析登录密码。密钥文件解析密码请参考[获取Windows弹性云服务器的密码](获取Windows弹性云服务器的密码.md)。

## 登录Windows弹性云服务器<a name="section34668256111127"></a>

1.  登录管理控制台。
2.  单击管理控制台左上角的![](figures/icon-region.png)，选择区域和项目。
3.  选择“计算 \> 弹性云服务器”。
4.  获取弹性云服务器密码。

    VNC方式登录弹性云服务器时，需已知其密码，然后再采用VNC方式登录。

    -   当您的弹性云服务器是采用密码方式鉴权时，请直接使用创建云服务器时设置的密码进行登录。
    -   当您的弹性云服务器是采用密钥方式鉴权时，密码获取方式请参见[获取Windows弹性云服务器的密码](获取Windows弹性云服务器的密码.md)。

5.  选择要登录的弹性云服务器，单击“操作”列下的“远程登录”。

    **图 1**  远程登录<a name="fig02125113112"></a>  
    ![](figures/远程登录.png "远程登录")

6.  在弹出的“登录Windows弹性云服务器”窗口中，选择“其他方式（VNC）”单击“立即登录”。
7.  （可选）如果界面提示“Press CTRL+ALT+DELETE to log on”，请单击远程登录操作面板上方的“Ctrl+Alt+Del”按钮进行登录。

    **图 2**  单击“Send Ctrl+Alt+Del”<a name="fig1380012985917"></a>  
    ![](figures/单击-Send-Ctrl+Alt+Del.png "单击-Send-Ctrl+Alt+Del")

8.  （可选）登录G1型弹性云服务器时，远程登录界面上无法显示鼠标。此时，需单击远程登录操作面板上方的“Local Crusor”按钮，鼠标就可以正常显示了。

    **图 3**  Local Crusor<a name="zh-cn_topic_0027268511_fig11301616132218"></a>  
    ![](figures/Local-Crusor.png "Local-Crusor")

9.  根据界面提示，输入弹性云服务器密码。

## 相关链接<a name="section2826432183510"></a>

-   [忘记密码怎么办？](重置密码使用场景介绍.md)
-   [Windows云服务器如何配置多用户登录？](https://support.huaweicloud.com/trouble-ecs/ecs_trouble_0900.html)
-   [无法登录到Windows云服务器怎么办？](https://support.huaweicloud.com/ecs_faq/zh-cn_topic_0018073217.html)

