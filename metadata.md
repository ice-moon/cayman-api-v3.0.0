# 元数据服务

## 设置元数据
`/store/metadata/set`

### 接口说明
设置object元数据

### 返回类型格式
`JSON`

### HTTP请求类型
`POST`

### 请求参数
|参数名|参数类型|参数说明|
|--|--|--|
|username|string|用户名|
|bucket|string|存储桶名|
|object|string|对象名|
|key|string|元数据键|
|value|string|元数据值|

### 返回结果
```json
{
    "code" : 200
}
```

### 使用示例
```bash
curl -XPOST http://192.168.1.100/store/metadata/set \
-F username=zltest \
-F bucket=zltestbucket&object=zltestobject&key=aaa&value=bbb
```