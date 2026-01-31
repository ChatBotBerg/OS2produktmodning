---
layout: default
title: "Indberetning, evaluering og prioritering af ændringsønsker"
author: "Anna-Lis Berg"
date: "19-12-2025"
status: "final" 
parent: "Git understøttet processer"
nav_order: 1
has_children: true
---
📆 _sidst opdateret: {{ site.time | date: '%B %d, %Y' }}_

# Indberetning, evaluering og prioritering af ændringsønsker

I forbindelse med håndtrering af ændringsønsker er det vigtigt at processen understøtter et bredt inflow af ønsker, samt at lægge op til at det er anvendernes driftsleverandører der indberette Produktspecifikke fejl, mangler og ændringsønsker på vegne af deres kunder.

Produktets koordinator, Product owner og Koordinationsgrupppe er alle ansvarlige for at sikre at ændringsønsker registreres, evalueres og prioriteres i git issues

Ændringshåndteringen foregår i det produktforvaltningsrepositories

- Når ændringsanmodniingen er registreret i git får den status modtaget
- Når ændringsanmodningen er gennemgået af koordinationsudvalget får den enten status af at være afvist under evaluering (i travle perioder kan status på hold også anvendes)
- Når ændringsanmodningen er udbygget med prioriterede usecases, accept kriterier, nonfunktionelle krav, kvalitetskrav får den status accepteret
- Herefter påbegyndes løsningsbeskrivelsen og opdeling i del leverancer 
- Når opgavens delelementer er færdig beskrevet, estimeret af en leverandør og bestilt af koordinationsudvalget får den status bestilt
- herefter følger status de gense status regler for udviklingsprojekter (påbegyndt)

- Hvis der ikke er midler til at dække det pågældende arbejde anvendes labelen crowdfunding needed



```mermaid
C4Context
     
           Boundary(b0, "", "") {

        Boundary(b1, "Produkt anvenderer", "") {
        Person_Ext(personA, "Lokal systemejer", "Systemejer i en anvender kommune")
        }

        Boundary(b2, "Mailsystem", "") {
        SystemQueue(SystemA, "Produktnavn@os2.eu", "Produktets fællesmail")
         }

        Boundary(b3, "Produkt anvenerer", "") {
        Person_Ext(personB, "Lokal driftsleverandør", "driftsleverandør til en anvenderkommune")
         }

        Boundary(b4, "Produkt ansvarlige", "") {
        Person(gruppeA, "OS2 produktforvaltere", "Produkt koordinator & Product Owner")
        Person(gruppeB, "Produkt ansvarlige", "Koordinationsgrupe med ansvar for prioritering af udviklingsønsker")

         }

        Boundary(b5, "Forvaltnings repository", "Strategisk og administrativt repository/ Dansk") {
        SystemQueue(SystemB, "Ændringsønske", "##Epic Github issue i standardiseret format på dansk der beskriver ændringen")
        SystemQueue(SystemD, "Løsningsbeskrivelse", "#FEATURE Git Issue i standardiseret format på dansk der hvordan man kunne løse opgaven")
        SystemQueue(SystemF, "Brugsscenarier", "#Usecase Git issue der Beskrivelse af de brugsscenarier der ønskes understøttet")
        SystemQueue(SystemG, "Testcases", "#CHOIR Git issue der neskriver hvordan man tester den pågøldende løsning")
          }
        
        Boundary(b6, "Produkt repositories", "Repositories der indeholder produktete kildekode / Engelsk") {
        System(SystemH, "Opgave element 1", "#TASK Github issue i standardiseret format på engelsk")
        System(SystemI, "Opgave element 2", "#TASK Github issue i standardiseret format på engelsk")
        System(SystemJ, "Opgave element 3", "#TASK Github issue i standardiseret format på engelsk")


          }
        BiRel(personA, SystemA, "Henvendelse via mail")
        BiRel(personB, SystemB, "Oprettelse af Ændringsønske")
        BiRel(gruppeA, SystemB, "Oprettelse af Ændringsønske")
        BiRel(gruppeB, SystemB, "Diskussion og prioritering af Ændringsønske")
        


        Rel(SystemA, gruppeA, "Videresender e-mails")
        Rel(SystemA, gruppeB, "Videresender e-mails")
        Rel(SystemB, SystemD, "Specifikation af løsningen")
        Rel(SystemD, SystemF, "prioriterede brugsscenarier")
        Rel(SystemD, SystemG, "Udledte Testscenarier")
        Rel(SystemD, SystemH, "Specifikation af opgave element")
        Rel(SystemD, SystemI, "Specifikation af opgave element")
        Rel(SystemD, SystemJ, "Specifikation af opgave element")

        UpdateRelStyle(personA, SystemA, $textColor="blue", $lineColor="blue", $offsetX="8")
        UpdateRelStyle(personB, SystemB, $textColor="blue", $lineColor="blue", $offsetX="8")
        UpdateRelStyle(SystemA, gruppeB, $textColor="blue", $lineColor="blue", $offsetX="8")
        UpdateRelStyle(SystemA, gruppeA, $textColor="blue", $lineColor="blue", $offsetX="8")
        UpdateRelStyle(gruppeB, SystemB, $textColor="red", $lineColor="red", $offsetX="8")
        UpdateRelStyle(personB, SystemB, $textColor="red", $lineColor="red", $offsetX="8")
        UpdateRelStyle(gruppeA, SystemB, $textColor="red", $lineColor="red", $offsetX="8")
        UpdateRelStyle(SystemB, SystemD, $textColor="red", $lineColor="red", $offsetX="8")
        UpdateRelStyle(SystemD, SystemF, $textColor="red", $lineColor="red", $offsetX="8")
        UpdateRelStyle(SystemD, SystemG, $textColor="red", $lineColor="red", $offsetX="8")
        UpdateRelStyle(SystemD, SystemH, $textColor="red", $lineColor="red", $offsetX="8")
        UpdateRelStyle(SystemD, SystemI, $textColor="red", $lineColor="red", $offsetX="8")
        UpdateRelStyle(SystemD, SystemJ, $textColor="red", $lineColor="red", $offsetX="8")

      }
 ```     