# 结合华为云KMS服务<a name="ecs_03_1413"></a>

华为云KMS服务内置了对擎天Enclave证明的支持。通过使用擎天Enclave SDK中包含的华为云KMS API，您可以在擎天Enclave实例中基于擎天Enclave证明来执行华为云KMS操作，比如解密、生成随机数和加密等操作。华为云KMS服务提取来自擎天Enclave的证明文档并根据预设的IAM授权策略对其进行访问权限控制。

比如，如下是一个IAM授权策略的举例。该授权策略允许调用KMS的解密数据或解密数据密钥功能API，但限制条件是要求请求者必须在擎天Enclave环境中运行，且Enclave的度量值PCR0和PCR8都必须和指定的PCR值相同。

```
{ 
    "Version": "1.1", 
    "Statement": [ 
        { 
            "Effect": "Allow", 
            "Action": [ 
                "kms:cmk:decrypt", 
                "kms:dek:decrypt" 
            ], 
            "Resource": "*", 
            "Condition": { 
                "StringEqualsIgnoreCase": { 
                    "kms:RecipientAttestation/PCR0": [ 
                        "c5158cb6ee9dbb0ead648c3dc80e472c85e0d67f19fb53fbd3fb94c3371aec63cdb93b80d727a7084248873b1d8e8b41" 
  
                    ], 
                    "kms:RecipientAttestation/PCR8": [ 
                        "705afb1012d27f4e07a25e674e6a17dec57305e29cd412184b7bcb78d9e67f16a0cc26d8706a4fab418a5da5788bc949" 
                    ] 
                } 
            } 
        }
     ]
}
```

