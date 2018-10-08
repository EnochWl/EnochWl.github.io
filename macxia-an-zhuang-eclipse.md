# Mac下安装eclipse（Mac 10.12/JDK/tomcat）

1、到官网[https://www.eclipse.org/downloads/eclipse-packages/](https://www.eclipse.org/downloads/eclipse-packages/)下载安装包

[![](/assets/11.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112141039416-194978036.png)

[![](/assets/12.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112141231166-1494703721.png)

2、安装

注意：安装ecllipse时一定要安装JDK先，最新版本的eclipse已经自动识别JDK，所以这些都不需要配置，装好就能用。

解压，双击tar.gz包，解压出app文件，把它拖入到应用程序

[![](/assets/13.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112165550463-1791702467.png)

双击打开就能运行。

[![](/assets/14.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112165716369-1488014373.png)

3、配置一些常用设置

▲jdk

其实这个默认已经安装包，自动识别，不过如果有特定的需求，可以手动指定，步骤如下：

[![](/assets/15.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112165836494-1983068740.png)

[![](/assets/16.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112165927947-899111128.png)

[![](/assets/17.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112165951963-803843044.png)

[![](/assets/18.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112170059072-323502481.png)

[![](/assets/19.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112170113119-127616237.png)

▲配置工作空间使用UTF-8格式

[![](/assets/20.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112170343744-1479996811.png)

▲在左侧栏顶部搜索”spelling”，找到spelling后取消拼写检查的选项，这个看个人需要

[![](/assets/21.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112170516416-131790441.png)

▲配置tomcat

下载tomcat插件，[http://marketplace.eclipse.org/content/eclipse-tomcat-plugin](http://marketplace.eclipse.org/content/eclipse-tomcat-plugin)

[![](/assets/22.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112171408744-379338744.png)

拖动到eclipse的工作空间，即可下载。

下面的图片说明已经开始安装：

[![](/assets/23.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112171506916-1089225545.png)

[![](/assets/24.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112171646338-1489153973.png)

如果这一步出错，请参考：[http://www.cnblogs.com/EasonJim/p/6919369.html](http://www.cnblogs.com/EasonJim/p/6919369.html)

[![](/assets/25.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112171726853-604628088.png)

现在才真正开始安装

[![](/assets/26.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112171755603-1349346047.png)

安装完成，重启

[![](/assets/27.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112172429994-526015142.png)

再次观察工具栏，发现已经有了tomcat的按钮

[![](/assets/28.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112172528385-1056103668.png)

开始配置tomcat

[![](/assets/29.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112172705635-1236428521.png)

测试运行，按第一个按钮启动tomcat

[![](/assets/30.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112172818213-1419890610.png)

在浏览器上测试

[![](/assets/31.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112172916510-874469184.png)

正常运行。

