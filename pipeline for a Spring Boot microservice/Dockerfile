# Build the application

FROM maven:3.9.9-eclipse-temurin-24 AS builder
WORKDIR /app
COPY . .
RUN mvn clean package -DskipTests

# Draw .jar file and run lightweight application

FROM eclipse-temurin:24-jdk

WORKDIR /app
COPY --from=builder /app/target/*.jar app.jar

ENTRYPOINT ["java", "-jar", "app.jar"]
