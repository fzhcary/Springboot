# Springboot

This is a sample springboot project.

It is simple example springboot application support database and microservices in its simplest form

step by step guide on windows
## init project
- create a spring boot app from the [spring initializer](https://start.spring.io/), choose web and database
- download the src
- install java SDK. version 17
- install intellij community version
- open project in intellij IDE

## config
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

## build and run
just right click the application and run
