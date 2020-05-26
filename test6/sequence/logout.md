 [返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/logout.md)

```
@startuml
title 基于GitHub的实验管理平台--登出的顺序图
actor users
database "前端存储Cookie\nSessionStorage" as 前端存储
users -> 前端存储 :点击登出
前端存储 --> users :销毁session，登出成功。
@enduml
```
