# Main Goals

1. SQL

    - DDL
        - Create table
        - Alter table
        - Etc.

    - DML
        - Select
        - Inner join
        - Left join
        - Right join
        - Group by + having
        - In clause
        - Update
        - Insert

1. JPA/Hibernate
    - JPA – bean to entity mapping using annotations
    - One-to-one, one-to-many, many-to-many – How to implement, annotations, etc.
    - Inheritance – 3 strategies

1. DAO/Repository pattern
    - Every entity has DAO
    - CrudDao – hand made (get, listAll, create, delete, update)
    - EntityManager – use to implement CRUD and other specific queries
    - [Hibernate Criteria API](https://www.tutorialspoint.com/hibernate/hibernate_criteria_queries.htm)
    - [JPA type safe query API](https://www.tutorialspoint.com/jpa/jpa_criteria_api.htm) + [JPA Metamodel](https://www.baeldung.com/hibernate-criteria-queries-metamodel)
    - HQL and JPQL – outside of the iteration scope, you can just take a look for information

1. Spring Data
    - CRUD operation easy
    - Custom queries using conventions
    - [Spring Data Specifications + JPA Criteria Query] (https://www.baeldung.com/spring-data-criteria-queries#specifications)

# Secondary goal
1. DB Migrations with Flyway

# Practical Task

1. Add persistence layer to Hangman game
    - Keep ongoing and completed games in the DB (instead in memory)
    - MariaDB/
    - GameRepository to be implemented as DAO pattern with custom CrudDao (see 3b, c, d, e)
1. Add game statistic keeping data for every completed game (separate table) – one to one relation to game
1. Make Ranking per gamer in separate table with one-to-many relation to statistics
1. When game ends update stats + ranking – RankingService
    - Stats and Rank entities use Spring Data
1. Rank page as home page and when game is over (top 10 players)
    - Top 10 ever Spring Data + conventions (4 a + b)
    - Top 10 for last 30 days use Spring Data specifications (4c)
1. Flayway migrations to initialize DB schema + some mockup data for statistics and ranking - https://flywaydb.org/getstarted/how