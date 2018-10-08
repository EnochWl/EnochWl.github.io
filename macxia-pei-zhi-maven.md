# Mac下配置maven和集成到ecclipse（Mac 10.12）

1、到官网下载maven，[http://maven.apache.org/download.cgi](http://maven.apache.org/download.cgi)

[![](/assets/101.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112175042775-1568434911.png)

下载好的tar.gz包解压出来，并重命名为maven3，拷贝到/usr/local目录下

[![](/assets/102.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112175244400-1974226324.png)

2、配置环境变量

运行命令

```
vim ~/.bashrc
```

结尾处插入

```
export MAVEN_HOME=/usr/local/maven3

export 
PATH
=${
PATH
}:${MAVEN_HOME}/bin
```

如图：

[![](/assets/103.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112175500275-1688799943.png)

提示：插入按i键，退出按exc键，然后输入:wq进行保存并退出。

使环境变量生效，输入：

```
source ~/.bashrc
```

查看maven是否安装成功，命令行输入

```
mvn -v
```

如图表示成功了：

[![](/assets/104.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112180348135-724373977.png)

3、配置eclipse

在eclipse中的偏好设置

[![](/assets/105.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112182018244-889433282.png)

[![](/assets/106.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112182705681-1791812570.png)

[![](/assets/107.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112231425572-10146569.png)

[![](/assets/108.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112232114260-1439175703.png)

配置好之后，基本完成。

4、新建maven项目进行测试

[![](/assets/109.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112232351291-1958024194.png)

[![](/assets/110.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112232554150-1436044333.png)

[![](/assets/111.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112232631588-921780065.png)

新建好的项目结构如下：

[![](/assets/112.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112232715166-39963675.png)



[![](/assets/113.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112233000463-835715262.png)

此时，可以看出正在下载jar包。

等待片刻。

然后在项目上右键，Run As，Maven build，之后，填入参数：

[![](/assets/114.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112233912728-262142899.png)

查看build的结果如下，表示成功：

[![](/assets/115.png)](https://images2015.cnblogs.com/blog/417876/201701/417876-20170112233943541-1674405186.png)

到此，配置全部搞定。

