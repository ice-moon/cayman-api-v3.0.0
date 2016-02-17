### 读取文件对象数据
`/api/cayman/store/object/read`

#### 接口说明
读取已存在文件数据。

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|存储桶名|
|objectid|string|yes|要读取的对象ID|
|offset|int64|yes|要读取的文件偏移量|
|len|int|yes|要读取连续多长的数据，单位byte|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/object read \
-F bucket=bucket-z \
-F dir=/directory1 \
-F name=a.txt \
-F size=2022
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":	{
		"cayman_metadata_field_objectid":"directory1/a.txt",
		"cayman_metadata_field_username":	"anonymous",
		"cayman_metadata_field_bucket":	"bucket-z",
		"cayman_metadata_field_name":	"a.txt",
		"cayman_metadata_field_dir":	"/directory1",
		"cayman_metadata_field_lastmodifytime":	"1455673028",
		"cayman_metadata_field_createtime":	"1455673028",
		"cayman_metadata_field_type":	4,
		"cayman_metadata_field_type":	"0"
	}
}
```

