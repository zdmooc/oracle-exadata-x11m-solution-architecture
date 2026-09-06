# Advanced Power Management X11M

## Objectif

Utiliser les fonctions de gestion de puissance X11M sans confondre optimisation énergétique et réduction de capacité licenciée.

## Concepts

- **Capacity-on-Demand (CoD)** : contrôle du nombre de cœurs actifs/licenciables ;
- **Advanced Power Management** : contrôle de la consommation électrique ;
- **power target** : plafond de puissance ;
- **low-power mode** : fonctionnement réduit dans des plages adaptées ;
- réduction de cœurs inutilisés : à traiter selon les capacités supportées et la version installée.

## Méthode d’architecte

1. mesurer CPU, mémoire, I/O, batch et pics ;
2. définir la capacité minimale pour N et N-1 ;
3. identifier une plage de puissance candidate ;
4. tester pics, batch, RAC failover et maintenance ;
5. vérifier l’impact sur latence et throughput ;
6. documenter le gain kWh et le risque ;
7. intégrer au runbook d’exploitation.

## Anti-patterns

- utiliser CoD comme mécanisme de power saving ;
- abaisser un power target sans test N-1 ;
- optimiser sur la moyenne et ignorer les batchs ;
- économiser quelques watts tout en conservant plusieurs racks sous-utilisés ;
- annoncer un gain carbone sans facteur d’émission ni PUE documenté.

## Décision

La priorité reste :

`right-sizing → consolidation → capacité évitée → power management`.

Le power management affine une architecture déjà cohérente ; il ne compense pas un surdimensionnement structurel.