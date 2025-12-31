# 2. Architecture réseau

## 2.1 Présentation générale

L’architecture réseau mise en place repose sur un environnement virtualisé à l’aide de Proxmox.

Le serveur de base de données est hébergé dans une machine virtuelle Debian fonctionnant en mode texte.

---

## 2.2 Environnement Proxmox

Le serveur Proxmox permet l’hébergement et la gestion des machines virtuelles du projet.

- Hyperviseur : Proxmox
- Type de machine : Machine virtuelle
- Système invité : Debian (mode texte)

---

## 2.3 Architecture logique

L’architecture est composée des éléments suivants :

- Un hôte Proxmox
- Une machine virtuelle Debian dédiée à la base de données
- Un accès distant via SSH depuis le poste administrateur

La machine virtuelle est connectée au réseau local via un pont réseau Proxmox (bridge).

---

## 2.4 Accès au serveur

L’administration du serveur s’effectue :
- par connexion SSH
- depuis le poste de l’administrateur
- via une adresse IP privée

Cette architecture permet une administration sécurisée et centralisée du serveur.
