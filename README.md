# Oracle Exadata X11M — Solution Architecture

> Parcours d’architecture solution Oracle Exadata X11M orienté banque, paiements, haute disponibilité, PRA, sécurité, capacité, licensing, FinOps, Green IT/GreenOps et exploitation.

## Objectif

Ce dépôt ne remplace pas `oracle-exadata-infra-ha-dr-course-labs-v5`.

- **V5** = apprendre, administrer et diagnostiquer la technologie Exadata.
- **Ce dépôt** = savoir **concevoir, justifier et défendre une architecture Exadata** devant un comité d’architecture, une production, une sécurité, un métier ou une gouvernance coûts/carbone.

Démarche :

`Besoin métier → criticité → NFR/SLA → workload → sizing → scénarios → architecture cible → HA/DR/MAA → sécurité → exploitation → licensing/FinOps → GreenOps → risques → ADR → HLD/LLD → validation`

## Positionnement 2026

Le socle principal est **Oracle Exadata X11M**, **Exascale** et **Exadata System Software 26.1**.

Points à maîtriser :

- X11M : DB Servers, Storage Servers HC/EF/XT, RDMA/RoCE, XRMEM, flash, Smart Scan ;
- X11M-Z et critères de choix ;
- Oracle Linux KVM, consolidation et Secure Fabric ;
- Exascale : pools, vaults, volumes, snapshots/clones et resource management ;
- VM Live Migration ;
- RAC, ASM/Grid Infrastructure ;
- Oracle MAA, services RAC, FAN/FCF, Application Continuity/TAC ;
- Data Guard / Active Data Guard, Broker, FSFO, Far Sync ;
- IORM / DBRM et noisy neighbor ;
- RMAN et ZDLRA ;
- TDE/Wallet, key management, audit, segmentation et cyber-résilience ;
- AHF, Exachk, TFA, ExaWatcher, AWR/ASH ;
- OECA / OEDA / OEDACLI ;
- Capacity-on-Demand et licensing ;
- Advanced Power Management ;
- FinOps / TCO / unit economics ;
- Green IT / GreenOps / allocation carbone ;
- on-premises, Cloud@Customer, OCI et scénarios hybrides/multicloud.

## Cas fil rouge — MayaBank Payment Platform

Cas entièrement synthétique destiné aux labs et aux livrables d’architecture.

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

## Scénarios à comparer

1. Dual Exadata X11M on-premises
2. Dual Exadata Cloud@Customer
3. OCI Exadata + DR
4. Hybride / multicloud

Chaque scénario est évalué sur : SLA/RPO/RTO, performance, capacité, sécurité, exploitation, patching, migration, licensing, TCO, réversibilité, énergie et empreinte.

## Structure

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

## Focus Licensing / FinOps / GreenOps

Le dépôt contient désormais :

- modèle CoD et cartographie des licences ;
- TCO 3/5 ans et unit economics ;
- allocation carbone par capacité, usage réel ou modèle hybride ;
- dashboard GreenOps ;
- Advanced Power Management ;
- modèle de décision **FinOps × GreenOps × Performance × Résilience** ;
- coût et empreinte du double-run de migration ;
- carbon break-even.

## Labs

Le parcours contient désormais **23 labs**. Le LAB 23 relie licensing, FinOps et GreenOps et impose une validation N/N-1 avant toute optimisation.

## Livrables attendus d’un architecte

- cadrage et NFR ;
- workload assessment ;
- sizing CPU/RAM/storage/I/O/network N et N-1 ;
- HLD/LLD ;
- architecture réseau/flux ;
- MAA/RAC/Data Guard/PRA ;
- backup/recovery/cyber-résilience ;
- modèle sécurité et key management ;
- observabilité/evidence pack ;
- patching/lifecycle ;
- licensing/CoD ;
- TCO/FinOps ;
- Green IT/GreenOps ;
- dossier de migration et double-run ;
- ADR ;
- matrice de risques ;
- matrice multicritère ;
- dossier de soutenance.

## Questions qu’un architecte doit savoir défendre

- Pourquoi Exadata et pourquoi X11M ?
- HC, EF ou XT ?
- ASM ou Exascale ?
- Bare Metal ou KVM ?
- Combien de cœurs actifs et pourquoi ?
- Le sizing tient-il après perte d’un DB Server ?
- RAC, Data Guard ou les deux ?
- Comment l’application reprend-elle après failover ?
- Broker/FSFO/Far Sync : quand et pourquoi ?
- Comment protéger contre panne site, erreur humaine et cyberattaque ?
- Quel TCO à 5 ans ?
- Quel coût par transaction ?
- Comment allouer correctement l’empreinte d’une plateforme mutualisée ?
- Quelle optimisation énergétique reste sûre en N-1 ?
- Quand la migration atteint-elle son carbon break-even ?

## Règle du dépôt

Une architecture n’est pas terminée parce qu’un schéma est joli. Elle doit relier :

**exigence → mesure → décision → justification → coût → impact environnemental → risque → contrôle → preuve de fonctionnement.**
