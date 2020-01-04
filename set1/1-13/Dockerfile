# TO BUILD CONTAINER RUN (inside repository)
# $ docker build -t spring-app .

# TO RUN CONTAINER
# $ docker run -p 8080:8080 -d  spring-app


FROM openjdk:latest
WORKDIR /app
COPY . /app
EXPOSE 8080
RUN ./mvnw package
CMD ["java", "-jar",  "./target/docker-example-1.1.3.jar"]
