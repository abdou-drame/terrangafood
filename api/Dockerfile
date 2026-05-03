# Dockerfile API TerrangaFood

# Étape 1 : Image de base légère Node.js 20 sur Alpine
FROM node:20-alpine

# Étape 2 : Répertoire de travail dans le conteneur
WORKDIR /app

# Étape 3 : Copier les fichiers de dépendances (package.json et package-lock.json)
COPY package.json package-lock.json* ./

# Étape 4 : Installer les dépendances de production uniquement
RUN npm install --production

# Étape 5 : Copier tout le code source restant
COPY . .

# Étape 6 : Documenter le port utilisé par l'API
EXPOSE 3001

# Étape 7 : Commande de démarrage du conteneur
CMD ["node", "src/app.js"]