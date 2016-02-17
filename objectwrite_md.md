### 上传数据块
`/api/cayman/store/object/write`

#### 接口说明
针对已创建文件上传数据块，大小不超过4M。

#### HTTP请求类型
`POST`

#### 请求参数
|参数名|类型|必选|说明|
|--|--|--|--|
|bucket|string|yes|对象所处桶名|
|objectid|string|yes|对象ID|
|offset|int64|yes|写入数据块的起始位置|
|len|int|yes|写入数据块大小|


#### 请求数据流部分

---
POST /api/cluster/storage/file/write HTTP/1.1
ACCESS-TOKEN: M2VlODJmMmItMzI0NC00ZDc2LWFhMDYtNjQ1Yzc5ODc1NjVl
Authorization: DATATOM DATATOM4UAcOR3uLx3bx49kIDdAhaRCAr:RTlGNjU3N0EyOTM2RkMyRkQxQTAzQkUyN0FBQUJEM0VDMjRBQ0Y0MA==
Connection: Close
Transfer-Encoding: chunked
Content-Type: multipart/form-data; boundary=wodmd5zTpvSlfvcSNu_awTp7nzXgWIZin3D
Host: 192.168.1.100
User-Agent: Apache-HttpClient/4.3.4 (java 1.5)
Accept-Encoding: gzip,deflate

--wodmd5zTpvSlfvcSNu_awTp7nzXgWIZin3D

Content-Disposition: form-data; name="fileid"
Content-Type: text/plain; charset=ISO-8859-1
Content-Transfer-Encoding: 8bit

--wodmd5zTpvSlfvcSNu_awTp7nzXgWIZin3D

Content-Disposition: form-data; name="PostData"; filename="multipart/form-data"
Content-Type: PostData
Content-Transfer-Encoding: binary

filecontent

--wodmd5zTpvSlfvcSNu_awTp7nzXgWIZin3D--

#### 使用示例
```sh
	Javascript 上传文件示例（代码片段）： 
					 
	var formData = new FormData();
        var func = (opts.file.mozSlice ? 'mozSlice' : (opts.file.webkitSlice ? 'webkitSlice' : 'slice'));

		// 文件数据块
        formData.append("file", opts.file[func](startSize, endSize));
        
		// 其他参数		
		formData.append("fileid", opts.fileid);
        formData.append("offset", startSize);
        formData.append("length", endSize - startSize);
        formData.append("filesize", size);
        var xhr = new XMLHttpRequest();
        xhr.open("POST", opts.target);
        xhr.setRequestHeader('Authorization', oauth);
        xhr.setRequestHeader('ACCESS-TOKEN', token);
        xhr.onreadystatechange = function(){
            if (xhr.readyState === 4){
                if(canceled) return;
                try{
                    var result = JSON.parse(xhr.responseText);
                    if(result.code === 200){
                        done = true;
                        owner.progress();
                        sendData();
                    }else{
                        done = false;
                        owner.onerror(result.msg);
                    }
                }catch(e){
                    owner.onerror("unknow error "+e);
                }
            }
        }
        xhr.send(formData);
```

#### 返回数据类型
`JSON`

#### 返回结果
```json
{
	"code":	200,
	"result":	{
		"md5":"3a0febb9c40b0f6b9094b919a30525b4"
	}
}
```

