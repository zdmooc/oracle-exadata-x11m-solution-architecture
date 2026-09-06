# Module 14 — Patching / Lifecycle

## Objectif

Définir une stratégie de maintenance qui maîtrise risque, compatibilité et indisponibilité.

## Périmètre

- Exadata System Software ;
- Oracle Linux ;
- Grid Infrastructure ;
- Oracle Database ;
- Storage Servers ;
- DB Servers ;
- firmware ;
- KVM ;
- outils OEDA/OEDACLI.

## Principes

- matrice de versions supportées ;
- préchecks ;
- sauvegarde/rollback ;
- rolling maintenance lorsque possible ;
- tests hors production ;
- validation fonctionnelle ;
- surveillance renforcée après changement.

## Point 26.1

Exadata VM Live Migration peut réduire l’impact de certaines maintenances KVM lorsque les prérequis sont satisfaits. Cette capacité doit être intégrée à la stratégie de maintenance, mais elle ne remplace ni RAC, ni Data Guard, ni un PRA.

## Livrables

- matrice de compatibilité ;
- stratégie patching ;
- calendrier ;
- procédure pré/post-check ;
- rollback ;
- RACI ;
- critères Go/No-Go.
