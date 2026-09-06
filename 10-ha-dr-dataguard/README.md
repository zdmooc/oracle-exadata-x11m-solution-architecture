# Module 10 — HA / DR / Data Guard

## Objectif

Concevoir une architecture qui traite séparément :

- haute disponibilité locale ;
- reprise après sinistre ;
- protection contre corruption ;
- continuité d’exploitation ;
- restauration après erreur humaine ou cyberattaque.

## Rôles

### RAC

RAC protège principalement contre la perte d’un nœud et permet de distribuer la charge au sein d’un cluster.

### Data Guard

Data Guard fournit une réplication vers une base standby, typiquement sur un autre site ou domaine de panne.

### Active Data Guard

À considérer lorsque la standby doit également servir des lectures, validations ou autres usages compatibles.

### RMAN / ZDLRA

Ils répondent au besoin de sauvegarde/restauration. Ils ne doivent pas être remplacés conceptuellement par Data Guard : une corruption logique peut être répliquée.

## Architecture de référence à étudier

```text
SITE A                                  SITE B
------                                  ------
Applications                            Applications / PRA
   |                                         |
SCAN                                      SCAN
   |                                         |
RAC Primary  ===== Data Guard =====>  RAC Standby
   |                                         |
Exadata X11M                            Exadata X11M
   |
RMAN / ZDLRA
```

## RPO 0 : règle d’architecture

Ne jamais écrire « RPO 0 » sans démonstration.

Vérifier :

- mode de protection ;
- transport SYNC/ASYNC ;
- latence inter-site ;
- débit redo ;
- stabilité réseau ;
- comportement lors de perte de lien ;
- politique de bascule ;
- risque accepté.

## RTO

Le RTO inclut plus que le démarrage de la base :

- détection ;
- décision ;
- bascule ;
- DNS / services / connexions ;
- validation applicative ;
- dépendances externes ;
- reprise des flux métiers.

## Tests obligatoires

- perte d’un nœud RAC ;
- perte d’un Storage Server ;
- perte réseau ;
- perte du site primaire ;
- switchover planifié ;
- failover non planifié ;
- reinstate / rebuild ;
- restauration RMAN ;
- corruption logique ;
- test ZDLRA ;
- retour au nominal.

## Livrables

- matrice pannes / protections ;
- schéma HA/DR ;
- RPO/RTO argumentés ;
- runbook switchover ;
- runbook failover ;
- runbook failback ;
- plan de tests PRA ;
- responsabilités et critères Go/No-Go.
