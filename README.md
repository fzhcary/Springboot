# Springboot

This is a sample springboot project.

It is simple example springboot application support database and microservices in its simplest form

## Project setup
step by step guide on windows
### init project
- create a spring boot app from the [spring initializer](https://start.spring.io/), choose web and database
- download the src
- install java SDK. version 17
- install intellij community version
- open project in intellij IDE

### config
modify project to support in-mem database H2
- add dependency in pom.xml
```
		<dependency>
			<groupId>com.h2database</groupId>
			<artifactId>h2</artifactId>
			<scope>runtime</scope>
		</dependency>
```
- add h2 driver
```
spring.datasource.driver-class-name=org.h2.Driver
```

### build and run
just right click the application and run


## folder structure
```agsl
|- src
|  |- main
|  |  |- java
|  |  |  |- com.example.demo
|  |  |  |  |- controller
|  |  |  |  |  |- MyController.java
|  |  |  |  |- model
|  |  |  |  |  |- MyModel.java
|  |  |  |  |- repository
|  |  |  |  |  |- MyRepository.java
|  |  |  |  |- service
|  |  |  |  |  |- MyService.java
|  |  |  |  |- DemoApplication.java
|  |  |- resources
|  |  |  |- application.properties
|  |- test
|  |  |- java
|  |  |  |- com.example.demo
|  |  |  |  |- MyControllerTest.java
|  |  |  |  |- MyServiceTest.java
|  |  |- resources
|- pom.xml

```
-   `src/main/java` contains the main source code of the project.
-   `com.example.demo` is the base package of the project.
-   `controller` contains the REST controllers that handle HTTP requests.
-   `model` contains the domain models or entities of the application.
-   `repository` contains the data access objects (DAOs) that interact with the database.
-   `service` contains the business logic of the application.
-   `DemoApplication.java` is the main class that bootstraps the Spring Boot application.
-   `src/main/resources` contains application configuration files, such as `application.properties` or `application.yml`.
-   `src/test/java` contains the unit and integration tests.
-   `pom.xml` is the Maven build file that contains project dependencies and build configurations.

## Tests
curl script
```
curl --location 'http://localhost:8080/person/add' \
--header 'Content-Type: application/json' \
--data '{"firstName":"John","lastName":"Doe","age":30}'

curl --location 'http://localhost:8080/person/1'
```
