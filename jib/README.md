# jib

This produces a layer Docker image by using jib.

The project can be build via `./mvnw verify jib:dockerBuild` and the container
can be started via `docker run --rm -p 8080:8080 spring-container-jib`.


## Requirements

An installation of JDK 11 and Docker is required.


## Modifications

The initial application was copied from example and the modifications done can
be seen at
https://github.com/mvitz/javaspektrum-spring-container/compare/addaef2...c898271.

