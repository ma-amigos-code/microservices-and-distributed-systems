# [Microservices and Distributed Systems](https://amigoscode.com/p/microservices)

## Getting Started
- **GitHub Repo** - https://github.com/amigoscode/microservices

## Bootstrap With Maven
- https://maven.apache.org/guides/mini/guide-creating-archetypes.html
- **Generate archetype command:** mvn archetype:generate -DgroupId=com.amigoscode -DartifactId=amigosservices -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
- Check use for <dependencyManagement> tag (spring boot parent project).

## Your First Microservice
- [Microservices](https://spring.io/microservices)
- [Spring Cloud](https://spring.io/projects/spring-cloud)
- [Online Spring Boot Banner Generator](https://devops.datenkollektiv.de/banner.txt/index.html)
- [Java 14 Record Keyword](https://www.baeldung.com/java-record-keyword)
- [Git commit for this section](https://github.com/amigoscode/microservices/commit/f92f2126ded6e5f432bbcff1bfe02ccdc23a3d98)

## Microservice Communication via HTTP
- Each microservice should have its own database. 
- [Git commit for this section](https://github.com/amigoscode/microservices/commit/2d0d8c2c710f7c388c72e4e66a9f04748acc751d)

## Service Discovery with Eureka
- Load balancer use a round-robin to assign a new request from the client
- [Git commit for this section](https://github.com/amigoscode/microservices/commit/f380637d80b3ff5990d3465a50da4ab35e0684d7)