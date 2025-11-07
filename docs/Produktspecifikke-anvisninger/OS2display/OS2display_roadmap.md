---
layout: default
title: "Revision af forvaltningsmodellen i OS2 display"
author: "Anna-Lis Berg"
date: "04-11-2025"
status: "Udkast" 
parent: "OS2display"
nav_order: 3
has_children: false
---

📆 _sidst opdateret: {{ site.time | date: '%B %d, %Y' }}_

# Revision af forvaltningsmodellen i OS2 display


Den startegiske plan for revision af forvaltningsmodellen i OS2display i forbindelse med opstart på den formelle overtagelse af produiktets kildekode.

Planenen følger den strategiske plan for overdargelse af kildekoden 8
Planenen følger den strategiske plan for overdargelse af kildekoden fra Aarhus Kommune til OS2 [JVF: OS2display overdragelse til OS2](https://chatbotberg.github.io/OS2produktmodning/docs/Produktspecifikke-anvisninger/OS2display/OS2display_handover.html)



## Fokus og omdrejningspunkt: Revision af forvaltningsmodellen i OS2 display

**Indsatsområder** (arbejdsstråmme)
1. Kontrakt og ejerskab 
2. Produktfællesskabets styringsmode 
3. Daglig praksis for vedligehold og dokumentation 
4. Produktudvikling, modenhed og kvalitet 

**Målsætning pr indsatsområde**

1. Kontrakt og ejerskab : 
   *Overdragelse af det juridiske ansvar*
   1. Juridisk ejerskab af kontrakt for udvikling og vedligehold af kildekoden skal overdrages fra Borgemesterens afdeling i Aarhus til OS2.
   2. Kontrakten for udvikling og vedligehold skal kunne sendes i offentlig udbud 
   3. Der skal udarbejdes kontrakter som understøtter brug af flere leverandører
2. Produktfællesskabets styringsmodel
   *Overdragelse af beslutningskompetence og forvaltningsansvar*
   1. Der skal etableres en styregruppe
   2. Produktfællesskabet skal have overdraget ansvaret for at identificere og prioritere udviklings og ændringsønsker 
   3. Der skal opbygges samarbejdsfællesskaber for hhv. anvendere, udviklingsleverandører og driftsansvarlige
   4. Der skal indføren en praksis for crowdfunding, strategisk prioritering og tværgående prioritering af kommunespecifikke udviklingsønsker.
3. Praksis for udvikling og dokumentation
   *overgang til OS2 best practice for vedligehold og dokumentation*
   1. Der skal etableres formelle godkendelses og review processer,  i henhold til gældende praksis for Open Source udvikling ( bla. separation og duity)
   2. Der skal etableres et  core-team med ansvar for at kvalitetssikre kildekode og dokumentation
   3. Der skal indføres en praksis for håndtering af frivillige kodebidrag fra anvendere og driftsleverandører
   4. Der skal ryddes op i github og indføres standardiserede rolle og ansvarsmodeller.
4. Produktmodning og videreudvikling
   *overdragelse af kildekode, IPR og produkt ansvar, samt justering af udviklingspraksis*
   1. Ansvaret for at godkende, prioritere, planlægge og igangsætte udviklings aktiviteter skal overdrages til koordinationsgruppen.
   2. Der skal aftaler en reprioritering af igangværende udviklingsinitiativer
   3. Den nyeste version af kildekoden skal gøres implementations uafhængig 
   4. Der skal udarbejdes automatiserede implementations scripts for hele løsningen

```mermaid
gantt
    dateFormat  YYYY-MM-DD
    title       OS2display Roadmap revision af firvaltningsmodellen
    excludes    weekends
    tickInterval 1quarter
    %% (`excludes` accepts specific dates in YYYY-MM-DD format, days of the week ("sunday") or "weekends", but not the word "weekdays".)


    section  Kontrakt og ejerskab 
    Overdragelses aftale underskrevet        :crit, milestone, a1,2026-02-01, 0d
    Juridisk ejerskab overdraget             :crit, milestone, a1,2026-04-01, 0d
    Vedligeholdelses aftale indgået          :crit, milestone, a1,2026-04-01, 0d
    Udviklingsaftaler på plads               :crit, milestone, a1,2026-05-01, 0d
    Kontraktmodel revideret                  :crit, milestone, a1,2027-01-01, 0d
    Start                                    : vert, v1, 2025-06-01,

    section Produktforvaltning
     Styregruppe etableret                   :crit, milestone, a1,2026-02-01, 0d
     Produktansvar overdraget til koordinationsgruppen :crit, milestone, a1,2026-01-01, 0d
     Erfagrupper for leverandører og anvendere aktiveret :crit, milestone, a1,2026-05-01, 0d
     Crowfundingsmodel formaliseret          : crit, milestone, a1,2026-08-01, 0d
     Årsskifte 25/26                         : vert, v2, 2026-01-01,
    
    section  Udviklings praksis
    Brugerdokumentation v 1 klar             :crit, milestone, a1,2026-04-01, 0d
    Implementerings dokumentation v 1        :crit, milestone, a1,2026-04-01, 0d
    Model for udviklings bidrag formaliseret (Code contribution)         : crit, milestone, a1,2026-08-01, 0d
    Github praksis satandardiseret          : crit, milestone, a1,2026-06-01, 0d
    Årsskifte 26/27                         : vert, v3, 2027-01-01,

    section  Produktudvikling
    Godkendelses processer revideret        :crit, milestone, a1,2026-04-01, 0d
    Plan for prioriterede udviklingsønsker - før overdragelse aftalt :crit, milestone, a1,2026-04-01, 0d
    Plan for prioriterede udviklingsønsker - efter overdragelse aftalt :crit, milestone, a1,2026-04-01, 0d
    Produktstrategi for 2027-28 klar :crit, milestone, a1,2026-08-01, 0d 
    Slut                                            : vert, v4, 2027-04-01,

```