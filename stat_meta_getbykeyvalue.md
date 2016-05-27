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
curl -XPOST http://192.168.1.100/api/cayman/store/stat/meta/meta/getbykeyvalue\
-F key=filetype\
-F value=video
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":{
        "objnums":5120
        "size":5120000
    }
}
```
#####其他返回说明
|code|说明|
|--|--|
|400|参数无效|
|409|此事件元数据已存在|
|417|获取统计信息失败|
