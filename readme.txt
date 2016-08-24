1.
用到的主要技术：
jersey(版本：1.18)+spring(版本：4+)+mybatis(3.2.8)+mysql

2.运行方式：
将项目导入到eclipse中，项目上右键 RUN AS ,选择 Maven Build, GOALS中填写“jetty:run”,访问端口以及参数在pom.xml 中进行修改；

2两个接口：
http://localhost:8081/helloworld/rest/user/test   查询
http://localhost:8081/helloworld/rest/user/add    新增

3.
数据库的连接信息都在applicationContext.xml 中进行修改；

4.数据库建表语句：
    CREATE TABLE `tb_user` (
      `USERID` int(10) unsigned zerofill NOT NULL AUTO_INCREMENT COMMENT '用户编码',
      `USERNAME` varchar(50) NOT NULL COMMENT '用户名',
      `PASSWORD` varchar(50) NOT NULL COMMENT '密码',
      `AGE` int(10) NOT NULL COMMENT '年龄',
      `DELETEFLAG` varchar(1) NOT NULL DEFAULT '0' COMMENT '删除标识',
      PRIMARY KEY (`USERID`),
      KEY `列 1` (`USERID`)
    ) ENGINE=InnoDB AUTO_INCREMENT=4 DEFAULT CHARSET=utf8 COMMENT='用户表';
