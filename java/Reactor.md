## Reactor

事件池，推送消息给订阅者

### Flux 

0-n异步事件，三种类型消息

### Mono

被压

subscribe 订阅钱无任务处理

observable

netty

```java
WebClient webClient = WebClient.create("http://localhost:8080");

public Mono<User> findById(Long userId) {
    return webClient
            .get()
            .uri("/users/" + userId)
            .accept(MediaType.APPLICATION_JSON)
            .exchange()
            .flatMap(cr -> cr.bodyToMono(User.class));
}
```



### 参考

Intro To Reactor Core https://www.baeldung.com/reactor-core

规范：

https://projectreactor.io/