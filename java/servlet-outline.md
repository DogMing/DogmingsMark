# JavaEE Web Applications

## 简介

        在Java 2平台中，Web组件为Web服务器提供了动态扩展功能。 Web组件是Java servlet，JSP页面或Web服务端点。 Web客户端和Web应用程序之间的交互如图3-1所示。客户端将HTTP请求发送到Web服务器。实现Java Servlet和JavaServer Pages技术的Web服务器将请求转换为HTTPServletRequest对象。该对象传递到Web组件，该组件可以与JavaBeans组件或数据库交互以生成动态内容。然后，Web组件可以生成HTTPServletResponse，也可以将请求传递给另一个Web组件。最终，Web组件生成一个HTTPServletResponse对象。 Web服务器将该对象转换为HTTP响应，并将其返回给客户端。

## 交互

![图3-1](https://docs.oracle.com/javaee/5/tutorial/doc/figures/web-requestHandling.gif "图 3-1")

图 3-1

## 模块

![图 3-2](https://docs.oracle.com/javaee/5/tutorial/doc/figures/web-technologies.gif  "图 3-2")

## 核心类/接口

Component|Interface/Class
--|:--
Servlets|javax.servlet.Servlet
Servlet Filters|javax.servlet.ServletFilter
Event Listeners|javax.servlet.ServletContextListener
Event Listeners|javax.servlet.ServletContextAttributeListener
Event Listeners|javax.servlet.ServletRequestListener
Event Listeners|javax.servlet.ServletRequestAttributeListener
Event Listeners|javax.servlet.http.HttpSessionListener
Event Listeners|javax.servlet.http.HttpSessionAttributeListener
Event Listeners|javax.servlet.http.HttpSessionBindingListener
Session|javax.servlet.http.HttpSession
Request|javax.servlet.http.HttpServletRequest
Response|javax.servlet.http.HttpServletResponse
applicationContext|xxxx

## 版本

- 2.4 [最基础的](https://docs.oracle.com/javaee/5/tutorial/doc/)
- 2.5 [提供注解的方式](https://docs.oracle.com/javaee/6/tutorial/doc/bnagb.html) 
- 3.1 [非阻塞I/O,http协议升级](https://docs.oracle.com/javaee/7/tutorial/overview007.htm#BNACJ)
- 4.0 [http2支持,服务端推送](https://download.oracle.com/otn-pub/jcp/servlet-4-final-spec/servlet-4_0_FINAL.pdf?AuthParam=1600941315_ec4a7c1a4965a8173648bf302be6bf34)
- 5.0 [换主子oracle->jakarta](https://jakarta.ee/specifications/servlet/5.0/servlet-spec-5.0-SNAPSHOT.html#file-upload)


## 问题

    1. 有状态与无状态  session 
    2. 并发 tomcat 容器如何实现并发？
    3. JSP 技术是什么，为什么后来不用了呢？
    4. EJB 技术是什么？ EJB 是微服务吗？现在的分布式服务端常用套路？
