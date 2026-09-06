# Module 06 — Oracle Exadata Exascale

## Objectif architecte

Comprendre ce qu’Exascale change dans le modèle de stockage Exadata et savoir décider quand l’intégrer dans une architecture cible.

## Concepts clés

- pool disks ;
- storage pools ;
- vaults ;
- files ;
- snapshots / clones ;
- Exascale volumes ;
- volume groups ;
- resource profiles ;
- IORM inter-vault ;
- DBRM intra-database.

## Idée principale

Exascale découple davantage les clusters Oracle Database / Grid Infrastructure du stockage Exadata sous-jacent et permet de partager dynamiquement un pool de stockage entre plusieurs clusters et bases avec isolation et contrôle des ressources.

## Chaîne logique simplifiée

```text
Exadata Storage Servers
        |
    Pool Disks
        |
   Storage Pool
        |
      Vaults
        |
 Databases / Volumes
```

## Différence conceptuelle avec ASM classique

ASM reste un socle central des architectures Oracle traditionnelles sur Exadata. Exascale introduit un modèle de stockage partagé et cloud-like où la capacité est gérée par pools et vaults, avec des mécanismes natifs de snapshots, clones, volumes et gestion de ressources.

L’architecte ne doit pas conclure automatiquement qu’Exascale remplace ASM dans tous les cas. La décision dépend des versions, du mode de déploiement, des contraintes d’exploitation, de la migration et des fonctionnalités recherchées.

## Points 26.1 à intégrer

System Software 26.1 étend notamment :

- la flexibilité de gestion des storage pools ;
- les snapshots immuables Exascale ;
- les resource profiles pour les volumes ;
- l’observabilité des volumes ;
- la migration des guest image files vers Exascale ;
- le support de scénarios de VM Live Migration.

## Questions d’architecture

- quelles bases doivent partager le même pool ?
- quels besoins d’isolation ?
- comment gérer les workloads critiques ?
- quelles exigences snapshots/clones ?
- quels besoins Dev/Test ?
- quel impact sur migration et exploitation ?
- quelles versions Oracle Database / Exadata System Software sont requises ?
- quelle stratégie de rollback ?

## Livrable

Produire un ADR :

**ADR — ASM classique vs Exascale pour MayaBank**

avec : contexte, contraintes, options, critères, décision, conséquences, risques et plan de validation.
