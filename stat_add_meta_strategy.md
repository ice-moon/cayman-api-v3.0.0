### 添加元数据统计策略
`/api/cayman/store/stat/meta/strategy/add`

#### 接口说明
添加元数据统计策略

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|key|string|true|基于元数据key进行统计|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/strategy/add
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200
}
```