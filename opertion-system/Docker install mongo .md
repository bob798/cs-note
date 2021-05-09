Docker install mongo 

```shell
 docker run --name some-mongo -p 27017:27017 -d mongo
 # login mongo
 docker exec -it some-mongo bash
 # 创建用户
  db.createUser({ user: "test", pwd: "test", roles: [{ role: "readWriteAnyDatabase", db: "admin" }] })
```

mongo cmd

```
db
# 进入db 如db不存在，直接创建
use db
show dbs
# 插入数据，新创建的db中无数据 不显示
db.myCollection.insertOne( { x: 1 } );
```

mongo shell https://docs.mongodb.com/manual/mongo/

create database：https://www.mongodb.com/basics/create-database

mongo 用户 添加 修改 删除 权限追加：https://www.luoruiyuan.cn/pages/id-84_uid-2_btid-20.html

权限说明

```
user：用户名

pwd：密码

db：指定该用户的数据库，admin是用于权限控制的数据库，如果没有需要新建一个

roles：指定用户的角色，可以用一个空数组给新用户设定空角色；在roles字段,可以指定内置角色和用户定义的角色。role里的角色可以选：

Built-In Roles（内置角色）：
    1. 数据库用户角色：read、readWrite;
    2. 数据库管理角色：dbAdmin、dbOwner、userAdmin；
    3. 集群管理角色：clusterAdmin、clusterManager、clusterMonitor、hostManager；
    4. 备份恢复角色：backup、restore；
    5. 所有数据库角色：readAnyDatabase、readWriteAnyDatabase、userAdminAnyDatabase、dbAdminAnyDatabase
    6. 超级用户角色：root  
    // 这里还有几个角色间接或直接提供了系统超级用户的访问（dbOwner 、userAdmin、userAdminAnyDatabase）
    7. 内部角色：__system
```

没有用户和密码,MongoDB的客户端NoSQL Manager for MongoDB是无法连接的

```
网上总结了四条
MongoDB是没有默认管理员账号，所以要先添加管理员账号，再开启权限认证。
切换到admin数据库，添加的账号才是管理员账号。
用户只能在用户所在数据库登录，包括管理员账号。
管理员可以管理所有数据库，但是不能直接管理其他数据库，要先在admin数据库认证后才可以。
使用经验：https://blog.csdn.net/u013066244/article/details/53874216
```

