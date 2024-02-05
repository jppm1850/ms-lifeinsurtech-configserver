# Config Server

It allows you to centralize, delegate and provision in one service the configurations of all applications in all environments.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

* [Java 17](https://www.oracle.com/technetwork/java/javase/downloads) - Programming Language.
* [Maven](https://maven.apache.org/) - Dependency Management.

### Installing

The following commands are executed for the compilation, packaging and installation of the artifact.

Maven dependency manager.
```
mvn clean
mvn install
```

## Running

Run the microservice providing the environment variables.

Maven dependency manager.
```
mvn spring-boot:run -Dspring-boot.run.arguments="--spring.cloud.config.server.git.uri=<GIT_URI> \
    --spring.cloud.config.server.git.username=<GIT_USERNAME> \
    --spring.cloud.config.server.git.password=<GIT_TOKEN> \
```

Execute the following command to test the config server's endpoint.

```
curl http://localhost:8888/{applicationName}/{profile}
```

## Built With

* [Java 17](https://www.oracle.com/technetwork/java/javase/downloads) - Programming Language.
* [Maven](https://maven.apache.org/) - Dependency Management.
* [Spring Boot](https://spring.io/projects/spring-boot) - Framework to microservices.

