# FinOps × GreenOps × Résilience

## Principe

Une optimisation Exadata n’est acceptable que si elle équilibre quatre dimensions :

1. **Performance** — temps de réponse, throughput, batch ;
2. **Résilience** — N-1, RPO, RTO, maintenance ;
3. **FinOps** — licences, infrastructure, cloud, exploitation ;
4. **GreenOps** — énergie, utilisation, capacité évitée, empreinte.

## Matrice de décision

| Action | FinOps | GreenOps | Performance | Résilience | Décision |
|---|---|---|---|---|---|
| réduire cœurs actifs | + | +/0 | risque | risque N-1 | tester |
| consolider workloads | + | + | risque noisy neighbor | dépend isolation | IORM/DBRM + test |
| déplacer données froides vers XT | + | + potentiel | dépend accès | neutre | mesurer |
| réduire power target | 0/+ | + | risque pic | risque failover | tester N-1 |
| ajouter DB Server | - | - | + | + | si besoin démontré |
| ajouter Storage Server | - | - | + I/O/capacité | + | si goulot storage |

## Architecture Decision Gate

Avant validation d’une optimisation, produire :

- métrique avant ;
- hypothèse ;
- scénario N ;
- scénario N-1 ;
- coût avant/après ;
- énergie/empreinte avant/après ;
- risque ;
- rollback ;
- preuve après mise en œuvre.

## Anti-pattern

Optimiser une seule dimension. Exemple : minimiser les licences en réduisant les cœurs actifs, puis découvrir qu’un failover RAC dépasse la capacité restante.

La cible recherchée est l’**efficience**, pas le minimum absolu de coût ou de puissance.