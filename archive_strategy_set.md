### 设置归档/回迁策略
`/api/cayman/archive/strategy/set`

#### 接口说明
设置归档/回迁策略

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|name|string|策略名|
|desc|string|策略描述|
|month|string|时间策略月|
|week|string|时间策略周|
|day|string|时间策略天|
|hour|string|时间策略时|
|minute|string|时间策略分|
|groupby|string|归档文件分组，type字段为restore时，此字段无效|
|device|string|策略归档设备，（默认tape）|
|matchrule|string|策略匹配规则，为json格式|
|ifremain|bool|是否保留源文件。如果type为restore，此字段无效|
|level|int|归档优先级|
|type|string|策略类型。"archive"、"restore"两种类型

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/archive/strategy/set \
-F name=testname \
-F desc=testdesc \
-F month=* \
-F week=* \
-F day=* \
-F hour=* \
-F minute=* \
-F groupby=* \
-F device=testdevice \
-F matchrule=[{"key":"testkey","value":"testvalue","match":"="}] \
-F ifremain=true \
-F level=50 \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
    "result":	{
		"strategyid":	"68dbf677-fc12-46ad-984d-648a52d0ea03"
	}
}
```

