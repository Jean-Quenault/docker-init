# Docker Compose pour PHPMyAdmin et MySQL

Ce projet configure un environnement dockerisé avec PHPMyAdmin et MySQL en utilisant Docker Compose.

## Prérequis

- Docker installé sur votre machine.
- Docker Compose installé sur votre machine.

## Installation et démarrage

1. **Cloner le dépôt** (si vous avez mis le fichier `docker-compose.yml` dans un dépôt git) ou simplement **placer le fichier `docker-compose.yml` dans un dossier** sur votre machine.

2. **Naviguer dans le dossier** contenant le fichier `docker-compose.yml`.

3. **Démarrer les services** avec la commande suivante :
   `docker-compose up -d`

Cette commande va télécharger les images nécessaires et démarrer les conteneurs en arrière-plan.

## Accéder à PHPMyAdmin

Ouvrez votre navigateur et allez à [http://localhost:8080](http://localhost:8080). Utilisez les identifiants suivants pour vous connecter :

- **Utilisateur** : `root`
- **Mot de passe** : `exemple` (remplacez-le par le mot de passe que vous avez défini dans le fichier `docker-compose.yml`).

## Structure du fichier

- `db` : Service pour le serveur MySQL.
- `phpmyadmin` : Service pour l'interface web PHPMyAdmin.
- `volumes` : Un volume nommé `dbdata` est créé pour la persistance des données MySQL.

## Bonnes pratiques

- Utilisation de volumes pour la persistance des données.
- Configuration via des variables d'environnement.
- Séparation des services en conteneurs distincts.
- Redémarrage automatique des services.

## Sécurité

- **Changez le mot de passe root** dans le fichier `docker-compose.yml` pour sécuriser votre base de données.
- Ne partagez pas votre fichier `docker-compose.yml` contenant des mots de passe ou des clés.

## Licence

Ce projet est privé.

## Références

Pour plus d'informations, veuillez consulter les ressources suivantes :

- [Docker Volumes Documentation](https://docs.docker.com/storage/volumes/)
- [Configurer Docker et Docker Compose sur AWS EC2 (Amazon Linux 2023 AMI)](https://medium.com/@fredmanre/how-to-configure-docker-docker-compose-in-aws-ec2-amazon-linux-2023-ami-ab4d10b2bcdc)
