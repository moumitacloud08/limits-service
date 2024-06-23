# limits-service

Application	                       Port
Limits Service	                   8080, 8081, ...
Spring Cloud Config Server	       8888
Currency Exchange Service	       8000, 8001, 8002, ..
Currency Conversion Service	       8100, 8101, 8102, ...
Netflix Eureka Naming Server	   8761
Netflix Zuul API Gateway Server	   8765
Zipkin Distributed Tracing Server  9411

- connect limits-service to spring-cloud-config-server
- Modify the application.properties file to bootstrap.properties
- add following properties:-
  spring.cloud.config.uri = http://localhost:8888

- if spring.profile.active does not work then also include below property
spring.cloud.config.profile = dev

Check the URI:-
http://localhost:8080/limits
http://localhost:8888/limit-service/default
http://localhost:8888/limits-service/qa
http://localhost:8888/limits-service/dev

