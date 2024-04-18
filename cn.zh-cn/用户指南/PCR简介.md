# PCR简介<a name="ecs_03_1410"></a>

QingTian Enclave的度量值是由标准可信度量运算得到的一组哈希值（Hashes）组成，这组哈希值保存在QingTian安全模块（QingTian Security Module, QTSM）的平台配置寄存器（Platform configuration registers，PCR）。

>![](public_sys-resources/icon-note.gif) **说明：** 
>QingTian Enclave度量值最多可支持32个PCR。QingTian系统占用index 0\~15的PCR，用户的Enclave应用可使用index 16\~31的PCR。
>使用debug-mode启动Enclave时，不进行镜像校验计算，QingTian系统的index 0\~15的PCR不做计算避免打印泄露。用户的Enclave应用可继续使用index 16\~31的PCR。

## 系统PCR<a name="zh-cn_topic_0000001359713190_section171527112615"></a>

<a name="zh-cn_topic_0000001359713190_table1239242172611"></a>
<table><thead align="left"><tr id="zh-cn_topic_0000001359713190_row154034222619"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0000001359713190_p41445531266"><a name="zh-cn_topic_0000001359713190_p41445531266"></a><a name="zh-cn_topic_0000001359713190_p41445531266"></a>PCR</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0000001359713190_p161443534268"><a name="zh-cn_topic_0000001359713190_p161443534268"></a><a name="zh-cn_topic_0000001359713190_p161443534268"></a>度量内容</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.1.4.1.3"><p id="zh-cn_topic_0000001359713190_p18144185332618"><a name="zh-cn_topic_0000001359713190_p18144185332618"></a><a name="zh-cn_topic_0000001359713190_p18144185332618"></a>备注</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0000001359713190_row1440104213267"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0000001359713190_p17144185382614"><a name="zh-cn_topic_0000001359713190_p17144185382614"></a><a name="zh-cn_topic_0000001359713190_p17144185382614"></a>PCR0</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0000001359713190_p1114416539261"><a name="zh-cn_topic_0000001359713190_p1114416539261"></a><a name="zh-cn_topic_0000001359713190_p1114416539261"></a>QingTian Enclave镜像文件</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0000001359713190_p1714475392613"><a name="zh-cn_topic_0000001359713190_p1714475392613"></a><a name="zh-cn_topic_0000001359713190_p1714475392613"></a>QingTian Enclave镜像文件本身，不包括证书与签名信息</p>
</td>
</tr>
<tr id="zh-cn_topic_0000001359713190_row1840114292616"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0000001359713190_p614418533263"><a name="zh-cn_topic_0000001359713190_p614418533263"></a><a name="zh-cn_topic_0000001359713190_p614418533263"></a>PCR8</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0000001359713190_p61441653182610"><a name="zh-cn_topic_0000001359713190_p61441653182610"></a><a name="zh-cn_topic_0000001359713190_p61441653182610"></a>QingTian Enclave镜像文件签名证书</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0000001359713190_p1014455315267"><a name="zh-cn_topic_0000001359713190_p1014455315267"></a><a name="zh-cn_topic_0000001359713190_p1014455315267"></a>QingTian Enclave镜像文件的签名证书</p>
</td>
</tr>
</tbody>
</table>

当前QingTian Enclave提供的度量值支持PCR0和PCR8，后续会进行扩展。

1.  PCR0是对QingTian Enclave镜像文件的度量值，在镜像制作完成时，PCR0的值就是确定的。以下是PCR0实例：

```
EXTEND_PCR: index: 0
EXTEND_PCR: data:  
0d1ae7330f437ee563178df30a7c7b7634125d31cac14f6784933db5e90080008438b38fdbb39c886ffe0586ab099b56
EXTEND_PCR res: data:  
b8c59692da8a5bcb739a83d15a0ceca670bd78da06cb2250ec70548f72254e674419e9888db9c0364a9b88dd58017a62
```

1.  PCR8是对QingTian Enclave镜像文件的签名证书的度量值，用户可以选择用自己的证书和私钥对镜像文件进行签名。只有当镜像文件使用了签名证书和私钥进行签名，才会有对应的PCR8。使用PCR8可以确认是镜像是通过特定的签名证书来进行签名的，即使镜像文件改变，只要指定的签名证书不变，PCR8就不会变化。以下是PCR8实例：

```
EXTEND_PCR: index: 8
EXTEND_PCR: data:
c5b3e075e00c261e7fc364f1541067b2a42d4b793225ab10e5cfb8eaca31b3d598af9dd2e491828c2569a9953401abcb
EXTEND_PCR res: data:  
4f8b066ce5ac24150612ba9a55bbb9211f626152ada40ede160f4d7ecbfa214c2a549181f6611a3d16a12ec88a577a01
```

