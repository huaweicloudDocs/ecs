# 删除云服务器组<a name="ZH-CN_TOPIC_0065817723"></a>

## 功能介绍<a name="zh-cn_topic_0057973160_section59750848"></a>

删除云服务器组。

## URI<a name="zh-cn_topic_0057973160_section886720"></a>

DELETE /v2.1/\{project\_id\}/os-server-groups/\{server\_group\_id\}

参数说明请参见[表1](#zh-cn_topic_0057973160_zh-cn_topic_0020212650_table62669527)。

**表 1**  参数说明

<a name="zh-cn_topic_0057973160_zh-cn_topic_0020212650_table62669527"></a>
<table><thead align="left"><tr id="zh-cn_topic_0057973160_zh-cn_topic_0020212650_row33894570"><th class="cellrowborder" valign="top" width="20.74%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.05%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.209999999999994%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0057973160_zh-cn_topic_0020212650_row8419032"><td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973160_zh-cn_topic_0020212650_p10852974"><a name="zh-cn_topic_0057973160_zh-cn_topic_0020212650_p10852974"></a><a name="zh-cn_topic_0057973160_zh-cn_topic_0020212650_p10852974"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.05%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973160_zh-cn_topic_0020212650_p6675738"><a name="zh-cn_topic_0057973160_zh-cn_topic_0020212650_p6675738"></a><a name="zh-cn_topic_0057973160_zh-cn_topic_0020212650_p6675738"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="60.209999999999994%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0057973160_row1856062192319"><td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0057973160_p16560926238"><a name="zh-cn_topic_0057973160_p16560926238"></a><a name="zh-cn_topic_0057973160_p16560926238"></a>server_group_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.05%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0057973160_p5560326232"><a name="zh-cn_topic_0057973160_p5560326232"></a><a name="zh-cn_topic_0057973160_p5560326232"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="60.209999999999994%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0057973160_p94577242237"><a name="zh-cn_topic_0057973160_p94577242237"></a><a name="zh-cn_topic_0057973160_p94577242237"></a>弹性云服务器组UUID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section8486123205213"></a>

无

## 响应消息<a name="section164423895218"></a>

无

## 请求示例<a name="zh-cn_topic_0057973160_section15049613"></a>

```
DELETE https://{endpoint}/v2.1/9c53a566cb3443ab910cf0daebca90c4/os-server-groups/5bbcc3c4-1da2-4437-a48a-66f15b1b13f9
```

## 返回值<a name="zh-cn_topic_0057973160_section11059103"></a>

请参考[通用请求返回值](通用请求返回值.md)。

