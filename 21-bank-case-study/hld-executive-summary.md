# MayaBank — HLD Executive Summary (draft)

## Besoin
Moderniser la plateforme Oracle de paiements critique afin de supporter 10 000 TPS, une croissance de 25 %/an, un fonctionnement 24/7 et un PRA deux sites.

## Orientation
Étudier une cible Exadata X11M avec séparation claire des mécanismes :

- RAC : disponibilité locale ;
- Data Guard : perte de site ;
- RMAN/ZDLRA : sauvegarde et restauration ;
- TDE : chiffrement ;
- IORM/DBRM : isolation des workloads ;
- ASM ou Exascale : décision à valider ;
- KVM ou bare metal : décision à valider.

## Décision non figée
Le HLD ne sélectionne pas encore une configuration matérielle exacte. Celle-ci dépend du workload assessment et du sizing N/N-1.

## Risques principaux
1. RPO 0 non démontré tant que la latence inter-site et le redo rate ne sont pas mesurés.
2. Sizing faux si basé uniquement sur les To.
3. PRA incomplet si les applications, clés TDE et dépendances réseau ne sont pas intégrées.
4. Surcoût si consolidation/licensing non optimisés.
5. Complexité opérationnelle si Exascale/KVM sont adoptés sans montée en compétence.

## Prochain jalon de conception
Valider NFR, workload, réseau, sizing et options d’architecture avant approbation du HLD final.
