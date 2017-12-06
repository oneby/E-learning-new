## 记录
___


1. 用户
    > 通过字段 role 来判断权限
    * 管理员
        * role >= 50
    * 教师用户
        * role >= 20 && role < 50
    * 普通用户
        * role >= 0 && role < 20
    * 黑名单
        * role < 0
    ```javascript
    const UserDataSchema = new Schema({
        name: String,
        password: String,
        email: String,
        role: String
    })
    ```
    * 管理员可录入用户
2. 文件 
    * 上传
    * 下载