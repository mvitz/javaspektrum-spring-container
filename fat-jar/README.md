# Fat-JAR

This packages the Fat-JAR into a Docker image with a custom Dockerfile.

After building the project via `./mvnw verify` the image can be build via
`docker build -t spring-container .` and the container can be started via
`docker run --rm -p 8080:8080 spring-container`.


## Requirements

An installation of JDK 11 and Docker is required.


## Modifications

The initial application was copied from the example and the real modifications
afterwards can be seen at https://github.com/mvitz/javaspektrum-spring-container/compare/12ee515b7f7a65a567099a72fdc57384e4f3a2ae...ae9ccea669eee5ad2ce1218afb450e225841fb31.

