### 读取文件对象数据
`/api/cayman/store/object/read`

#### 接口说明
读取已存在文件数据。

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|存储桶名|
|userid|string|yes|登录用户|
|objectid|string|yes|要读取的对象ID|
|offset|int64|yes|要读取的文件偏移量|
|length|int|yes|要读取连续多长的数据，单位byte|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/object/read \
-F bucket=bucket-z \
-F bucket=bucket-z \
-F objectid=directory1/a.txt \
-F offset=0 \
-F len=10
```

#### 返回数据类型
`binaray`

#### 返回结果
```json
直接返回内容的Buffer
```

