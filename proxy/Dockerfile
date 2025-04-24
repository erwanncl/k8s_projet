# Image de base : nginx
# copier default.conf dans : /etc/nginx/conf.d/default.conf
# Fichier HTML pour réponses BACKEND-NOT-FOUND : à copier dans /var/www/html/backend-not-found.html
# Configuration du proxy : copier proxy.conf dans /etc/nginx/includes/

# Utiliser l'image officielle de Nginx
FROM nginx:alpine

# Copier les fichiers de configuration Nginx dans le conteneur
COPY nginx.conf /etc/nginx/nginx.conf
COPY default.conf /etc/nginx/conf.d/default.conf
COPY proxy.conf /etc/nginx/includes/proxy.conf
COPY backend-not-found.html /var/www/html/backend-not-found.html
