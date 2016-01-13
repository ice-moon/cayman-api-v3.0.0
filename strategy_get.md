### 获取策略
`/api/cayman/archive/strategy/get`

#### 接口说明
获取归档策略

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|strategyid|string|策略id|


#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/archive/strategy/get \
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

