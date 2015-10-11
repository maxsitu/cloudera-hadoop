# cloudera-hadoop
本项目为公益项目，由飞谷云发起，是飞谷云计划第6期第5组项目。
开发过程中产生的相关文档可以合并到本仓库中。

# 科普

cloudera-hadoop是由[cloudera](https://github.com/cloudera)公司开发的一套快速部署hadoop集群的系统，提供免费版和收费版。
由于原生hadoop集群配置麻烦，不便管理，并不适合中小互联网公司，前Facebook 的首席数据科学家杰夫. 哈默巴赫尔(Jeff Hammerbacher)感受到这一痛点后主导开发了类似于wordpress（快速建立Php网站）的cloudera工具（快速建立hadoop系统），方便人们快速使用上Hadoop系统，展开相应大数据业务。

感受一下，一天之内完成了wordpress前端到hadoop后端的系统构建，然后找到投资人拿到银子的feel。

---

通常用CDH表示cloudera-hadoop套件，HUE则是一个配套的可视化Web管理界面
[HUE的GitHub传送门](https://github.com/cloudera/hue)

# 需求

最终交付物：自动化安装CDH5.5+HUE 的部署文档 以及 如何使用该系统管理文档。

# 思路

1. 配置主机，安装数据库、第三方库、防火墙、路由、环境变量等等
2. 安装与配置[Cloudera Manager Server](http://www.cloudera.com/content/cloudera/zh-CN/documentation/core/v5-3-x/topics/cm_vd.html) 和Agent，方便进一步可视化安装
3. 通过访问类似于 http://hadoop1:7180 完成可视化安装
4. 撰写相应文档，记录安装过程、使用方法、参考文献、常见问题等

详情可见文末 [参考文献](https://github.com/harryprince/cloudera-hadoop#参考文献)

# 项目信息

<!-- 跳板机信息如下：
ssh ： 210.14.77.99 22
user：open
password：保密 -->
---

项目环境为 centos6

集群信息（登录跳板机后SSH远程连接）

192.168.0.162  cm

192.168.0.163  master

192.168.0.164  slave01

192.168.0.165  slave02

本次项目需要为每个项目成员在主机上分别建立一个账号进行后续的操作
需要征集成员的GitHubID、主机UserID以及主机UesrID对应的密码
主机UserID以及主机UesrID对应的密码由成员自定义后发送到我的邮箱7harryprince@gmail.com 即可，组长将为组员在主机上分别建立对应的账号。

整个项目内容比较多，需要依据每个成员的可参与时间和偏好进行分工合作。

序号|成员 GitHub ID|主机 User ID|对应密码|权限
---|---|---|---|---
1|harryprince|harryprince|aaabbb666888|组长
2|ABC|abc|tttkkk123123|组员

# Cloudera-Hadoop系统构成：

序号|组件
---|---
1|Apache Hadoop (Common, HDFS, MapReduce, YARN)
2|Apache HBase
3|Apache ZooKeeper
4|Apache Oozie
5|Apache Hive
6|Hue (Apache licensed)
7|Apache Flume
8|Cloudera Impala (Apache licensed)
9|Apache Sentry
10|Apache Sqoop
11|Cloudera Search (Apache licensed)
12|Apache Spark

# 参考文献

1. [离线安装Cloudera Manager5.3.4与CDH5.3.4（一）](http://blog.csdn.net/scgaliguodong123_/article/details/46661881)

2. [离线安装Cloudera Manager5.3.4与CDH5.3.4（二）](http://blog.csdn.net/scgaliguodong123_/article/details/46664567)

3. [CDH 5 Requirements and Supported Versions](http://www.cloudera.com/content/cloudera/en/documentation/cdh5/v5-0-0/CDH5-Requirements-and-Supported-Versions/CDH5-Requirements-and-Supported-Versions.html)

4. [CDH 5 Quick Start Guide](http://www.cloudera.com/content/cloudera/en/documentation/cdh5/v5-0-0/CDH5-Quick-Start/CDH5-Quick-Start.html)

5. [CDH 5 Installation Guide](http://www.cloudera.com/content/cloudera/en/documentation/cdh5/v5-0-0/CDH5-Installation-Guide/CDH5-Installation-Guide.html)

6. [Hue Installation](http://www.cloudera.com/content/cloudera/en/documentation/core/latest/topics/cdh_ig_hue_installation.html)

7. [Cloudera 术语表](http://www.cloudera.com/content/cloudera/zh-CN/documentation/core/v5-3-x/topics/glossary.html)

# 鸣谢

感谢飞谷云提供主机支持，感谢项目成员提供的机会和平台。
任何疑问可随时发邮件至 7harryprince@gmail.com
