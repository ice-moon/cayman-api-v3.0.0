### 获取元数据实时key统计
`/api/cayman/store/stat/meta/getbykey`

#### 接口说明
获取元数据实时key统计

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|默认|
|--|--|--|--|--|
|key|string|true|统计的元数据key||
|sort|int|no|按size排序，0:不排序；1:正序；2:倒序|0|
|nums|int|no|列举个数|10|

#### 使用示例
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/meta/getbykey\
-F key=filetype\
-F sort=2 \
-F nums=2
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":{
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
#####其他返回说明
|code|说明|
|--|--|
|400|参数无效|
|417|获取统计失败|
