### 创建一个桶
`/api/cayman/store/bucket/create`

#### 接口说明
创建一个桶，隶属于请求的有效授权用户。

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|要创建存储桶名|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/bucket/create \
-F bucket=bucket-z \
-F objectid=directory1/a.txt \
-F size=2022 \
-F subuser=subuser1
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
		"cayman_metadata_field_size":	"0",
		"cayman_metadata_field_subuser": "subuser1"
	}
}
```

