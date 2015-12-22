### 获取元数据
`/store/metadata/get`

#### 接口说明
获取object元数据

#### 返回类型格式
`JSON`

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|username|string|用户名|
|bucket|string|存储桶名|
|object|string|对象名|
|key|string|元数据键|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/store/metadata/get \
-F username=testuser \
-F bucket=testbucket \
-F object=testobject \
-F key=aaa
```

#### 返回结果
```json
{
	"code":	200,
	"result":	{
		"aaa":	"bbb"
	}
}
```