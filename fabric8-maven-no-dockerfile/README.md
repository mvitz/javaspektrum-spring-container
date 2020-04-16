# fabric8 Maven without Dockerfile

This packages the Fat-JAR into a Docker image without a custom Dockerfile via
docker-maven-plugin from fabric8.

After invoking `./mvnw verify docker:build` the container can be started via
`docker run --rm -p 8080:8080 spring-container-fabric8-no-dockerfile`.


## Requirements

An installation of JDK 11 and Docker is required.


## Modifications

The initial application was copied from fabric8-maven and the modifications done
can be seen at
https://github.com/mvitz/javaspektrum-spring-container/compare/fe5683e...0d1c31d.

