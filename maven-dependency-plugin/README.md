# Maven Dependency Plugin

This packages all dependencies, retrieved via maven-dependency-plugin, into an
own layer.

After building the project via `./mvnw verify` the image can be build via
`docker build -t spring-container .` and the container can be started via
`docker run --rm -p 8080:8080 spring-container`.


## Requirements

An installation of JDK 11 and Docker is required.


## Modifications

The initial application was copied from fat-jar and the modifications done can
be seen at https://github.com/mvitz/javaspektrum-spring-container/compare/216a834...368226b.

