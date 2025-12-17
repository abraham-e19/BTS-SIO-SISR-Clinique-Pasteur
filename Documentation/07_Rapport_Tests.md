# 7. Rapport de tests

## 7.1 Objectifs des tests
Les tests réalisés ont pour objectif de valider le bon fonctionnement du serveur de base de données ainsi que des mesures de sécurité mises en place.

## 7.2 Tests réalisés

### Test 1 : Accès au serveur
- Connexion SSH au serveur Debian
- Résultat : OK

### Test 2 : État du service MariaDB
- Vérification de l’état du service
```bash
systemctl status mariadb
