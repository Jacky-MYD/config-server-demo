# config-server-demo
微服务仓库管理

新建springboot工程，配置仓库路径
```
spring:
  application:
    name: config-server
  cloud:
    config:
      server:
        git:
          uri: https://github.com/Jacky-MYD/config-server-demo.git
server:
  port: 1201
```
浏览器访问：http://localhost:1201/config-client/dev/master
  
  返回当前环境配置信息
  ```
  {"name":"config-client","profiles":["dev"],"label":"master","version":null,"state":null,"propertySources":[{"name":"https://github.com/Jacky-MYD/config-server-demo.git/config-client-dev.yml","source":{"info.profile":"dev"}},{"name":"https://github.com/Jacky-MYD/config-server-demo.git/config-client.yml","source":{"info.profile":"default"}}]}
  ```
