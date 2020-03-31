###     3.9 “修改密码”用例
<table>
  <caption align="center">"修改密码"用例规约</caption>
  <tr>
    <td>用例名称</td>
    <td>修改密码</td>
  </tr>
  <tr>
    <td>参与者</td>
    <td>系统维护员、图书管理员、读者</td>
  </tr>
  <tr>
    <td>前置条件</td>
    <td>
    	系统维护员、图书管理员或读者登录到系统<br>
    </td>
  </tr>
  <tr>  
    <td>后置条件</td>
    <td>
    	产生并保存修改记录和修改后的密码
	</td>
  </tr>
  <tr>
    <td colspan="2" align="center">主事件流</td>
  </tr>
  <tr>
    <td>参与者动作</td>
    <td>系统行为</td>
  </tr>
  <tr>
    <td>
		1.超级管理员、图书管理员或读者跳转到修改密码的页面 <br>
		2.超级管理员、图书管理员或读者填写旧密码及新密码 <br>
	</td>
    <td>
		3.系统保存新密码，用例结束
	</td>
  </tr>
  <tr>
    <td colspan="2" align="center">备选事件流</td>
  </tr>
  <tr>
    <td colspan="2">
    	1a.旧密码输入错误<br>
    	2a.系统提示旧密码输入错误<br>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center">业务规则</td>
  </tr>
  <tr>
    <td colspan="2">1.用户的编号不能修改<br>2.密码登录后才能做出修改</td>
  </tr>
</table>

#### "修改密码"用例流程图PlantUML源码如下：
```
@startuml
start
    :登录;
    :跳转到修改用户密码页面;
    :输入旧密码和新密码;
if (旧密码错误) then (yes)
    :提示旧密码错误;
else (no)
    :显示“修改密码成功”;
endif
stop
@enduml
```
#### "修改密码"用例流程图如下：
![8](test2_8)