# 获取Token并检验Token的有效期<a name="ecs_04_0008"></a>

## 操作场景<a name="section5686113311205"></a>

Token的有效期为24小时，获取Token后建议及时保存，避免频繁调用。无论是否重新获取Token，在有效期内的Token始终有效。使用Token前请确保Token离过期有足够的时间，防止调用API的过程中Token过期导致调用API失败。

针对用户调用接口中常常出现的Token过期导致的调用失败问题，本文将介绍获取Token并检验Token有效期的方法。

若Token即将超期（无法满足一次完整的API调用或者完整的一套组合的调用）则需要重新获取Token，防止调用过程中Token超期，调用中断。或推荐您[使用SDK](https://support.huaweicloud.com/sdkreference-ecs/ecs_sdk_0101.html)，采用AK/SK方式认证鉴权。

## 操作视频及相关链接<a name="section8351217162618"></a>

-   获取Token的操作指导可以参考：[https://bbs.huaweicloud.com/videos/102987](https://bbs.huaweicloud.com/videos/102987)
-   [获取IAM用户Token（使用密码）](https://support.huaweicloud.com/api-iam/iam_30_0001.html)
-   [检验Token有效性](https://support.huaweicloud.com/api-iam/iam_30_0004.html)
-   在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneCreateUserTokenByPassword)中运行调试获取Token。
-   在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneValidateToken)中运行检验Token有效性。

## 获取Token<a name="section1769514236234"></a>

接口调用前需要认证鉴权，因此需要提前获取token信息。后续调用API的消息头中“X-Auth-Token”的值即为Token值。

本例以获取华东-上海二区域的Token为例：

-   请求URI：POST https://iam.cn-east-2.myhuaweicloud.com/v3/auth/tokens
-   请求消息头：Content-Type=application/json
-   请求消息体：

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "password"
                ],
                "password": {
                    "user": {
                        "name": "请填写用户名",
                        "password": "用户登录密码",
                        "domain": {
                            "name": "用户所属的帐号名称"
                        }
                    }
                }
            },
            "scope": {
                "project": {
                    "name": "区域名称，本例为cn-east-2"
                }
            }
        }
    }
    ```


-   查看获取的Token：单击响应头，x-subject-token的取值即为获取的Token。请妥善保存Token信息，在后续的创建云服务器的请求头信息中需要使用Token认证。

    ```
    General:
       Request URL: https://iam.cn-east-2.myhuaweicloud.com/v3/auth/tokens
       Request Method: POST
       Status Code: 201
    Response Headers:
       cache-control: no-cache, no-store, must-revalidate
       connection: keep-alive
       content-length: 18401
       content-type: application/json; charset=UTF-8
       date: Thu, 27 May 2021 01:24:49 GMT
       expires: Thu, 01 Jan 1970 00:00:00 GMT
       pragma: no-cache
       server: api-gateway
       strict-transport-security: max-age=31536000; includeSubdomains;
       via: proxy A
       x-content-type-options: nosniff
       x-download-options: noopen
       x-frame-options: SAMEORIGIN
       x-iam-trace-id: token_cn-east-2_null_9bbec3983f3c7a5c146e709251760467
       x-request-id: d7796611318416bc8ffb2948a47fede8
       x-subject-token: MIISMAYJKoZIhvcNAQ...7xMUw==
       x-xss-protection: 1; mode=block;
    ```

-   查看Token过期时间：响应体中“expires\_at”表示该Token过期时间。

    ```
    {
    	"token": {
    		"expires_at": "2021-05-28T01:24:49.905000Z",
            ...
    	}
    }
    ```


## 检验Token的有效期<a name="section99501635172312"></a>

调用API时判断Token有效期是否充足，若您的应用程序缓存了Token，建议每12小时刷新一次Token。以确保Token有足够长的有效期。

您还可以主动查询某个Token的过期时间。通过调用[检验Token有效性](https://support.huaweicloud.com/api-iam/iam_30_0004.html)的接口查看Token的有效时期。

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneValidateToken)中调试该接口。

本例以检验华东-上海二区域的Token为例：

-   请求URI：GET https://iam.cn-east-2.myhuaweicloud.com/v3/auth/tokens
-   请求消息头：
    -   Content-Type=application/json;charset=utf8
    -   X-Auth-Token：管理员校验本帐号中IAM用户的token的有效性：拥有Security Administrator权限的token。

        IAM用户校验自己token的有效性：该IAM用户的token（无需特殊权限）。

        本例中使用的是IAM用户因此X-Auth-Token与待校验的Token相同。

    -   X-Subject-Token：待校验的token。

-   查看Token过期时间：响应体中“expires\_at”表示该Token过期时间。

    若Token即将超期（无法满足一次完整的API调用或者完整的一套组合的调用）则需要重新获取Token，防止调用过程中Token超期，调用中断。

    ```
    {
    	"token": {
    		"expires_at": "2021-05-28T01:24:49.905000Z",
            ...
    	}
    }
    ```


