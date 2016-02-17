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
|objectid|string|yes|对象ID|
|offset|int64|yes|写入数据块的起始位置|
|len|int|yes|写入数据块大小|
|PostData|binary|yes|具体上传的文件数据块，在HTTP 请求body中以multipart/form-data 格式上传，详解见以下说明|



---
POST /api/cluster/storage/file/write HTTP/1.1
ACCESS-TOKEN: M2VlODJmMmItMzI0NC00ZDc2LWFhMDYtNjQ1Yzc5ODc1NjVl
Authorization: DATATOM DATATOM4UAcOR3uLx3bx49kIDdAhaRCAr:RTlGNjU3N0EyOTM2RkMyRkQxQTAzQkUyN0FBQUJEM0VDMjRBQ0Y0MA==
Connection: Close
Transfer-Encoding: chunked
Content-Type: multipart/form-data; boundary=wodmd5zTpvSlfvcSNu_awTp7nzXgWIZin3D
Host: 192.168.1.100
User-Agent: Apache-HttpClient/4.3.4 (java 1.5)
Accept-Encoding: gzip,deflate

--wodmd5zTpvSlfvcSNu_awTp7nzXgWIZin3D

Content-Disposition: form-data; name="fileid"
Content-Type: text/plain; charset=ISO-8859-1
Content-Transfer-Encoding: 8bit

--wodmd5zTpvSlfvcSNu_awTp7nzXgWIZin3D

Content-Disposition: form-data; name="PostData"; filename="multipart/form-data"
Content-Type: PostData
Content-Transfer-Encoding: binary

filecontent

--wodmd5zTpvSlfvcSNu_awTp7nzXgWIZin3D--
---

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

