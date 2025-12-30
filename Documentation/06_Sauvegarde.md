# 6. Sauvegardes automatiques

## 6.1 Objectifs
La mise en place de sauvegardes automatiques permet d’assurer la disponibilité et l’intégrité des données en cas d’incident (panne, erreur humaine, attaque).

## 6.2 Stratégie de sauvegarde
La stratégie retenue repose sur les éléments suivants :
- une sauvegarde automatique quotidienne de la base de données applicative
- un stockage local sécurisé sur le serveur de base de données
- une conservation de plusieurs sauvegardes grâce au nommage par date
Cette approche permet de restaurer rapidement les données en cas de besoin.

## 6.3 Script de sauvegarde
Un script de sauvegarde a été mis en place afin d'automatiser l'export de la base de données MariaDB.

Le script utilise la commande mysqldump et génère un fichier de sauvegarde horodaté au format SQL dans un répertoire dédié.

#6.4 Emplacement des sauvegardes
Les sauvegardes sont stockées dans le répertoire suivant sur le serveur :
/home/admin-bdd/backups

Les fichiers générés portent un nom incluant la date et l'heure, ce qui permet d'identifier facilement chaque sauvegarde.

#6.5 Automatisation par cron
L'exécution du script de sauvegarde est automatisée à l'aide du service cron.

Une planification temporaire toutes les minutes a été mise enplace afin de tester le bon fonctionnement du script. 
Après validation, la planification a été définie pour une exéction quotidienne.


#Note 
Les identifiants de connexion à la base de données ne sont pas stockés en clair dans la documentation publique.
L’accès est restreint à l’utilisateur dédié au serveur.
