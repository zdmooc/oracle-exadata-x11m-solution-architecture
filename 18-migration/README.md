# Module 18 — Migration vers Exadata X11M

## Objectif

Concevoir une migration avec preuves, répétitions et retour arrière.

## Étapes

1. inventory des bases et dépendances ;
2. compatibilité versions/options ;
3. workload baseline ;
4. choix de méthode ;
5. préparation réseau/sécurité ;
6. répétition ;
7. validation performance ;
8. synchronisation finale ;
9. cutover ;
10. validation métier ;
11. rollback si nécessaire ;
12. stabilisation.

## Méthodes à étudier selon contexte

- Data Guard ;
- RMAN duplicate/restore ;
- Data Pump ;
- GoldenGate ;
- autres mécanismes Oracle validés selon versions et contraintes.

## Questions

- downtime maximal ?
- volume à transférer ?
- débit réseau ?
- changement de version ?
- changement d’architecture stockage ?
- chiffrement ?
- dépendances applicatives ?
- rollback possible jusqu’à quel point ?

## Livrables

- migration decision tree ;
- runbook ;
- calendrier ;
- préchecks ;
- critères Go/No-Go ;
- rollback ;
- tests ;
- plan d’hypercare.
