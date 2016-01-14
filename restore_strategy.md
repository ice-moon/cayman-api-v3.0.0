### 按策略回迁
`/api/cayman/archive/restore/matchrule`

#### 接口说明
按策略回迁文件

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|storagyid|string|策略id|


#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/archive/restore/matchrule \
-F storagyid=teststrategyid \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
    "strategyid":"teststrategyid"
}

