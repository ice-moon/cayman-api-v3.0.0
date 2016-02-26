### 异步计算文件MD5值
`/api/cayman/store/object/md5/calc/sync`

#### 接口说明
异步计算文件md5值，计算后结果可根据查询接口单独查询文件md5值。或通过本接口回调参数进行结果回调。此接口使用所有文件，无大小限制。回调http访问post类型。

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|存储桶名|
|objectid|string|yes|对象ID|
|callback_ip|string|no|回调ip|
|callback_port|string|no|回调端口|
|callback_uri|string|no|回调请求URI|
#### 回调参数
|参数名|类型|必选|说明|
|--|--|--|--|
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
	"code":	200，
}
```
#### 回调访问
```json
{
	"code":	200，
}
```
