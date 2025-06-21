# Image de base
FROM python:3.8-buster

# Informations du mainteneur
LABEL maintainer="Ihab Hilal <hilalihab91@example.com>"

# Définir le répertoire de travail
WORKDIR /

# Copier les fichiers nécessaires
COPY student_age.py /
COPY requirements.txt /

# Installer les dépendances
RUN apt update -y && apt install python3-dev libsasl2-dev libldap2-dev libssl-dev -y
RUN pip install -r requirements.txt

# Créer un dossier pour stocker les données
RUN mkdir /data

# Exposer le port 5000
EXPOSE 5000

# Commande de démarrage
CMD ["python3", "./student_age.py"]
