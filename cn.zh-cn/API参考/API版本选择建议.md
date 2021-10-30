# API版本选择建议<a name="ecs_01_0006"></a>

## API风格说明<a name="section18271554182719"></a>

当前ECS服务对外开放两类风格的API：

1.  ECS服务自定义规范的API（以下简称ECS API）
2.  顺从OpenStack社区标准原生规范的API

两种风格不同，功能相近。OpenStack风格API主要用于满足您在开源生态工具方面的对接需求，在某些功能上ECS API在OpenStack社区的API基础上，做了功能增强。为了更好的使用OpenStack风格API，建议您提前了解OpenStack相关概念与知识。

## 版本号介绍<a name="section1092352712223"></a>

弹性云服务器所提供的接口分为ECS接口与OpenStack原生接口。推荐您使用ECS接口。

Openstack API可以使用v2和v2.1两个版本号，v2.1版本支持v2版本所有功能，且v2.1版本支持微版本。如果使用Openstack API推荐用户使用v2.1接口。

>![](public_sys-resources/icon-note.gif) **说明：** 
>若使用v2版本的openstack API接口，只需要把对应的API接口URI中的v2.1版本号改为v2版本号即可。

## 微版本号介绍<a name="section16915142722416"></a>

微版本说明：标识API中小的改动。当接口URI使用v2.1版本的时候，用户可以指定微版本号使用相应API的新功能。使用[查询API版本信息列表](查询API版本信息列表.md)，可以查询当前支持的主版本和支持的最大与最小的微版本。

微版本的使用说明：用户想要使用微版本特性，需要在请求Openstack接口时，在请求头中加入微版本头：X-OpenStack-Nova-API-Version或者Openstack-API-Version，例如使用微版本2.26需要在https的请求头中加入：

X-OpenStack-Nova-API-Version: 2.26或Openstack-API-Version: compute 2.26

>![](public_sys-resources/icon-note.gif) **说明：** 
>当用户使用v2.1接口不传入微版本头时，默认使用的微版本Openstack-API-Version: compute 2.1\(X-OpenStack-Nova-API-Version: 2.1\)。

## 微版本请求样例<a name="section953273282314"></a>

假设使用弹性云服务器详情信息列表API接口查询"OS-EXT-SRV-ATTR:hostname"字段。

-   **使用v2接口，不加微版本号**
    -   GET: https://_\{Endpoint\}_/v2/74610f3a5ad941998e91f076297ecf27/servers/detail

        其中\{Endpoint\}为IAM的终端节点，请参考[终端节点](终端节点.md)获取。

    -   Headers:

        <a name="zh-cn_topic_0134193006_table19387710"></a>
        <table><tbody><tr id="zh-cn_topic_0134193006_row14795382"><td class="cellrowborder" valign="top" width="50%"><p id="zh-cn_topic_0134193006_p57575265"><a name="zh-cn_topic_0134193006_p57575265"></a><a name="zh-cn_topic_0134193006_p57575265"></a>Content-Type</p>
        </td>
        <td class="cellrowborder" valign="top" width="50%"><p id="zh-cn_topic_0134193006_p33084893"><a name="zh-cn_topic_0134193006_p33084893"></a><a name="zh-cn_topic_0134193006_p33084893"></a>application/json</p>
        </td>
        </tr>
        <tr id="zh-cn_topic_0134193006_row29328585"><td class="cellrowborder" valign="top" width="50%"><p id="zh-cn_topic_0134193006_p26805152"><a name="zh-cn_topic_0134193006_p26805152"></a><a name="zh-cn_topic_0134193006_p26805152"></a>X-Auth-Token</p>
        </td>
        <td class="cellrowborder" valign="top" width="50%"><p id="zh-cn_topic_0134193006_p23733724"><a name="zh-cn_topic_0134193006_p23733724"></a><a name="zh-cn_topic_0134193006_p23733724"></a>${token}</p>
        </td>
        </tr>
        </tbody>
        </table>

    -   响应消息体：

        ```
        {
          "servers": [
            {
              "tenant_id": "74610f3a5ad941998e91f076297ecf27",
              "addresses": {
                "05d4fb93-84e5-4964-853b-32992ffef627": [
                  {
                    "OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:20:17:95",
                    "OS-EXT-IPS:type": "fixed",
                    "addr": "192.168.0.228",
                    "version": 4
                  },
                  {
                    "OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:20:17:95",
                    "OS-EXT-IPS:type": "floating",
                    "addr": "192.168.51.61",
                    "version": 4
                  }
                ]
              },
              "metadata": {},
              "OS-EXT-STS:task_state": null,
              "OS-DCF:diskConfig": "MANUAL",
              "OS-EXT-AZ:availability_zone":"az1-dc1",
              "links": [
                {
                  "rel": "self",
                  "href": "https://None/v2.1/74610f3a5ad941998e91f076297ecf27/servers/89c312bb-285a-4026-a237-d441908c2f9e"
                },
                {
                  "rel": "bookmark",
                  "href": "https://None/74610f3a5ad941998e91f076297ecf27/servers/89c312bb-285a-4026-a237-d441908c2f9e"
                }
              ],
              "OS-EXT-STS:power_state": 1,
              "id": "89c312bb-285a-4026-a237-d441908c2f9e",
              "os-extended-volumes:volumes_attached": [
                {
                  "id": "c70c4b8e-33bd-4d1f-ab16-14a5a38cdeaf"
                }
              ],
              "OS-EXT-SRV-ATTR:host": "pod05.test.01",
              "image": {
                "links": [
                  {
                    "rel": "bookmark",
                    "href": "https://None/74610f3a5ad941998e91f076297ecf27/images/1189efbf-d48b-46ad-a823-94b942e2a000"
                  }
                ],
                "id": "1189efbf-d48b-46ad-a823-94b942e2a000"
              },
              "OS-SRV-USG:terminated_at": null,
              "accessIPv4": "",
              "accessIPv6": "",
              "created": "2018-05-11T03:21:56Z",
              "hostId": "fc7a8ff86bac050f0d9454b1b078dcc97060e819acbf06f04c3e338f",
              "OS-EXT-SRV-ATTR:hypervisor_hostname": "nova012@7",
              "key_name": "id_rsa",
              "flavor": {
                "links": [
                  {
                    "rel": "bookmark",
                    "href": "https://None/74610f3a5ad941998e91f076297ecf27/flavors/s3.small.1"
                  }
                ],
                "id": "s3.small.1"
              },
              "security_groups": [
                {
                  "name": "default"
                }
              ],
              "config_drive": "",
              "OS-EXT-STS:vm_state": "active",
              "OS-EXT-SRV-ATTR:instance_name": "instance-0016c624",
              "user_id": "f79791beca3c48159ac2553fff22e166",
              "name": "zt-test",
              "progress": 0,
              "OS-SRV-USG:launched_at": "2018-05-11T03:22:16.701600",
              "updated": "2018-05-11T03:22:51Z",
              "status": "ACTIVE"
            }
          ]
        }
        ```

    -   结论：响应消息体中没有"OS-EXT-SRV-ATTR:hostname"字段。


