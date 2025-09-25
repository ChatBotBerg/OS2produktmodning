---
layout: default
title: "Releaseplan 2025"
author: "Anna-Lis Berg"
date: "19-08-2025"
status: "Udkast"
parent: "OS2forms"
nav_order: 1
has_children: false
---

**Milepæle:**
- 15.09.2025: Releasen er klart defineret, dokumenteret og estimeret
- 29.09.2025: Releasen er godkendt af koordinationsgruppen
- 20.10.2025: Releasen er klar til test
- 10.11.2025: Releasen er testet og accepteret
- 17.11.2025: Releasen er gennemført (merget til main branch i kildekoden)

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       OS2Forms Scope af efterårsreleasen
    excludes    weekends
    tickInterval  1w
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section Scope af næste release
    Individuel forberedelse                        :des1, 2025-08-04, 10d
    Forberedelsesmøde i koordinations              :active, milestone, a2, 2025-08-14, 1d
    opsamlende aktiviteter                         :des2, after a2, 3d
    Opsamlende møde i koordinations                :active, milestone, a3, 2025-08-21, 1d
    Belcom forbereder forslag til forbedringer     :2025-08-11, 2025-08-27
    1. Møde med Belcom                             :crit, milestone, a3, 2025-08-27, 1d
    Opsamlende møde i Koordinationsgruppen         :active, milestone, a4, 2025-09-01, 1d
    Belcom konsoliderer og estimerer                :des3, after a3, 2025-09-17, 1d
    2. møde med Belcom                             :crit, milestone, a5, 2025-09-17, 1d
    Belcom færdiggør releaseplan                   :des4, after a5, 10d
    Releaseplan, incl estimat og detailplan leveret:crit, milestone, a6, after des4, 0d
    koordinationsgruppen evaluerer releaseplanen   :des5, after a6, 5d
    Releaseplan diskuteres i koordinationsgruppen  :milestone, a7, 2025-10-01, 1d
    3. møde med Belcom                             :milestone, a8, 2025-10-08, 1d
    Belcom opdaterer releaseplan                    :des6, after a8, 3d

```