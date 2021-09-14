# Spring Boot GraphQL Demo Project [![Twitter](https://img.shields.io/twitter/follow/piotr_minkowski.svg?style=social&logo=twitter&label=Follow%20Me)](https://twitter.com/piotr_minkowski)

In this demo repository I'm demonstrating the most interesting libraries and features for integrating Spring Boot with GraphQL.

## Important notes
This repository has been reorganized and now contains two different applications. First of them, `sample-app-kickstart` shows how to use the project called [GraphQL Kickstart](https://github.com/graphql-java-kickstart/graphql-spring-boot). The second of them `sample-app-netflix-dgs` shows how to use [Netflix DGS](https://netflix.github.io/dgs) library for GraphQL with Spring Boot.

## Getting Started 
1. How to simplify Spring Boot and GraphQL development with GraphQL Kickstart library. The article describes more advanced solution like filtering or joins with a database. The example is available in the branch [master](https://github.com/piomin/sample-spring-boot-graphql/tree/master/sample-app-kickstart). A detailed guide may be found in the following article: [An Advanced Guide to GraphQL with Spring Boot](https://piotrminkowski.com/2020/07/31/an-advanced-guide-to-graphql-with-spring-boot/)
2. How to simplify Spring Boot and GraphQL development with Netflix DGS library. The example is available in the branch [master](https://github.com/piomin/sample-spring-boot-graphql/tree/master/sample-app-netflix-dgs). A detailed guide may be found in the following article: [An Advanced GraphQL with Spring Boot and Netflix DGS](https://piotrminkowski.com/2021/04/08/an-advanced-graphql-with-spring-boot-and-netflix-dgs/).

## Executing Started 
1. To check health:  http://localhost:8080/actuator
2. To Launch grpahql: http://localhost:8080/graphiql
3. Sample Request:
      {
      employeesWithFilter(filter:
      {
      salary: {operator: "gt", value: "12000"},
      age: {operator: "gt", value: "30"},
      position: {operator: "eq", value: "Architect"}
      }) {
      id
      firstName
      lastName
      position
      salary
      age
      }
      }
