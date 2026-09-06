# ADR-001 — ASM classique vs Exascale

## Statut
Proposé — cas de lab MayaBank.

## Contexte
MayaBank doit héberger plusieurs bases critiques et non critiques avec croissance forte, besoins de consolidation, environnements Dev/Test et contraintes de PRA.

## Options
### A — ASM classique
Modèle éprouvé, connu des équipes Oracle, forte maturité opérationnelle.

### B — Exascale
Pool de stockage partagé, vaults, volumes, snapshots/clones et mécanismes de resource management plus cloud-like.

## Critères
| Critère | ASM | Exascale |
|---|---|---|
| Maturité équipe | Forte | À acquérir |
| Allocation dynamique | Classique | Forte |
| Snapshots/clones | Dépend du design | Fonctionnalités Exascale natives |
| Isolation multi-tenant | Diskgroups/architecture | Vaults + resource controls |
| Migration | Plus familière | Analyse versions/prérequis requise |
| Innovation 2026 | Stable | Forte évolution 26.1 |

## Décision de lab
Ne pas imposer Exascale par principe. Pour une nouvelle plateforme X11M 2026, **évaluer Exascale en option préférentielle lorsque les versions, l’exploitation et la migration sont compatibles**, puis valider par POC. ASM reste l’option de repli à faible risque opérationnel.

## Risques
- compétences Exascale insuffisantes ;
- incompatibilités de versions ;
- modèle opérationnel non maîtrisé ;
- retour arrière mal préparé.

## Validation
POC de provisioning, performance, snapshots/clones, resource management, backup/recovery et PRA avant décision finale.
