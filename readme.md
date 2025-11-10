# My Cool App

This is a demo project for **Spring Boot**.

## Main Features

*   **Spring Boot:** Provides a quick way to create stand-alone, production-grade Spring-based Applications.

*   **Spring Web:** Used for building web, including RESTful, applications using Spring MVC.

*   **Spring Boot DevTools:** Provides fast application restarts, LiveReload, and configurations for an enhanced development experience.

*   **Spring Boot Actuator:** Allows you to monitor and manage your application.

## Dependencies

*   `spring-boot-starter-web`

*   `spring-boot-devtools`

*   `spring-boot-starter-actuator`

*   `spring-boot-starter-test` (for testing)

## How to Run

1.  Clone the repository.

2.  Make sure you have Java 17 and Maven installed.

3.  Navigate to the project directory.

4.  Run the application using `./mvnw spring-boot:run`.

## How to see the actuator capabilities

The **application.properties** file is already configured to expose all actuator endpoints using management.endpoints.web.exposure.include=*.

This makes endpoints like health checks, application info, and beans available over HTTP.

To see the **actuator** capabilities in action:

1. Run the application.
   
2. Access the main actuator endpoint in your browser or with a tool like curl: **http://localhost:8080/actuator**

3. This will show you a list of all available endpoints. Here are a few examples:

◦ **http://localhost:8080/actuator/health**: Shows the application's health.

◦ **http://localhost:8080/actuator/info**: Displays general application information. You've already customized this in your application.properties file.

◦ **http://localhost:8080/actuator/beans**: Lists all the Spring beans in your application.

◦ **http://localhost:8080/actuator/mappings**: Shows all the @RequestMapping paths.

For security, in a production environment, you should be selective about which endpoints you expose. 

For example, you could replace * with a comma-separated list like health,info.
