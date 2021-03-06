### 获取元数据统计
`/api/cayman/store/stat/meta/get`

#### 接口说明
获取元数据统计

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|默认|
|--|--|--|--|--|
|key|string|true|统计事件key||
|sort|int|no|按size排序，0:不排序；1:正序；2:倒序|0|
|start|int|no|从第几条开始列举|0:从第一条开始|
|nums|int|no|列举个数|10|

#### 使用示例
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/meta/get\
-F key=test\
-F sort=2 \
-F start=0 \
-F nums=2
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
#####其他返回说明
|code|说明|
|--|--|
|400|参数无效|
|409|此事件元数据不存在|
|417|列举元数据统计事件失败|