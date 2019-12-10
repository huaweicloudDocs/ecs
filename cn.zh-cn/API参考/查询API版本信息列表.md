# 查询API版本信息列表<a name="ZH-CN_TOPIC_0065792793"></a>

## 功能介绍<a name="section54478915181842"></a>

返回Nova当前所有可用的版本。

为了支持功能不断扩展，Nova API支持版本号区分。Nova中有两种形式的版本号：

-   "主版本号": 具有独立的url。
-   "微版本号": 通过Http请求头X-OpenStack-Nova-API-Version来使用。

## URI<a name="section53791107181842"></a>

GET /

## 请求消息<a name="section108201017144216"></a>

无

## 响应消息<a name="section89511024194216"></a>

无

## 请求示例<a name="section39878380181842"></a>

```
GET https://{endpoint}/
```

## 响应示例<a name="section569124244211"></a>

```
{
 "versions": [{
  "links": [{
   "rel": "self",
   "href": "https://ecs.service.domain.com:443/v2/"
  }],
  "id": "v2.0",
  "updated": "2001-09-21T12:33:21Z",
  "status": "SUPPORTED"
 }]
}
```

## 返回值<a name="section12571834"></a>

请参考[通用请求返回值](通用请求返回值.md)。

