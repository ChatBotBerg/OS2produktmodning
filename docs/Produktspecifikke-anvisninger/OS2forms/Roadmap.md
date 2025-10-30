---
layout: default
title: "Roadmap og timeline for sekretariatssupport til OS2forms"
author: "Anna-Lis Berg"
date: "19-08-2025"
status: "Udkast" 
parent: "OS2forms"
nav_order: 1
has_children: false
---

📆 _sidst opdateret: {{ site.time | date: '%B %d, %Y' }}_

# OS2forms: Roadmap og Timeline for sekretariats-support

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       OS2Forms Roadmap for sekretariatssupport 2025/2026
    excludes    weekends
    tickInterval 1month
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)

    section  OS2forms bemanding
    Produktkoordinator udpeget   :crit, milestone, a1,2026-01-05, 0d
    Produkt Owner udpeget        :crit, milestone, a1,2026-02-01, 0d
    Start: vert, v1, 2025-03-01,
    Årsskifte : vert, v3, 2026-01-01,
    Os2forms financieret Produktkoordinator        :2026-01-01, 2026-08-30
    Os2forms financieret Product Owner (PO)        :2026-02-01, 2026-08-30
    Slut: vert, v3, 2026-08-01,
    Mødeledelse og Administration overdraget   :crit, milestone, a1,2026-03-01, 0d
    Produktforvaltning overdraget             :crit, milestone, a1,2026-04-01, 0d



    section  Sekretariasfunktion
    Handson support betralt af fællesskabet        :2025-00-01, 2026-01-01
    Oplærnig og videnoverdragelse                  :2026-01-05, 2026-03-01

    section  Community building
    Hands-on support fra sekretariatet               :2025-10-20, 2026-04-01
    Overdragelse af årshjul til produktkoordinatoren :2026-02-01, 2026-03-01

    section  Produktforvaltning
    Hands-on support fra sekretariatet (PO)        :2025-03-01, 2026-03-01
    Oplærnig og videnoverdragelse                  :2026-02-01, 2026-03-30


    section  Produktudvikling
    Handson support fra sekretariatet                           :2025-11-01, 2026-03-01
    Overdragelse til Produkt koordinator og Product owner       :2026-02-01, 2026-04-01

```

Sekretariatssupporten til OS2forms kan deles op i fire hovedspor, 2 administrative og 2 produkt tekniske
1. **Sekretariasfunktion**
   - Administration og økonomiopfølgning.
   - Mødeplanlægning og referat skrivning
   - onboarding af nye medlemmer 
   - opdatering af hjemmeside
   - Publisering af referater

2. **Community building** og crowdfunding
    - Etablering af årshjul for produktfællesskabet
     - årshjul og praksis for Communitymøder
    - årshjul og praksis for Brugerklub møder ( anvendere)
    -  - årshjul og praksis for teknisk erfagruppemøder (kommunale driftsafdelinger og drifts leverandører)
    - etablering af crowfundings model
        
3. **Produktforvaltning** og vedligehold af Kildekode
    - Releasemanagement & Bugfix håndtering ( optimering & opstramning incl 12 måbneders roadmap)
    - Transperans og sporbarhed i leverancen
    - Praksis for tværgående leverandørsamarbejde
    - Forbedret Leverandørsamarbejde'
    - Etablering af beslutningslog
    - escalleringspunkt for manglende leverandørsamarbejde
    - årshjul og praksis for leverandøropfølgning
      
5.  **Produktudvikling** leverandørsamarbejde
    - Etablering af transperant af issuetracking i Github
    - 12 mdr roadmap for feature udvikling
    - Praksis for overtagelse af Contributions
    -  Oprydning i og overflytning af åbne Issues


