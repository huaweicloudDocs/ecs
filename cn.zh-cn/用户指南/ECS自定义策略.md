# ECS自定义策略<a name="ZH-CN_TOPIC_0170265914"></a>

如果系统预置的ECS权限，不满足您的授权要求，可以创建自定义策略。自定义策略中可以添加的授权项（Action）请参考[《ECS API参考》](https://support.huaweicloud.com/api-ecs/zh-cn_topic_0020805967.html)中“ 策略及授权项说明”章节_。_

目前华为云支持以下两种方式创建自定义策略：

-   可视化视图创建自定义策略：无需了解策略语法，按可视化视图导航栏选择云服务、操作、资源、条件等策略内容，可自动生成策略。
-   JSON视图创建自定义策略：可以在选择策略模板后，根据具体需求编辑策略内容；也可以直接在编辑框内编写JSON格式的策略内容。

具体创建步骤请参见：[创建自定义策略](https://support.huaweicloud.com/usermanual-iam/iam_01_0605.html)。本章为您介绍常用的ECS自定义策略样例。

## ECS自定义策略样例<a name="section51981826152017"></a>

-   示例1：授权用户批量关闭云服务、删除云服务

    ```
    { 
        "Version": "1.1", 
        "Statement": [ 
            { 
                "Effect": "Allow", 
                "Action": [ 
                    " 
                         ecs:servers:stop 
                         ecs:servers:get 
                     " 
                ] 
            } 
        ] 
    }
    ```

-   示例2：拒绝用户删除云服务器

    拒绝策略需要同时配合其他策略使用，否则没有实际作用。用户被授予的策略中，一个授权项的作用如果同时存在Allow和Deny，则遵循Deny优先。

    如果您给用户授予ECS Admin的系统策略，但不希望用户拥有ECS admin中定义的删除云服务器权限，您可以创建一条拒绝删除云服务的自定义策略，然后同时将ECS Admin和拒绝策略授予用户，根据Deny优先原则，则用户可以对ECS执行除了删除云服务器外的所有操作。拒绝策略示例如下：

    ```
    { 
          "Version": "1.1", 
          "Statement": [ 
                { 
    		  "Effect": "Deny", 
                      "Action": [ 
                            "ecs:cloudServers:delete" 
                      ] 
                } 
          ] 
    }
    ```


