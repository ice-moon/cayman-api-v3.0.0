### 获取基本元数据
`/api/cayman/store/metadata/list/base`

#### 接口说明
列举object基本元数据

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|username|string|用户名|
|bucket|string|存储桶名|
|object|string|对象名|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/metadata/list/base \
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
		"dana_objectsize":	"1024",
		"dana_lastModified":	"1450751410360"
	}
}
```