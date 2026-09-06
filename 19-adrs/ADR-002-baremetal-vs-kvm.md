# ADR-002 — Bare Metal vs Oracle Linux KVM

## Statut
Proposé — cas de lab MayaBank.

## Contexte
MayaBank doit isoler plusieurs workloads Oracle tout en maintenant une haute disponibilité et une capacité de maintenance élevée.

## Option A — Bare Metal
Avantages : simplicité relative, chemin de performance direct, moins de couches à exploiter.

Inconvénients : flexibilité de consolidation et d’isolation plus limitée selon le scénario.

## Option B — KVM
Avantages : isolation, consolidation, flexibilité de placement et capacités de maintenance supplémentaires.

Inconvénients : couche d’exploitation supplémentaire, sizing et gouvernance plus complexes.

## Point 2026
Exadata System Software 26.1 introduit la VM Live Migration pour des VMs RDMA compatibles, ce qui renforce l’intérêt de KVM pour certaines maintenances et opérations de rééquilibrage.

## Décision de lab
Retenir KVM **uniquement si** la consolidation, l’isolation ou le cycle de vie justifient la complexité. Pour une plateforme dédiée à un seul workload critique, bare metal reste une option à comparer sérieusement.

## Validation
Benchmark, capacité N-1, procédures de patching, tests de live migration si applicable, analyse de licences et runbooks d’exploitation.
