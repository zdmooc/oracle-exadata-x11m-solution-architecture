# Sécurité Exadata — Architecture d’entreprise

## Objectif

Passer de TDE/Wallet à une défense en profondeur couvrant infrastructure, identité, clés, données, réseau et exploitation.

## Domaines

### Identité et privilèges
- least privilege ;
- séparation DBA / OS / sécurité / backup ;
- comptes nominatifs et bastion ;
- MFA lorsque l’écosystème le permet ;
- comptes break-glass gouvernés.

### Chiffrement et clés
- TDE ;
- wallet/keystore ;
- external key management/HSM lorsque requis ;
- sauvegarde et restauration des clés ;
- séparation des responsabilités ;
- rotation et procédure de perte de clé.

### Base
- Database Vault selon exigences ;
- audit ;
- masking/redaction pour usages concernés ;
- sécurité PDB/CDB ;
- revue des options exposées.

### Réseau
- segmentation management/client/backup/DG ;
- RDMA privé ;
- TLS/TCPS lorsque requis ;
- ACL/firewall ;
- flux explicitement documentés.

### Infrastructure
- Secure Boot/SELinux selon baseline ;
- SSH durci ;
- ILOM isolé ;
- patch CVE ;
- Secure RDMA Fabric Isolation en environnement virtualisé selon design supporté.

### Cyber-résilience
- backups protégés ;
- copies/recovery path séparés ;
- restore régulièrement testé ;
- reconstruction documentée ;
- scénario compromission DBA ;
- scénario corruption logique répliquée par Data Guard.

## Livrables

- threat model ;
- matrice de flux ;
- modèle IAM/RBAC ;
- architecture de clés ;
- baseline de durcissement ;
- audit/logging ;
- runbook cyber-recovery ;
- exceptions et risques acceptés.