# Oracle Exadata X11M — Solution Architecture

> Parcours d’architecture solution Oracle Exadata X11M orienté banque, paiements, haute disponibilité, PRA, sécurité, capacité, coûts et exploitation.

## Objectif

Ce dépôt ne remplace pas `oracle-exadata-infra-ha-dr-course-labs-v5`.

- **V5** = apprendre et diagnostiquer la technologie Exadata.
- **Ce dépôt** = savoir **concevoir, justifier et défendre une architecture Exadata** devant un comité d’architecture, une production, une sécurité ou un métier.

La démarche suivie est :

`Besoin métier → criticité → NFR/SLA → charge → capacité → scénarios → architecture cible → HA/DR → sécurité → exploitation → coûts → risques → ADR → HLD/LLD → validation`

## Positionnement 2026

Le socle principal est **Oracle Exadata X11M** avec prise en compte de **Exadata System Software 26ai / 26.1** et d’**Exascale**.

Points actuels à maîtriser :

- architecture X11M : DB Servers, Storage Servers, RDMA/RoCE, XRMEM, flash, Smart Scan ;
- Oracle Linux KVM et consolidation ;
- Exascale : pool disks, storage pools, vaults, volumes, snapshots/clones, resource management ;
- Exadata VM Live Migration introduite avec System Software 26.1 ;
- RAC, ASM/Grid Infrastructure, Data Guard / Active Data Guard ;
- IORM / DBRM et maîtrise du noisy neighbor ;
- RMAN et Zero Data Loss Recovery Appliance (ZDLRA) ;
- TDE / Wallet, segmentation, bastion, audit et durcissement ;
- OEDA / OEDACLI, capacité et configuration ;
- on-premises, Cloud@Customer, OCI et scénarios hybrides/multicloud ;
- coût, licences, capacité, FinOps et Green IT.

## Cas fil rouge — MayaBank Payment Platform

Le dépôt s’appuie sur un cas bancaire réaliste servant à produire les livrables d’architecture.

| Exigence | Hypothèse de travail |
|---|---:|
| Domaine | Paiements critiques 24/7 |
| Charge cible | 10 000 TPS |
| Données actives | 30 To |
| Historique | 100 To |
| Croissance | 25 % / an |
| Disponibilité | 99,99 % |
| RPO | 0 cible |
| RTO | < 30 min |
| Sites | 2 datacenters |
| Sécurité | TDE, séparation des rôles, audit |
| Sauvegarde | RMAN + ZDLRA |

Ces valeurs sont volontairement des **hypothèses de lab**. Elles doivent être remplacées par des mesures réelles lors d’un projet.

## Scénarios à comparer

1. **Deux sites Exadata X11M on-premises**
2. **Exadata Cloud@Customer sur deux sites**
3. **OCI Exadata + site de secours**
4. **Architecture hybride / multicloud**

Chaque scénario est évalué sur :

- SLA / RPO / RTO ;
- performance et latence ;
- capacité et croissance ;
- sécurité et conformité ;
- exploitabilité ;
- patching et maintenabilité ;
- complexité de migration ;
- coûts et licences ;
- dépendances réseau ;
- réversibilité ;
- empreinte infrastructure.

## Structure cible

```text
01-business-requirements/
02-nfr-sla-rpo-rto/
03-workload-assessment/
04-capacity-sizing/
05-x11m-architecture/
06-exascale/
07-rac-asm/
08-network-rdma-roce/
09-iorm-consolidation/
10-ha-dr-dataguard/
11-backup-zdlra/
12-security-tde-wallet/
13-observability/
14-patching-lifecycle/
15-cloud-multicloud/
16-cost-licensing/
17-greenit-capacity/
18-migration/
19-adrs/
20-reference-architectures/
21-bank-case-study/
22-labs/
docs/
diagrams/
templates/
```

## Livrables attendus d’un architecte

À la fin du parcours, le dépôt doit permettre de produire :

- dossier de cadrage ;
- matrice NFR ;
- workload assessment ;
- sizing CPU / RAM / stockage / IOPS / bande passante ;
- HLD Exadata X11M ;
- architecture réseau et flux ;
- stratégie RAC / Data Guard / PRA ;
- stratégie sauvegarde / restauration / cyber-résilience ;
- modèle sécurité ;
- stratégie de supervision ;
- stratégie patching/lifecycle ;
- dossier de migration ;
- matrice de risques ;
- matrice de décision multicritère ;
- ADR ;
- dossier de soutenance d’architecture.

## Ce qu’un architecte doit savoir défendre en entretien

- Pourquoi Exadata plutôt qu’une plateforme Oracle générique ?
- Pourquoi X11M ?
- Quand utiliser RAC, Data Guard ou les deux ?
- Comment atteindre un RPO proche de zéro sans promettre l’impossible ?
- ASM classique ou Exascale : quelles conséquences d’architecture ?
- HC, EF, XT : quel profil de données et quel coût ?
- Comment dimensionner sans partir uniquement du volume en To ?
- Comment éviter le noisy neighbor ?
- Quel impact de KVM et de la consolidation ?
- Comment patcher en minimisant l’indisponibilité ?
- Comment protéger la base contre panne site, erreur humaine et cyberattaque ?
- Comment organiser sauvegarde, restauration et ZDLRA ?
- Comment choisir entre on-prem, Cloud@Customer et OCI ?

## Références Oracle officielles

- Oracle Exadata System Overview : https://docs.oracle.com/en/engineered-systems/exadata-database-machine/dbmso/
- Exadata Database Machine Technical Architecture : https://docs.oracle.com/en/engineered-systems/exadata-database-machine/edbid/
- Oracle Exadata Exascale User’s Guide : https://docs.oracle.com/en/engineered-systems/exadata-database-machine/exscl/
- Exadata Product Management Blog : https://blogs.oracle.com/exadata/

## Règle du dépôt

Une architecture n’est pas considérée comme terminée parce qu’un schéma est joli. Elle doit relier :

**exigence → décision → justification → risque → contrôle → preuve de fonctionnement.**
