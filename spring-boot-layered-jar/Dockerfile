FROM adoptopenjdk/openjdk11:jdk-11.0.6_10-alpine-slim as builder

WORKDIR application

COPY ./target/spring-container-*.jar spring-container.jar

RUN java -Djarmode=layertools -jar spring-container.jar extract


FROM adoptopenjdk/openjdk11:jdk-11.0.6_10-alpine-slim

RUN mkdir -p /app && \
    chown -R daemon /app

USER daemon
WORKDIR /app

COPY --from=builder application/dependencies /app/
COPY --from=builder application/spring-boot-loader /app/

COPY --from=builder application/application /app/

CMD ["java", "org.springframework.boot.loader.JarLauncher"]
EXPOSE 8080

