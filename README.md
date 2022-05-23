# Projet-Docker

## Préparation de l'installation
Dans un premier temps nous allons installer les paquets pré-requis:

` sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common `

Ensuite, nous ajoutons la clé GPG officielle de Docker:
`curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -`

Maintenant nous allons ajouter le repos à Debian:
`sudo add-apt-repository \
   "deb [arch=arm64] https://download.docker.com/linux/debian \
   $(lsb_release -cs) \
   stable"`
   
## Installation Docker

Afin de récupérer les paquets, nous commençerons par lancer un apt update:
`sudo apt-get update`

Pour installer Docker, installez les paquets suivants:
`sudo apt-get install docker-ce docker-ce-cli containerd.io`
![image](https://user-images.githubusercontent.com/82390719/169856100-e333de39-e0d5-4025-b011-ad993da746cc.png)

Ensuite, pour vérifier la bonne installation de Docker , nous allons lancer le container "Hello-World":
`sudo docker run hello-world`

![image](https://user-images.githubusercontent.com/82390719/169856364-e0804383-bda0-4ceb-80fe-5589e9565fb2.png)

## Creation Dockerfile (serveur)

Nous avons créer un dossier serveur, puis dans celui-ci nous avons mis trois fichiers:
![image](https://user-images.githubusercontent.com/82390719/169857005-19a29da7-1eb7-4096-ad46-ed219cc386d6.png)

### Server.py

![image](https://user-images.githubusercontent.com/82390719/169857575-d77b2e16-f281-4696-9904-3157a272084b.png)

### Dockerfile
![image](https://user-images.githubusercontent.com/82390719/169857801-a25f13f1-ffc7-4f65-a614-927547aa869e.png)

### index.html

![image](https://user-images.githubusercontent.com/82390719/169857913-a7b18887-02a4-4861-8114-6ee9d34851a7.png)

## Creation Dockerfile (Client)

Dans notre dossier client, nous avons mis deux fichiers:
![image](https://user-images.githubusercontent.com/82390719/169858401-422054f9-0744-42da-b9d3-d47283376b29.png)

### client.py
![image](https://user-images.githubusercontent.com/82390719/169858558-4e7df9fa-3b0c-4863-9c86-f380a81a8a8b.png)

### Dockerfile

![image](https://user-images.githubusercontent.com/82390719/169858723-522c7c38-8d36-4203-89e3-e80cd481297b.png)

## Creation Dockerfile (Firewall)

## Docker-Compose

Nous allons maintenant éditer notre __'docker-compose.yml__ les commandes:


Nous pouvons ensuite exécuter le Docker-Compose avec
`docker-compose build`
`docker-compose up`






