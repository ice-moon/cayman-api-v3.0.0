### 设置策略
`/api/cayman/archive/strategy/delete`

#### 接口说明
删除归档策略

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|strategyid|string|策略id|


#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/archive/strategy/delete \
-F strategyid=542c7161-5003-451a-bbba-63d7d284db72 \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
}
```

