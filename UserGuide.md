# 简单介绍 #

长期以来，JAVA开发人员一直找不到好的社区系统，而现在广泛使用的PHP论坛又不能同时使用。
本项目提供了JAVA和Discuz! Ucenter的基本API接口， 你可以在此基础上集成你的应用。


# 安装方法 #

第一步：UCenter 添加应用

  * 应用名称: [你的系统名称]
  * 接口 URL: [你的应用地址] etc: http://yourhost:80/context/
  * 应用 IP:  [你的应用服务器的IP地址]
  * 通信密钥: 123456[随便设]，并将这个值考到config.properties里的UC\_KEY


第二步：客户端配置

> UC\_API = http://localhost/uc

> UC\_IP = 127.0.0.1

> UC\_KEY = 123456

> UC\_APPID = 3

> UC\_CONNECT =

第三步：启动客户端

> 将应用接口发布服务器上。启动。
> 注意：web.xml 中必须含有：

---

> 

&lt;servlet&gt;


> > 

&lt;servlet-name&gt;

api

&lt;/servlet-name&gt;


> > 

&lt;servlet-class&gt;

com.fivestars.interfaces.bbs.api.UC

&lt;/servlet-class&gt;


> > 

&lt;load-on-startup&gt;

2

&lt;/load-on-startup&gt;



> 

&lt;/servlet&gt;


> 

&lt;servlet-mapping&gt;


> > 

&lt;servlet-name&gt;

api

&lt;/servlet-name&gt;


> > 

&lt;url-pattern&gt;

/api/uc.php

&lt;/url-pattern&gt;



> 

&lt;/servlet-mapping&gt;



---


第四步：

运行测试程序：
http://localhost/context/Jsp_demo.jsp

结束！

祝你好运！

no\_ten[AT](AT.md)163.com
QQ:18786721