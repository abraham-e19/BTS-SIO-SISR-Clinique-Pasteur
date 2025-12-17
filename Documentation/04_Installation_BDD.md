# 4. Installation du serveur de base de données

## 4.1 Choix de la solution
Le serveur de base de données choisi est MariaDB.
Ce choix est motivé par sa stabilité, sa compatibilité avec MySQL et sa large utilisation dans les infrastructures professionnelles.

## 4.2 Installation de MariaDB
L’installation du serveur de base de données a été réalisée à l’aide du gestionnaire de paquets Debian :

```bash
apt install mariadb-server mariadb-client -y

