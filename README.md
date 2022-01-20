# Commandes pour lancer un nouveau projet

## Lancer les containers
docker-compose up-d

## Entrer dans le container 
docker-compose exec apache bash


## Créer un nouveau projet
Starting db_docker_symfony         ... done
Starting www_docker_symfony        ... done
Starting maildev_docker_symfony    ... done
Starting phpmyadmin_docker_symfony ... done

## ançons maintenant la création d’un nouveau projet Symfony (et changeons le propriétaire du fichier par l’utilisateur courant pour pouvoir les modifier facilement par la suite).

docker-compose exec apache composer create-project symfony/website-skeleton project
sudo chown -R $USER ./