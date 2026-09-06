# Questions d’entretien — Architecte Solution Exadata

## Architecture
1. Pourquoi Exadata plutôt qu’Oracle sur infrastructure générique ?
2. Qu’apporte X11M ?
3. Quel rôle jouent RDMA/RoCE, XRMEM, Flash Cache et Smart Scan ?
4. Comment choisissez-vous bare metal ou KVM ?
5. ASM ou Exascale : comment décidez-vous ?

## HA/DR
6. RAC protège contre quoi ?
7. Data Guard protège contre quoi ?
8. Pourquoi RAC + Data Guard ?
9. Peut-on garantir RPO 0 ?
10. Que contient réellement un RTO de 30 minutes ?
11. Que faites-vous si le WAN tombe ?
12. Comment revenez-vous au site primaire ?

## Data protection
13. Pourquoi Data Guard ne remplace pas RMAN ?
14. Quel rôle pour ZDLRA ?
15. Comment testez-vous une restauration ?
16. Comment gérez-vous corruption logique et cyberattaque ?

## Performance / sizing
17. Quelles métriques utilisez-vous avant sizing ?
18. Pourquoi les To ne suffisent-ils pas ?
19. Comment dimensionnez-vous N-1 ?
20. Comment évitez-vous le noisy neighbor ?

## Exploitation
21. Comment patcher sans interruption majeure ?
22. Quel apport de VM Live Migration 26.1 ?
23. Que supervisez-vous ?

## Décision
24. On-Prem, Cloud@Customer ou OCI : quels critères ?
25. Comment intégrez-vous licences, TCO et Green IT dans la décision ?

## Règle de réponse
Toujours répondre : **besoin → contrainte → options → décision → risque → preuve**.
