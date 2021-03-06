## Spring Cloud 实战项目

### 项目介绍
```
功能点：
    模拟商城，完整的购物流程、后端运营平台对前端业务的支撑，和对项目的运维，有各项的监控指标和运维指标。
技术点：
       核心技术为springcloud+vue两个全家桶实现，采取了取自开源用于开源的目标，所以能用开源绝不用收费框架，整体技术栈只有
    阿里云短信服务是收费的，都是目前java前瞻性的框架，可以为中小企业解决微服务架构难题，可以帮助企业快速建站。由于服务
    器成本较高，尽量降低开发成本的原则，本项目由 ? 个后端项目和 ? 个前端项目共同组成。真正实现了基于RBAC、jwt和oauth2的
    无状态统一权限认证的解决方案，实现了异常和日志的统一管理，实现了MQ落地保证100%到达的解决方案。
	
	核心框架：springcloud Edgware全家桶
	安全框架：Spring Security Spring Cloud Oauth2
	分布式任务调度：elastic-job
	持久层框架：MyBatis、通用Mapper4、Mybatis_PageHelper
	数据库连接池：Alibaba Druid
	日志管理：Logback	前端框架：Vue全家桶以及相关组件
	三方服务： 邮件服务、阿里云短信服务、七牛云文件服务、钉钉机器人服务、高德地图API
```
### 平台目录结构说明


```
├─paascloud-master----------------------------父项目，公共依赖
│  ├─passcloud-base-server
│  │  ├─eureka-server--------------------------微服务注册中心
│  │  │
│  │  ├─conf-server-----------------------微服务配置中心
│  │  │
│  │  ├─sleuth-server-------------------------微服务监控中心
│  │  │
│  │  ├─gateway-server--------------------------微服务网关中心
│  │  │
│  │  ├─admin-server--------------------------微服务注册监控中心
│  │  │
│  │  ├─turbine-server--------------------------微服务聚合监控中心
│  │  │
│  │
│  ├─paascloud-provider
│  │  │
│  │  ├─paascloud-provider-mdc------------------数据服务中心
│  │  │
│  │  ├─paascloud-provider-omc------------------订单服务中心
│  │  │
│  │  ├─paascloud-provider-opc------------------对接服务中心
│  │  │
│  │  ├─paascloud-provider-tpc------------------任务服务中心
│  │  │
│  │  └─paascloud-provider-uac------------------用户服务中心
│  │
│  ├─paascloud-provider-api
│  │  │
│  │  ├─paascloud-provider-mdc-api------------------数据服务中心API
│  │  │
│  │  ├─paascloud-provider-omc-api------------------订单服务中心API
│  │  │
│  │  ├─paascloud-provider-opc-api------------------对接服务中心API
│  │  │
│  │  ├─paascloud-provider-tpc-api------------------任务服务中心API
│  │  │
│  │  ├─paascloud-provider-sdk-api------------------可靠消息服务API
│  │  │
│  │  └─paascloud-provider-uac-api------------------用户服务中心API
│  │
│  ├─paascloud-common
│  │  │
│  │  ├─paascloud-common-base------------------公共POJO基础包
│  │  │
│  │  ├─paascloud-common-config------------------公共配置包
│  │  │
│  │  ├─paascloud-common-core------------------微服务核心依赖包
│  │  │
│  │  ├─paascloud-common-util------------------公共工具包
│  │  │
│  │  ├─paascloud-common-zk------------------zookeeper配置
│  │  │
│  │  ├─paascloud-security-app------------------公共无状态安全认证
│  │  │
│  │  ├─paascloud-security-core------------------安全服务核心包
│  │  │
│  │  └─paascloud-security-feign------------------基于auth2的feign配置
│  │

```


### 特殊说明


```
这里做一个解释由于微服务的拆分受制于服务器，这里我做了微服务的合并，比如OAuth2的认证服务中心和用户中心合并，
统一的one service服务中心和用户认证中心合并，支付中心和订单中心合并，其实这也是不得已而为之，
只是做了业务微服务中心的合并，并没有将架构中的 注册中心 监控中心 服务发现中心进行合并。
```


### 作者介绍

```
Spring Cloud 爱好者,现就任于鲜易供应链平台研发部.
```

### 架构图

![项目架构图](http://img.paascloud.net/paascloud/doc/paascloud-project.png)






