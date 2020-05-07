
# Build stage
#FROM maven:3.6.0-jdk-11-slim AS build
#COPY src /home/app/src
#COPY pom.xml /home/app
#RUN mvn -f /home/app/pom.xml clean package


# package docker
#FROM openjdk:8-jdk-alpine
#COPY --from=build /home/app/target/java-docker-1.0.0-SNAPSHOT.jar /tmp/app.jar
#COPY target/java-docker-1.0.0.jar /tmp/app.jar
#EXPOSE 8080
#ENTRYPOINT ["java","-jar","/tmp/app.jar"]

#FROM docker/openjdk/openjdk-8-rhel8
FROM artifactory.ual.com:443/docker/openjdk/openjdk-8-rhel8
#COPY target/java-docker-1.0.0-SNAPSHOT.jar /tmp/app.jar
COPY java-docker-1.0.0-SNAPSHOT.jar /tmp/app.jar
#RUN wget -O /tmp/app.jar https://artifactory.ual.com/artifactory/libs-snapshots-local/com/ual/cust/des/trvl/pocs/java-docker/1.0.0-SNAPSHOT/java-docker-1.0.0-SNAPSHOT.jar
EXPOSE 8083
ENTRYPOINT ["java","-jar","/tmp/app.jar"]
