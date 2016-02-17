### 列举用户所有桶
`/api/cayman/store/bucket/list`

#### 接口说明
列举请求有效授权用户的所有桶。

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|无|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/bucket/remove \
-F bucket=bucket-z \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200
}
```

