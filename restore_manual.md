### 手动回迁文件
`/api/cayman/archive/restorebymanual`

#### 接口说明
手动回迁文件

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|fileinfos|string|文件信息|



#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/archive/restorebymanual \
-F fileinfos=[{"objectname":"test","bucket":"bucket-z"},{"objectname":"test1","bucket":bucket-z}] \
-F callbackip=192.168.1.1 \
-F callbackport=21000 \
-F callbackurl=/cayman/test/callback \
-F callbackkey=type \
-F callbackcustom=test \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
    "result":[{
         "objectname":"test"
         "bucket":"bucket-z"
         "strategyname":"test"
    },
    {
         "objectname":"test1"
         "bucket":"bucket-z"
         "strategyname":"test1"
    }]
}
```

