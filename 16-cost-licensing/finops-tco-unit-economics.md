# FinOps Exadata — TCO et Unit Economics

## Objectif

Rendre chaque choix d’architecture mesurable en coût et comparable sur 3 à 5 ans.

## Périmètre TCO

- hardware / service Exadata ;
- Oracle Database et options ;
- Exadata System Software ;
- support ;
- datacenter, énergie et refroidissement ;
- réseau et interconnexion ;
- sauvegarde / ZDLRA ;
- PRA ;
- exploitation, astreinte et compétences ;
- migration et double-run ;
- capacité inutilisée ;
- croissance et extensions ;
- coûts cloud/ExaCC/OCI selon scénario.

## Unit economics à suivre

- €/PDB/an ;
- €/TB actif/an ;
- €/TB historique/an ;
- €/cœur actif/an ;
- €/million de transactions ;
- coût de la réserve N-1 ;
- coût du PRA ;
- coût de la surcapacité ;
- coût d’un DB Server ou Storage Server supplémentaire ;
- coût du double-run de migration.

## FinOps lifecycle

1. **Inform** — inventaire, allocation, mesures et hypothèses.
2. **Optimize** — right-sizing, CoD, consolidation, tiering HC/EF/XT, rétention et licences.
3. **Operate** — budget, seuils, alertes, revues mensuelles, gouvernance et décision d’extension.

## Scénarios MayaBank

Comparer au minimum :

- dual X11M on-premises ;
- dual Exadata Cloud@Customer ;
- OCI Exadata + DR ;
- hybride/multicloud.

## Sensibilité

Tester l’impact de :

- +25 % de croissance/an ;
- +30 % de redo ;
- perte d’un DB Server ;
- extension storage ;
- augmentation CoD ;
- option Oracle supplémentaire ;
- hausse des coûts énergie/cloud ;
- durée de double-run.

## Livrable

Un TCO 5 ans avec hypothèses, fourchettes, sensibilités, coûts unitaires, risques et recommandation.