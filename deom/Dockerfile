FROM maven:3.8.3-jdk-8-slim
VOLUME /tmp
COPY target/*.jar deom.jar
ENTRYPOINT ["java","-jar","/deom.jar"]
EXPOSE 8080