-   **使用v2.1接口，加微版本号**
    -   GET: https://_\{Endpoint\}_/v2.1/74610f3a5ad941998e91f076297ecf27/servers/detail

        其中\{Endpoint\}为IAM的终端节点，请参考[终端节点](终端节点.md)获取。

    -   Headers:

        <a name="zh-cn_topic_0134193006_table41684430"></a>
        <table><tbody><tr id="zh-cn_topic_0134193006_row5034912"><td class="cellrowborder" valign="top" width="50%"><p id="zh-cn_topic_0134193006_p5174700"><a name="zh-cn_topic_0134193006_p5174700"></a><a name="zh-cn_topic_0134193006_p5174700"></a>Content-Type</p>
        </td>
        <td class="cellrowborder" valign="top" width="50%"><p id="zh-cn_topic_0134193006_p16497581"><a name="zh-cn_topic_0134193006_p16497581"></a><a name="zh-cn_topic_0134193006_p16497581"></a>application/json</p>
        </td>
        </tr>
        <tr id="zh-cn_topic_0134193006_row14260509"><td class="cellrowborder" valign="top" width="50%"><p id="zh-cn_topic_0134193006_p14250600"><a name="zh-cn_topic_0134193006_p14250600"></a><a name="zh-cn_topic_0134193006_p14250600"></a>X-Auth-Token</p>
        </td>
        <td class="cellrowborder" valign="top" width="50%"><p id="zh-cn_topic_0134193006_p13447964"><a name="zh-cn_topic_0134193006_p13447964"></a><a name="zh-cn_topic_0134193006_p13447964"></a>${token}</p>
        </td>
        </tr>
        <tr id="zh-cn_topic_0134193006_row53922812"><td class="cellrowborder" valign="top" width="50%"><p id="zh-cn_topic_0134193006_p5671647"><a name="zh-cn_topic_0134193006_p5671647"></a><a name="zh-cn_topic_0134193006_p5671647"></a>X-OpenStack-Nova-API-Version</p>
        </td>
        <td class="cellrowborder" valign="top" width="50%"><p id="zh-cn_topic_0134193006_p56750271"><a name="zh-cn_topic_0134193006_p56750271"></a><a name="zh-cn_topic_0134193006_p56750271"></a>2.26</p>
        </td>
        </tr>
        </tbody>
        </table>

    -   响应消息体：

        ```
        {
          "servers": [
            {
              "tenant_id": "74610f3a5ad941998e91f076297ecf27",
              "addresses": {
                "05d4fb93-84e5-4964-853b-32992ffef627": [
                  {
                    "OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:20:17:95",
                    "OS-EXT-IPS:type": "fixed",
                    "addr": "192.168.0.228",
                    "version": 4
                  },
                  {
                    "OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:20:17:95",
                    "OS-EXT-IPS:type": "floating",
                    "addr": "192.168.51.61",
                    "version": 4
                  }
                ]
              },
              "metadata": {},
              "OS-EXT-STS:task_state": null,
              "description": "zt-test",
              "OS-EXT-SRV-ATTR:hostname": "zt-test",
              "OS-DCF:diskConfig": "MANUAL",
              "OS-EXT-AZ:availability_zone":"az-test-01",
              "links": [
                {
                  "rel": "self",
                  "href": "https://None/v2.1/74610f3a5ad941998e91f076297ecf27/servers/89c312bb-285a-4026-a237-d441908c2f9e"
                },
                {
                  "rel": "bookmark",
                  "href": "https://None/74610f3a5ad941998e91f076297ecf27/servers/89c312bb-285a-4026-a237-d441908c2f9e"
                }
              ],
              "OS-EXT-STS:power_state": 1,
              "id": "89c312bb-285a-4026-a237-d441908c2f9e",
              "os-extended-volumes:volumes_attached": [
                {
                  "delete_on_termination": true,
                  "id": "c70c4b8e-33bd-4d1f-ab16-14a5a38cdeaf"
                }
              ],
              "locked": false,
              "OS-EXT-SRV-ATTR:kernel_id": "",
              "OS-EXT-SRV-ATTR:host":"pod05.test.01" ,
              "OS-EXT-SRV-ATTR:ramdisk_id": "",
              "image": {
                "links": [
                  {
                    "rel": "bookmark",
                    "href": "https://None/74610f3a5ad941998e91f076297ecf27/images/1189efbf-d48b-46ad-a823-94b942e2a000"
                  }
                ],
                "id": "1189efbf-d48b-46ad-a823-94b942e2a000"
              },
              "accessIPv4": "",
              "OS-SRV-USG:terminated_at": null,
              "accessIPv6": "",
              "OS-EXT-SRV-ATTR:launch_index": 0,
              "created": "2018-05-11T03:21:56Z",
              "OS-EXT-SRV-ATTR:user_data": null,
              "hostId": "fc7a8ff86bac050f0d9454b1b078dcc97060e819acbf06f04c3e338f",
              "OS-EXT-SRV-ATTR:reservation_id": "r-pbqmaxer",
              "OS-EXT-SRV-ATTR:root_device_name": "/dev/vda",
              "host_status": "UP",
              "OS-EXT-SRV-ATTR:hypervisor_hostname": "nova012@7",
              "tags": [],
              "key_name": "id_rsa",
              "flavor": {
                "links": [
                  {
                    "rel": "bookmark",
                    "href": "https://None/74610f3a5ad941998e91f076297ecf27/flavors/s3.small.1"
                  }
                ],
                "id": "s3.small.1"
              },
              "security_groups": [
                {
                  "name": "default"
                }
              ],
              "config_drive": "",
              "OS-EXT-STS:vm_state": "active",
              "OS-EXT-SRV-ATTR:instance_name": "instance-0016c624",
              "user_id": "f79791beca3c48159ac2553fff22e166",
              "name": "zt-test",
              "progress": 0,
              "OS-SRV-USG:launched_at": "2018-05-11T03:22:16.701600",
              "updated": "2018-05-11T03:22:51Z",
              "status": "ACTIVE"
            }
          ]
        }
        ```

    -   结论：响应消息体中有"OS-EXT-SRV-ATTR:hostname"字段。


## 微版本响应样例<a name="section3389735132414"></a>

如果“version”和“min\_version”这两个值为空字符串，说明此endpoint不支持微版本。其中：

-   version： 最大微版本号。
-   min\_version：最小微版本号。

客户端应该指定最大和最小微版本范围内的微版本号去访问endpoint。客户端通过以下HTTP header指定微版本号：

X-OpenStack-Nova-API-Version: 2.4

从微版本2.27开始，也可以用以下header指定微版本：

Openstack-API-Version: compute 2.27

如下响应样例中支持的最大微版本为“2.14”，最小微版本为“2.1”：

```
{
  "versions": [
      {
          "id": "v2.0",
          "links": [
              {
                  "href": "http://openstack.example.com/v2/",
                  "rel": "self"
              }
          ],
          "status": "SUPPORTED",
          "version": "",
          "min_version": "",
          "updated": "2011-01-21T11:33:21Z"
      },
      {
          "id": "v2.1",
          "links": [
              {
                  "href": "http://openstack.example.com/v2.1/",
                  "rel": "self"
              }
          ],
          "status": "CURRENT",
          "version": "2.14",
          "min_version": "2.1",
          "updated": "2013-07-23T11:33:21Z"
      }
  ]
}
```

