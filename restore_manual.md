### 手动回迁文件
`/api/cayman/archive/restore/objectid`

#### 接口说明
手动回迁文件

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
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
