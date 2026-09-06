# Labs — Architecte Solution Exadata X11M

Ces labs ne cherchent pas uniquement à exécuter des commandes. Chaque lab doit produire une **décision ou un livrable d’architecture**.

## LAB 01 — Cadrer MayaBank

Produire : contexte, acteurs, criticité, contraintes et hypothèses.

## LAB 02 — Construire les NFR

Produire une matrice SLA / RPO / RTO / sécurité / capacité / conformité.

## LAB 03 — Workload Assessment

À partir d’un jeu de données AWR/ASH fictif ou réel anonymisé, identifier : CPU, DB time, I/O, latence, pics, batchs et croissance.

## LAB 04 — Sizing X11M

Construire une proposition compute/memory/storage avec hypothèses, marge et scénario N-1.

## LAB 05 — Choisir HC / EF / XT

Comparer profils de stockage selon données actives, historiques, I/O et coût.

## LAB 06 — ASM vs Exascale

Rédiger un ADR complet.

## LAB 07 — Bare Metal vs KVM

Évaluer isolation, consolidation, exploitation, maintenance, licences et capacité.

## LAB 08 — Architecture réseau

Dessiner les flux client, RDMA, management, backup et Data Guard.

## LAB 09 — IORM / Noisy Neighbor

Définir une politique de priorité pour 5 applications dont 2 critiques.

## LAB 10 — RAC

Concevoir le comportement lors de perte d’un nœud et vérifier la capacité N-1.

## LAB 11 — Data Guard

Choisir SYNC/ASYNC en fonction d’une latence et d’un débit redo donnés.

## LAB 12 — PRA

Écrire un runbook failover/failback avec critères Go/No-Go.

## LAB 13 — RMAN / ZDLRA

Concevoir rétention, restore tests et protection contre corruption/cyberattaque.

## LAB 14 — TDE / Wallet

Définir architecture de clés, responsabilités et procédures de secours.

## LAB 15 — Observabilité

Définir SLI/SLO, métriques, alertes et tableaux de bord.

## LAB 16 — Patching

Construire une stratégie de patching limitant l’indisponibilité et analyser l’apport de VM Live Migration 26.1.

## LAB 17 — Migration

Élaborer une migration vers X11M avec préchecks, répétitions, cutover et rollback.

## LAB 18 — Comparaison On-Prem / Cloud@Customer / OCI

Construire une matrice multicritère et recommander une cible.

## LAB 19 — TCO / Licensing

Construire un modèle de coûts 5 ans avec hypothèses explicites.

## LAB 20 — Green IT

Comparer capacité provisionnée, capacité utile, taux d’utilisation et pistes de consolidation.

## LAB 21 — HLD final

Assembler tous les choix dans une architecture cible cohérente.

## LAB 22 — Soutenance

Présenter la solution en 30 minutes puis répondre à une série de questions contradictoires de comité d’architecture.

## Critère de réussite

Un lab est terminé lorsque le dépôt contient :

1. hypothèses ;
2. décision ;
3. justification ;
4. schéma ou tableau si nécessaire ;
5. risques ;
6. preuve ou méthode de validation.
