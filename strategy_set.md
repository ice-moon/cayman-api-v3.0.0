### 设置策略
`/api/cayman/archive/strategy/set`

#### 接口说明
设置归档策略

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|name|string|策略名|
|desc|string|策略描述|
|month|string|策略月|
|week|string|策略周|
|day|string|策略天|
|hour|string|策略时|
|minute|string|策略分|
|groupby|string|策略分组|
|device|string|策略归档设备|
|matchrule|string|策略匹配规则|
|ifremain|bool|是否保留源文件|
|level|int|归档优先级|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/metadata/set \
-F name=testname \
-F desc=testdesc \
-F month=* \
-F week=* \
-F day=bbb
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
}
```

