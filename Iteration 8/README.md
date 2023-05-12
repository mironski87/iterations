# Main Goal

1. Security with Apache Shiro
    - [Terminology](https://shiro.apache.org/terminology.html)
    - points 1, 2 (without Session Management and Cryptography) and 3 (https://shiro.apache.org/reference.html)
    - [Spring Boot integration](https://shiro.apache.org/spring-boot.html)
    - decalrative security
        - path matching with [filter chain definition](https://shiro.apache.org/web.html#Web-FilterChainDefinitions) (ignore .ini file, we use JavaConfig with ShiroFilterChaninDefinition)
        - method level with @RequiresPermissions annotation
    - imperative (aka programmatic) with SecurityUtils.getSubject().*

# Practical Goal

Improve Hangman game scoring. A player can save his score only if he register user or login with existing one. Once logged, no need to login again after every game, the score should be immediately updated based on the logged in user. Use FORM authentication with JdbcRealm to implement the authentication. For authorization, only the scoring part will require logged in user to access it. No need of roles and permissions at this stage.