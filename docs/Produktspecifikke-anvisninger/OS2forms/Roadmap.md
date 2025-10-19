---
layout: default
title: "Roadmap og timeline "
author: "Anna-Lis Berg"
date: "19-08-2025"
status: "Udkast" 
parent: "OS2forms"
nav_order: 1
has_children: false
---
---

📆 _sidst opdateret: {{ site.time | date: '%B %d, %Y' }}_

# OS2forms: Roadmap og Timeliene for de strategisk indsatsområder

Nedenstående diagram er en anbefaling til hvilke aktiviteter der igangsættes inden forhver af de fire strategiske hovedspor i løbet af 2025 & 2026. 

**De 4 Hovedspor er flg:
1. **Produktstrategi** og udbredelse
2. **Produktudvikling** og vedligehold
3. **Produktfællesskab**,  engagement og inolvering
4. **Produktkoordination**, administration og kommunikation


```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       OS2Forms Roadmap for strategiske indsatsområder 2025/2026
    excludes    weekends
    tickInterval 1month
    Start: vert, v1, 2025-03-01,
    Årsskifte : vert, v3, 2026-01-01,
    Slut: vert, v3, 2026-06-01,
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section  Produktstrategi
    Etablering af samarbejde med KL        :2025-06-01, 2025-12-19


    section  Produktudvikling
    Hands-on support fra sekretariatet     :2025-03-01, 2026-01-01
    Optimeret releasestyring               :2025-06-01, 2025-11-01
    On-demand fejlterning                  :2025-10-01, 20256-01-20
    automatiseret kvalitets check          :2025-10-01, 20256-01-20


    section  Produktfællesskab
    Hands-on support fra sekretariatet               :2025-10-20, 2026-04-01
    Overdragelse og oplæring fra sekretariatet       :2026-02-01, 2026-06-01
    Os2forms financieret communitymanagement         :2026-01-01, 2026-06-30

    section  Produktkoordination
    Produkt koordinatore i sekretariatet             :2025-01-06, 2025-12-15
    Overdragelse og oplæring fra sekretariatet       :2025-12-01, 2026-04-01
    Os2forms financieret produktkoordination         :2026-01-01, 2026-06-30

```
