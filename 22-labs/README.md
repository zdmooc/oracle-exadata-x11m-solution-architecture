# Labs — Architecte Solution Exadata X11M

Ces labs ne cherchent pas uniquement à exécuter des commandes. Chaque lab doit produire une **décision ou un livrable d’architecture**.

## LAB 01 — Cadrer MayaBank
Produire : contexte, acteurs, criticité, contraintes et hypothèses.

## LAB 02 — Construire les NFR
Produire une matrice SLA / RPO / RTO / sécurité / capacité / conformité.

## LAB 03 — Workload Assessment
À partir d’un jeu AWR/ASH fictif ou anonymisé, identifier CPU, DB time, I/O, latence, pics, batchs et croissance.

## LAB 04 — Sizing X11M
Construire compute/memory/storage avec hypothèses, marge et N-1.

## LAB 05 — Choisir HC / EF / XT
Comparer profils de stockage selon activité, historique, I/O et coût.

## LAB 06 — ASM vs Exascale
Rédiger un ADR complet.

## LAB 07 — Bare Metal vs KVM
Évaluer isolation, consolidation, exploitation, maintenance, licences et capacité.

## LAB 08 — Architecture réseau
Dessiner flux client, RDMA, management, backup et Data Guard.

## LAB 09 — IORM / Noisy Neighbor
Définir une politique de priorité pour plusieurs applications.

## LAB 10 — RAC
Concevoir la perte d’un nœud et vérifier N-1.

## LAB 11 — Data Guard
Choisir SYNC/ASYNC selon latence et redo rate.

## LAB 12 — PRA
Écrire le runbook failover/failback avec critères Go/No-Go.

## LAB 13 — RMAN / ZDLRA
Concevoir rétention, restore tests et cyber-recovery.

## LAB 14 — TDE / Wallet
Définir architecture de clés, responsabilités et secours.

## LAB 15 — Observabilité
Définir SLI/SLO, métriques, alertes, AHF/Exachk et evidence pack.

## LAB 16 — Patching
Construire une stratégie de patching et analyser VM Live Migration.

## LAB 17 — Migration
Préchecks, répétitions, cutover, rollback et double-run.

## LAB 18 — On-Prem / Cloud@Customer / OCI
Construire une matrice multicritère et recommander une cible.

## LAB 19 — TCO / Licensing
Construire un TCO 5 ans et un modèle CoD/licensing.

## LAB 20 — Green IT
Comparer capacité provisionnée/utilisée, allocation carbone et consolidation.

## LAB 21 — HLD final
Assembler tous les choix dans une cible cohérente.

## LAB 22 — Soutenance
Présenter la solution en 30 minutes face à un comité contradictoire.

## LAB 23 — Licensing / FinOps / GreenOps
Relier cœurs actifs, licences, TCO, énergie, empreinte, N-1 et résilience. Voir [`LAB-23-finops-greenops-licensing.md`](LAB-23-finops-greenops-licensing.md).

## Critère de réussite

Un lab est terminé lorsque le dépôt contient :

1. hypothèses ;
2. mesures ou données d’entrée ;
3. décision ;
4. justification ;
5. schéma/tableau si nécessaire ;
6. risques ;
7. coût/impact lorsque pertinent ;
8. preuve ou méthode de validation.
