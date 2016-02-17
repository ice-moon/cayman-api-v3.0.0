### 下载整个文件对象
`/api/cayman/store/object/download`

#### 接口说明
下载整个文件对象

#### HTTP请求类型
`Get`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|存储桶名|
|objectid|string|yes|要读取的对象ID|

#### 使用示例
```sh
curl -XGET http://192.168.1.100/api/cayman/store/object/download？debug=true&bucket=bucket-z&objectid=directory1/a.txt
```

#### 返回数据类型
`binaray`

#### 返回结果
```json
直接返回整个
```

