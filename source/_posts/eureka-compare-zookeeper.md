---
 title: eureka(AP) 和 zookeeper (CP)区别
---

### 这两个都是微服务的注册中心;也是我们经常聊的问题,以下是本人对此的了解

### eureka

   1. eureka 是什么
      eureka 是一个微服务的服务管理注册中心，它用于注册服务，提供服务给外部的客服端调用,eureka 是 Netflix开源的注册中心
      它分为客户端和服务端,
      1. 如何注册一个客户端
          1. 添加依赖
          ```
         
           <groupId>org.springframework.clound</groupId>
           <artifactId>spring-cloud-starter-eureka-client</artifactId>
          ```
          2. 配置 yaml 或者 properties 文件
          ```
            eureka: 
               client: 
                 serviceUrl: 
                     defaultZone: https://{serverName}:port/eureka/
         ```
         
      2. 如何注册一个服务端
         1. 添加依赖
          ```
            <groupId>org.springframework.clound</groupId>
            <artifactId>spring-cloud-starter-eureka-client</artifactId>
         ```
         2. 配置yaml或者properties
         
         ```
           eureka: 
             client:
               tls:
                enabled: true
                key-store: <path-of-key-store>
                key-store-type: PKCS12
                key-store-password: <key-store-password>
                key-password: <path-of-trust-store>
                trust-store: <path-of-strust-store>
                trust-store-type: PKCS12
                trust-store-password: <trust-store-password>
         
         ```
   2. zookeeper 同理zookeeper也是一份服务注册中心，用于注册服务，提供给外部客户端调用
