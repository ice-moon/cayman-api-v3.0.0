### 上传数据块
`/api/cayman/store/object/write`

#### 接口说明
针对已创建文件上传数据块，大小不超过4M。

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|对象所处桶名|
|dir|string|yes|创建的文件目录名|
|name|string|yes|文件名|
|size|int|no|要上传文件的真实大小,单位byte。默认为0，即上传一个空文件|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/object create \
-F bucket=testbucket \
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
		"cayman_metadata_field_objectid":	"dawei/a.txt",
		"cayman_metadata_field_username":	"anonymous",
		"cayman_metadata_field_bucket":	"bucket-z",
		"cayman_metadata_field_name":	"a.txt",
		"cayman_metadata_field_dir":	"/dawei",
		"cayman_metadata_field_lastmodifytime":	"1455673028",
		"cayman_metadata_field_createtime":	"1455673028",
		"cayman_metadata_field_type":	4,
		"cayman_metadata_field_type":	"0"
	}
}
```

