 [返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/rechage_info.md)
```

@startuml
actor users
database 数据库
users -> 数据库 :修改请求，接受修改数据。
数据库 --> users :反馈信息，修改成功。
@enduml

```