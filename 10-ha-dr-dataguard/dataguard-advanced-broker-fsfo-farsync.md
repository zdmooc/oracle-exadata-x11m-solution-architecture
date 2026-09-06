# Data Guard avancé — Broker, FSFO, Far Sync

## Objectif

Passer d’un simple schéma Primary/Standby à une vraie architecture de PRA exploitable.

## Décisions structurantes

### Transport

- SYNC : à évaluer pour RPO 0 lorsque latence et débit redo le permettent ;
- ASYNC : adapté lorsque la distance/latence rend SYNC incompatible avec les SLO ;
- Far Sync : à évaluer lorsque l’objectif de protection exige une architecture intermédiaire de transport redo.

### Broker

Utiliser Data Guard Broker pour centraliser configuration, états, switchover/failover et contrôles, sous gouvernance d’exploitation.

### Fast-Start Failover

FSFO peut automatiser le basculement sous conditions. Il faut définir :

- seuils ;
- observer(s) ;
- emplacement tiers ;
- conditions de perte réseau ;
- protection contre décisions ambiguës ;
- procédure de reinstate ;
- conditions de désactivation pendant maintenance.

## Runbook minimal

1. qualifier l’incident ;
2. vérifier rôle et état DG ;
3. mesurer transport/apply lag ;
4. confirmer disponibilité applicative du standby ;
5. Go/No-Go ;
6. switchover ou failover ;
7. déplacer/reconfigurer services ;
8. valider transactions ;
9. rétablir protection ;
10. reinstate/rebuild ancien primaire ;
11. analyse post-incident.

## Tests obligatoires

- switchover planifié ;
- panne primaire ;
- perte réseau inter-site ;
- lag important ;
- observer indisponible ;
- standby non prêt ;
- failback ;
- exercice applicatif complet.

## Règle

Un RPO 0 n’est jamais déclaré uniquement parce que SYNC est configuré. Il doit être démontré avec latence, redo rate, protection mode, architecture réseau et tests.