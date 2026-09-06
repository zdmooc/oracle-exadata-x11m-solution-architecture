# Module 17 — Green IT / GreenOps / Capacity Efficiency

## Objectif

Concevoir et exploiter Exadata avec une vision conjointe de l’utilisation réelle, de l’énergie, de l’empreinte environnementale, du coût et de la résilience.

## Parcours

1. [`greenit-methodology.md`](greenit-methodology.md) — Build/Use, PUE, allocation carbone, données actives/froides.
2. [`greenops-operating-model.md`](greenops-operating-model.md) — KPI, revues et boucle d’amélioration continue.
3. [`advanced-power-management.md`](advanced-power-management.md) — power target, low-power mode et garde-fous N-1.
4. [`finops-greenops-resilience.md`](finops-greenops-resilience.md) — décisions multicritères.

## Principes

- ne pas réduire l’empreinte à `kgCO2e/Go` ;
- distinguer capacité installée, active, utilisée et évitée ;
- séparer CoD/licensing de la gestion énergétique ;
- mesurer l’effet de la consolidation ;
- intégrer le PRA, les backups, la réplication et les données froides ;
- documenter PUE et facteurs d’émission lorsque l’on calcule des kgCO2e ;
- intégrer le double-run de migration ;
- vérifier chaque optimisation en N et N-1.

## KPI cibles

- CPU utilisée / CPU active ;
- cœurs actifs / installés ;
- RAM utilisée / provisionnée ;
- TB actifs / totaux ;
- taux de consolidation ;
- puissance moyenne / pic ;
- kWh/mois ;
- kgCO2e/mois ;
- €/million de transactions ;
- kgCO2e/million de transactions.

## Livrables

- modèle d’allocation carbone ;
- dashboard GreenOps ;
- budget capacité ;
- recommandations right-sizing/consolidation ;
- stratégie power management ;
- plan de rétention/tiering ;
- analyse de sensibilité ;
- preuve de gains réellement obtenus.