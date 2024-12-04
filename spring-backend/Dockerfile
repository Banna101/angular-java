From ubuntu:latest

RUN apt update
RUN apt install openjdk-8-jdk -y
RUN apt install maven

COPY . /opt/

WORKDIR /opt/

RUN mvn clean package -Dmaven.test.skip=true

EXPOSE 8080

CMD [ "java -jar target/spring-backend-v1.jar" ]
