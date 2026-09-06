# Oracle MAA et continuité applicative

## Objectif

Concevoir la disponibilité de bout en bout : base, cluster, site, client applicatif et reprise automatique.

## Chaîne de disponibilité

`Application → pool JDBC/OCI → service RAC → RAC → Data Guard → site standby → backup/recovery`

Une base disponible ne signifie pas qu’une transaction applicative reprend correctement.

## Mécanismes

- RAC : disponibilité locale et maintenance rolling ;
- services RAC : placement, affinité et priorités ;
- FAN / Fast Connection Failover : notification rapide des changements ;
- Application Continuity / Transparent Application Continuity : reprise de certaines sessions/requêtes selon prérequis ;
- Data Guard / Active Data Guard : protection de site et réplication ;
- Broker / FSFO : orchestration et automatisation du failover ;
- RMAN / ZDLRA : restauration après corruption, suppression ou cyberincident ;
- GoldenGate : à évaluer pour certains besoins actifs/actifs logiques, pas comme substitut automatique à Data Guard.

## Mapping exigence → mécanisme

| Risque | Mécanisme principal |
|---|---|
| panne instance | RAC + service |
| panne DB Server | RAC + capacité N-1 |
| maintenance | rolling + services/AC selon cas |
| panne site | Data Guard |
| perte automatique primaire | Broker/FSFO selon gouvernance |
| transaction interrompue | AC/TAC selon compatibilité |
| corruption logique | backup/recovery + stratégie restore |
| cyberattaque | sauvegardes protégées + procédure de reconstruction |

## Livrables

- matrice de panne ;
- services applicatifs ;
- stratégie de reconnexion ;
- choix AC/TAC ;
- stratégie DG ;
- runbook switchover/failover ;
- critères d’automatisation ;
- tests de chaos/panne et critères de succès.