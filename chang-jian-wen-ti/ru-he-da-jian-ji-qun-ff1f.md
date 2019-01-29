# 集群搭建

行云趣码平台支持用户搭建各种高可用集群，包括rabbitmq、zookeeper、mongodb等应用的高可用集群。

下面以rabbitmq和MongoDB为例讲述搭建高可用集群的过程。

## rabbitmq集群搭建

1.镜像选择：这里我们选择rabbitmq:3.6.16-management镜像，拉入镜像组件并在镜像名称框中填入rabbitmq:3.6.16-management

![](/assets/import122.png)

2.开放5672和15672端口

![](/assets/import123.png)

3.添加环境变量：添加MY\__POD\_NAME_和_RABBITMQ\_\_ERLANG_\_COOKIE。\_并配置多副本，存储路径及服务名称。

![](/assets/import124.png)

4.集群初始化

