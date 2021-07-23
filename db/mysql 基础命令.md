## mysql 基础命令

创建库

```sql
create database database_name;
导出数据库
mysqldump -h IP -u 用户名 -p -d 数据库名 > 导出的文件名

IS NULL: 当列的值是NULL,此运算符返回true。
IS NOT NULL: 当列的值不为NULL, 运算符返回true
```





```sql
# 备份数据
mysqldump -h132.72.192.432 -P3307 -uroot -p8888 htgl > bak.sql;
# 恢复数据
mysql -uusername -ppassword db1 <tb1tb2.sql

```

### 密码

```sql
# 修改mysql密码
alter user 'root'@'%' identified by 's12yLcigDhNt';
```

####  密码重置

#### 修改mysql 配置

1. 关闭mysql服务

2. 修改 /etc/mysql/my.cnf 文件

3. 增加

```
skip-grant-tables
```

4. 重启mysql 服务

#### 修改密码

```
flush privileges;
alter user 'root'@'localhost' identified by '123';
```

生成表名大小写转换sql

```sql
SELECT
concat( 'alter table ', TABLE_NAME, ' rename to ', UPPER( TABLE_NAME ), ';' ) AS ‘修改脚本’
FROM
information_schema.TABLES
WHERE
TABLE_SCHEMA = 'febs'
```

参考：https://www.cnblogs.com/ivictor/p/9243259.html

