Official documentation: https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/

# Tasks:

## 1. (First main goal) Get to know [Spring Boot](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#features)

- [Naming conventions and code placement](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#using.structuring-your-code) (we add root package per layer and then package per feature)
- [Auto-configuration](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#using.auto-configuration)
- [Embedded container](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#features.developing-web-applications.embedded-container)
- [Spring Boot and Spring MVC](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#features.developing-web-applications.spring-mvc)
- Spring Boot application configuration:
    - https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#features.external-config
    - https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#howto.properties-and-configuration
## 2. (Secondary goal) Docker
- How Docker works
- pull, run, start, stop, restart
- [Dockerfile](https://cloud.google.com/blog/topics/developers-practitioners/comparing-containerization-methods-buildpacks-jib-and-dockerfile)
- Spring Boot & Docker:
    - https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#features.container-images
    - https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#howto.testing.testcontainers
## 3. (Praktical task)
- Refactor Hangman game to use Spring Boot and remove all manual configurations in favor to auto-configurations + application.yml
- Try to build docker image of the application and then run the app from the docker image