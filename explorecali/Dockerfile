FROM maven:3.5-jdk-8-alpine as build
ARG project  
RUN echo -e 'test1' > /test1.txt
WORKDIR pwd
RUN mvn install

FROM java:8
WORKDIR /
ADD target/explorecali-2.0.0-SNAPSHOT.jar //
EXPOSE 8080
ENTRYPOINT [ "java", "-jar", "/explorecali-2.0.0-SNAPSHOT.jar"]
