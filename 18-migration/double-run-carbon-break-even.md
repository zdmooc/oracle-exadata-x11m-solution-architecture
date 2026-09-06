# Migration Exadata — Double-run, coût et carbon break-even

## Objectif

Évaluer une migration non seulement sur le cutover technique, mais aussi sur la période de coexistence source/cible.

## Phases

1. discovery et baseline ;
2. compatibilité/version/options ;
3. sizing cible ;
4. préparation réseau/sécurité ;
5. migration pilote ;
6. répétitions ;
7. synchronisation finale ;
8. cutover ;
9. hypercare ;
10. décommissionnement source.

## Double-run

Pendant la coexistence, les deux plateformes peuvent consommer simultanément :

- infrastructure ;
- licences/support ;
- énergie ;
- stockage ;
- réplication ;
- backup ;
- exploitation.

Le dossier de migration doit donc calculer :

`surcoût double-run = coût source + coût cible + migration - coûts évités`

et, lorsque les données sont disponibles :

`sur-empreinte double-run = empreinte source + empreinte cible pendant coexistence`.

## Carbon break-even

Le gain environnemental d’une cible n’est pas instantané si la migration nécessite une période de double-run ou du nouveau matériel.

Documenter :

- empreinte initiale ;
- empreinte cible ;
- durée coexistence ;
- fabrication additionnelle prise en compte selon méthode ;
- date à laquelle le cumul des gains compense le surcoût initial.

## Go/No-Go

Le cutover doit intégrer :

- performance ;
- fonctionnel ;
- RPO/RTO ;
- backup/restore ;
- sécurité ;
- observabilité ;
- rollback ;
- licences ;
- coût ;
- impact environnemental.

## Livrables

- migration decision tree ;
- calendrier de répétitions ;
- plan de cutover/rollback ;
- coût du double-run ;
- carbon break-even ;
- plan de décommissionnement ;
- critères de succès.