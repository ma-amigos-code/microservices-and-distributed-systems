# [Microservices and Distributed Systems](https://amigoscode.com/p/microservices)

## Getting Started
- **GitHub Repo** - https://github.com/amigoscode/microservices

## Bootstrap With Maven
- https://maven.apache.org/guides/mini/guide-creating-archetypes.html
- **Generate archetype command:** mvn archetype:generate -DgroupId=com.amigoscode -DartifactId=amigosservices -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=false
- Check use for **dependencyManagement** tag (spring boot parent project).

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

## Open Feign
- [Spring Cloud OpenFeign](https://spring.io/projects/spring-cloud-openfeign)
- [Section End Git Commit](https://github.com/amigoscode/microservices/commit/a17dc61ce08617ab75a05924f118fe5d217e799c)

## Exercise 1
- [Section End Git Commit](https://github.com/amigoscode/microservices/commit/730f3303fc36620612580a356be2d9cbeda28783)

## Distributed Tracing
- [Spring Cloud Sleuth](https://spring.io/projects/spring-cloud-sleuth)
- [OpenTracing](https://opentracing.io/)
- [Zipkin](https://zipkin.io/)
- **Docker command:** zipkin: image: openzipkin/zipkin container_name: zipkin ports: - "9411:9411"
- [Section End Git Commit](https://github.com/amigoscode/microservices/commit/e20ce91aa45d944d8b731b613e75022647d6326a)

## Api Gateway With Spring Cloud Gateway
- [GOOGLE Cloud Load Balancing](https://cloud.google.com/load-balancing)
- [AWS Elastic Load Balancing](https://aws.amazon.com/elasticloadbalancing/)
- [NGINX HTTP Load Balancing](https://docs.nginx.com/nginx/admin-guide/load-balancer/http-load-balancer/)
- [What Is Load Balancing?](https://www.nginx.com/resources/glossary/load-balancing)
- [Spring Cloud Gateway](https://spring.io/projects/spring-cloud-gateway)
- Use http://localhost:8083/api/v1/customer on postman to use the load-balancer instead direct request
- [Section End Git Commit](https://github.com/amigoscode/microservices/commit/6e7c7006b47710948c1bc588f41518b0a6a70008)

## Message Queues
- [RabbitMQ: AMQP 0-9-1 Model Explained](https://www.rabbitmq.com/tutorials/amqp-concepts.html)
- [RabbitMQ](https://www.rabbitmq.com/)
- [APACHE KAFKA](https://kafka.apache.org/)
- [Amazon Simple Queue Service](https://aws.amazon.com/sqs/)
- [When to use RabbitMQ over Kafka?](https://stackoverflow.com/questions/42151544/when-to-use-rabbitmq-over-kafka)

## RabbitMQ
- [Section End Git Commit](https://github.com/amigoscode/microservices/commit/a1176e4e799fadb265631ddbf3076443b7b221ca)