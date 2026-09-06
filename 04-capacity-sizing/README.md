# Module 04 — Capacity Sizing

## Objectif

Dimensionner une architecture Exadata à partir d’une charge réelle et non d’une simple volumétrie en To.

## Entrées minimales

- CPU actuelle et pics ;
- mémoire utilisée et pression mémoire ;
- DB time / AAS ;
- sessions concurrentes ;
- transactions/s ;
- lectures/écritures par seconde ;
- IOPS ;
- débit MB/s ou GB/s ;
- latence ;
- taille active ;
- historique ;
- taux de croissance ;
- fenêtres batch ;
- sauvegardes ;
- réplication ;
- contraintes de failover.

## Principe

Le sizing doit couvrir le **steady state** et les **failure states**.

Exemple : si un cluster doit continuer après perte d’un DB Server, les nœuds restants doivent absorber la charge critique sans dépasser les seuils retenus.

## Méthode

### 1. Baseline

Collecter AWR/ASH/OEM et métriques OS sur plusieurs périodes représentatives.

### 2. Classifier la charge

- OLTP ;
- analytics ;
- batch ;
- mixte ;
- lecture dominante ;
- écriture dominante.

### 3. CPU

Calculer besoin moyen, pic, croissance, consolidation et réserve de panne.

### 4. Mémoire

Évaluer SGA/PGA, OS, VM éventuelles et marge.

### 5. Stockage

Ne pas confondre :

- capacité brute ;
- capacité utile ;
- redondance ;
- espace DATA ;
- espace RECO ;
- snapshots/clones ;
- historique ;
- croissance ;
- marge opérationnelle.

### 6. I/O

Mesurer :

- random read/write ;
- sequential scan ;
- IOPS ;
- throughput ;
- latency ;
- effet attendu de Smart Scan, flash et XRMEM.

### 7. Réseau

Dimensionner :

- trafic client ;
- fabric ;
- backup ;
- Data Guard ;
- management.

### 8. Croissance

Produire au minimum une projection 3 ans et 5 ans.

## Anti-patterns

- dimensionner uniquement sur les To ;
- utiliser la moyenne CPU sans les pics ;
- oublier les batchs de fin de journée/mois ;
- ignorer la charge de réplication et sauvegarde ;
- dimensionner sans scénario de panne ;
- considérer toutes les données historiques comme actives ;
- surdimensionner sans justification économique.

## Livrables

- tableau d’hypothèses ;
- baseline ;
- sizing compute ;
- sizing memory ;
- sizing storage ;
- sizing network ;
- croissance 3/5 ans ;
- scénario N et N-1 ;
- risques et marges.
