# Spring 的 IoC（DI)

[文档地址Spring 5.3.8](https://docs.spring.io/spring-framework/docs/5.3.8/reference/html/core.html#spring-core)

## BeanFactory & ApplicationContext

Spring 通过 org.springframework.beans 和 org.springframework.context 包中的实现，来实现控制反转（依赖注入）。期中核心是 BeanFactory 和 ApplicationContext 接口。  
BeanFactory 通过 getBean ,containsBean ,isSingleLon ,isPrototype ,isTypeMatch ,getType ,getAliase 方法，提供了管理任何 Bean 的高级管理机制。  
ApplicationContext 是 BeanFactory 的子接口，额外提供了 AOP ，事件消息，国际化，特殊分层的整合。