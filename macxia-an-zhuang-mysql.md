# Mac下安装MySQL（Mac 10.12）

系统：Mac OS 10.12

MySQL：5.7.15

**前言：**

安装mysql有两种方式：1为官方下载dmg安装包。

**安装步骤：**

一、官方下载dmg安装包进行安装

1、登陆官网下载

[https://downloads.mysql.com/archives/community/](https://downloads.mysql.com/archives/community/)

[![](/assets/417876-20170112015632369-658606563.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112015632369-658606563.png)

2、解压出pkg文件

[![](/assets/417876-20170112021126760-1316383060.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112021126760-1316383060.png)

3、安装

[![](/assets/417876-20170112021149244-449090488.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112021149244-449090488.png)

[![](/assets/417876-20170112021158306-295705897.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112021158306-295705897.png)

[![](/assets/417876-20170112021223244-1952874972.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112021223244-1952874972.png)

[![](/assets/417876-20170112021313572-1471559485.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112021313572-1471559485.png)

安装完成。

4、测试

▲验证是否安装成功，进入/usr/local/mysql/bin/，用ls命令查看是否有mysql

[![](/assets/417876-20170112024504994-564741458.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112024504994-564741458.png)

▲启动mysql的服务，输入以下命令：

```
sudo /usr/local/mysql/support-
files
/mysql.server 
start
```

注意，start为启动，那么stop就是停止，全命令如下：

```
sudo /usr/local/mysql/support-
files
/mysql.server stop
```

▲修改mysql初始化密码

避免服务已经启动，所以第一步先关闭mysql的服务

```
sudo /usr/local/mysql/support-
files
/mysql.server stop
```

开启安全模式启动mysql，这种方式可以不用输入默认密码

```
sudo /usr/local/mysql/bin/mysqld_safe --skip-grant-tables
```

出现如下画面是启动成功

[![](/assets/417876-20170112025955556-157240274.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112025955556-157240274.png)

此时，关闭这个终端窗口，再重新启动一个

进入/usr/local/mysql/bin/，以root身份启动mysql

```
./mysql -u root
```

[![](/assets/417876-20170112030211369-1233431346.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112030211369-1233431346.png)

输入以下命令修改密码，其中PASSWORD里面就是要设置的密码

```
UPDATE mysql.user 
SET
 authentication_string=PASSWORD('root') WHERE User='root';
```

```
FLUSH PRIVILEGES;
```

[![](/assets/417876-20170112030451228-1201238217.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112030451228-1201238217.png)

退出mysql，输入

```
quit;
```

停止mysql服务

```
sudo /usr/local/mysql/support-
files
/mysql.server stop
```

再启动mysql服务

```
sudo /usr/local/mysql/support-
files
/mysql.server 
start
```

[![](/assets/417876-20170112030702056-743541117.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112030702056-743541117.png)

使用以下命令进入mysql

```
./mysql -u root -p
```

此时，要求输入密码，就是前面设置的root密码

[![](/assets/417876-20170112030827510-208344692.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112030827510-208344692.png)

再测试是否正常

```
show databases;
```

此时，如果出现：ERROR 1820 \(HY000\): You must reset your password using ALTER USER statement before executing this statement.的错误提示时，需要再设置一次密码

```
SET
 PASSWORD = PASSWORD('root');
```

[![](/assets/417876-20170112031309525-2077952956.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112031309525-2077952956.png)

再测试是否正常

[![](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112031351291-2053243565.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112031351291-2053243565.png)

一切正常。

5、优化使用

▲通过上面的操作，每次都要进入到mysql的目录上进行启动，那么有两种方式alias和ln进行设置，ln其实不推荐，路径时很大的问题。推荐使用alias。

```
alias mysql
=/usr/local/mysql/bin/mysql
```

6、后话

其实对比发现，用dmg安转包安装的有很多好处，比如开机自动启动这些，全部都有gui工具使用

在系统的偏好设置上如下：

[![](/assets/417876-20170112034645494-1582023783.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112034645494-1582023783.png)

[![](/assets/417876-20170112034707525-1143536342.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112034707525-1143536342.png)

所以，非常推荐使用此方法安装在开发环境。

而对于linux下，命令行操作时首选。

