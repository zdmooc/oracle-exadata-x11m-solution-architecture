# Module 16 — Licensing / FinOps / TCO

## Objectif

Relier les décisions d’architecture Exadata au modèle économique, aux licences et au coût total sur 3 à 5 ans.

## Parcours

1. [`licensing-architecture.md`](licensing-architecture.md) — produits, options, CoD, KVM, PRA et gouvernance licensing.
2. [`finops-tco-unit-economics.md`](finops-tco-unit-economics.md) — TCO, unit economics, scénarios et sensibilités.
3. [`../17-greenit-capacity/finops-greenops-resilience.md`](../17-greenit-capacity/finops-greenops-resilience.md) — arbitrer coût, énergie, performance et résilience.

## Questions d’architecte

- Quelle part du coût vient réellement des licences ?
- Le nombre de cœurs actifs couvre-t-il N-1 ?
- Quelle réserve coûte cher mais est nécessaire ?
- Quelle capacité est inutilisée ?
- Quel est le coût du PRA ?
- Quel est le coût du double-run de migration ?
- Une consolidation réduit-elle réellement le TCO sans créer de noisy neighbor ?
- Quel scénario on-prem / ExaCC / OCI est le plus efficient à 5 ans ?

## Livrables

- inventaire licences ;
- matrice produits/options ;
- modèle CoD ;
- TCO 5 ans ;
- unit economics ;
- scénarios de sensibilité ;
- recommandations d’optimisation ;
- hypothèses contractuelles à faire valider par la gouvernance Oracle.

## Règle

Ce dépôt explique les mécanismes techniques et les décisions d’architecture. Il ne remplace jamais les contrats, Ordering Documents, politiques internes ou validations de licensing applicables.