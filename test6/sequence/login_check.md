 [返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/login_check.md)


```
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor #Black
skinparam titleFontSize 24
Title 登录认证流程图

database "前端存储Cookie\nSessionStorage" as 前端存储
actor Login页面
actor API服务
database 数据库存储

== Login登录页面 ==
数据库存储->数据库存储:有每个用户的账号信息
API服务->API服务:生成接口服务
Login页面->API服务:点击事件
API服务->Login页面:
Login页面->Login页面:用户输入用户名和密码，进行登陆操作
API服务->API服务:使用RSA根据私钥解密收到的加密密码，得到用户密码
API服务->数据库存储:从数据库取出用户名以及hash密码
数据库存储->API服务:比对输入的用户名和密码是否匹配
API服务->前端存储:调用login_user(),\n将用户的ID值写到'session'中\n并设置失效时间
API服务->Login页面:返回成功信息
== 登陆后会将当前用户存入session==

@enduml

```