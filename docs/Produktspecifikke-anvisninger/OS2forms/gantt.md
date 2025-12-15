---
layout: default
title: "Releaseplan 2025"
author: "Anna-Lis Berg"
date: "19-10-2025"
status: "final"
parent: "OS2forms"
nav_order: 2
has_children: false
---

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       OS2Forms efterårsrelease 2025
    excludes    weekends
    tickInterval 1week
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section Scope af næste release
    Individuel forberedelse                        :des1, 2025-08-04, 2025-08-13
    Forberedelsesmøde i koordinations              :active, milestone, a1, 2025-08-14, 0d
    Belcom forbereder forslag til forbedringer     :2025-08-11, 2025-08-27
    1. Møde med Belcom                             :crit, milestone, a2, 2025-08-27, 0d
    Belcom konsoliderer og estimerer               :des3, after a2,2025-09-17
    Releaseplan, incl estimat og detailplan leveret:crit,milestone, a3, 2025-09-15, 0d
    2. scopint møde med Bellcom                    :crit, milestone, a4, 2025-09-17, 0d
    koordinationsgtuppen evaluerer releaseplanen   :des5, after a4, 2025-09-30
    Releaseplan er endelig godkendt                :crit, milestone, a5,2025-10-01, 0d
    Bellcom og ITK klargør releasen i test         :des6, after a5, until a6
    Kickoffpå test (møde)                          :milestone, a6,2025-10-29, 0d
    Test af efterårsreleasn                        :des6, after a6, 2025-11-14
    Releasen gennemføres                           :des7, 2025-11-14, 2025-11-20
    Releasen er afsluttet                          :crit, milestone, a10,2025-11-20, 0d

```

**Seneste revision af releasplanen er som flg:**
- 27.08.2025: 1.scopingmøde med Bellcom
- 17.09.2025: 2 scopingmøde med Bellcom 
- 15.09.2025: Releasen er klart defineret, dokumenteret og estimeret
- 01-10-2025:  Releasen blev  godkendt af koordinationsgruppen  (forsinket 2 arbejdsdage)
- 28.10.2025: Releasen er klar til test ( forsinket 5 arbejdsdage)
- 29.10.2025 : Kickoff på test /Virtuel møde med Bellcom kl 10.00 – 11.00
- 14.11.2025: Releasen er testet og accepteret (udskudt 4 arbejdsdage)
- 20.11.2025: Releasen er gennemført (merget til main branch)  ( udskudt 3 arbejdsdage)

**Baggrund for forsinkelser og udskydelser**:

- Den forsinkede godkendelse af scope resulterede desværre i at ITK – Aarhus ikke fik færdiggjort klargøring af de identificerede bugfix inden deres udviklere gik på planlagt efterårsferie.
- Bellcom kan naturligvis ikke ikke færdiggøre testen før ITK har færdiggjort dette arbejde.
- ITK har  allokeret ressourcer til at få deres arbejde afsluttet på mandag, men der løber Bellcom ind i planlagt ferie hos deres udviklere, hvilket betyder at de først kan færdiggøre den sidste del af arbejdet i starten af uge 44. 

**Kickoff møde:**

For at sikre fokus og kvalitet for teste er det planlagte leverandørmøde med Bellcom den 29 oktober erstattet med et Kickoff møde på test.
Alle de kommuner der er repræsenteret i koordinationsgruppen er blevet bedt om at sende en testansvarlig/testkoordinator til dette møde. 

Mødeinvitation er sendt til koordinationsudvalget, med note om at de selv skal videresende til rette vedkommende. 

