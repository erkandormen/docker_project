### STAGE 1: Build ###
FROM maven:3.8.1-jdk-11 AS build
RUN mkdir -p /workspace
WORKDIR /workspace
COPY pom.xml /workspace
COPY src /workspace/src
RUN mvn -f pom.xml clean package

### STAGE 2: Run ###
FROM openjdk:8-alpine
COPY --from=build /workspace/target/*.jar app.jar
ENTRYPOINT ["java","-jar","bankofStates.jar"]