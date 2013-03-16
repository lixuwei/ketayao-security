本项目不是本人的，作者的都在google code上我只是发布到github上，如需最新的版本请移步到google code上checkout
keta-security是一个开源的java开源权限系统，使用了maven作为项目管理，基本框架使用了现在流行的SpringMVC+Spring+Hibernate（springside作为项目粘合构架），安全框架用的是简单易用的Apache Shiro，
UI显示用的是比较火的基于Jquery的DWZ，数据层封装使用了傻瓜式的Spring Data Jpa包。

系统描述：主要基于角色的权限管理，可以动态创建模块，配置权限，易于扩展，细化到每个按钮的权限控制。

使用方法一（java源代码）：

1.当然是要安装了maven，导入相关依赖包。

2.导入测试数据security\src\main\resources\sql\mysql\schema.sql

3.运行security\src\test\java\com\ketayao\test\QuickStartServer.java

4.访问地址：localhost:9090/security

5.用户名：admin 密码：123456

使用方法二（war包）：
1.导入测试数据security\src\main\resources\sql\mysql\schema.sql
2.丢进你的web容器（tomcat等等）。
3.输入你的地址，用户名：admin 密码：123456

----version 1.0.0
1.修改了applicationContext-shiro.xml和spring-mvc.xml配置文件，修复不能shiro不能进行方法检查的bug。
2.将验证码的使用进行了演示，只需要在applicationContext-shiro.xml配置com.ketayao.security.shiro.CaptchaUsernamePasswordToken，   
     在web.xml配置com.ketayao.security.shiro.SimpleCaptchaServlet，设置shiroDbRealm的isUseCaptcha为true即可。
     
----version 1.1.0
1.把dwz-ria升级到1.4.5版本。
2.修复了一些登录验证的小bug。     
