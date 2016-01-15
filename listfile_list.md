### 列举文件
`/api/cayman/archive/listfile/list`

#### 接口说明
列举文件

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|strategyid|string|策略id|
|isarchived|int|是否归档（归档为1，未归档为0）|
|starttime|int64|开始时间|
|endtime|int64|结束时间|
|page|int|列举第几页内容，默认为1|
|perpage|int|每页列举内容条数，默认20|


#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/archive/listfile/list \
-F strategyid=teststrategyid \
-F isarchived=0 \
-F starttime=1313334344421 \
-F endtime=15121244342323 \
-F offset=0 \
-F offend=100 \
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
	"result":	[{
		"cayman_metadata_field_match_strategy":	"test",
		"cayman_metadata_field_isarchive":	"0",
		"cayman_metadata_field_lastarchivetime":	134,
		"cayman_archive_strategy_matchrule":	"[{\"key\":\"test\",\"value\":\"test\",\"match\":\"=\"}]",
		"cayman_archive_strategy_time":	"2",
		"cayman_archive_strategy_groupby":	"*",
		"cayman_archive_strategy_device":	"",
		"cayman_archive_strategy_ifremain":	true,
		"cayman_archive_strategy_level":	50,
		"cayman_archive_strategy_status":	-1
	}]
}
```

