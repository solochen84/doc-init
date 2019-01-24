# 发布应用设置密码

## 发布mysql如何设置密码？

1. 在组件参数设置界面添加一个输入参数pwd（命名任意）和一个环境变量：MYSQL\_ROOT\_PASSWORD（这个是MySQL镜像指定的环境变量，命名不能改），并将这个输入参数和这个环境变量关联起来。

![](/assets/import116.png)

2. 发布上述组件时，就会要求输入pwd这个参数的密码，而这个输入参数又绑定了MYSQL\_ROOT\_PASSWORD的环境变量，那么输入的密码就设置成了。

## ![](/assets/import117.png)发布redis如何设置密码？

在组件参数中勾选“执行命令”，并设置执行命令：

redis-server --requirepass "123456"，发布后则需要密码连接

![](/assets/import118.png)

## 发布MongoDB如何设置密码？

1. 只需要在组件设置时，添加2个环境变量MONGO\_INITDB\_ROOT\_USERNAME和MONGO\_INITDB\_ROOT\_PASSWORD即可，当然你也可以将环境变量与输入参数绑定，以便在发布时手工输入，请参考“发布Mysql如何设置密码”

![](/assets/import119.png)

## 发布Rabbitmq如何设置密码？

1. 在组件参数设置界面添加一个输入参数user（代表用户名，命名任意）和一个环境变量：RABBITMQ\_DEFAULT\_USER（这个是rabbitMQ镜像指定的环境变量，命名不能改），并将这个输入参数和这个环境变量关联起来。同样，添加另一个输入参数password（代表密码，命名任意）和一个环境变量RABBITMQ\_DEFAULT\_PASS，并将这个输入参数和这个环境变量关联起来。

![](/assets/import120.png)

2. 发布上述组件时，就会要求输入user和password这2个参数的密码

![](/assets/import121.png)

