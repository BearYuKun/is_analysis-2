 [返回](https://github.com/wangfan212/is_analysis/blob/master/test6/rechange_password.md)

```
@startuml
title 修改密码的顺序图
actor users
database 数据库
database "前端存储Cookie\nSessionStorage" as 前端存储
users -> 前端存储 :修改密码
前端存储 --> 数据库 :将新密码写入数据库
数据库 --> users :修改成功

@enduml
```