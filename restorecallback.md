# 回迁回调

#### 返回结果说明
|返回值|返回值类型|参数说明|
|--|--|--|
|taskid|string|任务id|
|strategyid|string|策略id|
|fileinfos|json|文件信息|
|deldaytime|int|延迟删除时间|
|successcount|int|成功文件数|
|failurecount|int|失败文件数|



#### 返回数据类型
`JSON`

#### 返回结果
```json
{
    "code" : 200
    “result”:{
          "taskid":"1"
          "strategyid":"test"
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