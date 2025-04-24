# Use the slim (alpine) Maven image as build
FROM maven:3.5-jdk-8-alpine AS build

# Set the container application directory to /code

# ~~~ Installation des dépendances ~~~

# Copy pom.xml from the current folder to /code/pom.xml in the container

# Execute the following commands in the container :
# mvn dependency:resolve
# mvn verify

# ~~~ Installation des sources ~~~

# Copy src/main folder to /code/src/main folder in the container

# Execute the command "mvn package" in the container

# ~~~ Exécution de l'application ~~~

# Now change the base Docker image to openjdk 8 (you can use the jre alpine version to improve performance)

# Copy from the 'build' container the produced jar : /code/target/worker-jar-with-dependencies.jar in the root path of this container : /

# Define the command to be run when launching the container

# Étape 1 : build Maven
FROM maven:3.8.5-openjdk-17 AS builder
WORKDIR /app
COPY . .
RUN mvn clean package

# Étape 2 : runtime avec le .jar
FROM eclipse-temurin:17-jdk
WORKDIR /app
COPY --from=builder /app/target/worker-jar-with-dependencies.jar app.jar
CMD ["java", "-jar", "app.jar"]
