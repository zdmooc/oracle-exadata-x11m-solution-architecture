# Module 03 — Workload Assessment

## Objectif

Construire une photographie fiable de la charge avant tout sizing ou migration.

## Sources

- AWR ;
- ASH ;
- OEM ;
- statistiques OS ;
- statistiques stockage ;
- métriques réseau ;
- historique des incidents ;
- calendrier métier.

## Mesures

- DB Time / DB CPU ;
- Average Active Sessions ;
- CPU moyenne et pics ;
- SGA / PGA ;
- sessions ;
- TPS ;
- redo rate ;
- physical reads/writes ;
- IOPS ;
- throughput ;
- latence ;
- top SQL ;
- temps batch ;
- croissance des données.

## Classifications

Identifier les périodes :

- nominal ;
- pointe ;
- batch ;
- clôture ;
- incident ;
- maintenance.

## Livrable

Produire une baseline avec percentiles et pics, puis relier chaque contrainte observée à une décision de sizing ou d’architecture.

## Anti-pattern

Un snapshot de 15 minutes ou une moyenne mensuelle ne suffit pas pour dimensionner une plateforme critique.
