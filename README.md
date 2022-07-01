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

## Packaging Microservices to Runnable Jar
- [Welcome to Apache Maven](https://maven.apache.org/index.html)
- [Apache Maven Compiler Plugin](https://maven.apache.org/plugins/maven-compiler-plugin/)
- [Spring Boot Maven Plugin Documentation](https://docs.spring.io/spring-boot/docs/current/maven-plugin/reference/htmlsingle/)
- [Introduction to the Build Lifecycle](https://maven.apache.org/guides/introduction/introduction-to-the-lifecycle.html)
- [Section End Git Commit](https://github.com/amigoscode/microservices/commit/60a9c39d8962f5cf3fa21d7f5ca84d4f9dcae442)

## Packaging Jars to Docker Images
- [Amazon Elastic Container Registry (Amazon ECR)](https://aws.amazon.com/ecr/)
- [Docker Hub](https://hub.docker.com/)
- [Spring Boot Maven Plugin Documentation](https://docs.spring.io/spring-boot/docs/current/maven-plugin/reference/htmlsingle/)
- [GoogleContainerTools/jib](https://github.com/GoogleContainerTools/jib)
- [adoptopenjdk](https://hub.docker.com/_/adoptopenjdk)
- [eclipse-temurin](https://hub.docker.com/_/eclipse-temurin/)
- `mvn clean package -P build-docker-image`
- [Spring Profiles](https://docs.spring.io/spring-boot/docs/current/reference/html/features.html#features.profiles)
- [Section End Git Commit](https://github.com/amigoscode/microservices/commit/7315fb413b3852599bcf9abd88657270a4bf60df)
- **To download from docker-hub using docker-compose.yml file:** docker compose pull
- docker compose up -d
- docker logs <ImageName>
- docker compose down

## Kubernetes AKA k8s
- [Kubernetes](https://kubernetes.io/)
- Clusters:
  - Cluster is a set of nodes
  - Node - Virtual Machine (VM) or Physical Machine
- Kubernetes Cluster:
  - **Master Node**: the brain of the cluster (decisions are made)
  - **Worker Node**: heavy lifting works (running your application)
  - Both communicate by kubernetes
- [etcd](https://etcd.io/)
- [containerd](https://containerd.io/)
- [minikube](https://minikube.sigs.k8s.io/docs/)
- [**kubectl**](https://kubernetes.io/docs/tasks/tools/#kubectl) (kubernetes command line tool) will allow us to interact with our cluster:
  - Run commands gains our cluster
    - Deploy
    - Inspect
    - Edit resources
    - Debug
    - View logs
    - ETC
- [Kubernetes Getting started](https://kubernetes.io/docs/setup/)
- **POD**:
  - is the smallest deployable unit in Kubernetes and not containers
  - has its unique IP address
  - is a collection of containers
  - represents a running process
  - share same network and volumes
  - never create pods on its own. use controllers instead
  - ephemeral and disposable
- The truth about pods:
  - Never deploy pods using **kind:Pod**
  - Don't treat pods like pets
  - They are ephemeral (lives for a very short time)
  - Pods on its own don't self-heal
- Deployments:
  - Manages release of new application
  - Zero downtime deployments
  - Create _ReplicaSet_
- Services:
  - How do we access how app?
  - Not using port-forward. **Only testing**
- Service Discovery:
  - Mechanism for application and microservices to locate each other on a network
  - [What is DNS? | How DNS works](https://www.cloudflare.com/learning/dns/what-is-dns/)
  - [CoreDNS: DNS and Service Discovery](https://coredns.io/)
  - KubeProxy: 
    - Network proxy that runs on each node. Implementing part of the Kubernetes **Service**.
    - Maintains network rules to allow communication to **pods** from inside and outside the cluster.
    - Implements a controller that watches the API server for new **Services** and **Endpoints**
    - Creates Local **IPVS (IP Virtual Server)** rules that tell node to intercept traffic destines to the service **ClusterIP**
- minikube commands:
  - **Start cluster:** minikube start --memory=4g
  - minikube status
- kubectl commands:
  - kubectl get pods
  - kubectl run hello-world --image=amigoscode/kubernetes:hello-world --port=80
  - kubectl port-forward pod/hello-world 8080:80
  - kubectl delete pod hello-world

## Deploying Postgres RabbitMQ and Zipkin to k8s
- kubectl commands:
  - Apply YMLs from **bootstrap/postgres** folder: `kubectl apply -f bootstrap/postgres`
  - **Execute postgres-0 pod:** `kubectl exec -it postgres-0 -- psql -U amigoscode`
  - `kubectl get services`
- minikube commands:
  - minikube service --url rabbitmq
  - **To access services on the specified port:** minikube tunnel
- [Section End Git Commit](https://github.com/amigoscode/microservices/commit/f2e56b7a2e5749a149acdcbb16be088616bb9ca2)

## Refactoring Microservices for k8s
- No need for API Gateway Anymore
  - k8s offers a service type called LoadBalancer and this will provision a load balancer according to your cloud environment. I.e. AWS, GCP or Azure. It is best to use managed load balancer instead of managing and configure ours.
- No need for Eureka (service discovery), k8s offers that for free.
- **@FeignClient(value = "fraud")** won't work because we are not using Eureka client, then we need to specify the URL
- We don't need to specify ports for PODS, we just need to specify the **service name**
- Put **SPRING_PROFILES_ACTIVE=default** on Environment variables inside configurations on IntelliJ
- [Section End Git Commit](https://github.com/amigoscode/microservices/commit/9185c4a446640855c97bf733fe0a2f44a551018d)

## Deploying Microservices to k8s
- `kubectl apply -f minikube/services/customer`
- `kubectl describe pod customer-74db9d484-pj5rp`
- `kubectl logs customer-74db9d484-pj5rp -f`
- `kubectl scale --replicas=0 deployment customer`
- [Section End Git Commit](https://github.com/amigoscode/microservices/commit/bc06317c26e63aa66bc6e6406a1f413532ce5b7b)

## Managed Kubernetes Cluster with Linode
- Commands for this sections
  - **Commands Used**  
    export KUBECONFIG=~/amigoscode-kubeconfig.yml  

    kubectl get nodes
    kubectl get ns
   
    kubectl apply -f path
    kubectl delete -f path  
    
    kubectl get po
    kubectl get svc
    kubectl get po -w  
    
    kubectl logs postgres-0  
    
    kubectl exec -it postgres-0 -- psql -U amigoscode    
    
    kubectl describe pod podName  
    
    kubectl logs podName
    kubectl logs -f podName  
    
    kubectl exec -it postgres-0 -- psql -U linpostgres -h lin-4621-419-pgsql-primary.servers.linodedb.net
    kubectl exec -it postgres-0 -- psql --help
    kubectl exec -it postgres-0 -- psql -U linpostgres -h lin-4621-419-pgsql-primary.servers.linodedb.net
    kubectl exec -it postgres-0 -- bash  
    
    psql -U host -U username -d database
    \d
    \dt
    \c databaseName
    create database dbName;
    select * from tableName;
- [linode](https://www.linode.com/)
- $env:KUBECONFIG = "C:\Users\AAA.bluemix\plugins\container-service\clusters\customernameabc\kube-config-hou02-clusternameabc.yml"