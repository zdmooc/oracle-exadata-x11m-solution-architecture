# Module 20 — Reference Architectures

## Objectif

Maintenir plusieurs architectures de référence, chacune reliée à un contexte d’usage et à des compromis explicites.

## RA-01 — Dual X11M On-Premises

- Exadata X11M sur deux sites ;
- RAC local ;
- Data Guard inter-site ;
- RMAN / ZDLRA ;
- TDE ;
- supervision centralisée.

**Usage :** forte maîtrise infrastructure, proximité applicative, exigences datacenter internes.

## RA-02 — Dual Exadata Cloud@Customer

- Exadata Cloud@Customer sur deux domaines de panne ;
- responsabilités partagées ;
- Data Guard ;
- intégration réseau et sécurité entreprise.

**Usage :** besoin de modèle cloud tout en gardant les données dans le datacenter client.

## RA-03 — OCI Exadata + DR

- Exadata Database Service dans OCI ;
- stratégie DR ;
- connectivité FastConnect/VPN selon contexte ;
- intégration IAM, sécurité et observabilité.

**Usage :** stratégie cloud avec forte dépendance aux services OCI.

## RA-04 — Hybride / Multicloud

- applications distribuées ;
- Exadata comme plateforme de données critique ;
- interconnexion cloud/datacenter ;
- résilience réseau renforcée.

**Usage :** SI distribué ou trajectoire de transformation progressive.

## Règle

Une reference architecture n’est jamais une cible automatique. Elle doit être adaptée aux NFR, au workload, aux contraintes réseau, à la souveraineté, à l’exploitation et au coût.
