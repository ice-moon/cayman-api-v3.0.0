### 查询指定文件的MD5值
`/api/cayman/store/object/md5/query`

#### 接口说明
查询文件对象MD5值，不会重新计算，直接查询之前计算结果，如无计算过，返回为空。

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|存储桶名|
|objectid|string|yes|对象ID|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/object/md5/query \
-F bucket=bucket-z \
-F objectid=directory1/a.txt    

```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200，
	"result":{
	    "md5":"4048733e5169de433046c96dc63a9860"
	}
}
```

