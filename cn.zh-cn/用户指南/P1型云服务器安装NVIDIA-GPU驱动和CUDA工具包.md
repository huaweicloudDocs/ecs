# P1型云服务器安装NVIDIA GPU驱动和CUDA工具包<a name="ZH-CN_TOPIC_0093345963"></a>

## 操作场景<a name="section671317415422"></a>

使用私有镜像创建的P1型弹性云服务器，请确认在制作私有镜像时已安装NVIDIA驱动。如果未安装，需在P1型云服务器创建完成后进行驱动安装，实现计算加速功能。对于其他类型弹性云服务器，无需执行本操作，创建成功后是否需要安装相关驱动，具体请以[实例和应用场景](http://support.huaweicloud.com/productdesc-ecs/zh-cn_topic_0035470096.html)章节的“使用须知”为准。

## 前提条件<a name="section073732576"></a>

-   已绑定弹性公网IP。
-   已根据[表1](#table16574141765514)，下载对应操作系统所需驱动的安装包。

**表 1**  NVIDIA驱动下载

<a name="table16574141765514"></a>
<table><thead align="left"><tr id="row85812017155513"><th class="cellrowborder" valign="top" width="17%" id="mcps1.2.4.1.1"><p id="p1018825145513"><a name="p1018825145513"></a><a name="p1018825145513"></a>需要下载的驱动</p>
</th>
<th class="cellrowborder" valign="top" width="32%" id="mcps1.2.4.1.2"><p id="p19587191710551"><a name="p19587191710551"></a><a name="p19587191710551"></a>安装包名称</p>
</th>
<th class="cellrowborder" valign="top" width="51%" id="mcps1.2.4.1.3"><p id="p10589141755518"><a name="p10589141755518"></a><a name="p10589141755518"></a>下载地址</p>
</th>
</tr>
</thead>
<tbody><tr id="row9592141711559"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.1 "><p id="p20626154685513"><a name="p20626154685513"></a><a name="p20626154685513"></a>GPU驱动</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.4.1.2 "><p id="p13597111716554"><a name="p13597111716554"></a><a name="p13597111716554"></a>NVIDIA-Linux-x86_64-375.66.run</p>
</td>
<td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.3 "><p id="p359918174554"><a name="p359918174554"></a><a name="p359918174554"></a><a href="http://www.nvidia.com/download/driverResults.aspx/118955/en-us" target="_blank" rel="noopener noreferrer">http://www.nvidia.com/download/driverResults.aspx/118955/en-us</a></p>
</td>
</tr>
<tr id="row18601171712555"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.1 "><p id="p362634625512"><a name="p362634625512"></a><a name="p362634625512"></a>CUDA Toolkit</p>
</td>
<td class="cellrowborder" valign="top" width="32%" headers="mcps1.2.4.1.2 "><p id="p660320178554"><a name="p660320178554"></a><a name="p660320178554"></a>cuda_8.0.61_375.26_linux.run</p>
</td>
<td class="cellrowborder" valign="top" width="51%" headers="mcps1.2.4.1.3 "><p id="p14605517155515"><a name="p14605517155515"></a><a name="p14605517155515"></a><a href="https://developer.nvidia.com/compute/cuda/8.0/Prod2/local_installers/cuda_8.0.61_375.26_linux-run" target="_blank" rel="noopener noreferrer">https://developer.nvidia.com/compute/cuda/8.0/Prod2/local_installers/cuda_8.0.61_375.26_linux-run</a></p>
</td>
</tr>
</tbody>
</table>

## 操作步骤<a name="section146153428432"></a>

1.  登录P1型弹性云服务器，并执行以下命令，切换至root权限。

    **sudo su**

2.  安装NVIDIA驱动的依赖包gcc和g++。
    -   对于Ubuntu 16.04 64bit，执行以下命令：

        **sudo** **apt-get install gcc**

        **sudo apt-get install g++**

        **sudo apt-get install make**

    -   对于CentOS 7.3，无需执行该操作。
    -   对于Debian 8.0，执行以下命令：

        **sudo** **apt-get install gcc**

        **sudo apt-get install g++**

        **sudo apt-get install make**

        **sudo apt-get install linux-headers-$\(uname -r\)**


3.  （可选）禁用Nouveau驱动。

    如果弹性云服务器安装了Nouveau驱动，为避免安装NVIDIA驱动时发生冲突，需先禁用。

    1.  执行以下命令，查看弹性云服务器是否安装Nouveau驱动。

        **lsmod | grep nouveau**

        -   是，执行[3.b](#li2691446193813)。
        -   否，执行[4](#li7971016194610)。

    2.  <a name="li2691446193813"></a>将如下语句添加至文件“/etc/modprobe.d/blacklist-nouveau.conf“的末尾。如果没有该文件，请新建一个。

        **blacklist nouveau**

        **options nouveau modeset=0**

    3.  执行以下命令，重新生成一个initramfs。

        **update-initramfs -u**

    4.  执行以下命令，重启弹性云服务器。

        **reboot**


4.  <a name="li7971016194610"></a>（可选）关闭X服务。

    如果弹性云服务器当前为图形化界面，为避免安装NVIDIA驱动时发生冲突，需先关闭X服务。

    1.  执行以下命令，切换至多用户模式。

        **systemctl set-default multi-user.target**

    2.  执行以下命令，重启弹性云服务器。

        **reboot**


5.  （可选）安装GPU驱动。

    您可以使用CUDA Toolkit安装包中自带的GPU驱动，或者单独下载配套的GPU驱动版本。如无特殊要求，推荐您安装[前提条件](#section073732576)中提供的GPU驱动版本“NVIDIA-Linux-x86\_64-375.66.run”，该版本已经过充分验证。

    下载并安装GPU驱动的通用方法如下：

    1.  将下载的GPU驱动安装包“NVIDIA-Linux-x86\_64-_xxx.yy_.run”上传到弹性云服务器的“/tmp”目录下。

        其中，驱动下载地址：[http://www.nvidia.com/Download/index.aspx?lang=en](http://www.nvidia.com/Download/index.aspx?lang=en)

        **图 1**  下载GPU驱动<a name="fig3284155103612"></a>  
        ![](figures/下载GPU驱动.png "下载GPU驱动")

    2.  执行以下命令，安装GPU驱动。

        **sh ./NVIDIA-Linux-x86\_64-_xxx.yy_.run**

    3.  执行以下命令，删除压缩包。

        **rm -f NVIDIA-Linux-x86\_64-_xxx.yy_.run**


6.  安装CUDA Toolkit。

    如无特殊要求，推荐您安装[前提条件](#section073732576)中提供的CUDA Toolkit版本“cuda\_8.0.61\_375.26\_linux.run”，该版本已经过充分验证。

    下载并安装CUDA Toolkit的通用方法如下：

    1.  将下载的CUDA Toolkit安装包“cuda\__a.b.cc_\__xxx.yy_\_linux.run”上传到弹性云服务器的“/tmp”目录下。

        其中，CUDA Toolkit下载地址：[https://developer.nvidia.com/cuda-downloads](https://developer.nvidia.com/cuda-downloads)

    2.  执行以下命令，修改权限。

        **chmod +x cuda\__a.b.cc_\__xxx.yy_\_linux.run**

    3.  执行以下命令，安装CUDA Toolkit。

        **./cuda\__a.b.cc_\__xxx.yy_\_linux.run -toolkit -samples -silent -override --tmpdir=/tmp/**

    4.  执行以下命令，删除压缩包。

        **rm -f cuda\__a.b.cc_\__xxx.yy_\_linux.run**

    5.  执行如下三条命令，验证是否安装成功。

        **cd /usr/local/cuda/samples/1\_Utilities/deviceQueryDrv/**

        **make**

        **./deviceQueryDrv**

        回显信息中包含“Result = PASS”，表示CUDA Toolkit和GPU驱动安装成功。

        ```
        ./deviceQueryDrv Starting...  
           
         CUDA Device Query (Driver API) statically linked version   
         Detected 1 CUDA Capable device(s)  
           
         Device 0: "Tesla P100-PCIE-16GB"  
           CUDA Driver Version:                           8.0  
           CUDA Capability Major/Minor version number:    6.0  
           Total amount of global memory:                 16276 MBytes (17066885120 bytes)  
           (56) Multiprocessors, ( 64) CUDA Cores/MP:     3584 CUDA Cores  
           GPU Max Clock rate:                            1329 MHz (1.33 GHz)  
           Memory Clock rate:                             715 Mhz  
           Memory Bus Width:                              4096-bit  
           L2 Cache Size:                                 4194304 bytes  
           Max Texture Dimension Sizes                    1D=(131072) 2D=(131072, 65536) 3D=(16384, 16384, 16384)  
           Maximum Layered 1D Texture Size, (num) layers  1D=(32768), 2048 layers  
           Maximum Layered 2D Texture Size, (num) layers  2D=(32768, 32768), 2048 layers  
           Total amount of constant memory:               65536 bytes  
           Total amount of shared memory per block:       49152 bytes  
           Total number of registers available per block: 65536  
           Warp size:                                     32  
           Maximum number of threads per multiprocessor:  2048  
           Maximum number of threads per block:           1024  
           Max dimension size of a thread block (x,y,z): (1024, 1024, 64)  
           Max dimension size of a grid size (x,y,z):    (2147483647, 65535, 65535)  
           Texture alignment:                             512 bytes  
           Maximum memory pitch:                          2147483647 bytes  
           Concurrent copy and kernel execution:          Yes with 2 copy engine(s)  
           Run time limit on kernels:                     No  
           Integrated GPU sharing Host Memory:            No  
           Support host page-locked memory mapping:       Yes  
           Concurrent kernel execution:                   Yes  
           Alignment requirement for Surfaces:            Yes  
           Device has ECC support:                        Enabled  
           Device supports Unified Addressing (UVA):      Yes  
           Device PCI Domain ID / Bus ID / location ID:   0 / 0 / 6  
           Compute Mode:  
              < Default (multiple host threads can use ::cudaSetDevice() with device simultaneously) >  
         Result = PASS 
        ```



