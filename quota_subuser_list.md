### 列举子用户配额
`/api/cayman/store/quota/subuser/list`

#### 接口说明
列举子用户名配额 

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|默认值|
|--|--|--|--|
|sort|int|no|按spaceused排序，0:不排序；1:正序；2:倒序|0|
|start|int|no|从第几条开始列举|0:从第一条开始|
|nums|int|no|列举个数|10|

#### 使用示例
```sh
curl -XPOST http://192.168.1.100/api/cayman/store/quota/subuser/list\
-F sort=2 \
-F start=0 \
-F nums=1 
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":{
      "total": 99,
      "source": [
        {
        "subuser": "test1", 
        "createtime": 1452654019, 
        "quotasize": 512000000, 
        "spaceused": 512, 
        "objectnums": 0
        }
      ]
    }
}
```