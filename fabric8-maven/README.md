# fabric8 Maven

This packages the Fat-JAR into a Docker image with a custom Dockerfile via
docker-maven-plugin from fabric8.

After invoking `./mvnw verify docker:build` the container can be started via
`docker run --rm -p 8080:8080 spring-container-fabric8`.


## Requirements

An installation of JDK 11 and Docker is required.


## Modifications

The initial application was copied from the example and the real modifications
afterwards can be seen at https://github.com/mvitz/javaspektrum-spring-container/compare/2774e16...bacf7dc.

