### 设置归档回调
`/api/cayman/archive/set/archivecallback`

#### 接口说明
设置归档回调接口

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|callbackip|string|回调ip|
|callbackport|int|回调端口|
|callbackurl|string|回调url|



#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/archive/archivebymanual \
-F callbackip=192.168.1.1 \
-F callbackport=21000 \
-F callbackurl=/cayman/test/callback \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
}
```


