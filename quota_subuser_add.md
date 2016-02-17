### 添加子用户配额
`/api/cayman/store/quota/subuser/add`

#### 接口说明
添加子用户配额 

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|默认值|
|--|--|--|--|--|
|subuser|string|yes|子用户名||
|quotasize|int64|no|配额值|0:无限制|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/quota/subuser/add \
-F subuser=user1 \
-F quotasize=512000000
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
}
```