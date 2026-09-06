# MayaBank — FinOps / GreenOps Dashboard (synthetic)

> Jeu de données pédagogique. Aucune donnée d’entreprise réelle.

## Objectif

Piloter simultanément capacité, coût, empreinte et résilience sur la plateforme de paiements MayaBank.

## KPI mensuels

| Domaine | KPI | Valeur | Seuil / cible | Décision |
|---|---|---:|---:|---|
| Compute | CPU moyenne | TBD | < 60 % | |
| Compute | CPU pic | TBD | < 75 % | |
| Résilience | CPU après N-1 | TBD | < 80 % | |
| Licensing | Cœurs actifs / installés | TBD | optimisé | |
| Mémoire | RAM utilisée / provisionnée | TBD | < 75 % | |
| Storage | TB actifs / totaux | TBD | suivi | |
| Storage | données froides | TBD | tiering | |
| I/O | IOPS pic | TBD | marge 30 % | |
| DG | redo rate | TBD | réseau dimensionné | |
| FinOps | €/million transactions | TBD | tendance ↓ | |
| GreenOps | kWh/mois | TBD | tendance ↓ | |
| GreenOps | kgCO2e/million transactions | TBD | tendance ↓ | |

## Revues de décision

### Exemple A — réduire des cœurs actifs

Valider :
- CPU pic ;
- N-1 ;
- batch ;
- RAC failover ;
- croissance 12/36 mois ;
- économie licence ;
- effet énergie ;
- rollback.

### Exemple B — déplacer l’historique vers XT

Valider :
- fréquence d’accès ;
- latence acceptable ;
- compression ;
- backup ;
- licensing des fonctions utilisées ;
- économie capacité ;
- effet carbone.

### Exemple C — réduire power target

Valider en charge normale, pic, N-1 et maintenance avant généralisation.

## Principe

Le comité d’architecture ne valide pas une optimisation parce qu’elle est moins chère ou moins énergivore. Il valide une configuration qui reste conforme aux SLO, au RPO/RTO et aux exigences de sécurité.