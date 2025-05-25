# 🚀 Spring Boot Microservice

## 📝 Overview
This is a simple Spring Boot project featuring integrated CI/CD using GitLab , as well as Docker and security scanning support.

## 🔧 Prerequisites
- Java 24+
- Maven 3.9+ 
- Docker 
- GitLab (for CI/CD)

## 🚀 Setup & Run
### Local Run
Clone the repository and navigate into the project directory:
```bash
git clone https://gitlab.com/khkhkhkhader/Gitlab-CI-CD.git
cd 'Gitlab-CI-CD/pipeline for a Spring Boot microservice'
```
Build the project:
```bash
mvn clean install
```

Run the application:
```bash
java -jar target/*.jar
```

### Run with Docker
Build the Docker image:
```bash
docker build -t spring-boot-app .
```

Run the Docker container:
```bash
docker run -p 8080:8080 spring-boot-app
```

## 🔄 CI/CD Pipeline
The project includes a GitLab CI/CD pipeline triggered automatically for every merge request:
- **Build Stage**: Using `maven:3.9.9-eclipse-temurin-24` image to build the project with Maven and Java 24.
- **Security Scan**: Trivy scans for vulnerabilities in Docker images and dependencies in the pipeline.
- **Docker Publish**: Optional step to publish Docker images.
- **Deploy or Test**: Additional stages can be configured based on your needs.

