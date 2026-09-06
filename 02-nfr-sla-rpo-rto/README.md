# Module 02 — NFR / SLA / RPO / RTO

## Objectif

Formaliser les exigences non fonctionnelles qui pilotent les choix Exadata.

## NFR à cadrer

- disponibilité ;
- performance ;
- capacité ;
- latence ;
- sécurité ;
- conformité ;
- sauvegarde ;
- PRA ;
- exploitabilité ;
- maintenabilité ;
- évolutivité ;
- réversibilité ;
- coût.

## RPO

Le RPO exprime la quantité maximale de données que le métier accepte de perdre. Un RPO 0 doit être démontré par le mode de transport, la latence, le débit redo et le comportement en cas de perte de lien.

## RTO

Le RTO couvre toute la reprise du service métier, pas uniquement l’ouverture de la base : détection, décision, bascule, réseau, services Oracle, application, dépendances et validation métier.

## Livrable

Construire une matrice :

| Exigence | Cible | Mesure | Mécanisme | Preuve |
|---|---|---|---|---|
| Disponibilité | | | | |
| RPO | | | | |
| RTO | | | | |
| TPS | | | | |
| Latence | | | | |
| Sécurité | | | | |
