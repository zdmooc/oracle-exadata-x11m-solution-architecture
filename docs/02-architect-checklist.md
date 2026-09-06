# Checklist Architecte Solution Exadata

## Métier
- [ ] criticité et coût de panne connus
- [ ] périodes de pointe identifiées
- [ ] dépendances applicatives connues

## NFR
- [ ] SLA défini
- [ ] RPO justifié
- [ ] RTO bout en bout
- [ ] exigences sécurité/conformité

## Workload
- [ ] AWR/ASH représentatifs
- [ ] CPU/DB Time/AAS
- [ ] mémoire
- [ ] TPS/redo
- [ ] IOPS/throughput/latence
- [ ] données actives/historiques
- [ ] croissance

## Architecture
- [ ] bare metal vs KVM décidé
- [ ] ASM vs Exascale décidé
- [ ] HC/EF/XT décidé
- [ ] RAC/services définis
- [ ] IORM/DBRM défini
- [ ] réseaux et flux documentés

## Résilience
- [ ] N-1 dimensionné
- [ ] Data Guard mode justifié
- [ ] RMAN/ZDLRA
- [ ] restore testé
- [ ] PRA testé
- [ ] clés TDE récupérables au PRA

## Exploitation
- [ ] observabilité
- [ ] patching
- [ ] rollback
- [ ] capacity management
- [ ] RACI

## Décision
- [ ] scénarios comparés
- [ ] TCO/licensing
- [ ] risques
- [ ] ADR
- [ ] HLD
- [ ] preuves de validation
