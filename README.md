# otw
一个简单go-micro微服务框架

### 项目知识点
* 1.go-micro && micro 使用
* 2.Dockefile构建 && docker-compose 服务编排
* 3.consul 服务注册与发现
* 4.内部rpc 通信，对外restful api(Gin)
* 5.api-gateway 使用Gin路由
* 6.make && Makefile 编译代码及构建docker image
* 7.常规业务postgresql及 偏写入MongoDB使用
* 8.
### 项目架构
~~~
api-gateway/
user-services/
  client/
     client.go
  config/
      config.go
  handlers/
      user-role.go
      user.go
  proto/
  Dockerfile
  main.go
  Makefile
  repos/
       database.go
     
order-services/
crm-services/
finance-services/
common-helper/
~~~
