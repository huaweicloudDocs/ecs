# pip安装软件时出现错误：command ´gcc´ failed with exit status 1<a name="ZH-CN_TOPIC_0107412162"></a>

## 问题描述<a name="section4545101482614"></a>

安装Python库软件时，需配置pip源。以中国科技大学镜像源为例：

```
[root@test home]# cat /root/.pip/pip.conf 
[global]
index-url = https://pypi.mirrors.ustc.edu.cn/simple/
trusted-host = pypi.mirrors.ustc.edu.cn
```

安装过程中，系统报错"command ´gcc´ failed with exit status 1"，如[图1](#fig15547217122815)所示。但是，在用pip安装Python库软件之前，确认已经使用yum命令安装了gcc。

**图 1**  安装报错<a name="fig15547217122815"></a>  
![](figures/安装报错.png "安装报错")

## 问题原因<a name="section2028651416307"></a>

缺少openssl-devel支持。

## 处理方法<a name="section12023073012"></a>

以安装psutil模块为例：

1.  执行以下命令，安装openssl-devel。

    **yum install gcc libffi-devel python-devel openssl-devel -y**

2.  再次使用pip安装python库软件，可以看到系统不再报错，如[图2](#fig850134793413)所示。

    **图 2**  安装成功<a name="fig850134793413"></a>  
    ![](figures/安装成功.png "安装成功")


