# “修改用户信息”用例 [返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/README.md)
## 1. 用例规约

|用例名称|修改用户信息|
|-------|:-------------|
|功能|修改用户的GitHub用户名称|
|参与者|学生，老师|
|前置条件|必须先登录，并且查看用户现有的GitHub用户名|
|后置条件| |
|主事件流| 1.用户填写GitHub用户名称 <br/> 2.用户提交修改信息 <br/>3.系统存储修改后的GitHub用户名称|
|备选事件流|1a. 如果用户输入的GitHub用户名称为空 <br/>&nbsp;&nbsp; 1.系统清空用户的GitHub用户名称|

## 2. 业务流程

### [源码](https://github.com/Wangfan212/is_analysis/blob/master/test6/sequence/rechange_info.md)


![登录认证流程图](rechange_info.svg)

## 3. 接口设计

### [详情](https://github.com/Wangfan212/is_analysis/blob/master/test6/api/api5.md)


## 4. 算法描述
无
    
## 5. 参照表

+ 参照上一页中的数据库设计中的 users。