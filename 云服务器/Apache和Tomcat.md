来源：知乎
# 同
- 是web网络服务器，区别于一般所说的服务器。
- Apache基金会组织开发的
- 提供http服务功能
- 开源免费
# 异
- apache是web服务器（静态解析，如html）（支持php插件）（支持tomcat拓展）
- tomcat是java应用服务器（动态解析，如jsp）
- tomcat是一个servlet**容器**（jsp最终也会变成servlet）
- apache httpd VS apache tomcat
# tips
- Apache + Tomcat这样整合可以减少tomcat的服务开销。把静态解析部分交给apache，动态解析（涉及业务逻辑等）部分交给tomcat。
- Apache + Tomcat + JDK，jdk是为了连接数据库。
- 区分web服务器，web网络服务器，服务器，应用服务器
