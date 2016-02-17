### 列举桶内文件对象
`/api/cayman/store/bucket/listobject`

#### 接口说明
列举指定桶内文件对象

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|要列举哪个桶内的文件对象|
|dirname|string|no|要列举桶内哪个目录下文件，默认"/",即根目录下文件对象|
|page|int|no|列举第几页文件对象，默认为1|
|perpage|int|no|列举多少个文件对象，默认为20|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/bucket/listobject
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"total":	"36",
	"result":	[{
			"cayman_metadata_field_objectid":	"FFFFFF.txt",
			"cayman_metadata_field_bucket":	"bucket-z",
			"cayman_metadata_field_username":	"anonymous",
			"cayman_metadata_field_name":	"FFFFFF.txt",
			"cayman_metadata_field_dir":	"/",
			"cayman_metadata_field_size":	18,
			"cayman_metadata_field_createtime":	1455605018,
			"cayman_metadata_field_lastmodifytime":	1455606415,
			"cayman_metadata_field_type":	0,
			"cayman_metadata_field_subuser":	""
		}, {
			"cayman_metadata_field_objectid":	"ZZZZZ.txt",
			"cayman_metadata_field_bucket":	"bucket-z",
			"cayman_metadata_field_username":	"anonymous",
			"cayman_metadata_field_name":	"ZZZZZ.txt",
			"cayman_metadata_field_dir":	"/",
			"cayman_metadata_field_size":	9,
			"cayman_metadata_field_createtime":	1455604910,
			"cayman_metadata_field_lastmodifytime":	1455604910,
			"cayman_metadata_field_type":	0,
			"cayman_metadata_field_subuser":	""
		}]
```

