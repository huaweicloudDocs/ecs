# pip安装包或wget下载包时下载速度很慢<a name="ZH-CN_TOPIC_0107490388"></a>

## 问题描述<a name="section4323119112812"></a>

使用wget命令下载软件包时，下载速度远远小于带宽大小，如[图1](#fig17394493307)所示。

**图 1**  wget下载包<a name="fig17394493307"></a>  
![](figures/wget下载包.png "wget下载包")

## 问题原因<a name="section16898143618318"></a>

pip官方网站是用https来访问的，每次使用pip安装python第三方模块的时候，pip首先要在官网下载相应模块的源码包，然后再对其进行安装，所以需要openssl相关包。

## 处理方法<a name="section2477445336"></a>

执行以下命令，安装openssl相关包。

**yum install openssl openssl-devel**

