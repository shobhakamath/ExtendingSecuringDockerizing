FROM maven:3.5-jdk-8-alpine
WORKDIR /
ADD . //
EXPOSE 8080
ENTRYPOINT [ "mvn", "spring-boot:run", "-Dspring.profiles.active=mysql"]

