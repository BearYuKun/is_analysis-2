
[返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/README.md)

```
@startuml
actor teachers
actor students
actor users
users <|-- teachers
users <|-- students
package 业务用例集 {
teachers ---> (选择课程)
teachers ---> (评定成绩)
(评定成绩) ---> (考试成绩)
(评定成绩) ---> (平时成绩)
(评定成绩) ---> (实验成绩)
teachers ---> (学生列表)
teachers ---> (选择学期)
teachers ---> (查看成绩)
(学生列表) ---> (学生管理)
students ---> (查看成绩)
students ---> (选择学期)
students ---> (选择课程)
}

package 用户用例集 {
users --up-> (登录)
users --up-> (登出)
users --up-> (查看用户信息)
users --up-> (修改用户信息)
users --up-> (修改密码)
}

@enduml
```