### 获取日期维度统计

`/api/cayman/store/stat/meta/date/get`

#### 接口说明
获取日期空间使用统计

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|getdate|string|true|要获取统计的日期，获取某天:20160101, 获取某月:201601|

#### 使用示例1
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/date/get\
-F getdate=20160101
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
#### 使用示例2
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/date/get\
-F getdate=201601
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":	{
		"date":	"201601",
		"mon_inc_objnums":	21,
		"mon_inc_size":	21,
		"source":	[ {
				"date":	"20160122",
				"inc_objnums":	10,
				"inc_size":	10
			}, {
				"date":	"20160121",
				"inc_objnums":	11,
				"inc_size":	11
			}]
	}
}
```
#####其他返回说明
|code|说明|
|--|--|
|400|参数无效|
|409|日期统计不存在|
|417|获取元数据失败|