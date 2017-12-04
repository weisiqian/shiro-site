# Apache Shiro 网站概述

Apache Shiro 是一个可以访问的静态网站，网址是：http://shiro.apache.org

网站内容使用 Markdown 和 HTML 编写。这些文件经过一个工具扫描后，这个工具根据需要将页面模板应用到每一个被扫描的文件的内容，并将呈现的静态.html文件输出到'publish'目录。

使用这个工具发布网站更改的内容就像是在`publish`目录提交任何内容来进行版本控制一样简单。ASF基础架构将看到提交并自动将更改推送到ASF的产品Web服务器。

## 生成和发布

这个用于生成静态内容的工具是 [SCMS](https://github.com/lhazlewood/scms).  一旦scms被安装并且在你电脑的`$ PATH`中, 在命令行生成和发布网站是很容易的。
 
下面的例子假设你拥有对`publish`目录的SVN提交权限，通常是因为你是一个Apache Shiro项目提交者：
    
    cd site
    # This next command will take a few seconds, be patient :)
    scms trunk publish
    # Open up the local publish/index.html file in your web browser.  Ensure the changes reflect what you want. 
    #
    # This next commands will publish changes to live ASF web servers.  Be confident the changes are what you want:
    svn add .
    svn commit -m "my change description"

