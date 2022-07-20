# Stack-Plex

Installation de la stack Plex (Plex, Jackett, Radarr, Sonarr, VPN, Transmission, Overserr) via Docker.
Ce projet contient mes docker-compose pour l'installation de la stack Plex, des remarques ainsi que des conseils lors de non fonctionnement.

# Explication des différentes briques

Précédemment j'ai énoncé les différents services que je vais utiliser pour déployer et automatiser le téléchargement de mes films et séries. Dans cette partie, je vais m'éfforcer à expliquer avec mes mots, les fonctionnalités proposées par les différents conteneurs.

  - Plex : Il s'agit de la pièce maitresse de notre installation. Plex est un media center, pour faire simple il permet de lire des fichiers vidéos sous plusieurs format (.mkv, mp4,...) présent sur la machine. Son interface web ergonomique permet une compréhension rapide de l'environnement dans lequel on évolue. Les films et séries ajoutés sur l'interface se voient dotés d'un synopsie, du casting ainsi que des avis critiques de site référent dans la matière. Une image en vaut mille mots, voici la visualisation que nous pouvons avoir lorsqu'on selectionne un film.
![image](https://user-images.githubusercontent.com/96300960/180069454-41c04b11-9307-4b59-b026-d74c54b6fa4b.png)
  - Jackett : Il va nous permet de traduire les requêtes de nos conteneur Radarr et Sonarr, en requête utilisable pour aller chercher dans les flux RSS. Dans mon cas Jackett va chercher les demandes de mes conteneurs dans les flux RSS de site de Torrent (à l'image de Ygg ou de torrent public)
  - Radarr : 


# Informations avant d'utiliser les fichiers

  - Vérifier que les dossiers soient les mêmes que moi ou modifier les répertoires dans les docker-compose
  - Pour le dashboard grafana, il faut cliquer sur le type de requête et re-selectionner prometheus. Normalement les données devraient s'afficher.
  - Il se peut qu'il y ait des erreurs avec le docker-compose du VPN, pour l'accès à Transmission. Pour cela il faut voir le Nginx qui sert de reverse proxy pour l'interface web de Transmisson. Transmission se trouve dans le réseau du VPN afin qu'on puisse télécharger et seed sans problème.
