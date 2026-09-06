# LAB 11 — Data Guard SYNC vs ASYNC

## Objectif
Relier RPO, latence et redo à un choix de transport.

## Scénarios
Étudier plusieurs RTT inter-site et plusieurs débits redo.

## Travail
1. Identifier impact du SYNC sur commits.
2. Évaluer perte potentielle en ASYNC.
3. Définir comportement lors de perte WAN.
4. Relier choix au SLA métier.

## Livrable
ADR mode Data Guard + hypothèses réseau à mesurer.

## Terminé si
« RPO 0 » n’est utilisé que si la chaîne technique et opérationnelle le justifie.