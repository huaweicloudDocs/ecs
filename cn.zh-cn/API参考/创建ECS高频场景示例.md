# 创建ECS高频场景示例<a name="ZH-CN_TOPIC_0000001162037223"></a>

## 操作场景<a name="section2067082251414"></a>

本节内容介绍了使用API购买ECS过程中的一些常见问题及处理方法。

**表 1**  使用API创建ECS的常见问题及处理方法

<a name="table91827208246"></a>
<table><thead align="left"><tr id="row13182112010248"><th class="cellrowborder" valign="top" width="30.270000000000003%" id="mcps1.2.3.1.1"><p id="p81821620162413"><a name="p81821620162413"></a><a name="p81821620162413"></a>问题描述</p>
</th>
<th class="cellrowborder" valign="top" width="69.73%" id="mcps1.2.3.1.2"><p id="p141821920122411"><a name="p141821920122411"></a><a name="p141821920122411"></a>处理方法</p>
</th>
</tr>
</thead>
<tbody><tr id="row718262062410"><td class="cellrowborder" valign="top" width="30.270000000000003%" headers="mcps1.2.3.1.1 "><p id="p81821520132416"><a name="p81821520132416"></a><a name="p81821520132416"></a><a href="#section841342610363">购买包周期ECS</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.73%" headers="mcps1.2.3.1.2 "><p id="p41822206247"><a name="p41822206247"></a><a name="p41822206247"></a>为您介绍购买包周期资源的参数设置。</p>
</td>
</tr>
<tr id="row618242016240"><td class="cellrowborder" valign="top" width="30.270000000000003%" headers="mcps1.2.3.1.1 "><p id="p10182172011244"><a name="p10182172011244"></a><a name="p10182172011244"></a><a href="#section13736183144411">删除包周期ECS/退订包周期ECS</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.73%" headers="mcps1.2.3.1.2 "><p id="p181821420152412"><a name="p181821420152412"></a><a name="p181821420152412"></a>包周期资源需要通过退订的方式才可以被删除。</p>
</td>
</tr>
<tr id="row6182620162418"><td class="cellrowborder" valign="top" width="30.270000000000003%" headers="mcps1.2.3.1.1 "><p id="p118215201249"><a name="p118215201249"></a><a name="p118215201249"></a><a href="#section12338101168">查询可用的公共镜像</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.73%" headers="mcps1.2.3.1.2 "><p id="p1018210208248"><a name="p1018210208248"></a><a name="p1018210208248"></a>购买ECS时候前查询公共镜像信息可以通过在GET请求后通过‘?’和‘&amp;’添加不同的查询条件组合。</p>
</td>
</tr>
<tr id="row918212205247"><td class="cellrowborder" valign="top" width="30.270000000000003%" headers="mcps1.2.3.1.1 "><p id="p1218232016247"><a name="p1218232016247"></a><a name="p1218232016247"></a><a href="#section115381558613">包周期资源续费</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.73%" headers="mcps1.2.3.1.2 "><p id="p81829206244"><a name="p81829206244"></a><a name="p81829206244"></a>包年/包月资源即将到期时，可进行包年/包月资源的续订。指定资源ID，续费方式，续费时间，订单支付方式。</p>
</td>
</tr>
<tr id="row18182620172411"><td class="cellrowborder" valign="top" width="30.270000000000003%" headers="mcps1.2.3.1.1 "><p id="p81822020112419"><a name="p81822020112419"></a><a name="p81822020112419"></a><a href="#section5431157557">创建订单后资源未开通</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.73%" headers="mcps1.2.3.1.2 "><p id="p9182720192416"><a name="p9182720192416"></a><a name="p9182720192416"></a>创建完成后查不到资源信息可能是订单尚未支付，查看订单的状态并完成订单支付。</p>
</td>
</tr>
<tr id="row131828205247"><td class="cellrowborder" valign="top" width="30.270000000000003%" headers="mcps1.2.3.1.1 "><p id="p201831120122414"><a name="p201831120122414"></a><a name="p201831120122414"></a><a href="#section413314335610">查询规格资源是否可购买/资源是否售罄</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.73%" headers="mcps1.2.3.1.2 "><p id="p31834201241"><a name="p31834201241"></a><a name="p31834201241"></a>查询某一具体的云服务器规格在某可用区是否资源充足，通过响应信息中的cond:operation:status和cond:operation:az字段的取值判断在区域和可用区的取值。</p>
</td>
</tr>
<tr id="row1418316206248"><td class="cellrowborder" valign="top" width="30.270000000000003%" headers="mcps1.2.3.1.1 "><p id="p61831520182410"><a name="p61831520182410"></a><a name="p61831520182410"></a><a href="#section171001547869">付费方式</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.73%" headers="mcps1.2.3.1.2 "><p id="p1718392017249"><a name="p1718392017249"></a><a name="p1718392017249"></a>创建包周期的云服务器时（chargingMode为prePaid），通过extendparam.isAutoPay字段控制订单的支付方式。</p>
</td>
</tr>
<tr id="row17183152017241"><td class="cellrowborder" valign="top" width="30.270000000000003%" headers="mcps1.2.3.1.1 "><p id="p3183172018245"><a name="p3183172018245"></a><a name="p3183172018245"></a><a href="#section14991749361">查询资源的可用配额</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.73%" headers="mcps1.2.3.1.2 "><p id="p518352072420"><a name="p518352072420"></a><a name="p518352072420"></a>调用<a href="https://support.huaweicloud.com/api-ecs/ecs_02_0801.html" target="_blank" rel="noopener noreferrer">查询租户配额</a>接口，通过maxTotalInstances可以查看云服务器的最大申请数量，通过totalInstancesUsed可以查看当前云服务器使用个数。</p>
</td>
</tr>
<tr id="row1913017202619"><td class="cellrowborder" valign="top" width="30.270000000000003%" headers="mcps1.2.3.1.1 "><p id="p1791381792616"><a name="p1791381792616"></a><a name="p1791381792616"></a><a href="#section44361551269">查询资源价格</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.73%" headers="mcps1.2.3.1.2 "><p id="p3913121772618"><a name="p3913121772618"></a><a name="p3913121772618"></a>使用<a href="https://support.huaweicloud.com/api-oce/bcloud_01001.html" target="_blank" rel="noopener noreferrer">查询按需产品价格</a>和<a href="https://support.huaweicloud.com/api-oce/bcloud_01002.html" target="_blank" rel="noopener noreferrer">查询包年/包月产品价格</a>，根据云服务类型、资源类型、云服务区和资源规格四个条件来查询产品价格。</p>
</td>
</tr>
</tbody>
</table>

