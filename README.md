# 有了@Component为什么还需要@Bean？

## 1. @Bean可以将代码与定义分离
```java
@Profile("like")
@Configuration
public class AppConfigWithActiveProfile {
    @Bean
    public Subject subject(){
        Subject subject = new Subject();
        subject.setLike("物理");
        return subject;
    }
}
```

## 2. @Bean可以定义方法级别

## 3. @Bean可以将容器之外的类交给Spring容器管理

```java
@Configuration
public class ThirdPartClassAsBean {
    @Bean
    public ObjectMappper jsonMapper(){
        return new ObjectMapper();
    }
}
```