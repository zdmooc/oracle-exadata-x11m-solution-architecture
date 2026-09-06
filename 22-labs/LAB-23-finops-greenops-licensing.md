# Lab 23 — Licensing, FinOps et GreenOps

## Objectif

Construire une décision d’architecture qui optimise coût et empreinte sans casser N-1, RPO/RTO ou performance.

## Données synthétiques à définir

- cœurs installés et actifs ;
- CPU moyenne/pic ;
- comportement N-1 ;
- volume actif/historique ;
- IOPS/throughput ;
- redo rate ;
- puissance moyenne/pic ;
- coût licences/support ;
- facteur carbone/PUE ;
- croissance 3/5 ans.

## Travail demandé

1. proposer un nombre de cœurs actifs ;
2. vérifier N-1 ;
3. calculer un TCO 5 ans ;
4. calculer des unit economics ;
5. proposer un modèle d’allocation carbone ;
6. simuler une consolidation ;
7. simuler un power target ;
8. identifier les données candidates XT ;
9. calculer l’effet du double-run de migration ;
10. produire une recommandation finale.

## Livrable

Un mini dossier de décision contenant : hypothèses, calculs, matrice FinOps/GreenOps/Résilience, risques, ADR et critères de validation.