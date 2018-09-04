# 从零开始构建您的第一个多应用项目

如果您需要更多的组件和服务来支持您的应用，那么您可以参照以下步骤搭建一个具有多个组件多个应用的项目。

下面以python+mysql为例讲解如何从零构建您的第一个多体应用，假设您已经写好了您的代码（需要包含[Dockerfile](/chapter1/ji-ben-gai-nian.md "Dockerfile")），此处我们需要两个组件，以下是我们需要的两份代码：

python：[https://github.com/huangzw1/python-mysql-template.git](https://github.com/huangzw1/python-mysql-template.git)

mysql：[https://github.com/huangzw1/mysql.git](https://github.com/huangzw1/mysql.git)

1.接下来我们设计应用的架构，拉入一个标准组件下的代码组件

![](/assets/import47.png)

2.在使用技术栈中选择Git仓库地址，将python的代码库地址填入，在技术栈处选择Dockerfile in source

![](/assets/import48.png)

3.组件配置

![](/assets/import49.png)

4.下一步，完成，到此我们设计好了python组件

5.再次拉入代码组件，按照python组件的方式填入Git地址，选择技术栈为Dockerfile in source。但mysql组件的组件配置应按下图配置

![](/assets/import50.png)

6.组件连线及参数填充

将mysql组件的输出参数（3306端口服务地址）连接到python组件的输入参数（MYSQLADDR），在python组件参数设置栏中的MYSQLPWD处选择引用mysql组件的ROOT\_PWD。

![](/assets/import51.png)

7.到此，我们的架构图设计完毕，点击右上方的保存架构图，点击确定跳转到发布页面，若您想做额外配置请参考[发布配置](/fa-bu/fa-bu-pei-zhi.md)，这里我们不做额外配置，仅输入mysql的密码，点击确定即可将应用发布到云端。

![](/assets/import52.png)

8.应用发布成功后，点击立即访问，或者查看配置，点击域名即可访问到您的应用。

