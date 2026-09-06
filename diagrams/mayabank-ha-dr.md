# Diagramme — MayaBank HA/DR

```mermaid
flowchart TB
  subgraph A[Datacenter A]
    APP_A[Payment Applications]
    SCAN_A[Oracle SCAN / Services]
    RAC_A[Oracle RAC Primary]
    EXA_A[Exadata X11M]
    APP_A --> SCAN_A --> RAC_A --> EXA_A
  end

  subgraph B[Datacenter B]
    APP_B[PRA Applications]
    SCAN_B[Oracle SCAN / Services]
    RAC_B[Oracle RAC Standby]
    EXA_B[Exadata X11M]
    APP_B --> SCAN_B --> RAC_B --> EXA_B
  end

  RAC_A == Data Guard ==> RAC_B
  EXA_A --> Z[RMAN / ZDLRA]
  EXA_B --> Z
  K[Key/Wallet Recovery] -.-> RAC_A
  K -.-> RAC_B
  O[Observability] -.-> RAC_A
  O -.-> RAC_B
```

## À vérifier
- mode Data Guard ;
- latence et bande passante ;
- localisation ZDLRA ;
- architecture des clés ;
- capacité N-1 ;
- orchestration applicative de la bascule.
