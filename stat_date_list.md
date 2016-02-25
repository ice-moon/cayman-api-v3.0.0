### 列举日期维度统计

`/api/cayman/store/stat/meta/date/list`

#### 接口说明
获取日期空间使用统计

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|默认值|
|--|--|--|--|--|
|start|int|no|从最近第几天开始列举|0:从昨天开始|
|nums|int|no|往前列举统计的天数|7|


#### 使用示例
```
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/date/list\
-F nums=2
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":[
	    {
	        "date":"20160102"
    		"inc_size":	1024,
    		"inc_objnums": 512
		},
	    {
	        "date":"20160101"
    		"inc_size":	1024,
    		"inc_objnums": 512
		}
    ]
}
```