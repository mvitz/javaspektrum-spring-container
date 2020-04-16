# Fat-JAR

This packages the Fat-JAR into a Docker image with a custom Dockerfile.

After building the project via `./mvnw verify` the image can be build via
`docker build -t spring-container .` and the container can be started via
`docker run --rm -p 8080:8080 spring-container`.


## Requirements

An installation of JDK 11 and Docker is required.


## Modifications

The initial application was copied from example and the modifications done can
be seen at
https://github.com/mvitz/javaspektrum-spring-container/compare/12ee515...ae9ccea.

