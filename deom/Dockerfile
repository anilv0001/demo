FROM openjdk:8
RUN mvn clean install
EXPOSE 8080
ADD target/deom.jar deom.jar
ENTRYPOINT ["java","-jar","/deom.jar"]