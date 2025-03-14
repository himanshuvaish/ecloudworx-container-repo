# # For Java 8, try this
# # FROM openjdk:8-jdk-alpine

# # For Java 11, try this
# FROM adoptopenjdk/openjdk11:alpine-jre

# # Refer to Maven build -> finalName
# ARG JAR_FILE=target/spring-boot-web.jar

# # cd /opt/app
# WORKDIR /opt/app

# # cp target/spring-boot-web.jar /opt/app/app.jar
# COPY ${JAR_FILE} spring-boot-web.jar

# # java -jar /opt/app/app.jar
# ENTRYPOINT ["java","-jar","spring-boot-web.jar"]

# ## sudo docker run -p 8080:8080 -t docker-spring-boot:1.0
# ## sudo docker run -p 80:8080 -t docker-spring-boot:1.0
# ## sudo docker run -p 443:8443 -t docker-spring-boot:1.0

# For Java 11, try this
FROM openjdk:11-jre-slim

# Refer to Maven build -> finalName
ARG JAR_FILE=target/spring-boot-web.jar

# Set the working directory
WORKDIR /opt/app

# Copy the jar file to the container
COPY ${JAR_FILE} spring-boot-web.jar

# Specify the entry point for the application
ENTRYPOINT ["java","-jar","spring-boot-web.jar"]