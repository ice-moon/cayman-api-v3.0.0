### 获取子用户配额
`/api/cayman/store/quota/subuser/get`

#### 接口说明
获取子用户配额 

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|subuser|string|yes|子用户名|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/quota/subuser/get \
-F subuser=test1
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":{
        "subuser": "test1", 
        "createtime": 1452654019, 
        "quotasize": 512000000, 
        "spaceused": 0, 
        "objectnums": 0
    }
}
```
#####其他返回说明
|code|说明|
|--|--|
|400|参数无效|
|417|获取子用户配额失败|