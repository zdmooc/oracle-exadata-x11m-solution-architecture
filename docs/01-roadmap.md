# Roadmap — Architecte Solution Exadata X11M

## Niveau 1 — Cadrage

Savoir transformer une demande métier en contraintes d’architecture :

- criticité métier ;
- volumétrie ;
- charge OLTP / analytics / batch ;
- fenêtres de traitement ;
- SLA ;
- RPO / RTO ;
- exigences réglementaires et sécurité ;
- croissance ;
- contraintes de datacenter et réseau ;
- budget et licences.

**Livrable :** dossier de cadrage + matrice NFR.

## Niveau 2 — Comprendre X11M

Maîtriser :

- DB Servers ;
- Storage Servers ;
- RoCE / RDMA ;
- XRMEM ;
- Flash Cache ;
- Smart Scan ;
- IORM ;
- Oracle Linux KVM ;
- OEDA/OEDACLI.

**Livrable :** HLD physique/logique annoté.

## Niveau 3 — Stockage ASM et Exascale

Comparer :

- ASM / Grid Infrastructure ;
- Exascale storage pools / vaults / volumes ;
- redondance ;
- performance ;
- isolation ;
- snapshots / clones ;
- implications d’exploitation.

**Livrable :** ADR ASM vs Exascale selon scénario.

## Niveau 4 — Sizing

Passer de la charge au dimensionnement :

- CPU ;
- RAM ;
- DB cache ;
- IOPS ;
- débit ;
- latence ;
- capacité utile ;
- croissance ;
- marge ;
- sauvegarde ;
- PRA.

**Livrable :** workbook de sizing + hypothèses + marges.

## Niveau 5 — HA / DR

Concevoir :

- RAC local ;
- Data Guard inter-site ;
- Active Data Guard si justifié ;
- Fast-Start Failover si adapté ;
- protection contre panne nœud, stockage, cluster et site ;
- stratégie de bascule et retour arrière.

**Livrable :** architecture HA/DR + runbook PRA + matrice de tests.

## Niveau 6 — Protection des données

- RMAN ;
- FRA/RECO ;
- ZDLRA ;
- restauration ;
- validation de sauvegarde ;
- rétention ;
- cyber-résilience ;
- séparation des responsabilités.

**Livrable :** politique backup/recovery et preuves de restore.

## Niveau 7 — Sécurité

- TDE ;
- Wallet/keystore ;
- RBAC ;
- réseau d’administration ;
- bastion ;
- segmentation ;
- audit ;
- durcissement ;
- SELinux ;
- gestion des secrets et certificats.

**Livrable :** security architecture + flux + contrôles.

## Niveau 8 — Exploitation

- observabilité ;
- OEM / métriques ;
- alerting ;
- capacity management ;
- patching ;
- maintenance ;
- VM Live Migration avec System Software 26.1 lorsque les prérequis sont satisfaits ;
- gestion des incidents et problèmes.

**Livrable :** modèle opérationnel + calendrier de maintenance.

## Niveau 9 — Choix de plateforme

Comparer :

- X11M on-premises ;
- Exadata Cloud@Customer ;
- OCI Exadata ;
- hybride / multicloud.

**Livrable :** matrice multicritère + recommandation.

## Niveau 10 — Soutenance d’architecture

Être capable de présenter en 30 minutes :

1. contexte métier ;
2. risques ;
3. NFR ;
4. scénarios ;
5. architecture cible ;
6. sizing ;
7. HA/DR ;
8. sécurité ;
9. exploitation ;
10. coûts ;
11. risques résiduels ;
12. décision.

**Objectif final :** défendre l’architecture et ses compromis, pas réciter des fonctionnalités Oracle.
