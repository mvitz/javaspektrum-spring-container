# Spring Boot Unzip

This extracts the Fat-JAR via Spring Boot layertools in a multi stage Dockerfile
and copies each directory as a separate layer.

After building the project via `./mvnw verify` the image can be build via
`docker build -t spring-container-layered-jar .` and the container can be
started via `docker run --rm -p 8080:8080 spring-container-layered-jar`.


## Requirements

An installation of JDK 11 and Docker is required.


## Modifications

The initial application was copied from spring-boot-unzip and the modifications
done can be seen at
https://github.com/mvitz/javaspektrum-spring-container/compare/b7fab88...036ad4a.

