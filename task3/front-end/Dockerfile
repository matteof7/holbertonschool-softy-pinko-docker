# Étape 1 : partir de l’image officielle Nginx la plus récente
FROM nginx:latest

# Étape 2 : copier les fichiers du front-end dans le dossier web de Nginx
COPY ./softy-pinko-front-end /var/www/html/softy-pinko-front-end

# Étape 3 : copier la configuration personnalisée de Nginx
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/default.conf
