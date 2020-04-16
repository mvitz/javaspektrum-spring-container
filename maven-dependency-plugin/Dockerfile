FROM adoptopenjdk/openjdk11:jdk-11.0.6_10-alpine-slim

RUN mkdir -p /app/lib && \
    chown -R daemon /app

USER daemon
WORKDIR /app

COPY ./target/dependency/ /app/lib
COPY ./target/spring-container-*.jar /app/spring-container.jar

CMD ["java", "-classpath", "/app/spring-container.jar:/app/lib/*", "de.mvitz.spring.container.Application"]
EXPOSE 8080

