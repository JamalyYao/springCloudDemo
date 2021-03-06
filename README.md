# springCloudDemo
## 博客地址
- [SpringCloud(一)使用Eureka实现服务注册与发现](https://blog.csdn.net/chenxyz707/article/details/80395790)
- [SpringCloud(二)配置中心](https://blog.csdn.net/chenxyz707/article/details/80467447)
- [SpringCloud(三)声明式Web服务客户端Feign](https://blog.csdn.net/chenxyz707/article/details/80508612)
- [SpringCloud(四)客户端负载均衡Ribbon](https://blog.csdn.net/chenxyz707/article/details/80548084)
- [SpringCloud(五)SpringCloud的限流、熔断和降级——Hystrix](https://blog.csdn.net/chenxyz707/article/details/80913725)
- [SpringCloud(六)Hystrix仪表盘Dashboard](https://blog.csdn.net/chenxyz707/article/details/81567647)
- [SpringCloud(七)路由网关Zuul](https://blog.csdn.net/chenxyz707/article/details/82854142)
- [SpringCloud(八)链路追踪Sleuth](https://blog.csdn.net/chenxyz707/article/details/82999783)

## Eureka
Eureka的高可用需要修改host文件添加一行
`127.0.0.1  eureka1 eureka2 eureka3`

## 配置中心
### 配置中心仓库
`springCloudConfig-master`文件夹里面是仓库里的配置文件。
启动之前请修改配置中心的仓库地址
### 关于GitLab
GitLab使用`Docker`部署
```shell
docker pull gitlab/gitlab-ce
```
如果从Docker仓库获取太慢或者经常失败，可以从国内仓库获取。
```shell
docker pull registry.docker-cn.com/gitlab/gitlab-ce
```
运行指令
```shell
docker run -d -p 1443:443 -p 10800:80 --name gitlab --restart always gitlab/gitlab-ce:latest
```
启动后直接打开 http://ip:10800 访问GitLab需要初始化密码，这里修改密码为`123456789`。
如果访问502，仔细查看内存是否足够。此处使用4G内存，3G可能会有问题。

**当然如果直接使用GitHub就不用考虑这些问题**
### 关于加解密失败
如果加密失败可以参考我的博客https://blog.csdn.net/chenxyz707/article/details/80487733 。
## Hystrix
### 配置文件
`config.properties`和`application.yml`中的Hystrix的配置项共同生效，且`application.yml`优先级高。

## 其他


