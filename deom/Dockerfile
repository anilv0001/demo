# FROM openjdk:8-jdk-alpine
# VOLUME /tmp
# COPY target/*.jar deom.jar
# ENTRYPOINT ["java","-jar","/deom.jar"]
# EXPOSE 8080

#
# Build stage
#
FROM maven:3.8.2-jdk-11 AS build
COPY . .
RUN mvn clean package -DskipTests

#
# Package stage
#
FROM openjdk:11-jdk-slim
COPY --from=build /target/*.jar deom.jar
# ENV PORT=8080
EXPOSE 8080
ENTRYPOINT ["java","-jar","deom.jar"]
