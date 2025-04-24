# Utiliser l'image Maven pour construire le projet
FROM maven:3.5-jdk-8-alpine AS build
WORKDIR /code
COPY pom.xml /code/pom.xml
COPY src /code/src
RUN mvn package

# Utiliser l'image OpenJDK pour exécuter le JAR
FROM openjdk:8-jre-alpine
COPY --from=build /code/target/worker-jar-with-dependencies.jar /worker-jar-with-dependencies.jar
CMD ["java", "-XX:+UnlockExperimentalVMOptions", "-XX:+UseCGroupMemoryLimitForHeap", "-jar", "/worker-jar-with-dependencies.jar"]
