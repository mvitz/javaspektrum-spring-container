FROM adoptopenjdk/openjdk11:jdk-11.0.9_11-alpine-slim

RUN mkdir -p /app && \
    chown -R daemon /app

USER daemon
WORKDIR /app

COPY ./target/spring-container-*.jar /app/spring-container.jar

CMD ["java", "-jar", "/app/spring-container.jar"]
EXPOSE 8080

