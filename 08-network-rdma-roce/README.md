# Module 08 — Network / RDMA / RoCE

## Objectif

Concevoir les réseaux Exadata comme des domaines fonctionnels distincts et vérifier les dépendances de performance et de résilience.

## Réseaux à distinguer

- client/application network ;
- Exadata RDMA Network Fabric sur RoCE ;
- management ;
- backup ;
- Data Guard / inter-site ;
- accès supervision ;
- accès bastion/administration.

## Questions d’architecture

- quelles zones de sécurité ?
- quelles routes et ACL ?
- quelle redondance de liens/switches ?
- quelle latence inter-site ?
- quel débit redo maximal ?
- quel débit backup ?
- quelles dépendances DNS/NTP/LDAP/PKI ?
- quelles MTU et exigences réseau sont applicables ?

## Data Guard

Le choix SYNC/ASYNC dépend directement de la latence, de la stabilité réseau et du redo rate. Le réseau doit donc être mesuré avant de promettre un RPO.

## Livrables

- schéma de zones ;
- matrice de flux ;
- besoins bande passante ;
- hypothèses latence ;
- redondance ;
- dépendances externes ;
- tests de perte de lien.
