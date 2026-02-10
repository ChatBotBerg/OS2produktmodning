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
2. **Udvikling** og Teknisk dokumentation
3. **TEST-opsætning** i 3 kommuner.
4. **Kombit-test** testforløb planlagt af sammen med Kombit
5. **Klargøring** og produktionsmodning
6. **Udruldning** og idriftsættelse

```mermaid
flowchart LR
   Afklaring --> Udvikling --> Test-Implementering --> Integrationstest --> Klargøring --> Udruldning
```


**Milepæle:**
- 08.10.2025: projektet bliver fremlagt for  Styregryppen
- 10.11.2025: Styregruppen beslutter at igangsætte projektetet.
  25.06.2026: Release af kildekode
  

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
    Udvikling                                                  :des2, 2026-02-16, 2026-06-21
    Test opsætning                                             :des3, 2026-04-20, 2026-04-26
    Kombit-test                                                :des3, 2026-04-20, 2026-04-26
    Klargøring                                                 :des3, 2025-10-01, 2026-02-01   
    Udruldning                                                 :des3, 2025-10-01, 2026-02-01 
```
```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       "Detailplan for udvikling, teknisk test og teknisk dokumentation"
    excludes    weekends
    tickInterval 1quarter
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section Udviling
    Start                                                      : vert, v1, 2025-10-01,
    SLUT                                                       : vert, v1, 2026-11-15, 
    Projektstart                                               :crit, milestone, 2025-11-10, 0d

    section Udviling
    Teknisk afklaring og forundersøgelse                       :des1, 2025-10-01, 2026-02-08
    Udvikling af integrationsmodulet                           :des2, 2026-02-16, 2026-03-29
    Oprettelse af PR (release kandidat) (ITK)                  :des3, 2026-04-06, 2026-04-13
    commit af PR (release kandidat)                            :crit, milestone, 2026-04-13, 0d
    QA af PR                                                   :des4, 2026-04-13, 2026-04-15
    Codereview og teknisk test                                 :des5, 2026-04-13, 2026-04-26
    Løbende udbedring af identificerede fejl                   :des6, 2026-04-15, 2026-04-26
    Godkendelse af PR Releasekandidat (Bellcom)                :crit, milestone, 2026-04-27, 0d
    Release af kildekode i test branch (Bellcom)               :des7, 2026-04-27, 2026-05-08
    Release af kildekode i core (Bellcom)                      :des7, 2026-06-22, 2026-06-26

    section Dokumentation og vejledning
    Udarbejdelse af Teknisk Dokumentation                      :des3, 2026-02-16, 2026-03-29
    Udarbejdelse af imlplementationsvejledning                 :des2, 2026-02-16, 2026-03-29
    Konsolidering af dokumentations leverancen (ITK)           :des3, 2026-04-06, 2026-04-13
    QA af Dokumentationsleverancen ( Bellcom)                  :des4, 2026-04-13, 2026-04-15
    Review af Dokumentation og Vejledninger                    :des6, 2026-04-13, 2026-04-26
    Løbende opdatering af Dokumentation og vejledninger        :des7, 2026-04-15, 2026-04-26
    Godkendelse af Dokumentationsleverancen                    :crit, milestone, 2026-04-27, 0d
    Publicering af dokumentation (Bellcom)                     :des7, 2026-04-27, 2026-05-05
```
