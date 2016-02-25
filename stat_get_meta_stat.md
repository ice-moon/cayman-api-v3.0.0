### 获取元数据统计
`/api/cayman/store/stat/meta/get`

#### 接口说明
获取元数据统计

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|默认|
|--|--|--|--|--|
|id|string|true|统计事件id||
|sort|int|no|按size排序，0:不排序；1:正序；2:倒序|0|
|start|int|no|从第几条开始列举|0:从第一条开始|
|nums|int|no|列举个数|10|

#### 使用示例
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/meta/get\
-F id=7b910c4c-3fe5-4bb9-812f-82a4860fb352\
-F sort=2\
-F start=0 \
-F nums=1 
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
		"createtime":	1456192187,
		"description":	"各文件类型分类统计",
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