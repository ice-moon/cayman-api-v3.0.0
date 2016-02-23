### 获取日期维度统计

`/api/cayman/store/stat/meta/date/get`

#### 接口说明
获取日期空间使用统计

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|getdate|string|true|要获取统计的日期，格式:2016-01-01|

#### 使用示例
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/date/get\
-F getdate=2016-01-01
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":	{
		"inc_size":	1024,
		"inc_objnums": 512
	}
}
```