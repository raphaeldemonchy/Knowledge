# Utiliser une image de base Python
FROM python:3.9-slim

# Définir le répertoire de travail à l'intérieur du conteneur
WORKDIR /app

# Installer MkDocs et le thème Material
RUN pip install --upgrade pip \
    && pip install mkdocs \
    && pip install mkdocs-material

# Copier tout le contenu de ton répertoire local vers le répertoire de travail du conteneur
COPY . .

# Exposer le port 8000 pour accéder au serveur MkDocs
EXPOSE 8000

# Commande pour lancer le serveur MkDocs
CMD ["mkdocs", "serve", "--dev-addr=0.0.0.0:8000"]
