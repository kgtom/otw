# otw
一个简单go-micro微服务框架

### 项目知识点
* 1.go-micro && micro 使用
* 2.Dockefile构建 && docker-compose 服务编排
* 3.consul 服务注册与发现
* 4.内部服务直接rpc、nsq 通信，对外restful api(Gin)
* 5.api-gateway 使用Gin路由
* 6.make && Makefile 编译代码及构建docker image
* 7.常规业务postgresql及 偏写入MongoDB
* 8.常用设计模式

### 常用设计模式
* 1.外观模式:用来包装一组接口用于方便使用，例如：api-gateway api聚合
* 2.代理模式:不直接操作类本身，基于接口编程或者基于代理类操作，例如：repository中interface接口或者 各个service中client的作为代理类
* 3.
### 项目架构(以order-service为例)
~~~
# tom @ tom-pc in ~/goprojects/src/otw [11:46:51] 
$ tree                      
.
├── ReadMe.md
├── api-gateway
│   ├── handlers
│   │   ├── handler.go
│   │   └── orderHander.go
│   └── main.go
├── order-service
│   ├── Dockerfile
│   ├── Makefile
│   ├── client
│   │   └── client.go
│   ├── config
│   │   └── config.go
│   ├── handers
│   │   └── handler.go
│   ├── main.go
│   │
│   ├── proto
│   │   ├── order.micro.go
│   │   ├── order.pb.go
│   │   └── order.proto
│   └── repos
│       ├── OrderRepository.go
│       └── repositoryBase.go
└──── docker-compose.yaml


~~~
