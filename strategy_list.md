### 列举策略
`/api/cayman/archive/strategy/list`

#### 接口说明
列举所有策略

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|type|string|要列举什么类型的策略."archive" or "restore",默认为"all"
|page|int|列举第几页内容，默认为1|
|perpage|int|每页列举内容条数，默认20|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/archive/strategy/list \
-F from=0 \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
    "result":	{
		"strategies":	[{
				"cayman_archive_strategy_id":	"68dbf677-fc12-46ad-984d-648a52d0ea03",
				"cayman_archive_strategy_yname":	"wss",
				"cayman_archive_strategy_desc":	"This is an archive strategy.",
				"cayman_archive_strategy_matchrule":	"[{\"key\":\"test\",\"value\":\"test\",\"match\":\"=\"}]",
				"cayman_archive_strategy_time":	"* * * * *",
				"cayman_archive_strategy_groupby":	"*",
				"cayman_archive_strategy_device":	"",
				"cayman_archive_strategy_ifremain":	true,
				"cayman_archive_strategy_level":	50,
				"cayman_archive_strategy_status":	-1,
				"cayman_archive_strategy_type":	"archive"
			}]
	}
}
```

