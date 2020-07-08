FROM maven:3.5-jdk-8-alpine
WORKDIR /
ADD . //
RUN echo "$PWD"
RUN mvn install

FROM java:8
WORKDIR /
ADD target/explorecali-2.0.0-SNAPSHOT.jar //
EXPOSE 8080
ENTRYPOINT [ "java", "-jar", "/explorecali-2.0.0-SNAPSHOT.jar"]
