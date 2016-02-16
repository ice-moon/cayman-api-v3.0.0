### 对象管理
---------

文件上传数据块限制大小为4M，超出 4M的文件应该采用分块上传	机制（每次上传小于4M，下图是文件上传的一般流程：




(1) 创建文件 --/api/cayman/storage/object/create
(2) 上传数据块 --/api/v2/core/object/write
(3) 大于4M的文件重复 （2）的步骤，上传时指定 offset, len
(4) 上传完成后调用 finish 接口，通知服务器上传完成 --/api/v2/core/object/finish
(5) 服务器后台会自动对文件进行索引等操作。