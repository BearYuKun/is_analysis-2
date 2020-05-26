[返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/README.md)

```
@startuml
class users {
    <b>github_username<b> （用户GitHub账号）
    associated_name （关联真实名字）
    update_date （用户GitHub账号修改日期）
    password （用户密码）
}
class teachers{
    <b>teacher_id</b> （老师工号）
    department （老师所属部门）
    teacher_name （老师名字）
}
class students{
    <b>student_id</b> （学号）
    class （班级）
    tests_sum （各个实验成绩）
    result_sum（成绩汇总）
    web_sum （网站正确与否汇总）
}
class grades {
    <b>student_id</b> （学号）
    <b>test_id</b> （实验编号）
    grade（年级）
    major （专业）
}
class tests {
    <b>test_id</b> （实验编号）
    name （实验名称）
    result （分数）
    memo （评价）
    update_date （修改日期）
}

users <|- students
users <|-- teachers
students "1" -- "1"  grades
tests "n" -- "1"  students
teachers "n" -- "n"  grades
teachers "1" -- "n"  students
tests "n" -- "1"  teachers
@enduml

```