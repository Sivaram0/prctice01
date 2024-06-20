FROM openjdk:17-jdk-alpine
Workdir /app
RUN wget https://khajareferenceapps.s3.ap-south-1.amazonaws.com/spring-petclinic-3.2.0-SNAPSHOT.jar
EXPOSE 8080
ENTRYPOINT ["java","-jar","spring-petclinic.jar"]
