# Use an official OpenJDK 17 runtime as a base image
FROM eclipse-temurin:17-jdk-alpine
# Set the working directory inside the container
WORKDIR /app
# Copy the Spring Boot application JAR file into the container
COPY target/*.jar app.jar
# Expose the port the app runs on
EXPOSE 8080
# Run the Spring Boot application
ENTRYPOINT ["java", "-jar", "app.jar"]
