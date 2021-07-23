## mysql-error

\- Failed to validate connection com.mysql.cj.jdbc.ConnectionImpl@2c01a219 (Communications link failure

#### The last packet successfully received from the server was 2,362,858 milliseconds ago. The last packet sent successfully to the server was 2,362,897 milliseconds ago.). Possibly consider using a shorter maxLifetime value.

这个问题应该是nacos设置的数据库连接的有效期大于了数据库那边设置的有效期， 导致连接池继续复用已被数据库测关闭的连接导致的。可以尝试修改加长mysql的连接有效期。或可以在jdbcurl上增加以下配置 先行解决。

```
&autoReconnect=true&failOverReadOnly=false
```

#### Could not get Connection for extracting meta-data; nested exception is org.springframework.jdbc.Cann

时区问题，可通过jdbc或my.cnf修改

### java.sql.SQLNonTransientConnectionException: Could not create connection to database server. Attempt，

**serverTimezone=UTC&useSSL=false&allowPublicKeyRetrieval=true**
