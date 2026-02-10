---
layout: default
title: "Fordelingskomponentens udviklingsplan"
author: "Anna-Lis Berg"
date: "10-02-2026"
status: "daft"
parent: "OS2forms"
nav_order: 6
has_children: false
---
# Etablering af OS2forms integration til fordelingskomponenten

OS2forms koordinations og styregruppe besluttede i efteråret at igangsætte udvikling og implementering af en OS2forms‑integration til KOMBITs fordelingskomponent. 
Hovedformålet med etablering af en sådan komponeent var at effektivisere datahåndtering og muliggøre udfasning af de anvendte 3 parts selvbetjeningsløsninger.

Etablering af OS2forms integrationen kan deles op i 5 hovedfaser, med hver sit fokus og omdrejningspunkt.

1. **Afklaring** og afgrænsning.
2. **Udvikling** og test
3. **Implementering** i 3 test kommuner.
4. **Klargøring** og dokumentation
5. **Udruldning** og idriftsættelse

```mermaid
flowchart LR
   Afklaring --> Udvikling --> Implementering --> Klargøring --> Udruldning
```


**Milepæle:**
- 08.10.2025: projektet bliver fremlagt for  Styregryppen
- 10.11.2025: Styregruppen beslutter at igangsætte projektetet.
- 

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       "Roadmap og milepæle"
    excludes    weekends
    tickInterval 1quarter
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section Milepæle
    Start                                                      : vert, v1, 2025-10-01,
    SLUT                                                       : vert, v1, 2026-10-22, 
    Projektstart                                               :crit, milestone, 2025-11-10, 0d
    Afklaring                                                  :des1, 2025-10-01, 2026-02-01
    Udvikling                                                  :des2, 2025-09-15, 2025-09-29
    Implementering                                             :des3, 2025-10-01, 2026-02-01
    Klargøring                                                 :des3, 2025-10-01, 2026-02-01   
    Udruldning                                                 :des3, 2025-10-01, 2026-02-01 
```
