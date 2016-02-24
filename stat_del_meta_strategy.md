### 删除元数据统计事件
`/api/cayman/store/stat/meta/strategy/del`

#### 接口说明
删除元数据统计事件

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|id|string|true|统计事件id|

#### 使用示例
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/strategy/del\
-F id=8b74b9ce-f9d5-49de-a630-723a30ef2389
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200
}
```