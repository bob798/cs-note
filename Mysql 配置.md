## Mysql 配置

数据库目录：/var/lib/mysql  
配置文件默认在：/etc/my.cnf  
相关命令：/usr/bin  
**数据库文件默认在**：cd /usr/share/mysql

相关配置查看：**show variables like ‘%dir%’;**



mysql 配置

 表名大小敏感 lower_case_table_names

设置为1

```
取值范围有三个，分别是0、1、2. 
1. 设置成0：表名按你写的SQL大小写存储，大写就大写小写就小写，比较时大小写敏感。 
2. 设置成1：表名转小写后存储到硬盘，比较时大小写不敏感。 
3. 设置成2：表名按你写的SQL大小写存储，大写就大写小写就小写，比较时统一转小写比较。
```



