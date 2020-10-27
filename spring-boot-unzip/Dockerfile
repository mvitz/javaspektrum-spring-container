FROM adoptopenjdk/openjdk11:jdk-11.0.9_11-alpine-slim as builder

WORKDIR application

COPY ./target/spring-container-*.jar spring-container.jar

RUN jar xf spring-container.jar


FROM adoptopenjdk/openjdk11:jdk-11.0.9_11-alpine-slim

RUN mkdir -p /app/BOOT-INF && \
    chown -R daemon /app

USER daemon
WORKDIR /app

COPY --from=builder application/BOOT-INF/lib /app/BOOT-INF/lib/
COPY --from=builder application/org /app/org/

COPY --from=builder application/BOOT-INF/classes /app/BOOT-INF/classes/
COPY --from=builder application/META-INF /app/META-INF/

CMD ["java", "org.springframework.boot.loader.JarLauncher"]
EXPOSE 8080

