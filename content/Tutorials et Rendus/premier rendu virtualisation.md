# Récapitulatif du TP n°1 : Rappel Docker

## Objectif

Révision des commandes Docker essentielles et déploiement de conteneurs pour diverses applications comme Apache, MySQL et MongoDB.

## Tâches effectuées

### Déploiement Simple de Docker Conteneur Apache

1. Téléchargement de l'image Apache :

```bash
docker pull httpd
```

2. Création et lancement du conteneur :

```bash
docker run -d -p 80:80 --name apache httpd
```

3. Suppression du conteneur Apache :

```bash
docker rm -f apache
```

### Utilisation de Dockerfile pour Apache

1. Construction de l'image personnalisée :

```bash
docker build -t custom-apache .
```

2. Création et lancement du conteneur :

```bash
docker run -d -p 80:80 --name apache custom-apache
```

3. Suppression du conteneur :

```bash
docker rm -f apache
```

### Déploiement de Docker Conteneur MySQL

1. Téléchargement de l'image MySQL :

```bash
docker pull mysql
```

2. Création et lancement du conteneur :

```bash
docker run -d -p 3306:3306 --name mysql-test -e MYSQL_ROOT_PASSWORD=secret mysql
```

3. Suppression du conteneur MySQL :

```bash
docker rm -f mysql-test
```

### Utilisation de volume avec MySQL

1. Création et lancement du conteneur avec volume :

```bash
docker run -d -p 3306:3306 --name mysql-test -e MYSQL_ROOT_PASSWORD=secret -v $(pwd)/mysql-data:/var/lib/mysql mysql
```

2. Suppression du conteneur et du volume :

```bash
docker rm -f mysql-test
```
### Déploiement de Réseau Docker avec MongoDB et mongo-express

1. Création du réseau :

```bash
docker network create reseau-mongo
```

2. Déploiement de MongoDB :

```bash
docker run -d --network reseau-mongo -e MONGO_INITDB_ROOT_USERNAME=admin -e MONGO_INITDB_ROOT_PASSWORD=secret --name mongo mongo
```

### Docker Compose

1. Lancement de l'application :

```bash
docker-compose up -d
```

2. Arrêt de l'application :

```bash
docker-compose down
```

## Conclusions

Les commandes Docker de base ont été revues avec succès et des conteneurs pour Apache, MySQL et MongoDB ont été déployés. Des volumes et des réseaux ont également été créés pour le stockage et la communication entre les conteneurs.