# Use a smaller official OpenJDK runtime as a parent image
FROM openjdk:17-jdk-slim

# Set the working directory inside the container
WORKDIR /app

# Download the jar file into the container at /app
RUN apt-get update && apt-get install -y wget \
    && wget https://khajareferenceapps.s3.ap-south-1.amazonaws.com/spring-petclinic-3.2.0-SNAPSHOT.jar -O spring-petclinic.jar \
    && apt-get remove --purge -y wget \
    && apt-get autoremove -y \
    && rm -rf /var/lib/apt/lists/*

# Expose the port that the application will run on
EXPOSE 8080

# Set the entry point to run the jar file
ENTRYPOINT ["java", "-jar", "spring-petclinic.jar"]
