# 从零开始构建您的第一个单体应用项目

为了让您更快地掌握行云趣码这个系统的用法以及感受到它的独特魅力，下面我们一起从零搭建一个项目（此处以一个python hello world的demo为例），从编写代码开始，到应用发布到云端，再到测试，运维。。。

1.编写您的代码（包括Dockerfile）

此demo包含三个文件：

main.py

```
#main.py
#!flask/bin/python
# -- coding: utf-8 --

__author__ = 'cloudtogo'

from flask import Flask


app = Flask(__name__)


@app.route('/')
def hello():
    return "hello world!!!"

if __name__ == '__main__':
    app.run(host='0.0.0.0',port=5000)
```

Dockerfile

```
# 基础镜像信息
FROM registry.local/factory/pythonbase:1.0
# 创建目录
RUN mkdir -p /usr/local/ph
# 拷贝文件
ADD ./ /usr/local/ph
# 设置工作目录
WORKDIR /usr/local/ph
# 安装requirements
RUN pip install --no-cache-dir -r requirements.txt
CMD ["python", "./main.py"]
EXPOSE 5000
```

requirements.txt

```
flask
```

2.将您的代码放在github上，您也可以选择我们为您准备好的示例代码：[https://github.com/solochen84/ph.git](https://github.com/solochen84/ph.git)

3.新建项目

点击应用工厂首页的“+创建新项目”按钮

![](/assets/import37.png)

在弹出框中选择“Blank”模板，下一步，填入自定义的项目名称和项目描述，点击完成进入架构图设计界面。

![](/assets/import38.png)

4.设计架构图

在架构图设计器中拉入一个代码组件

![](/assets/import30.png)

点击下一步，在Git仓库地址中填入您的github代码库的地址，也可以使用我们已为您准备好的代码：[https://github.com/solochen84/ph.git，并选择技术栈为Dockerfile](https://github.com/solochen84/ph.git，并选择技术栈为Dockerfile) in source。

![](/assets/import31.png)

下一步，添加网络服务，协议为HTTP，并修改端口号为5000（程序中指定了端口号），再下一步，点击完成即可。

![](/assets/import33.png)

到此，架构图设计完毕，点击保存架构图，并选择发布应用

![](/assets/import32.png)

5.发布应用

跳转到发布配置界面，这里我们按照默认配置，点击确定

![](/assets/import34.png)

6.确定后应用进入发布状态，等待应用发布成功，即可访问

![](/assets/import35.png)

7.如果您需要在发布过程中查看发布的日志，那么您可以点击应用列表上的“运维监控”或者左侧菜单中的“运维”，再在组件的菜单中选择日志，来随时查看组件的发布情况。

![](/assets/import60.png)

8.访问应用：可在查看配置中点击域名，访问应用。

![](/assets/import36.png)如果您事先写好了代码，那么仅需几分钟，您的应用就可以在行云上跑起来。

您也可以选择使用行云内置的CloudIDE来编写您的代码，具体的使用方法见[CloudIDE](/bian-ma/cloudide.md)。

