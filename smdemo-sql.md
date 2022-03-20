```sql
--任务发布
CREATE TABLE `daskclaim` (
  `daskname` varchar(20) NOT NULL COMMENT '任务名',
  `daskcontent` varchar(100) NOT NULL COMMENT '任务内容',
  `overtime` datetime(6) NOT NULL COMMENT '截止时间',
  PRIMARY KEY (`daskname`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8

```



```sql
----签到情况
CREATE TABLE `qiandao` (
  `id` int(32) NOT NULL,
  `username` varchar(10) NOT NULL COMMENT '用户名',
  `begintime` datetime(6) NOT NULL COMMENT '开始时间',
  `overtime` datetime(6) NOT NULL COMMENT '结束时间',
  `totaltime` double NOT NULL COMMENT '签到时长',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8


```



```sql
--任务提交
CREATE TABLE `daskup` (
  `daskname` varchar(20) NOT NULL COMMENT '任务名',
  `clic` varchar(30) NOT NULL COMMENT '下载链接',
  `filename` varchar(20) NOT NULL COMMENT '文件名',
  PRIMARY KEY (`daskname`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8

```



```sql
--未完成名单
CREATE TABLE `definishname` (
  `daskname` varchar(20) NOT NULL COMMENT '任务名',
  `id` int(32) NOT NULL COMMENT '用户id',
  `username` varchar(10) NOT NULL COMMENT '未完成用户名',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8

```



```sql
--已完成名单
CREATE TABLE `finishname` (
  `daskdame` varchar(20) NOT NULL COMMENT '任务名',
  `id` int(11) NOT NULL COMMENT '用户id',
  `usename` varchar(10) NOT NULL DEFAULT 'null' COMMENT '已完成名',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8

```



```sql
--创建账户
CREATE TABLE `zhanghu` (
  `id` int(32) NOT NULL AUTO_INCREMENT,
  `username` varchar(10) NOT NULL COMMENT '用户名',
  `password` varchar(10) NOT NULL COMMENT '密码',
  `direction` varchar(10) NOT NULL COMMENT '方向',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8

```

