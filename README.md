# Documentation du Projet
## Introduction
Ce projet est une application Spring Boot configurée pour fonctionner avec Docker. Ce document vous guide à travers les étapes nécessaires pour configurer votre environnement et exécuter l'application.

## Prérequis
Avant de commencer, assurez-vous d'avoir installé les éléments suivants :

Docker : Téléchargez et installez Docker depuis [le site officiel de Docker.](https://www.docker.com/products/docker-desktop/)
Docker Compose : Docker Compose est généralement inclus avec Docker Desktop, mais vérifiez que vous pouvez l'utiliser en exécutant ```docker-compose --version``` dans votre terminal.
## Cloner le Référentiel
Ouvrez votre terminal.
Clonez le référentiel du projet :
```
git clone https://github.com/dalillali/livraison_repas.git
cd https://github.com/dalillali/livraison_repas.git
```
## Configuration de l'Application
Assurez-vous que le fichier `application.properties` est correctement configuré pour la connexion à la base de données MySQL :
```
spring.application.name=repas
spring.datasource.url=jdbc:mysql://mysql-db:3306/food_delivery
spring.datasource.username=root
spring.datasource.password=root
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
server.port=8080
```
## Construction et Exécution du Projet
Construire l'image Docker : Exécutez la commande suivante pour construire les images Docker : 

```docker-compose build```
Lancer les services : Après la construction, lancez les services avec :
```docker-compose up```
Cette commande démarre à la fois l'application Spring Boot et la base de données MySQL. Vous devriez voir des logs des deux services.
## Accéder à l'Application
Une fois les services démarrés, vous pouvez accéder à l'application à l'adresse suivante :
```http://localhost:8080```
## Commandes Utiles
Voici quelques commandes utiles pour gérer votre projet Docker :
### Arrêter les services :
  ```docker-compose down```
### Redémarrer les services :
  ```docker-compose restart```
### Afficher les logs des services :
  ```docker-compose logs```


