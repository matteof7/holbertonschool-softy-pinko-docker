# Étape 1 : partir de l'image officielle Ubuntu
FROM ubuntu:latest

# Étape 2 : mise à jour du système et installation des dépendances
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y python3 python3-pip

# Étape 3 : supprimer le fichier EXTERNALLY-MANAGED
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Étape 4 : installer Flask et son extension CORS
RUN pip3 install flask
RUN pip3 install flask-cors

# Étape 5 : définir le répertoire de travail
WORKDIR /app

# Étape 6 : copier le fichier Python
COPY ./api.py /app/api.py

# Étape 7 : lancer le serveur Flask
CMD ["python3", "api.py"]
