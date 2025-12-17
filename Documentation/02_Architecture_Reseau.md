# 2. Architecture réseau

## 2.1 Présentation générale
L’architecture mise en place repose sur une infrastructure virtualisée permettant d’héberger les différents serveurs nécessaires au système d’information de la Clinique Pasteur.

Le serveur de base de données est installé sur une machine virtuelle Debian hébergée par l’hyperviseur Proxmox. Cette approche permet d’assurer une meilleure flexibilité, une isolation des services et une gestion simplifiée des ressources.

## 2.2 Environnement de virtualisation
- Hyperviseur : Proxmox VE
- Type de virtualisation : Machine virtuelle
- Serveur hébergé : Debian 12 (mode texte)
- Rôle du serveur : Serveur de base de données

## 2.3 Positionnement du serveur dans le réseau
Le serveur de base de données est positionné sur le réseau interne de la clinique.  
Il n’est pas directement accessible depuis le réseau public afin de limiter les risques de sécurité.

L’accès au serveur s’effectue :
- par SSH pour l’administration
- par le service de base de données pour les serveurs applicatifs autorisés

## 2.4 Cloisonnement et sécurité
Le cloisonnement réseau permet de séparer :
- le réseau administratif
- le réseau médical
- le réseau public

Le serveur de base de données est accessible uniquement depuis les segments réseau autorisés, conformément aux exigences de sécurité et de confidentialité des données.

## 2.5 Schéma d’architecture
Un schéma d’architecture réseau est fourni dans le dossier `/Schemas` afin d’illustrer le positionnement du serveur au sein de l’infrastructure.
