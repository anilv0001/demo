FROM openjdk:8 As build
COPY . .
RUN mvn clean package -DskipTests
FROM maven:3.8.3-jdk-8-slim
COPY --from=build /target/demo-0.0.1-SNAPSHOT.jar demo.jar
EXPOSE 8080
ENTRYPOINT ["java","-jar","demo.jar"]