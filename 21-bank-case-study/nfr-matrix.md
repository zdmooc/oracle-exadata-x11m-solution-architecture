# MayaBank — NFR Matrix de départ

> Hypothèses de lab, à valider.

| ID | Domaine | Cible | Mécanisme candidat | Preuve attendue |
|---|---|---|---|---|
| NFR-001 | Disponibilité | 99,99 % | RAC + redondance + procédures | Tests HA + mesure SLA |
| NFR-002 | RPO | 0 cible | Data Guard à qualifier | Test perte site + mesure redo |
| NFR-003 | RTO | < 30 min | PRA automatisé/industrialise | Exercice PRA chronométré |
| NFR-004 | Performance | 10 000 TPS cible | X11M + sizing | Test charge représentatif |
| NFR-005 | Capacité | 30 To actifs + 100 To historique | HC/EF/XT à décider | Sizing 3/5 ans |
| NFR-006 | Croissance | 25 % / an | Capacity management | Revue trimestrielle |
| NFR-007 | Chiffrement | Données au repos chiffrées | TDE | Audit configuration + recovery wallet |
| NFR-008 | Backup | Restore démontrable | RMAN + ZDLRA | Tests restore/recover |
| NFR-009 | PRA | 2 sites | Data Guard + runbooks | Test annuel/semestriel selon politique |
| NFR-010 | Exploitation | Maintenance maîtrisée | rolling + KVM/live migration si retenu | Test patching |
