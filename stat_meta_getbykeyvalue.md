### 获取元数据实时keyvalue统计
`/api/cayman/store/stat/meta/getbykeyvalue`

#### 接口说明
获取元数据实时keyvalue统计

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|--|
|key|string|true|统计的元数据key|
|value|string|true|统计的元数据value|

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
