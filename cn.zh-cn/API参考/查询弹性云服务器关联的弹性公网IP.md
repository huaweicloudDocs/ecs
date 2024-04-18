# 查询弹性云服务器关联的弹性公网IP<a name="ecs_04_0006"></a>

## 场景描述<a name="section10764922102711"></a>

本章节指导用户通过弹性云服务器和弹性公网IP接口，查询弹性云服务器关联的弹性公网IP详情。

## 涉及接口<a name="section2036914547282"></a>

本示例场景涉及如下接口调用：

-   [查询弹性云服务器详情](#li2096242823112)
-   [根据公网IP查询公网IP详情](#li136736121430)

## 操作步骤<a name="section47476132395"></a>

1.  <a name="li2096242823112"></a>查询弹性云服务器详情
    -   接口相关信息

        URI格式： GET /v1/\{project\_id\}/cloudservers/\{server\_id\}

        详情请参见“[查询云服务器详情](查询云服务器详情.md)”。

    -   请求示例

        GET https://_\{endpoint__\}_/v1/743b4c0428d945316666666666666666/cloudservers/893c7791-f1df-4c3d-8383-3caae9656c62

        \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?ECS)获取。

    -   响应示例

        ```
        {
        	"server": {
        		"fault": null,
        		"id": "b8b1b475-d6c9-4733-a3db-c3a526407286",
        		"name": "ecs-test",
        		"addresses": {
        			"24bbb54c-659f-4141-8db9-a957e12b6ee8": [{
        				"version": "4",
        				"addr": "192.168.0.16",
        				"OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:37:de:ee",
        				"OS-EXT-IPS:type": "fixed",
        				"OS-EXT-IPS:port_id": "390b39b0-9a77-4ec2-ae1e-3af358f78999"
        			},
        			{
        				"version": "4",
        				"addr": "121.xx.xx.64",
        				"OS-EXT-IPS-MAC:mac_addr": "fa:16:3e:37:de:ee",
        				"OS-EXT-IPS:type": "floating",
        				"OS-EXT-IPS:port_id": "390b39b0-9a77-4ec2-ae1e-3af358f78999"
        			}]
        		},
        		"flavor": {
        			"disk": "0",
        			"vcpus": "2",
        			"ram": "4096",
        			"id": "c6s.large.2",
        			"name": "c6s.large.2"
        		},
        		"accessIPv4": "",
        		"accessIPv6": "",
        		"status": "SHUTOFF",
        		"progress": null,
        		"hostId": "604599c4eeeaa05d8865749e4c97979e14d74c6639a08460051b3a97",
        		"updated": "2021-02-18T12:38:39Z",
        		"created": "2021-02-18T12:37:42Z",
        		"metadata": {
        			"metering.image_id": "6674d782-54ba-4f04-896d-95edd50f2eb9",
        			"metering.imagetype": "gold",
        			"metering.resourcespeccode": "c6s.large.2.linux",
        			"image_name": "CentOS 8.2 64bit",
        			"os_bit": "64",
        			"cascaded.instance_extrainfo": "stopped_release_resource:True,pcibridge:1",
        			"metering.resourcetype": "1",
        			"vpc_id": "24bbb54c-659f-4141-8db9-a957e12b6ee8",
        			"os_type": "Linux",
        			"charging_mode": "0",
        			"__support_agent_list": "ces"
        		},
        		"tags": [],
        		"description": "",
        		"locked": false,
        		"config_drive": "",
        		"tenant_id": "0b3ade290700f3612f29c005b9d16666",
        		"user_id": "0b3ade2a03800fec1f20c005d6116666",
        		"key_name": null,
        		"os-extended-volumes:volumes_attached": [{
        			"device": "/dev/vda",
        			"bootIndex": "0",
        			"id": "0dc13ef4-dcf6-49d2-8d34-395d94767917",
        			"delete_on_termination": "true"
        		}],
        		"OS-EXT-STS:task_state": null,
        		"OS-EXT-STS:power_state": 4,
        		"OS-EXT-STS:vm_state": "stopped",
        		"OS-EXT-SRV-ATTR:host": "604599c4eeeaa05d8865749e4c97979e14d74c6639a08460051b3a97",
        		"OS-EXT-SRV-ATTR:instance_name": "instance-003ef12a",
        		"OS-EXT-SRV-ATTR:hypervisor_hostname": "5edb1b44af14ebaaa784cfba010f78f113b1fd0865fef854c264a925",
        		"OS-DCF:diskConfig": "MANUAL",
        		"OS-EXT-AZ:availability_zone": "cn-east-3c",
        		"os:scheduler_hints": {
        			
        		},
        		"OS-EXT-SRV-ATTR:root_device_name": "/dev/vda",
        		"OS-EXT-SRV-ATTR:ramdisk_id": "",
        		"enterprise_project_id": "0",
        		"OS-EXT-SRV-ATTR:user_data": null,
        		"OS-SRV-USG:launched_at": "2021-02-18T12:37:57.000000",
        		"OS-EXT-SRV-ATTR:kernel_id": "",
        		"OS-EXT-SRV-ATTR:launch_index": 0,
        		"host_status": "UP",
        		"OS-EXT-SRV-ATTR:reservation_id": "r-q8xjhqzk",
        		"OS-EXT-SRV-ATTR:hostname": "ecs-test",
        		"OS-SRV-USG:terminated_at": null,
        		"sys_tags": [{
        			"key": "_sys_enterprise_project_id",
        			"value": "0"
        		}],
        		"security_groups": [{
        			"id": "d0d30ee2-5b34-44d4-b5a3-68b9d64e7286",
        			"name": "Sys-WebServer"
        		}],
        		"image": {
        			"id": "6674d782-54ba-4f04-896d-95edd50f2eb9"
        		},
        		"hypervisor": null,
        		"auto_terminate_time": ""
        	}
        }
        ```

2.  <a name="li136736121430"></a>根据公网IP查询公网IP详情
    -   接口相关信息

        URI格式： GET /v1/\{project\_id\}/publicips

        详情请参见“[查询弹性公网IP列表](https://support.huaweicloud.com/api-eip/eip_api_0003.html)”。

    -   请求示例

        GET https://_\{endpoint__\}_/v1/743b4c0428d945316666666666666666/publicips?public\_ip\_address=121.xx.xx.64

        \{endpoint\}信息请从[地区和终端节点](https://developer.huaweicloud.com/endpoint?ECS)获取。

        public\_ip\_address参数传入的公网IP地址从[1](#li2096242823112)的返回信息中获取，从返回body体中的"server"下的"address"信息中找到"OS-EXT-IPS:type"为"floating"的"addr"字段，即为公网IP地址。

    -   响应示例

        ```
        {
        	"publicips": [{
        		"id": "92597d39-b81d-42b0-8d02-fe8afe7ef076",
        		"type": "5_bgp",
        		"port_id": "390b39b0-9a77-4ec2-ae1e-3af358f78999",
        		"public_ip_address": "121.xx.xx.64",
        		"private_ip_address": "192.168.0.16",
        		"status": "ACTIVE",
        		"tenant_id": "0b3ade290700f3612f29c005b9d16666",
        		"create_time": "2021-02-18 12:38:08",
        		"bandwidth_id": "3a087bbd-0bcf-4401-9e2b-6a96fa2e3471",
        		"bandwidth_name": "ecs-test-bandwidth-891e",
        		"bandwidth_share_type": "PER",
        		"bandwidth_size": 5,
        		"profile": {},
        		"enterprise_project_id": "0",
        		"ip_version": 4
        	}]
        }
        ```

