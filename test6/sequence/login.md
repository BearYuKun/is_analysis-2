 [返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/login.md)

```
@startuml
title 基于GitHub的实验管理平台--登录的顺序图
actor users
database 数据库
users -> 数据库 :输入用户名密码
数据库 -->users :验证密码与用户名，成功即登录。
@enduml
```
