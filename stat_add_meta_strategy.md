### 添加元数据统计事件
`/api/cayman/store/stat/meta/strategy/add`

#### 接口说明
添加元数据统计事件

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|key|string|true|基于元数据key进行统计|
|description|string|false|统计事件描述|

#### 使用示例
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/strategy/add\
-F key=filetype\
-F description=各文件类型分类统计
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":	{
		"id":	"7b910c4c-3fe5-4bb9-812f-82a4860fb352",
		"key":	"filetype",
		"createtime":	1456192187,
		"description":	"各文件类型分类统计"
	}
}
```
#####其他返回说明
|code|说明|
|--|--|
|400|参数无效|
|409|此事件元数据已存在|
|417|添加元数据统计事件失败|