# OECA / OEDA / OEDACLI — Conception et lifecycle

## Objectif

Faire de la configuration Exadata un livrable d’architecture traçable et reproductible.

## OECA

À utiliser pour comparer des configurations et valider capacité, puissance, réseau et contraintes de rack selon les possibilités Oracle disponibles.

## OEDA

Le worksheet OEDA doit matérialiser les choix d’architecture :

- hostname / DNS ;
- IP management ;
- client network ;
- SCAN / VIP ;
- VLAN ;
- NTP ;
- réseau backup / additional ;
- GI/RAC ;
- ASM DATA/RECO ou choix Exascale ;
- KVM/VM clusters si applicable ;
- rôles et responsabilités.

## OEDACLI

À intégrer au lifecycle pour les modifications supportées : évolution de configuration, réseaux additionnels et autres changements documentés.

## Gate de readiness

Avant déploiement :

1. NFR validés ;
2. sizing N/N-1 ;
3. configuration matérielle ;
4. adressage ;
5. DNS/NTP ;
6. VLAN/MTU/routage/ACL ;
7. stockage ;
8. backup/DG ;
9. sécurité ;
10. puissance/refroidissement ;
11. versions supportées ;
12. rollback et responsabilités.

## Livrables

- configuration OECA retenue ;
- worksheet OEDA ;
- IP plan ;
- matrice réseaux/flux ;
- checklist readiness ;
- journal des changements OEDACLI ;
- ADR pour toute dérogation.