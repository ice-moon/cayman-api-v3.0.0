### 获取元数据
`/api/cayman/store/metadata/get`

#### 接口说明
获取object元数据

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|username|string|yes|用户名|
|bucket|string|yes|存储桶名|
|object|string|yes|对象名|
|key|string|yes|元数据键|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/metadata/get \
-F username=testuser \
-F bucket=testbucket \
-F object=testobject \
-F key=aaa
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":	{
		"aaa":	"bbb"
	}
}
```