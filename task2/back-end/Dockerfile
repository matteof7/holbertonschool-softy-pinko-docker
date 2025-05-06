# Étape 1 : partir de l’image officielle Ubuntu la plus récente
FROM ubuntu:latest

# Étape 2 : mettre à jour la liste des paquets et installer Python 3 ainsi que pip3 (le gestionnaire de paquets Python)
RUN apt-get update && apt-get install -y python3 python3-pip

# Étape 3 (optionnelle) : supprimer le fichier EXTERNALLY-MANAGED si une erreur "This environment is externally managed" apparaît lors de l'installation de paquets Python
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Étape 4 : installer le framework Flask avec pip3 (pour créer des applications web en Python)
RUN pip3 install flask

# Étape 5 : définir le répertoire de travail sur /app
WORKDIR /app

# Étape 6 : copier le fichier Python dans l’image Docker
COPY ./api.py /app/api.py

# Étape 7 : lancer le serveur Flask lorsque le conteneur démarre
CMD ["python3", "api.py"]
