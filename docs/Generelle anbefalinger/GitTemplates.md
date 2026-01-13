---
layout: default
title: "Git understøttet produktforvaltning"
author: "Anna-Lis Berg"
date: "19-12-2025"
status: "final" 
parent: "Generelle anvisninger"
nav_order: 15
has_children: true
---
# Git understøttet produktforvaltning

Man skaber både transperans og sporbarhed i produktforvaltningen, hvis man:
1. Flytter diskusioner og beslutninger ud af mails og mødereferater og ind i git Issues. 
2. Anvender labels til Kategorisering af bla Issue type og Issue status
3. Linker issues pullrequests, commit beskeder og releasenotes sammen

En sådan ændring vil medføre at man blandt andet:
1. Indberetter ændringsønsker, fejl og mangler i Git Issues
2. Dokumenterer Arktieturprincipper og strategiske beslutninger i Gis issues
3. Dokumenterer risici og risici håndtering i git issues
4. Anvender kommentarfunktionen i Git til afklaring og diskussion

Skiftet fra mails og mødereferater til Git kan imidlertid føles som en relativ stor  forandring for produkt anvendere, koordinationsgruppe og styregruppe.

De mest kritiske problemstillinger i forbindelse med en sådan forandring er flg:
- Git er et teknisk værktøj med en fast syntaks som det kan være svært for anvendere og beslutningstagere at anvende
- Git's standard sprog er engelsk, men OS2's Anvendere og beslutningstagere foretrækker at kommunikere på dansk
- Ændringsønsker fra anvendere skal evalueres, prioriteres og udbygges inden de kan estimeres, prioriteres, bestilles og igangsættes
  - konverteres til løsningsbeskrivelser og splittes op i delleverancer
  - udbygges med både usecases og accept kriterier
  - udbygges med nonfunktionelle krav, kvalitetskrav og testcases
- Ændringsønsker fra anvendere medføre ofte ændringer i flere forskellige dele af produktet,  
- Ændringsønsker fra anvendere går ofte på tværs af flere kode repositories


Det anbefales derfor at man i forbindelse med overgangen til git understøttet produktforvaltning også etablere flg:
- et git baseret **dokumentationssite** hvor man blandt andet udstiller 
  - ændringsønsker og releaseplaner
  - arkitekturprincipper og produktstrateger
  - samarbejdsprocesser og udviklingspraksis
  - brugervejledninger og implementationsbeskrivelser
  - produktbeskrivelser og teknisk domumentation
- et strategisk **produktforvaltningsrepository** hvor 
  - strategier og mål diskuteres og beslutninger dokumenteres
  - Beslutninger og risici diskuteres og dokumenteres 
  - Ændringsønsker evalueres, raffineres og proioriteres inden 

Derudover er det vigtigt at implementere 
- standard templates til både anvendere, udvikler og beslutningstagere
- generiske labels til sortering af Issues 
- ensartedede, standadiserede og enkle processflow 
- automatiserede processer for publisering af materiale   

## Økosystemet omkring Git understøttet Produktforvaltning

Økosystemet omkiringden git udnderstøttede produktforvaltning består af

1. en Git organisation for produktet
2. en adgangsgivende gruppering af organisationens medlemmer
3. et produktforvaltnings repository
4. et Dokumentations repository der automatisk renderes op på git pages ( eller lignende)
5. en rælkke tekniske repositories 

```mermaid
C4Context
    
     Boundary(b0, "OS2 Produktlandskabet", "") {

        Boundary(b1, "Produkt Anvendelse", "") {
        Person_Ext(personA, "Anvendere")
        Person_Ext(personB, "Driftsleverandører")
         } 
       
       Boundary(b3, "OS2 Produkt forvaltning", "") {
        Person(PersonC, "Product Owner")
        Person(PersonD, "Produkt koordinator")
        Person(gruppeA, "Koordinationsgruppe")
        Person(gruppeB, "Styregruppen")
        Person(gruppeC, "Faggruppe")
    
         }
  
        Boundary(b2, "Produkt udvikling", "") {
        Person(gruppeG, "Core team")
        Person(GruppeE, "Vedligehold")
        Person(gruppeD, "Udvikling")
        Person(gruppeF, "Bidragsyder")
        Person(GruppeH, "Testgruppe")
        Person(GruppeJ, "Teknisk referencegruppe")
        
         }  
        Boundary(b4, "Git Repositories", "") {
        Boundary(b5, "Organisatoriske Git Repositories", "") {
        System(SystemA, "Produktforvaltning")
        System(SystemB, "Produktdokumentation")
        
         }
       Boundary(b6, "Tekniske Git Repositories", "") {
        System(SystemC, "Core 1")
        System(SystemD, "Core 2")
        System(SystemF, "Core N")
    
        System(SystemG, "Contribution 1")
        System(SystemH, "Contribution 2")
        System(SystemI, "Contribution 3")
        System(SystemJ, "Contribution N")
         }
    }
        
      }
 ```     

