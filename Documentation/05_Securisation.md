# 5. Sécurisation du serveur

## 5.1 Objectifs de sécurité
La sécurisation du serveur a pour objectif de protéger les données hébergées et de limiter les accès non autorisés, conformément aux exigences de sécurité et de confidentialité (RGPD).

## 5.2 Pare-feu UFW
Un pare-feu a été mis en place afin de contrôler les flux réseau entrants.

Installation et activation du pare-feu :
```bash
apt install ufw -y
ufw allow ssh
ufw allow 3306/tcp
ufw enable
