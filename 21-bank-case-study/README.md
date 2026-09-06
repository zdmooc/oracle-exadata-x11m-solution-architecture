# Cas fil rouge — MayaBank Payment Platform

## Contexte

MayaBank modernise une plateforme de paiements critique exploitée 24/7. La cible doit supporter une croissance forte, réduire le risque opérationnel et fournir une stratégie PRA démontrable.

## Hypothèses de départ

| Domaine | Valeur de lab |
|---|---:|
| Charge cible | 10 000 TPS |
| Données actives | 30 To |
| Historique | 100 To |
| Croissance | 25 % / an |
| Disponibilité | 99,99 % |
| RPO cible | 0 |
| RTO cible | < 30 min |
| Sites | 2 |
| Base | Oracle Database |
| Protection | RAC + Data Guard à étudier |
| Sauvegarde | RMAN + ZDLRA |
| Chiffrement | TDE |

## Questions d’architecture

1. Quel scénario Exadata est le plus adapté ?
2. Quelle taille de rack / configuration est nécessaire ?
3. Quel niveau de redondance et quelle architecture réseau ?
4. RAC doit-il être utilisé sur chaque site ?
5. Data Guard doit-il fonctionner en SYNC ou ASYNC ?
6. La latence inter-site permet-elle réellement le RPO visé ?
7. ASM ou Exascale selon le scénario ?
8. Quel profil HC / EF / XT pour données actives, historiques et sauvegardes ?
9. Comment isoler les workloads critiques ?
10. Comment gérer patching, maintenance et réduction du downtime ?
11. Quel plan de restauration après corruption logique ou cyberattaque ?
12. Quel TCO à 5 ans ?

## Scénarios

### A — Dual on-premises X11M

Deux plateformes Exadata X11M, une par datacenter, avec Data Guard inter-site.

### B — Dual Exadata Cloud@Customer

Même logique de proximité datacenter avec modèle cloud opéré.

### C — OCI Exadata + DR

Production OCI Exadata, stratégie DR adaptée au niveau de dépendance réseau et à la souveraineté requise.

### D — Hybride / multicloud

Architecture intégrant Exadata Cloud et composants applicatifs répartis entre cloud(s) et datacenters.

## Matrice de décision à produire

| Critère | Poids | A | B | C | D |
|---|---:|---:|---:|---:|---:|
| RPO/RTO | 20 | | | | |
| Performance | 15 | | | | |
| Résilience | 15 | | | | |
| Sécurité | 10 | | | | |
| Exploitabilité | 10 | | | | |
| Migration | 10 | | | | |
| Coûts | 10 | | | | |
| Réversibilité | 5 | | | | |
| Green IT | 5 | | | | |

## Livrable final

Le dossier de soutenance doit contenir :

- executive summary ;
- NFR ;
- workload assessment ;
- sizing ;
- scénarios ;
- matrice de décision ;
- architecture cible ;
- flux réseau ;
- HA/DR ;
- backup/recovery ;
- sécurité ;
- observabilité ;
- patching ;
- migration ;
- coûts ;
- risques ;
- ADR ;
- plan de tests PRA.
