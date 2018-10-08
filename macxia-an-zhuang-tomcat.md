# 

# Mac下安装tomcat8（Mac 10.12）

1、到官网下载tomcat8

[http://tomcat.apache.org/download-80.cgi ](http://tomcat.apache.org/download-80.cgi)

说明：tomcat最好不要下载最新的，选择一个适中的最好。

[![](/assets/1.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112114923869-1670815662.png)

2、安装

▲解压并重命名文件夹为tomcat8

▲拷贝tomcat8整个文件夹到/usr/local/目录

[![](/assets/2.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112115507510-1415934466.png)

3、配置tomcat

▲进入到上面的目录/usr/local/tomcat8

[![](/assets/3.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112115955681-537097611.png)

▲启动tomcat

再次进入到bin目录，然后运行

```
./startup.sh
```

会出现如下提示

[![](/assets/4.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112120222650-1939302343.png)

说明时权限不足，需要加入bin目录下全部文件的权限

```
sudo chmod 755 *.sh
```

[![](/assets/5.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112124325213-24284867.png)

再次运行启动命令

```
./startup.sh
```

出现以下信息，成功运行

[![](/assets/6.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112124520213-504805141.png)

测试一下看是否web访问正常

在浏览器上输入[http://127.0.0.1:8080/地址，注意：这里8080是tomcat的，mac下默认安装了apache，这个是80端口的，修改端口时要注意。](http://127.0.0.1:8080/地址，注意：这里8080是tomcat的，mac下默认安装了apache，这个是80端口的，修改端口时要注意。)

[![](/assets/7.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112124743916-1487600692.png)

成功安装。

再次点击【Manager App】进入管理界面，此时会提示你输入账号密码，但是默认我们没有设置过，所以直接点击取消按钮。出现如下信息：

[![](/assets/8.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112124958900-2112880780.png)

是告诉你配置密码的节点和默认初始化账号密码。

再次进入到/usr/local/tomcat8/conf/tomcat-users.xml，增加如上所示节点

对于要如何编辑，命令行或者软件都可以。

[![](/assets/9.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112125436025-82711396.png)

保存，再次刷新浏览器试下这个账号和密码，发现还是不正确。

再次回到终端，把服务停止了再启动

```
./shutdown.
sh

./startup.sh
```

再次刷新浏览器，用设置账号密码登录，发现成功登录。

[![](/assets/10.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112125809869-392583741.png)

