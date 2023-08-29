FROM openjdk:8
VOLUME /tmp
COPY target/*.jar deom.jar
ENTRYPOINT ["java","-jar","/deom.jar"]
EXPOSE 8080