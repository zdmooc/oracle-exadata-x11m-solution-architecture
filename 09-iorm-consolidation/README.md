# Module 09 — IORM / Consolidation / Noisy Neighbor

## Objectif

Garantir qu’une plateforme consolidée ne sacrifie pas les workloads critiques aux charges moins prioritaires.

## Concepts

- IORM ;
- DBRM ;
- plans de ressources ;
- priorités ;
- limites ;
- consolidation de plusieurs bases ;
- isolation des workloads ;
- Exascale resource management selon scénario.

## Cas MayaBank

Supposer cinq applications :

1. paiement temps réel — critique ;
2. autorisation — critique ;
3. reporting — important ;
4. batch réglementaire — important ;
5. analytics — non critique en journée.

L’architecte doit définir comment protéger les deux premières lorsque les trois autres consomment fortement les ressources I/O.

## Questions

- quels workloads partagent le même Exadata ?
- quelles priorités métier ?
- quels seuils et garanties ?
- comment mesurer la contention ?
- comment valider le plan en charge ?
- quelle gouvernance pour modifier les priorités ?

## Livrables

- classification des workloads ;
- politique IORM/DBRM ;
- scénario de saturation ;
- critères de validation ;
- procédure de changement ;
- risques de consolidation.
