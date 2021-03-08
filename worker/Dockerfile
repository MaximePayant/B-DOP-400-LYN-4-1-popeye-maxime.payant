#
# EPITECH PROJECT, 2021
# Tek2
# File description:
# Dockerfile
#

## === BUILDER =============>
FROM maven:3.5-jdk-8-alpine AS builder
WORKDIR /app/build

COPY src/    /app/build/src/
COPY pom.xml /app/build

RUN mvn dependency:resolve
RUN mvn -f /app/build/pom.xml package


## === RUN =================>
FROM openjdk:8-jre-alpine

COPY --from=builder /app/build/target/worker-jar-with-dependencies.jar /app/worker.jar
CMD [ "java", "-jar", "/app/worker.jar", "--link", "redis:redis" ]