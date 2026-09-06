# Green IT Exadata — Méthode d’architecture

## Objectif

Évaluer l’empreinte environnementale d’une plateforme Exadata sans réduire l’analyse à un ratio unique par Go.

## Décomposer l’empreinte

`empreinte totale = fabrication + utilisation + refroidissement + réseau + stockage/backup + part mutualisée`

La méthode doit distinguer :

- **Build** : fabrication et amortissement du matériel ;
- **Use** : énergie réellement consommée ;
- PUE / refroidissement ;
- durée de vie ;
- taux d’utilisation ;
- redondance ;
- réplication ;
- sauvegarde ;
- données actives et froides ;
- capacité évitée grâce à la consolidation.

## Trois modèles d’allocation à comparer

### A — Allocation par capacité

Simple, reproductible, utile pour un premier ordre de grandeur.

Limite : deux workloads de même taille peuvent avoir des profils CPU/I/O très différents.

### B — Allocation par usage réel

Pondérer selon CPU, I/O, stockage, redo, backup, snapshots et activité.

Plus fidèle, mais nécessite des mesures fiables.

### C — Allocation hybride

Séparer une part fixe mutualisée et une part variable consommée :

`allocation = socle partagé + CPU + I/O + stockage actif + stockage froid + réplication + backup`

C’est le modèle privilégié pour les études d’architecture lorsque les données sont disponibles.

## Indicateurs

- kgCO2e/an par workload ;
- kgCO2e/TB actif ;
- kgCO2e/million de transactions ;
- capacité installée vs utilisée ;
- taux de consolidation ;
- CPU active vs installée ;
- données froides / totales ;
- capacité évitée par consolidation ;
- empreinte du PRA ;
- empreinte temporaire du double-run.

## Règle d’architecture

Une optimisation carbone n’est valide que si les SLO, le N-1, le RPO/RTO, la sécurité et la maintenabilité restent respectés.