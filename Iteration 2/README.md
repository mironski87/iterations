# Iteration 2 (2 weeks)

1. [Spring Core](https://docs.spring.io/spring-framework/docs/current/spring-framework-reference/core.html#spring-core)
    - Design pattern used in Spring
        + Dependency Injection (DI) и Inversion of Control (IoC)
        + Proxy (Посредник)

    - [Spring Beens and its life cycle](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans)
        + Ways to turn POJO to Spring Been (annotation, xml, Java config, etc.)
        + Spring application context life cycle-а and Spring Been life cycle

    - [Dependency injection types supported by Spring](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-annotation-config)

    - Ways to resolve missing dependency, dependency to interface with few implementations, etc.
        + [Primary](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-autowired-annotation-primary)
        + [Qualifiers](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-autowired-annotation-qualifiers)
        + [Generic qualifiers](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-generics-as-qualifiers)

    - [Java Configuration](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-java)

    - [Classpath scan](https://docs.spring.io/spring-framework/docs/current/reference/html/core.html#beans-classpath-scanning)
    
    - AOP in Spring (AspectJ и Spring AOP style approach)

1. Write pure Spring Core application (no spring boot) to demonstrate and train the learned kind of dependency injection, AOP, classpath scan, etc.

1. [Junit 5 + AssertJ](https://assertj.github.io/doc/) + [Mockito](https://site.mockito.org/)
 

# Practical task 1:

1. Build standalone application based on org.springframework.context.annotation.AnnotationConfigApplicationContext that encapsulates API for playing Hangman. Store the result in memory encapsulated in GameRepository and the logic in GameService with the following public methods ([use interfaces and implementations](https://www.linkedin.com/pulse/why-interfaces-recommend-spring-sachin-gorade/?trk=read_related_article-card_title)

    - startNewGame - returns Game description + ID of the game
    - makeTry - accepts the ID of the game and numbers to try, returns Game description + ID of the game
    - getGame - accepts the ID of the game and returns the Game if exists, otherwise null or if you prefer empty Optional
    - Write unit tests to prove startNewGame, getGame, makeTry and all helper methods (if any) work properly using Junit, Mockito and AssertJ and make 80% code coverage
    - Implementation should allow few player to play at the same time

# Practical task 2:

### Refactor existing Hangman to:

1. Have presentation layer and business logic layer
1. Business Logic layer should use the practical task 1
1. The web application should start the Spring application context
1. The presentation logic should remain the same, but use the business logic to play the game