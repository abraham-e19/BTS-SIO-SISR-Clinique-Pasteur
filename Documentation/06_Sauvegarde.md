# 6. Sauvegardes automatiques

## 6.1 Objectifs
La mise en place de sauvegardes automatiques permet d’assurer la disponibilité et l’intégrité des données en cas d’incident (panne, erreur humaine, attaque).

## 6.2 Stratégie de sauvegarde
La stratégie retenue repose sur :
- une sauvegarde quotidienne de la base de données
- un stockage local sécurisé
- une conservation des sauvegardes sur plusieurs jours

## 6.3 Script de sauvegarde
Un script de sauvegarde a été créé afin d’automatiser l’export de la base de données :

```bash
#!/bin/bash
DATE=$(date +%F)
mysqldump -u root -p clinique > /root/sauvegardes/clinique_$DATE.sql
