### 获取元数据统计
`/api/cayman/store/stat/meta/get/multi`

#### 接口说明
根据值获取统计信息

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|默认|
|--|--|--|--|--|
|statquery|string|true|统计事件id||

#### statquery语句语法说明
|字段|释义|必选|说明|
|--|--|--|--|
|key|查询的key值|yes|可填多组|
|relation|查询的key值与value的关系|yes|值为"include","must"分别为包含和绝对等于的意思|
|value|查询的value值|yes|可填多组|
#### 使用示例
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/meta/get/multi\
-F id={"name":[{"relation":"include","value":"abcd"}],"type":[{"relation":"must","value":"video"}],"uuid":[{"relation":"must","value":"test"},{"relation":"should","value":"test1"}]}
```
其中name/type/uuid为key值，其中key值中的json数组可为多个，之间为and关系，参照uuid key值写法。
#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":	{
		"name":	[{
				"value":	"abcd",
				"objnums":	1,
				"size":	533369
			}],
		"type":	[{
				"value":	"video",
				"objnums":	1,
				"size":	77244
			}],
		"uuid":	[{
				"value":	"test",
				"objnums":	2,
				"size":	146153
			}]
	}
}
```
#####其他返回说明

|code|说明|
|--|--|
|400|参数无效|
|417|查询统计信息失败|

