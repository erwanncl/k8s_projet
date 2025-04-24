# Use official node image (tag 10-slim)

# Set the container application directory to /app

# ~~~ Installation des dépendances ~~~

# Copy package*.json from the current folder to the current folder in the container

# Execute the following commands in the container :
# npm install -g nodemon 
# npm cache clean --force
# mv /app/node_modules /node_modules

# ~~~ Installation des sources ~~~

# Copy the current folder (of the project) to the current folder in the container

# Execute the following command in the container :
# npm ci

# ~~~ Exécution de l'application ~~~

# Set the environment variable PORT to 80

# Make port 80 available for links and/or publish

# Define the command "nodemon server.js" to be run when launching the container

FROM node:14-alpine
WORKDIR /app
COPY . /app
RUN npm install
EXPOSE 80
CMD ["node", "server.js"]

