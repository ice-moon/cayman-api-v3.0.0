### 手动归档文件
`/api/cayman/archive/archivebymanual`

#### 接口说明
手动归档文件

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|user|string|用户名|
|bucket|string|桶名|
|objid|string|文件id|


#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/archive/archivebymanual \
-F bucket=testbucket \
-F objid=testobjid \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
}
```
