# Module 11 — Backup / RMAN / ZDLRA

## Objectif

Concevoir une stratégie de protection des données indépendante de la seule réplication Data Guard.

## Périmètre

- RMAN ;
- FRA / RECO ;
- rétention ;
- sauvegardes complètes/incrémentales ;
- validation ;
- restauration ;
- recovery ;
- Zero Data Loss Recovery Appliance ;
- protection cyber ;
- copie hors domaine de panne.

## Principes

Data Guard protège contre certaines pannes, mais une corruption ou une erreur logique peut être propagée. La sauvegarde et la restauration restent des fonctions distinctes.

## Questions d’architecture

- quels RPO/RTO de restauration ?
- quelle rétention ?
- quel volume quotidien de redo ?
- quelle fenêtre de backup ?
- quel débit réseau ?
- où sont placées les copies ?
- comment protéger les sauvegardes contre suppression ou compromission ?
- à quelle fréquence teste-t-on réellement un restore ?

## ZDLRA

À évaluer pour centraliser et renforcer la protection Oracle Database, réduire la perte de données et industrialiser la restauration. Le dimensionnement doit prendre en compte redo, changements, rétention, nombre de bases et objectifs de recovery.

## Livrables

- politique de backup ;
- architecture RMAN/ZDLRA ;
- matrice de rétention ;
- flux ;
- tests de restore ;
- RACI ;
- procédure de recovery cyber.
