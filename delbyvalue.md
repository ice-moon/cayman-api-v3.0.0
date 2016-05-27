### 删除元数据
`/api/cayman/store/metadata/delbyvalue`

#### 接口说明
删除所有匹配到值的值

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|username|string|yes|用户名|
|bucket|string|yes|存储桶名|
|kv|string|yes|元数据键值（支持一次性删除多个键的值，但是只能一次性删除一个键的一个值）|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/metadata/delbyvalue \
-F username=testuser \
-F bucket=testbucket \
-F kv=[{"key":"yy","value":"wss"}]
```
#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200
}
```
#####其他返回说明
|code|说明|
|--|--|
|400|参数无效|
|409|此元数据无权限修改|
|417|删除元数据的值失败|