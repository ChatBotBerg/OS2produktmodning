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
    title       "2025 Release plan
    excludes    weekends
    tickInterval 1week
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    Section Plan for efterårsreleasen 2025
    Scoping                                                    :des1, 2025-08-04, 2025-09-15
    Releasen er klart defineret, dokumenteret og estimeret     :crit, milestone, a2,2025-09-15, 0d
    Belcomm fremlægger resultatet af afklaringen               :crit, milestone, a3,2025-09-17, 0d
    Evaluering                                                 :des2, 2025-09-15, 2025-09-29
    Releasen er godkendt af koordinationsgruppen               :crit, milestone, a4,2025-09-29, 0d
    Detailplanlægning                                          :des2, 2025-09-15, 2025-09-29
    Releasen er klar til test                                  :crit, milestone, a5,2025-10-20, 0d
    Releasen er testet og accepteret                          :crit, milestone, a6,2025-11-10, 0d
    Releasen er gennemført (merget til main branch):crit, milestone, a5,2025-11-17, 0d
```
