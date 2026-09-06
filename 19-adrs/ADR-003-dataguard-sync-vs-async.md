# ADR-003 — Data Guard SYNC vs ASYNC

## Statut
Proposé — dépend des mesures inter-site.

## Contexte
MayaBank vise un RPO 0 et un RTO inférieur à 30 minutes entre deux sites.

## SYNC
Réduit le risque de perte de redo validé mais ajoute une dépendance à la latence et à la stabilité du réseau sur le chemin de commit selon le mode de protection retenu.

## ASYNC
Réduit l’impact de la distance réseau sur la production mais peut laisser un écart de redo non transporté lors d’une perte brutale du site primaire.

## Décision de lab
**Aucune décision finale sans mesure.** Le RPO 0 impose d’abord de valider RTT, redo rate, bande passante, stabilité réseau et comportement lors de rupture WAN. Si ces contraintes rendent SYNC incompatible avec le SLA de latence transactionnelle, l’exigence métier ou l’architecture doit être revue.

## Tests
- RTT nominal/P95/pic ;
- redo MB/s nominal/P95/pic ;
- perte d’un lien ;
- congestion ;
- bascule ;
- RPO réellement observé ;
- impact sur commit latency.
