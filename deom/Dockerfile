FROM openjdk:8-jdk-alpine
VOLUME /tmp
COPY target/*.jar deom.jar
ENTRYPOINT ["java","-jar","/deom.jar"]
EXPOSE 8080