# UserServiceApplication
Microservice for authenticating the user.

  ## Requirements

For building and running the application you need:

- [Java 11](https://www.oracle.com/in/java/technologies/javase/jdk11-archive-downloads.html)
- [Maven 3](https://maven.apache.org)
- [MySQL 5.7](https://dev.mysql.com/downloads/mysql/5.7.html)

## Running the application locally

First Make sure your mysql is running fine in local if you want to run the application locally. You can change mysql `username` and `password` from `application.properties` within the resources package.

There are several ways to run a Spring Boot application on your local machine. One way is to execute the `main` method in the `de.codecentric.springbootsample.Application` class from your IDE.

Alternatively you can use the [Spring Boot Maven plugin](https://docs.spring.io/spring-boot/docs/current/reference/html/build-tool-plugins-maven-plugin.html) like so:

```shell
mvn clean install
mvn spring-boot:run
```

If you are not running the eureka server along with it, discovery client will always be failing while pinging the eureka server

## Flow

1. Admin user creates an user with specific role
2. The user gets mail on his username/email.
3. By clicking on the verification link user account gets activated
