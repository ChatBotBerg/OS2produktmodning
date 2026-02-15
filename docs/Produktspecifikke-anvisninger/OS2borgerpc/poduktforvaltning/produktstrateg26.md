---
layout: default
title: "Produktstrategi 2026-2027"
author: "Anna-Lis Berg"
date: "10-12-2025"
status: "final" 
parent: "OS2borgerpc"
nav_order: 1
has_children: false
---

📆 _sidst opdateret: {{ site.time | date: '%B %d, %Y' }}_

# OS2borgerpc Produktstrategi 2026-2027  

OS2borgerpc står overfor en gennemgribende opgradering, revision og modernisering, som blandt andet inkludere en omkostningstung opgradering af det underliggende styresystem ( Ubuntu 22.04) og dertilhørende omskrivninge i kodebasen. 

De indledende analyser har vist at det bliver omkostningstungt at gennemføre en sådan opgradering og ressourcekrævende at vedligeholde løsningen efterfølgende. 
Derfor har produktets styre- og koordinationsgruppe besluttet at det er tid til se sig om efter alternative moderne løsninger.

Produktstrategien for 2026/2027 er derfor at man holder den eksisterende løsning sikker og stabil og dens kodebase opdateret, imedens man i paralell afprøver og produktionsmodner en moderne og digitalsuverænt erstatning.

Den overordnede strategi for 2026 og 2027 er som flg:
1. **OS2borgerPC v2 forvaltningen fortsætter i sin nuværende form**, med fokus på sikkerheds opdatering og driftsstabilitet, samt minimal indsats i forhold til featureudvilling.
2. **OS2borgerpc V3 designes og produktmodnes i et paralell projekt**,  med fokus på afprøvning og evaluering af eksisterende Open-Source løsninger og konfigurering af en moderne og digital suveræn biblioteksPC. 


# OS2borgerpc: Produktstrategi 2026/2027 produkt roadmap
```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       Os2 borgerPC Produktstrategi 2026/27
  
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)
 
   section OS2borgerpc v2
   slut                                            : vert, v4, 2027-06-01,
   Årsskifte 26                                    : vert, v2, 2026-01-01,
   Vedligehold ved frikøb                     :des4, 2025-08-02, 2026-05-01
   Indgåelse af vedligeholdelses kontrakt     :des5, 2026-03-01, 2026-05-01
   Kontraktuel vedligehold og viderudvikling  :des6, 2026-05-01, 2027-06-01
   Overgang til pro vedligehold for UBUNTU 22.04 :crit, milestone, m1,2027-04-01, 0d
   
   section  OS2borgerpc v 3
   Årsskifte 27                                    : vert, v3, 2027-01-01,
   POC Arkitektur design                    :des1, 2025-08-02, 2025-12-02
   Klargøring af POC                       :des1, 2025-12-02, 2026-02-01
   Hackatons & POC Iterationer             :des1, 2026-02-01, 2026-05-01
   MVP udvikling                         :des1, 2026-05-01, 2026-09-01
   Produktionsmodning                      :des1, 2026-09-01, 2027-02-01
   Release af v1                          :crit, milestone, m1,2027-02-01, 0d
   Migrering                            :des5, 2027-02-01, 2027-07-
``` 

