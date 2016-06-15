### 上传文件对象
`/api/cayman/log/upload`

#### 接口说明
上传文件对象

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|存储桶名|
|object|string|yes|要创建的对象ID，ex：dir1/a.txt|
|subuser|string|no|子用户名|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/log/upload \
-F bucket=bucket-z \
-F object=directory1/a.txt \
-F subuser=test \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200
}
```


