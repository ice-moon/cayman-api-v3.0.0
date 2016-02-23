### 获取元数据统计
`/api/cayman/store/stat/meta/list`

#### 接口说明
获取元数据统计

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|默认|
|--|--|--|--|--|
|id|string|true|策略id||
|nums|int|no|列举个数|0:全部|
|sort|bool|no|是否按空间使用量倒序排序|false|

#### 使用示例
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/list\
-F id=7b910c4c-3fe5-4bb9-812f-82a4860fb352\
-F nums=1 \
-F sort=true
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":{
	    "total":99,
	    "key":"filetype",
    	"source":[
	    {
	        "value":"video",
	        "objnums":5120
	        "size":5120000
	    },
	    {
	        "value":"audio",
	        "objnums":512
	        "size":512000
	    }
    	]
    }
}
```