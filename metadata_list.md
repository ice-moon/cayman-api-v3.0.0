### 获取所有元数据
`/api/cayman/store/metadata/list`

#### 接口说明
列举object所有元数据

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|username|string|yes|用户名|
|bucket|string|yes|存储桶名|
|object|string|yes|对象名|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/metadata/list \
-F username=testuser \
-F bucket=testbucket \
-F object=testobject 
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":	{
		"aaa":	"bbb",
		"aaa1":	"bbb1",
		"aaa2":	"bbb2"
	}
}
```