## golang 初识

### net网络

#### 基于tcp的http服务

http架构在tcp之上，基于tcp请求，增加http返回协议，完成对http处理。

### tcp

https://hiberabyss.github.io/2018/03/14/unix-socket-programming/

### 并发

并发发送http get请求，通过 waitGroup控制协程的执行流程，等待子流程执行完毕后，在关闭主协程main方法

### IO

read、write如何理解？

工具类

- io
- ioutil
- bufio

### 引用类型工具包

#### strings 字符工具包

### 字符串格式化

- Printf 格式化输出
- Sprintf 格式化，并返回字符串
- Fprintf 格式化，并输出到io.writes
