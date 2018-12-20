将服务端代码打jar包，并且启动三个服务端，每个服务端加载不同的配置。

java -Xmx256m -Xms256m -jar springCloudDemo-eureka.jar --spring.profiles.active=eureka1
java -Xmx256m -Xms256m -jar springCloudDemo-eureka.jar --spring.profiles.active=eureka2
java -Xmx256m -Xms256m -jar springCloudDemo-eureka.jar --spring.profiles.active=eureka3
