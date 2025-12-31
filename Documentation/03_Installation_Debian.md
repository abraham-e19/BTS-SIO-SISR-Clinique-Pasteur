# 3. Installation du serveur Debian

## 3.1 Création de la machine virtuelle
La machine virtuelle a été créée sur l’hyperviseur Proxmox avec les caractéristiques suivantes :
## Création de la VM Debian (mode texte)

1. Interface web Proxmox
2. **Create VM**
3. Nom : `Debian-Text`
4. ISO : `debian-xx.x.x-amd64.iso`
5. OS Type : Linux
6. BIOS : Default
7. Disque : 20 Go (SCSI)
8. CPU : 2 cores
9. RAM : 2048 Mo
10. Réseau : `vmbr0` (VirtIO)

Ce choix permet d’obtenir un serveur léger, stable et sécurisé.

## 3.2 Installation du système
1. Démarrer la VM
2. Choisir **Install** (⚠️ pas Graphical Install)
3. Langue : Français
4. Pays : France
5. Clavier : Français

## Réseau

- Configuration automatique DHCP
- Nom de machine : `debian-text`
- Domaine : laisser vide

## Comptes utilisateurs

- Mot de passe **root**
- Création utilisateur standard

## Partitionnement

- **Guidé – utiliser un disque entier**
- **Tout dans une seule partition**
- Confirmer l’écriture

## Sélection des logiciels

✔ Serveur SSH

✔ Utilitaires standards du système

❌ **Environnement de bureau Debian (décoché)**

👉 Résultat : **mode texte uniquement**

Seuls les utilitaires standards du système ont été installés.

## 3.3 Configuration post-installation
Une fois le système installé, les actions suivantes ont été réalisées :

### Mise à jour du système
```bash
apt update && apt upgrade -y
