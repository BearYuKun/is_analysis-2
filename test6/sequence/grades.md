 [返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/grades.md)

```
@startuml
title 基于GitHub的实验管理平台--评定成绩用例的顺序图
actor teachers
actor students
== 查看成绩 ==
teachers -> grades
students -> grades
grades -> tests
tests -->grades
grades --> teachers:每个实验的信息、成绩和评语
grades --> students:每个实验的信息、成绩和评语
== 评定成绩 ==
teachers -> tests : 录入并提交每个实验的成绩
tests --> grades
@enduml
```
