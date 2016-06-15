### 修改多个文件对象子用户
`/api/cayman/store/object/subuser/modifymulti`

#### 接口说明
修改多个文件对象子用户

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|存储桶名|
|objectids|string|yes|对象ID|
|newsubuser|string|yes|新添加的子用户|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/object/subuser/modifymulti \
-F bucket=bucket-z \
-F objectids=directory1/a.txt,test.txt   \
-F newsubuser=subuser2

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
|417|修改subuser失败|
|417|获取对象元数据失败|


