#### springcloud常用组件
> 项目中使用的技术如下：
- Eureka注册中心 （支持集群部署）
- Config注册中心 （支持集群部署）
- Zuul 服务网关  （支持集群部署）
- Hystrix 断路器
- Ribbon 负载均衡
- Feign 负载均衡
- Turbine 聚合监控
- Bus 消息总线
- RabbitMQ 消息中间件

#### 项目启动 
##### 1、前期准备
- 首先在本地电脑的host文件中，配置好虚拟域名；
  我本地host文件中的配置如下（注意中间空格）：
```
127.0.0.1 server.eureka.node1.com server.eureka.node2.com
```
- 安装rabbitmq
```
rabbitmq目前只用在配置中心，实现动态刷新spring bean，建议安装。
```

##### 2、开发环境（以下是我本机环境）

- jdk1.8
- idea 2020.1

##### 3、服务启动
1、启动eureka注册中心 
```
（建议运行至少2个eureka服务器节点，方可看到高可用集群效果）
```
<br/>

2、启动config配置中心
```
（建议运行至少2个config配置中心节点，方可看到高可用集群效果）
```
<br/>

3、启动zuul服务网关
```
（建议运行至少2个zuul服务网关节点，方可看到高可用集群效果）
```
<br/>

4、启动hystrix dashboard仪表盘服务

<br/>

5、启动user服务
```
（建议运行至少2个user服务节点，方可看到高可用集群效果）
```
<br/>

6、启动rainze-spring-cloud-consumption应用 测试服务 当然自己可以在按需要集成自己的模块
```
（建议运行至少2个shop应用节点，方可看到高可用集群效果）
```
<br/>

#### 打开eureka控制台，查看各服务的集群信息

#### 个人博客
www.liyuze.work
...