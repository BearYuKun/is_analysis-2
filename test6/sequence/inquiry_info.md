 [返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/inquiry_info.md)

```
@startuml
title 基于GitHub的实验管理平台--查看用户信息的顺序图
actor users
database 数据库
users -> 数据库 :查看用户信息
数据库 -->users :返回用户查询的信息
@enduml
```