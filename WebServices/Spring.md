##Spring


####Spring Init
- start.spring.io

###Beans
####what are Beans

####what are dependency for Beans
- Autowired means the class depends on the object

####where to search for beans
- spring scan, no need for spring boot
- beans is managed by application context

####Springboot
- @SpringBootApplication will enable scan on all components


####Spring Boot Starter Project Options
- As we see from Spring Boot Starter Web, starter projects help us in quickly getting started with developing specific types of applications.
- spring-boot-starter-web-services - SOAP Web Services
- spring-boot-starter-web - Web & RESTful applications
- spring-boot-starter-test - Unit testing and Integration Testing
- spring-boot-starter-jdbc - Traditional JDBC
- spring-boot-starter-hateoas - Add HATEOAS features to your services
- spring-boot-starter-security - Authentication and Authorization using Spring Security
- spring-boot-starter-data-jpa - Spring Data JPA with Hibernate
- spring-boot-starter-cache - Enabling Spring Framework’s caching support
- spring-boot-starter-data-rest - Expose Simple REST Services using Spring Data REST
- spring-boot-starter-actuator - To use advanced features like monitoring & tracing to your application out of the box
- spring-boot-starter-undertow, spring-boot-starter-jetty, spring-boot-starter-tomcat - To pick your specific choice of Embedded Servlet Container
- spring-boot-starter-logging - For Logging using logback
- spring-boot-starter-log4j2 - Logging using Log4j2

####SpringBoot ctuator
- brings a lot of monitoring
- need configuration on it

![actuator](../image/actuator.PNG)


####SprintBoot Dev tools



####POST and send correct status back

```java
@PostMapping("/surveys/{surveyId}/questions")
  ResponseEntity<?> add(@PathVariable String surveyId,
          @RequestBody Question question) {

      Question createdTodo = surveyService.addQuestion(surveyId, question);

      if (createdTodo == null) {
          return ResponseEntity.noContent().build();
      }

      URI location = ServletUriComponentsBuilder.fromCurrentRequest()
              .path("/{id}").buildAndExpand(createdTodo.getId()).toUri();

      return ResponseEntity.created(location).build();

  }
```
