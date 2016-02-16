### 删除元数据配额
`/api/cayman/store/quota/del`

#### 接口说明
删除元数据配额 

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|quotaname|string|yes|配额名|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/quota/del \
-F quotaname=videoquota
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
}
```