FROM openjdk:15-jdk-slim AS builder

WORKDIR /app

COPY mvnw .
COPY .mvn .mvn
COPY pom.xml .
COPY src src

RUN ./mvnw dependency:go-offline

CMD ["./mvnw", "spring-boot:run"]
