# Baseline technologique — septembre 2026

Dernière vérification : 2026-09-06.

## Génération matérielle de référence

Le parcours est centré sur **Oracle Exadata X11M**.

Points structurants :

- DB Servers et Storage Servers X11M ;
- Exadata RDMA Network Fabric sur RoCE ;
- XRMEM ;
- Smart Flash Cache ;
- Smart Scan / SQL Offload ;
- variantes de stockage à étudier selon le besoin, notamment HC / EF / XT ;
- Oracle Linux KVM lorsque la virtualisation est retenue.

## System Software

Deux branches actuelles doivent être distinguées :

- **26ai / 26.1** : nouvelle branche fonctionnelle 2026 ;
- **25ai / 25.2** : branche toujours maintenue.

Au 2026-09-06, les dernières mises à jour Oracle publiées en août 2026 sont :

- **26.1.2.0.0** ;
- **25.2.13.0.0**.

Toujours vérifier la matrice de versions supportées et les MOS/KB Oracle avant toute recommandation de production.

## Capacités majeures 26.1 à connaître

- Exadata VM Live Migration ;
- Smart Flash Cache optimizations ;
- Partner Cache improvements ;
- Snapshot-Aware XRMEM ;
- Storage Server security hardening ;
- Flexible Exascale Storage Pool Management ;
- Exascale Immutable Snapshots ;
- Exascale Resource Profiles for volumes ;
- Exascale Direct Volume Observability ;
- migration de guest image files vers Exascale ;
- coexistence / conversion IPv4 et IPv6 ;
- custom guest gold image ;
- évolutions IORM.

## Références officielles

- What’s New in Exadata System Software 26.1: https://docs.oracle.com/en/engineered-systems/exadata-database-machine/dbmso/whats-new-oracle-exadata-system-software-release-26-1.html
- Exadata System Overview: https://docs.oracle.com/en/engineered-systems/exadata-database-machine/dbmso/
- Exadata Technical Architecture: https://docs.oracle.com/en/engineered-systems/exadata-database-machine/edbid/
- Exascale User’s Guide: https://docs.oracle.com/en/engineered-systems/exadata-database-machine/exscl/
- Oracle Exadata Product Management: https://blogs.oracle.com/exadata/

## Règle de maintenance du dépôt

Avant un entretien, une proposition commerciale ou une architecture réelle, revalider :

1. dernière release Exadata System Software ;
2. versions Oracle Database supportées ;
3. fonctionnalités dépendantes de versions ;
4. modèles matériels disponibles ;
5. contraintes Cloud@Customer / OCI / multicloud ;
6. licensing et support.
