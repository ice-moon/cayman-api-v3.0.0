### 删除元数据
`/api/cayman/store/metadata/del`

#### 接口说明
删除object元数据

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
curl -XPOST http://192.168.1.100/api/cayman/store/metadata/del \
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
	"code":	200
}
```
#####其他返回说明
|code|说明|
|--|--|
|400|参数无效|
|409|此元数据无权限修改|
|417|删除元数据失败|