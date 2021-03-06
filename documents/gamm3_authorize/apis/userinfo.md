# 获取用户基本信息

接口地址：

> https://gamm3.ztgame.com/sns/account/userinfo

调用方式：   
**post**

参数：

| 参数         |  是否必须 | 说明       |
| ---         |  --- | ---       |
| appid        | 是      | 应用唯一标识 |
| access_token | 是      | 接口调用凭证 |
| openid       | 是      | 用户对应应用唯一标识|
| sign         | 是      | 签名串，见[签名算法](../signAlgorithm.md)|


正确返回示例：

```
{
    code: 0,
    msg: '成功',
    data: {
        'account': 'bigWame',
        'tname': '王五',
        'nickname': '大肚子',
        'phone': '17777777777',
        'sex': '1',
        'birth": '2005-03-28'
    }
}
```

**参数说明：**
| account | 说明  |
| ---     | ---    |
| account | 巨人通行证账号 |
| nickname | 昵称 |
| tname    | 真实姓名 |
| sex | 性别 
| birth | 生日 |

**错误示例**

```
{
    code: '30001',
    msg: '签名错误',
    data:{}
}
```