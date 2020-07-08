FROM maven:3.5-jdk-8-alpine
WORKDIR /
ADD . //
RUN mvn package -DskipTests


FROM java:8
EXPOSE 8080
ENTRYPOINT [ "java", "-jar", "target/explorecali-2.0.0-SNAPSHOT.jar"]
