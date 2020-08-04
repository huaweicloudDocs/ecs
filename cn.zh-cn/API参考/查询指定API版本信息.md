# 查询指定API版本信息<a name="ZH-CN_TOPIC_0065792794"></a>

## 功能介绍<a name="section553655182144"></a>

返回指定版本的信息。

为了支持功能不断扩展，Nova API支持版本号区分。Nova中有两种形式的版本号：

-   "主版本号": 具有独立的url。
-   "微版本号": 通过Http请求头X-OpenStack-Nova-API-Version来使用，从 2.27 版本开始支持新的微版本头：OpenStack-API-Version。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >如果使用OpenStack-API-Version的请求头，version对应的value取值格式为 compute 微版本号。
    >例如：key为OpenStack-API-Version的时候value需要填compute 2.27。


## URI<a name="section961608182144"></a>

GET /\{api\_version\}

参数说明请参见[表1](#table46110007)。

**表 1**  参数说明

<a name="table46110007"></a>
<table><thead align="left"><tr id="row14148614"><th class="cellrowborder" valign="top" width="20.74%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.99%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.27%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17201924"><td class="cellrowborder" valign="top" width="20.74%" headers="mcps1.2.4.1.1 "><p id="p51178607"><a name="p51178607"></a><a name="p51178607"></a>api_version</p>
</td>
<td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.2 "><p id="p51826478"><a name="p51826478"></a><a name="p51826478"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="59.27%" headers="mcps1.2.4.1.3 "><p id="p37195178"><a name="p37195178"></a><a name="p37195178"></a>API版本号。例如: v2</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section108201017144216"></a>

无

## 响应消息<a name="section89511024194216"></a>

无

## 请求示例<a name="section19667838182144"></a>

```
GET https://{endpoint}/v2
```

## 响应示例<a name="section20327115469"></a>

```
{
 "version": {
  "min_version": "",
  "media-types": [{
   "type": "application/vnd.openstack.compute+json;version=2",
   "base": "application/json"
  }],
  "links": [{
   "rel": "self",
   "href": "https://ecs.service.domain.com:443/v2/"
  },
  {
   "rel": "describedby",
   "href": "http://docs.openstack.org/",
   "type": "text/html"
  }],
  "id": "v2.0",
  "updated": "1999-02-20T11:33:21Z",
  "version": "",
  "status": "SUPPORTED"
 }
}
```

## 返回值<a name="section12571834"></a>

请参考[通用请求返回值](通用请求返回值.md)。

