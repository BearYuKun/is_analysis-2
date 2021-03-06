# “登录”用例 [返回](https://github.com/Wangfan212/is_analysis/blob/master/test6/README.md)
## 1. 用例规约

|用例名称|登录|
|-------|:-------------|
|功能|登录平台|
|参与者|访客|
|前置条件| |
|后置条件|登录成功后，跳转到主页|
|主事件流| 1. 访客输入用户名和密码，选择用户类型<br/>2.系统判断用户名，密码，用户类正确，允许登录<br/>3.系统在客户端以Cookie形式存储登录用户信息，保持登录的持久性。|
|备选事件流|1a. 输入的用户名或者密码为空 <br/>&nbsp;&nbsp; 1.提示重新输入 <br/> &nbsp;&nbsp; 2.访客重新提交登录信息 <br/>2a.系统判断用户名，密码，用户类不正确，不允许登录 <br/>&nbsp;&nbsp; 1.提示重新输入 <br/> &nbsp;&nbsp; 2.访客重新提交登录信息 |

## 2. 业务流程

### [源码](https://github.com/Wangfan212/is_analysis/blob/master/test6/sequence/login.md)

![登录认证流程图](login.svg)


## 3. 接口设计
### [详情](https://github.com/Wangfan212/is_analysis/blob/master/test6/api/api7.md)


## 4. 算法描述 
### [源码](https://github.com/Wangfan212/is_analysis/blob/master/test6/login_check.md)



![登录认证流程图](login_check.svg)
    
## 5. 参照表

+ 参照上一页中的数据库设计中的 users。
