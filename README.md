# Stack-Plex
Installation de la stack Plex (Plex, Jackett, Radarr, Sonarr, VPN, Transmission, Overserr) via Docker.
Ce projet contient mes docker-compose pour l'installation de la stack Plex ainsi que des remarques, des conseils lors de non fonctionnement.

# Informations avant d'utiliser les fichiers.

  - Vérifier que les dossiers soient les mêmes que moi ou modifier les répertoires dans les docker-compose
  - Pour le dashboard grafana, il faut cliquer sur le type de requête et re-selectionner prometheus. Normalement les données devraient s'afficher.
  - Il se peut qu'il y ait des erreurs avec le docker-compose du VPN, pour l'accès à Transmission. Pour cela il faut voir le Nginx qui sert de reverse proxy pour l'interface web de Transmisson. Transmission se trouve dans le réseau du VPN afin qu'on puisse télécharger et seed sans problème.
