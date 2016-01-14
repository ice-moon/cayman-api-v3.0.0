### 修改元数据配额
`/api/cayman/store/quota/modify`

#### 接口说明
修改元数据配额 

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|默认值|
|--|--|--|--|--|
|quotaname|string|yes|配额名||
|description|string|no|配额描述|空字符串|
|quotamaxsize|int64|no|默认配额值|-1:无限制|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/quota/modify \
-F quotaname=videoquota \
-F description=videoquota \
-F quotamaxsize=1024000000
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
}
```