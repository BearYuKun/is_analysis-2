 [返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/students_list.md)


```
@startuml
title 学生列表用例的顺序图
actor teachers
    teachers ->students
	students -> grades
	grades -> tests
	tests --> teachers:每个学生的信息、及每个实验的成绩
@enduml
```