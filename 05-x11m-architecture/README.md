# Module 05 — Architecture Exadata X11M

## Objectif architecte

Comprendre les briques X11M suffisamment pour prendre des décisions de solution : topologie, consolidation, performance, résilience, exploitation et capacité.

## Briques à maîtriser

- Database Servers ;
- Exadata Storage Servers ;
- réseau RDMA sur RoCE ;
- XRMEM ;
- Smart Flash Cache ;
- Smart Scan / SQL Offload ;
- IORM ;
- Oracle Linux ;
- Oracle Linux KVM selon scénario ;
- Grid Infrastructure / ASM ou Exascale ;
- OEDA / OEDACLI.

## Vue logique

```text
Applications
    |
SCAN / Services Oracle
    |
Oracle RAC / Database
    |
Grid Infrastructure
    |
RDMA / RoCE Fabric
    |
Exadata Storage Servers
    |-- XRMEM
    |-- Flash Cache
    |-- Smart Scan
    |-- Persistent Storage
```

## Questions de conception

### Compute

- combien de bases et de clusters ?
- bare metal ou KVM ?
- besoins CPU/RAM par workload ?
- marge de croissance et failover ?
- densité de consolidation acceptable ?

### Storage

- profil OLTP, analytics ou mixte ?
- capacité active vs historique ?
- IOPS, débit et latence ?
- HC / EF / XT selon besoin ?
- ASM classique ou Exascale ?

### Réseau

- fabric RDMA ;
- client network ;
- backup network ;
- management ;
- interconnexion Data Guard ;
- segmentation et zones de sécurité.

### Résilience

- perte d’un DB Server ;
- perte d’un Storage Server ;
- perte d’un switch/fabric ;
- perte d’un rack ;
- perte d’un site.

## Point 2026

Exadata System Software 26.1 introduit notamment la VM Live Migration pour les environnements KVM compatibles, en conservant les connexions RDMA pendant la migration. L’architecte doit considérer cette capacité dans la stratégie de maintenance, sans la confondre avec un mécanisme de PRA inter-site.

## Livrables

- schéma physique X11M ;
- schéma logique RAC / storage ;
- matrice des réseaux ;
- matrice des pannes ;
- ADR bare metal vs KVM ;
- ADR ASM vs Exascale ;
- hypothèses de sizing.
