# Spring Boot Buildpacks

This produces a layer Docker image by using Buildpacks.

The project can be build via `./mvnw spring-boot:build-image` and the container
can be started via `docker run --rm -p 8080:8080 spring-container-buildpacks`.


## Requirements

An installation of JDK 11 and Docker is required.


## Modifications

The initial application was copied from example and the modifications done can
be seen at
https://github.com/mvitz/javaspektrum-spring-container/compare/c600d97...ab229e6.

