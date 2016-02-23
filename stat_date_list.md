### 列举日期维度统计

`/api/cayman/store/stat/meta/date/get`

#### 接口说明
获取日期空间使用统计

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|默认值|
|--|--|--|--|--|
|nums|int|true|列举最近的统计的天数|1|

#### 使用示例
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/date/get\
-F nums=10
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":	{
	    "total":2,
	    "source":[
    	    {
    	        "date":"2016-01-02"
        		"inc_size":	1024,
        		"inc_objnums": 512
    		},
    	    {
    	        "date":"2016-01-01"
        		"inc_size":	1024,
        		"inc_objnums": 512
    		}
	    ]
	}
}
```