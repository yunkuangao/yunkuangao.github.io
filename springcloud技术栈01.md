---
layout: post
title: springcloud技术栈01
date: 2019-7-8
Author: yunkuangao
categories: 
tags: [document]
comments: true
---

## 转载自[https://blog.csdn.net/oDuoYu1/article/details/82494321](https://blog.csdn.net/oDuoYu1/article/details/82494321)

近年来，微服务架构正逐渐成为互联网业界的一种主流服务机制。早期的互联网应用大多是单体架构，随着业务的不断累加，代码量不断增大，逻辑混乱，扩展性也会随之降低，导致系统的复杂性持续升高，维护成本也会随之增加等痛点问题。那么，微服务概念的出现，就能够很好的降低甚至解决单体架构的痛点。微服务主要就是对系统应用进行有效的拆分，拆分后的应用仅需实现自己的业务逻辑，而无需考虑其他，拆分出来的应用各司其职，这样就是一个轻量级的应用，可以实现快捷开发和部署。Spring Cloud的应运而生，为微服务架构提供了一套生态较为完整的分布式系统解决方案。

Spring Cloud作为Spring家族的新成员，不仅继承了家族的优秀传统，身后有一大帮兄弟给它撑腰，这些兄弟也就组成了Spring Cloud微服务架构的生态链。换言之，Spring Cloud就是一系列框架的有序集合，充分利用Spring Boot的便利性，简化了分布式系统基础设施的开发，如服务发现注册、配置中心、消息总线、负载均衡、断路器、数据监控等，都可以用Spring Boot的开发风格做到一键启动和部署。通过Spring Boot风格进行再封装屏蔽掉了复杂的配置和实现原理，最终提供给开发者一套简单易懂、易部署和易维护的分布式系统开发工具包。以下是Spring Cloud生态圈一众伙伴的简要介绍。

Spring Cloud Config：配置管理工具包，可以将配置放到远程服务器，集中化管理集群配置，目前支持本地存储、Git以及Subversion。

Spring Cloud Bus：事件、消息总线，用于在集群（例如，配置变化事件）中传播状态变化，官方集成了RabbitMQ，可与Spring Cloud Config联合实现热部署。

Spring Cloud Netflix：多种Netflix组件提供的开发工具包，其中包括Eureka、Hystrix、Zuul、Ribbon等。

Spring Cloud Netflix Eureka：这是 Spring Cloud Netflix 微服务套件中的一部分，主要负责完成微服务架构中的服务治理功能，包括服务注册中心、服务注册与服务发现机制的实现，同时实现负载均衡和中间层服务器的故障转移。

Spring Cloud Netflix Hystrix：熔断器，容错管理工具，旨在通过熔断机制控制服务和第三方库的节点,从而对延迟和故障提供更强大的容错能力。

Spring Cloud Netflix Zuul：网关，提供动态路由、监控、弹性、安全等边缘服务的框架。Zuul 相当于是设备和 Netflix 流应用的 Web 网站后端所有请求的前门。

Spring Cloud Netflix Ribbon：提供客户端的负载均衡，有多种负载均衡策略可供选择，可配合服务发现和断路器使用。

Spring Cloud Netflix Turbine：聚合服务器发送事件流数据的一个工具，用来监控集群下hystrix的metrics情况。

Spring Cloud Netflix Archaius：配置管理API，包含一系列配置管理API，提供动态类型化属性、线程安全配置操作、轮询框架、回调机制等功能。

Spring Cloud Feign：声明式、模板化的服务调用组件。

Spring Cloud Sleuth：日志收集工具包，封装了Dapper和log-based追踪以及Zipkin和HTrace操作，为SpringCloud应用实现了一种分布式追踪解决方案。

Spring Cloud Security：基于spring security的安全工具包，提供应用安全控制。

Spring Cloud Zookeeper：操作Zookeeper的工具包，用于使用zookeeper方式的服务发现和配置管理。

Spring Cloud Stream：数据流操作开发包，封装了与Redis,Rabbit、Kafka等发送接收消息。

Spring Cloud CLI：基于 Spring Boot CLI，可以命令行方式快速建立云组件。

Spring Cloud Task：提供计划任务管理、任务调度。

项目组小葵花Cloud课堂的一张简图奉上：

[](https://img-blog.csdn.net/2018090714084956?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L29EdW9ZdTE=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)