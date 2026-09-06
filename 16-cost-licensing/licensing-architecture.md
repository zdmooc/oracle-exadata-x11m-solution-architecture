# Licensing Oracle Exadata X11M — Architecture Decision Guide

## Objectif

Donner à l’architecte une méthode de décision pour relier architecture, cœurs actifs, options Oracle, PRA, consolidation et coût.

## Principes

- distinguer capacité physique, cœurs actifs, cœurs licenciables et consommation électrique ;
- ne jamais confondre Capacity-on-Demand (CoD) et Advanced Power Management ;
- considérer séparément Oracle Database Enterprise Edition, Exadata System Software et les options/produits complémentaires ;
- documenter l’impact des choix RAC, Active Data Guard, Partitioning, In-Memory, Multitenant, GoldenGate et autres options utilisées ;
- traiter explicitement le licensing du site PRA selon le contrat applicable ;
- en KVM, vérifier les règles applicables aux partitions reconnues et ne jamais extrapoler une règle contractuelle depuis une simple limite vCPU ;
- recalculer le modèle de licences à chaque changement de topologie, de nombre de cœurs actifs, de VM, de PRA ou d’option.

## Capacity-on-Demand

CoD permet de limiter le nombre de cœurs actifs sur les Database Servers. Il s’agit d’un mécanisme de capacité/licensing, pas d’un mécanisme de réduction dynamique de puissance.

Questions d’architecte :

1. Quel nombre de cœurs actifs couvre N et N-1 ?
2. Quelle croissance à 3 et 5 ans ?
3. Quelle marge est réellement nécessaire pour maintenance et failover ?
4. Quel coût de licence est évité par rapport à une activation complète ?
5. Quelle procédure de gouvernance encadre une augmentation de cœurs ?

## KVM et consolidation

Le design doit relier :

`workload → VM cluster → vCPU → cœurs physiques actifs → règles de partitionnement/licensing → N-1 → coût`.

Une consolidation dense n’est valide que si les SLO restent respectés après perte d’un DB Server et pendant les opérations de maintenance.

## Matrice de suivi

| Workload | Environnement | Produit/option | Cœurs/vCPU | DR | Hypothèse licence | Source contractuelle | Risque |
|---|---|---|---:|---|---|---|---|
| MayaPay | PROD | DB EE | TBD | Oui | À valider | Ordering/contrat | Moyen |

## Livrables

- inventaire licences par workload ;
- cartographie physique → VM → DB/PDB ;
- tableau CoD ;
- modèle de licences N / N-1 / PRA ;
- hypothèses contractuelles ;
- risques de non-conformité ;
- scénarios d’optimisation ;
- décision validée par gouvernance licensing.