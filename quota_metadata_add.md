### 添加元数据配额
`/api/cayman/store/quota/add`

#### 接口说明
添加元数据配额 

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|quotaname|string|配额名|
|bucket|string|存储桶名|
|object|string|对象名|
|key|string|元数据键|
|value|string|元数据值|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/metadata/set \
-F username=testuser \
-F bucket=testbucket \
-F object=testobject \
-F key=aaa \
-F value=bbb
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
}
```