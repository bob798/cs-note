## Springboot



### springboot Pom 排除依赖包

```java
<dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
        <exclusions>
            <exclusion>
                <groupId>com.fasterxml.jackson.core</groupId>
                <artifactId>jackson-core</artifactId>
            </exclusion>
            <exclusion>
                <groupId>com.fasterxml.jackson.core</groupId>
                <artifactId>jackson-databind</artifactId>
            </exclusion>
            <exclusion>
                <groupId>com.fasterxml.jackson.core</groupId>
                <artifactId>jackson-annotations</artifactId>
            </exclusion>
        </exclusions>
    </dependency>
```

### RestTemplate 

#### 配置超时时间

https://stackoverflow.com/questions/13837012/spring-resttemplate-timeout

#### Rest template post set header 

```java
 HttpHeaders headers = new HttpHeaders();
        headers.setContentType(MediaType.APPLICATION_JSON);
         ResponseEntity<StartResult> result = restTemplate.postForEntity(startUrl, new HttpEntity<>(params, headers), StartResult.class);
```

### SpringMVC

#### 上传文件大小限制

```
spring.servlet.multipart.maxFileSize
spring.servlet.multipart.maxRequestSize
```

