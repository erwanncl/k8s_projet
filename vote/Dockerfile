# Use official python runtime base image

# Set the container application directory to /app

# ~~~ Installation des sources ~~~
# Copy our code from the current folder to /app inside the container

# ~~~ Installation des dépendances ~~~
# Add requirements.txt to container folder /app/requirements.txt 
# Execute pip install -r requirements.txt

# ~~~ Exécution de l'application ~~~
# Make port 80 available for links and/or publish

# Define the command to be run when launching the container : `python app.py`

FROM python:3.7-alpine
WORKDIR /app
COPY . /app
RUN pip install -r requirements.txt
EXPOSE 80
CMD ["python", "app.py"]

