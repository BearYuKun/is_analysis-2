# 实验一：业务流程建模


  学号  |  班级  |  姓名   |    

201710414318 | 软工3班 | 王帆 |


## 流程图1：考试及成绩管理流程
### 流程说明：
<pre>
1.教务处公布考试信息
2.老师给出考试信息并申请
3.系主任对相应申请做出审批
4.教务处根据情况做出试卷并安排学生考试
5.学生考试，答卷
6.老师进行改卷给出分数并对答卷进行存档和给出成绩单
7.教务出根据成绩单安排补考
</pre>
### 业务流程图如下：

![1](https://github.com/wangfan212/is_analysis/blob/master/test1/1.png)

PlantUML代码如下：
<pre>
title **<期末考试流程>**
@startuml
|教务处|
start
:安排考试;
:考试安排表;
|#AntiqueWhite|教师|
:教师出卷;
fork
:试卷A or B;
fork again
:打印审批表;
|系主任|
:审批签字;
:打印审批表;
fork end
|教务处|
:打印试卷;
:试卷;
|#AntiqueWhite|学生|
:参加考试;
:答卷;
|教师|
:批改试卷，给出成绩;
|教师|
:阅卷出成绩;
fork
:成绩单]
|教务处|
if (有不及格?) then (是)
else(否)
end
endif
:安排补考;
:补考安排表]
fork again
|教师|
:答卷]
:装订存档;
endfork
:期末考试流程结束;
stop
@enduml
	</pre>






## 流程图：客户维修服务流程
### 流程说明：

<pre>
1.客户申请服务
2.业务经理根据是否为新老客户，进行安排并且制定方案。
3.判断客户是否满意。否则结束服务，是则签订合同。
4.业务经理进行安排和填写派工单。
5.工人根据派工单领取材料和进行服务。
6.客户验收填写反馈信息。
7.客户经理提交派工单给财务人员。
财务人员进行尾款结算。
</pre>


### 业务流程图如下：

![2](https://github.com/wangfan212/is_analysis/blob/master/test1/2.png)


### PlantUML代码如下：

<pre>
@startuml
|客户|
start
:申请服务;
|#AntiqueWhite|业务经理|
if (是新客户吗) then (是)
:登记客户信息;
else(否)
endif
:上门勘察;
:制定方案;
|客户|
if (满意吗) then (否)
stop
else (是)
:签订服务合同;
|业务经理|
fork
:安排工人;
fork again
:安排材料;
end fork
:填写派工单;
|工人|
:领取材料;
:上门服务;
|客户|
:验收并填写反馈意见;
|业务经理|
:交回派工单;
|#AntiqueWhite|财务人员|
:结算领款;
stop
@enduml
</pre>

