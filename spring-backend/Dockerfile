From ubuntu:latest

# Update package lists and install dependencies
RUN apt update
RUN apt install openjdk-8-jdk -y
RUN apt install maven -y

# Copy application files to the container
COPY . /opt/

# Set the working directory
WORKDIR /opt/

# Build the application, skipping tests
RUN mvn clean package -Dmaven.test.skip=true

# Expose the application port
EXPOSE 8080

# Define the command to run the application
CMD [ "java", "-jar", "target/spring-backend-v1.jar" ]
