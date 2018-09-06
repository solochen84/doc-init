# Git仓库地址

git仓库克隆地址支持包括GitHub、Bitbucket或其他Git仓库，当您的代码托管在以上的这些Git仓库中时，您可以直接copy仓库地址，放到行云让它跑起来。

1.从标准组件中拉入一个代码组件，在“使用技术栈”页面下选择“Git仓库地址”，将您的代码库copy进来，如[https://github.com/solochen84/ph.git](https://github.com/solochen84/ph.git)

![](/assets/import78.png)

因为这个代码库中自带了Dockerfile，所以技术栈的选择为“Dockerfile in source”

![](/assets/import79.png)

注：要让您的代码跑起来，那么您需要有运行环境。在这里您可以通过编写Dockerfile来配置支持您程序运行的环境。若您的代码结构中已经包含了Dockerfile，那么您可以在技术栈处选择Dockerfile in source。如果没有，那么您可以选择自定义Dockerfile，然后编写Dockerfile（可以通过填参数，也可以自己编写。

