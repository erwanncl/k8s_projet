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
CMD ["java", "-XX:+UnlockExperimentalVMOptions", "-XX:+UseCGroupMemoryLimitForHeap", "-jar", "/worker-jar-with-dependencies.jar"]
