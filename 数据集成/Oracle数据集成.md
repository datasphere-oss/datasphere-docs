### Oracle数据集成介绍

#### Oracle同步到Hashdata

* 配置数据库源端

1. 选择Oracle数据库作为源端数据库
2. 为数据源命名: OracleSource
3. 选择处理器: OracleReader
4. 填写源端数据库的用户名: scott
5. 填写连接数据库的 JDBC 驱动 URL: 192.168.0.1:1521:orcl
6. 填写数据库需要同步的表: SCOTT.TEST
7. 填写源端数据库的密码:*******

* 配置数据库目标端

1. 选择输入流为:OracleStream
2. 选择处理器: DatabaseWriter
3. 为数据目标命名: HashdataTarget
4. 填写目标数据库的用户名: gpadmin
5. 填写连接目标数据库的 JDBC 驱动 URL: jdbc:postgresql://192.168.0.2:5432/gpadmin
6. 填写目标数据库的表清单: SCOTT.TEST,GPADMIN.TEST;
7. 填写目标数据库的密码:*******
8. 根据你的需要设置同步参数：

> 批量策略: EventCount:1,Interval:0


