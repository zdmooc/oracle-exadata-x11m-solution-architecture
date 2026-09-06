# GreenOps Exadata — Exploitation responsable

## Objectif

Transformer les objectifs Green IT en pratiques d’exploitation mesurables et répétables.

## Boucle GreenOps

1. mesurer ;
2. comparer aux seuils ;
3. identifier la surcapacité ou les dérives ;
4. simuler l’impact d’une optimisation ;
5. vérifier N-1 / PRA / batch / pics ;
6. décider ;
7. appliquer ;
8. mesurer le gain réel.

## KPI mensuels

| KPI | Finalité |
|---|---|
| CPU utilisée / CPU active | détecter surcapacité compute |
| cœurs actifs / cœurs installés | suivre CoD |
| RAM utilisée / provisionnée | détecter marge excessive |
| TB actifs / TB totaux | identifier données froides |
| IOPS et MB/s utiles | relier stockage à l’usage |
| taux de consolidation | mesurer mutualisation |
| puissance moyenne / pic | suivre efficacité énergétique |
| kWh/mois | suivre Use |
| PUE | intégrer refroidissement |
| kgCO2e/mois | pilotage environnemental |
| €/mois et €/transaction | pilotage FinOps |
| kgCO2e/million transactions | efficacité métier |

## Revues GreenOps

### Hebdomadaire
- anomalies de capacité ;
- croissance inhabituelle ;
- saturation ou sous-utilisation ;
- événements énergie/power cap.

### Mensuelle
- capacité vs forecast ;
- coûts ;
- licences ;
- empreinte ;
- données froides ;
- extensions évitables ;
- actions de consolidation.

### Trimestrielle
- re-simulation N-1 ;
- revue CoD ;
- revue rétention ;
- revue HC/EF/XT ;
- revue FinOps × GreenOps × résilience.

## Guardrail

Ne jamais réduire capacité, puissance ou redondance sans démontrer que les SLO restent acceptables en régime normal, en N-1 et pendant la maintenance.