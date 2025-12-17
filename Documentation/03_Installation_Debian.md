# 3. Installation du serveur Debian

## 3.1 Création de la machine virtuelle
La machine virtuelle a été créée sur l’hyperviseur Proxmox avec les caractéristiques suivantes :
- Système d’exploitation : Debian 12 (Bookworm)
- Mode d’installation : Texte (sans interface graphique)
- Processeur : 2 vCPU
- Mémoire vive : 2 Go
- Stockage : 20 Go
- Carte réseau : bridge vmbr0

Ce choix permet d’obtenir un serveur léger, stable et sécurisé.

## 3.2 Installation du système
L’installation a été réalisée à partir de l’image ISO Debian netinst.
Lors de l’installation, les choix suivants ont été effectués :
- langue et clavier configurés
- nom de machine défini
- création du compte administrateur
- partitionnement automatique du disque
- installation minimale sans environnement graphique

Seuls les utilitaires standards du système ont été installés.

## 3.3 Configuration post-installation
Une fois le système installé, les actions suivantes ont été réalisées :

### Mise à jour du système
```bash
apt update && apt upgrade -y
