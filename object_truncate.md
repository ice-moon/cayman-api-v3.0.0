### 截断文件对象
`/api/cayman/store/object/truncate`

#### 接口说明
截断文件对象到指定大小。

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|存储桶名|
|objectid|string|yes|对象ID|
|newsize|int64|yes|指定要截断文件后的大小|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/object/exist \
-F bucket=bucket-z \
-F objectid=directory1/a.txt \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200
}
```

