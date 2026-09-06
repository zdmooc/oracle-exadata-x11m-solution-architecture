# AHF / Exachk / TFA / ExaWatcher — Readiness et diagnostic

## Objectif

Intégrer les contrôles de santé et la collecte de preuves au cycle d’architecture et de mise en production.

## Outils

- AHF : framework de santé et diagnostic ;
- Exachk : contrôles de conformité/best practices Exadata ;
- TFA : collecte de diagnostics ;
- ExaWatcher : métriques historiques infrastructure ;
- AWR/ASH : comportement base/workload ;
- CellCLI : cellules et stockage ;
- OEM/observabilité : supervision et tendances.

## Gates

### Avant mise en production
- health check ;
- absence de findings critiques non acceptés ;
- validation réseau, storage, GI/RAC, DG et backup ;
- baseline performance ;
- test N-1 ;
- test restore ;
- test PRA.

### Avant patching
- état cluster ;
- capacité résiduelle ;
- sauvegarde récente ;
- DG sain ;
- findings Exachk ;
- espace et alertes ;
- plan rollback.

### Après changement
- re-run health checks ;
- comparer baseline ;
- vérifier latence/throughput ;
- confirmer DG/backup ;
- conserver evidence pack.

## Evidence pack

Conserver : date, version, configuration, résultats de contrôles, écarts acceptés, responsable, décision Go/No-Go et preuves post-change.