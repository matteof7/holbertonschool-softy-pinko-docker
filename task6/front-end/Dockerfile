FROM nginx:latest

# Supprime la config par défaut pour éviter conflit
RUN rm /etc/nginx/conf.d/default.conf

# Copie les fichiers du front-end dans le dossier standard Nginx
COPY ./softy-pinko-front-end /usr/share/nginx/html

# Copie ta configuration personnalisée
COPY ./softy-pinko-front-end.conf /etc/nginx/conf.d/

EXPOSE 9000
