# Module 07 — RAC / Grid Infrastructure / ASM

## Objectif

Savoir positionner RAC et ASM dans une architecture Exadata sans les traiter comme des automatismes.

## RAC

À évaluer pour :

- disponibilité locale ;
- répartition de charge ;
- maintenance ;
- montée en charge ;
- services Oracle et affinité applicative.

## Questions d’architecture

- combien d’instances ?
- quels services Oracle ?
- quel comportement en N-1 ?
- quelle capacité restante après perte d’un nœud ?
- quels risques liés aux connexions applicatives ?
- comment gérer les batchs et workloads sensibles ?

## ASM / Grid Infrastructure

Maîtriser :

- disk groups ;
- DATA / RECO ;
- normal/high redundancy selon contexte ;
- rebalance ;
- capacity headroom ;
- interactions avec Exadata Storage Servers.

## Décisions attendues

- RAC ou single instance ;
- nombre d’instances ;
- politique de services ;
- ASM classique ou Exascale ;
- niveau de redondance ;
- stratégie de maintenance.

## Livrables

- topologie RAC ;
- matrice services/instances ;
- stratégie ASM ;
- scénario N-1 ;
- ADR si plusieurs options sont possibles.
