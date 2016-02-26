### 同步计算文件MD5值
`/api/cayman/store/object/md5/calc/sync`

#### 接口说明
同步计算文件md5值，同步返回结果。注：此接口不适用于大于100M的文件，文件过大建议使用异步计算接口！

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|存储桶名|
|objectid|string|yes|对象ID|
|newsubuser|string|yes|新添加的子用户|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/object/md5/calc/sync \
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