## 购买包周期ECS<a name="section841342610363"></a>

购买包周期ECS可以使用[创建弹性云服务](https://support.huaweicloud.com/api-ecs/ecs_02_0101.html)接口，相对于创建按需的ECS，只需要在请求body中指定extendparam.chargingMode参数值为“prePaid”，即包年包月，指定订购的周期等。extendparam的详细参数解释请参见[创建云服务器的extendparam字段数据结构说明](https://support.huaweicloud.com/api-ecs/zh-cn_topic_0167957246.html#ZH-CN_TOPIC_0167957246__table7721122141311)。

如下所示，在cn-north-1区域购买一台包周期ECS，时长为一个月，且下单后自动支付，自动续订。

```
{
    "server": {
        "name": "newserver",
        "availability_zone": "cn-north-1a",
        "flavorRef": "s3.small.1",
        "imageRef": "8da46d6d-6079-4e31-ad6d-a7167efff892",
        "root_volume": {
            "volumetype": "SATA"
        },
        "vpcid": "7e1a7e70-3f3e-4581-955e-26a4848d8f31",
        "nics": [
	        {
		 "subnet_id": "04548cde-4067-48b0-9323-5c7b67ac13fc"
	        }	
        ],
        "data_volumes": [
	   {
                "volumetype": "SSD", 
                "size": 50
            }
        ],
        "publicip": {
            "id": "publicip_123", 
            "eip": {
                "iptype": "5_bgp",
                "bandwidth": {
                    "size": 10, 
                    "sharetype": "PER"
                }
            }
        },
        "extendparam": {
            "chargingMode": "prePaid",
            "periodType": "month",
            "periodNum": 1,
            "isAutoRenew": "true",
            "isAutoPay": "true",
            "regionID": "cn-north-1"
        }
    }
}
```

包周期ECS创建后会返回一个order\_id，即订单ID。

```
{
    "job_id": "ff808082739334d80173943ec9b42130",
    "order_id": "CS2007281506xxxxx",
    "serverIds": [
        "fe0528f0-5b1c-4c8c-9adf-e5d5047b8c17"
    ] 
}
```

上面请求体中extendparam.isAutoPay取值为true，表示自动支付，如果不填该字段或取值为false，则需要手动去支付，手动支付可以填写优惠券和折扣券等信息。手动支付需要调用[支付包年/包月产品订单](https://support.huaweicloud.com/api-oce/api_order_00016.html)支付，示例如下。

```
POST https://bss.myhuaweicloud.com/v2/orders/customer-orders/pay

{
    "order_id": "CS20052715001E4CR"
}
```

## 删除包周期ECS/退订包周期ECS<a name="section13736183144411"></a>

包周期ECS无法直接调用ECS接口删除，需要调用[退订包年/包月资源](https://support.huaweicloud.com/api-oce/api_order_00019.html)接口进行退订。

```
POST https://bss.myhuaweicloud.com/v2/orders/subscriptions/resources/unsubscribe

{
  "resource_ids": [
    "21e09f37c5c9420c8746ad5c71fb3aab"
  ],
  "unsubscribe_type": 1
}
```

其中resource\_ids表示资源ID，对退订ECS来说，就是购买包周期ECS时返回的serverIds。

## 查询可用的公共镜像<a name="section12338101168"></a>

使用镜像服务的[查询镜像列表](https://support.huaweicloud.com/api-ims/ims_03_0602.html)的API可以根据不同条件查询镜像列表信息，在GET请求后通过‘?’和‘&’添加不同的查询条件组合。

如需查询公共镜像列表。

```
GET /v2/cloudimages?__imagetype=gold&visibility=public&protected=true
```

请注意调用镜像服务接口注意替换镜像服务的Endpoint信息。

查询镜像列表时，建议使用分页查询才能返回全部的镜像列表。通过指定marker和limit实现镜像列表的分页查询。

marker表示从哪个镜像开始查询，取值为镜像ID。limit表示查询几条镜像记录，取值为整数，默认取值为500。

```
GET /v2/cloudimages?__imagetype=gold&visibility=public&protected=true&marker=af92bb51-ec9d-4b02-912f-da0b3f0f7635&limit=5
```

如需查询其他的镜像类型

-   公共镜像列表查询

    GET /v2/cloudimages?\_\_imagetype=gold&visibility=public&protected=true

-   私有镜像列表查询

    GET /v2/cloudimages?owner=\{project\_id\}

-   可以使用的共享镜像列表

    GET /v2/cloudimages?member\_status=accepted&visibility=shared&\_\_imagetype=shared

-   被拒绝的共享镜像列表

    GET /v2/cloudimages?member\_status=rejected&visibility=shared&\_\_imagetype=shared

-   未接受的共享镜像列表

    GET /v2/cloudimages?member\_status=pending&visibility=shared&\_\_imagetype=shared

-   裸金属服务器某规格支持的公共镜像列表

    GET /v2/cloudimages?\_\_imagetype=gold&\_\_support\_xxx=true&virtual\_env\_type=Ironic


如果未指定镜像类型，那么可以通过响应信息中的\_\_imagetype字段判断镜像类型。

## 包周期资源续费<a name="section115381558613"></a>

包年/包月资源即将到期时，可进行包年/包月资源的续订。通过调用[续订包年/包月资源](https://support.huaweicloud.com/api-oce/api_order_00018.html)接口进行续费。

如下所示，指定资源ID，按月续费，续费1个月，到期后转按需，并自动支付订单。

```
POST https://bss.myhuaweicloud.com/v2/orders/subscriptions/resources/renew

{
    "resource_ids": [
        "96308d5efd7841b9a4dac673d84d0e14"
    ],
    "period_type": 2,
    "period_num": 1,
    "expire_policy": 1,
    "is_auto_pay": 1
}
```

续费成功后会返回一个order\_id，即订单ID。

```
{
  "order_ids": [
    "CS190401192xxxxxx"
  ]
}
```

上面请求体中isAutoPay取值为1，表示自动支付，如果不填该字段或取值为0，则需要手动去支付，手动支付可以填写优惠券和折扣券等信息。手动支付需要调用[支付包年/包月产品订单](https://support.huaweicloud.com/api-oce/api_order_00016.html)支付，以下示例是使用一张优惠券，优惠券类型为代金券的请求示例。

```
POST https://bss.myhuaweicloud.com/v2/orders/customer-orders/pay

{
    "coupon_infos": [
        {
            "id": "CP2005270256xxxxxx",
            "type": 301
        }
    ],
    "order_id": "CS190401192xxxxxx"
}
```

## 创建订单后资源未开通<a name="section5431157557"></a>

订单创建后未查询到服务器信息，可能是由于指定了自动支付：请求体中extendparam.isAutoPay取值为false或续费时isAutoPay取值为0。

通常服务器创建后会返回一个order\_id，即订单ID。

```
{
    "job_id": "ff808082739334d80173943ec9b42130",
    "order_id": "CS2007281506xxxxx",
    "serverIds": [
        "fe0528f0-5b1c-4c8c-9adf-e5d5047b8c17"
    ] 
}
```

通过调用[查询订单的资源开通详情](https://support.huaweicloud.com/api-oce/api_order_00001.html)接口查看订单的状态

请求示例

```
GET 
https://bss.myhuaweicloud.com/v1.0/{domain_id}/common/order-mgr/orders-resource/CS2007281506xxxxx
```

响应示例

```
{
    "totalSize": 1,
    "resources": [
        {
            "resourceId": "01c*****5f7",
            "cloudServiceType": "hws.service.type.ec2",
            "regionCode": "xxxxx",
            "resourceType": "hws.resource.type.vm",
            "resourceSpecCode": "h1.8xlarge.4.gwc01",
            "resourceSize": null,
            "resouceSizeMeasureId": null,
            "status": 6
        }
}
```

响应示例中"status": 6说明订单状态为待付款。此时需要手动支付该订单

手动支付可以填写优惠券和折扣券等信息。

手动支付需要调用[支付包年/包月产品订单](https://support.huaweicloud.com/api-oce/api_order_00016.html)支付，以下示例是使用一张优惠券，优惠券类型为代金券的请求示例。

```
POST https://bss.myhuaweicloud.com/v2/orders/customer-orders/pay

{
    "coupon_infos": [
        {
            "id": "CP2005270256xxxxxx",
            "type": 301
        }
    ],
    "order_id": "CS2007281506xxxxx"
}
```

## 查询规格资源是否可购买/资源是否售罄<a name="section413314335610"></a>

如需查询某一具体的云服务器规格在某可用区是否资源充足，可以通过调用[查询规格详情和规格扩展信息列表](https://support.huaweicloud.com/api-ecs/zh-cn_topic_0020212656.html)查看该规格的详细信息。并通过响应信息中的cond:operation:status和cond:operation:az字段的取值判断在区域和可用区的取值。

例如查询华东上海二可用区一的资源情况，请求URI如下。

```
GET https://ecs.cn-east-2.myhuaweicloud.com/v1/05041fea8a8025662f4ac00927982f3e/cloudservers/flavors?availability_zone=cn-east-2a
```

响应信息

```
{
    "id": "c3.3xlarge.2", 
    "name": "c3.3xlarge.2", 
     ...
    "os_extra_specs": {
        "cond:spot_block:operation:az": "cn-east-2a(sellout),cn-east-2b(normal),cn-east-2c(normal),cn-east-2d(normal)",
        "cond:operation:az":  ,"cn-east-2d(sellout),cn-east-2a(normal),cn-east-2b(normal)"
        ...
        "cond:operation:status": "abandon", 
        "cond:spot_block:operation:interrupt_policy":  "cn-east-2d(immediate),cn-east-2a(immediate),cn-east-2b(immediate),cn-east-2c(immediate)", 
        "resource_type": "IOoptimizedC3_2"
    }
}
```

响应信息中通过cond:operation:status和cond:operation:az字段的取值判断资源是否可用。

优先查看cond:operation:az的取值，如果某个可用区没有在cond:operation:az参数中配置时默认使用cond:operation:status的取值。

例如本例中，c3.3xlarge.2在华东上海二的可用区一、可用区二正常商用，可用区四售罄，可用区三在在cond:operation:az中无配置信息，则以cond:operation:status的取值为准，即c3.3xlarge.2在华东上海二的可用区三下线。

## 付费方式<a name="section171001547869"></a>

创建包周期的云服务器时（chargingMode为prePaid），通过extendparam.isAutoPay字段控制订单的支付方式。

取值为true在订单创建完成后自动支付。

取值为false订单需要用户手动支付。手动支付可以填写优惠券和折扣券等信息。

手动支付需要调用[支付包年/包月产品订单](https://support.huaweicloud.com/api-oce/api_order_00016.html)接口进行支付，以下示例是使用一张优惠券，优惠券类型为代金券的请求示例。

```
POST https://bss.myhuaweicloud.com/v2/orders/customer-orders/pay

{
    "coupon_infos": [
        {
            "id": "CP2005270256xxxxxx",
            "type": 301
        }
    ],
    "order_id": "CS190401192xxxxxx"
}
```

## 查询资源的可用配额<a name="section14991749361"></a>

如需查询当前账号的资源配额信息，包括已使用的配额，可以通过调用[查询租户配额](https://support.huaweicloud.com/api-ecs/ecs_02_0801.html)接口。

```
GET https://ecs.cn-east-2.myhuaweicloud.com/v1/05041fea8a8025662f4ac00927982f3e/cloudservers/limits
```

响应信息如下，例如通过maxTotalInstances可以查看云服务器的最大申请数量，通过totalInstancesUsed可以查看当前云服务器使用个数。

```
{
	-"absolute": {
		"maxServerMeta": 128,
		"maxPersonality": 5,
		"maxImageMeta": 128,
		"maxPersonalitySize": 10240,
		"maxSecurityGroupRules": 20,
		"maxTotalKeypairs": 1000,
		"totalRAMUsed": 22528,
		"totalInstancesUsed": 4,
		"maxSecurityGroups": 10,
		"totalFloatingIpsUsed": 0,
		"maxTotalCores": 8000,
		"totalSecurityGroupsUsed": 1,
		"maxTotalFloatingIps": 10,
		"maxTotalInstances": 1000,
		"totalCoresUsed": 11,
		"maxTotalRAMSize": 16384000,
		"maxServerGroups": 32,
		"maxServerGroupMembers": 16,
		"totalServerGroupsUsed": 0,
		"maxTotalSpotInstances": 20,
		"maxTotalSpotCores": 320,
		"maxTotalSpotRAMSize": 655360,
		"totalSpotInstancesUsed": 0,
		"totalSpotCoresUsed": 0,
		"totalSpotRAMUsed": 0,
		"maxFaultDomainMembers": 200,
		"limit_by_flavor": []
	}
}
```

## 查询资源价格<a name="section44361551269"></a>

使用[查询按需产品价格](https://support.huaweicloud.com/api-oce/bcloud_01001.html)和[查询包年/包月产品价格](https://support.huaweicloud.com/api-oce/bcloud_01002.html)，根据云服务类型、资源类型、云服务区和资源规格四个条件来查询产品价格。

例如查询华东上海二可用区、通用计算型、Linux操作系统、s6.small.1规格的包月，一个月的价格。

```
POST https://bss.myhuaweicloud.com/v2/bills/ratings/period-resources/subscribe-rate
```

```
{
	"product_infos": [

		{
			   "id": "1",
			"cloud_service_type": "hws.service.type.ec2",
			"resource_type": "hws.resource.type.vm",
			"resource_spec": "s6.small.1.linux",
			"region": "cn-east-2",
			"available_zone": "cn-east-2a",
			"period_type": 2,
			"period_num": 1,
			"subscription_num": 1
		}
	],
	"project_id": "05041fea8a8025662f4ac00927982f3e"
}
```

响应信息如下所示，其中official\_website\_amount字段的取值即为包年/包月产品价格。

```
{
	-"official_website_rating_result": {
		"official_website_amount": 32.2,
		"measure_id": 1,
		-"product_rating_results": [-{
			"id": "1",
			"product_id": "00301-233164-0--0",
			"official_website_amount": 32.2,
			"measure_id": 1
		}]
	},
	"optional_discount_rating_results": [],
	"currency": "CNY"
}
```

