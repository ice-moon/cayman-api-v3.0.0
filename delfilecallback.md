# 删除文件回调

#### 返回结果说明
|返回值|返回值类型|参数说明|
|--|--|--|
|taskid|string|任务id|
|strategyid|string|策略id|
|groupname|string|分组名|
|fileinfos|json|文件信息|
|AKgroup|string|AK归档组|
|deldaytime|int|文件信息|



#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
    “result”:{
          "taskid":"1"
          "strategyid":"test"
          "groupname":"vedio"
          "AKgroup":"group1"
          "deldaytime":10
          "successcount":200
          "failurecount":0
          "fileinfos":[{
                 "objectid":"test1"
                 "bucket":"bucket-z"
           },
           {
                 "objectid":"test1"
                 "bucket":"bucket-z"
           }]
    }
}
```

