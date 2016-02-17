### 删除文件对象
`/api/cayman/store/object/remove`

#### 接口说明
通知cayman完成文件上传。

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|存储桶名|
|objectid|string|yes|对象ID|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/object finish \
-F bucket=bucket-z \
-F objectid=directory1/a.txt

```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200
}
```

