---
layout: default
title: "Open Source Healthanalyzer POC 2025"
author: "Anna-Lis Berg"
date: "19-09-2025"
status: "Udkast" 
parent: "Produktspecifikke anvisninger"
nav_order: 5
has_children: false
---
---

📆 _sidst opdateret: {{ site.time | date: '%B %d, %Y' }}_

# Open Source Healthanalyzer POC 2025

Arbejdsgruppen bag KL-rapporten om de 10 mest genbrugelige open-source løsninger i den danske offentlige sektor har behov for at effektivisere og objektivisere indsamling og vurdering af datagrundlaget, samt for at kunne reproducere målingerne på en ensartet, gennemsigtig og effektiv måde.

Denne skrivelse beskriver, hvordan en open-source Healthanalyzer kan bidrage til at imødekomme disse behov og understøtte en datadrevet beslutningsproces.

# Hvad der formålet med en Open-Source Healthanalyzer

Formålet med en open-source Healthanalyzer er at skabe et objektivt og kvantificerbart datagrundlag til identificering og vurdering af open-source løsninger i den offentlige sektor. 
Ved anvendelse af automatiserede og standardiserede målinger opnås hurtig, konsekvent og pålidelig evaluering af løsningernes modenhed, åbenhed og skalerbarhed. 
Dette sikrer høj datakvalitet, øget troværdighed og effektivitet i vurderingsprocessen, samtidig med at det understøtter overholdelse af open-source-principper og compliance.

1. **Objektiv evaluering:** Med en Healthanalyzer kan man kvantitativt vurdere open-source produkters modenhed i en struktureret, målbar og objektiv proces, hvilket reducerer subjektiviteten ved traditionelle selvevalueringer og ekspertvurderinger.
2. **Effektiv ressourceudnyttelse**: Tidligere erfaringer har vist, at manuel evaluering kan være tidskrævende og ressourcekrævende. En automatiseret løsning kan give indsigt i realtid med mindre ressourceforbrug.
3. **Strategisk værktøj:** Healthanalyzeren vil med tiden kunne fungere som et strategisk værktøj for danske kommuner og offentlige myndigheder til kontinuerligt at vurdere og optimere brugen af open-source løsninger.

# Hvad der formålet med en  Proof of concept (POC)
En POC (Proof of Concept) har som overordnet formål at demonstrere, at en idé, teori eller teknologi er gennemførlig og kan fungere i praksis. Det bruges ofte til at teste centrale funktionaliteter, validere konceptet og afgøre, om det er værd at udvikle videre på. En POC hjælper med at identificere potentielle problemer tidligt og kan understøtte beslutningen om videre investering i projektet.

Formålet med at anvende en POC på Healthanalyzeren til at skabe datagrundlaget for KL rapporten over 10 genbrugelige løsninger, er at udnytte det akutte behov for dataindsalming til at vurdere healthanalyzerens potentiale som datafeed for etablering af et nationalt katalog over Open-source løsningers, modenhed og genanvendelighed.


## Metode for at implementere en POC
1. **Iterativ og trinvis proces**: Start med et Hackathon for at etablere grundlaget og derefter en POC for midlertidige evalueringer. Dette sikrer, at man hurtigt kan justere kursen baseret på indledende resultater.
2. **Involvering af interessenter**: Inkluder både tekniske eksperter, kommunale repræsentanter og open-source miljøet for at sikre, at løsningen er brugbar og bredt accepteret.
3. **Kosteffektivitet**: Organisering af POC og tilhørende workshops såsom Snakathon kan gennemføres med et klart budget, som fokuserer på omkostningseffektive metoder som Micro-Hackathons og europæisk baserede hostingløsninger.
4. **Dokumentation og læring**: Under processen dokumenteres erfaringerne grundigt, hvilket hjælper med fremtidig beslutningstagning og sikrer, at læring fra POC'en kan anvendes til udviklingen af en mere moden løsning (MVP).

Der er 3 aktiviteter i den forelsåede POC, som til sammen har til formål at skabe grundlaget for at vurdere hvorvidt den afprøvede løsning har potentiale nok til at man ønsker at gå videre med aftestningen. 

***De 3 aktiviteret er :***
1. ***Hackaton*** : en udviklings workshhop hvor man får skabt fungerende arkiktektur, workflow og grænseflade for at kunne hente og præsentere målinger (data)
2. ***POC*** : resultatet af Hackaton'net spundet op i et midlertidigt miljø der kan danne grundlag for den videre ide-generering
3. ***Snakaton***: en afklarings workshop hvor man får defineret og raffineret de metrikker der skal måles på, og de rapporter og dashboards der skal stilles til rådighed under MVP'en

***Når disse tre aktiviteter er gennemført har man flg:***
1. Data feed til KL rapporten
2. Anbefalingeer til hvilke metrikker man med fordel vil kunne anvende til fremtifdige evalutering af Open-Source løsninger
4. anbefaling til eventuelle ændringer og/eller udvidelser af Health analyzeren
7. Scope for en evt MVP implementering af Health analyzeren

***Disclaimer:*** 

Det er vigtigt at påpege at resultatet af POC'en udelukkende er et datasæt og en række erfaringer.
POC'en er en slags laboratorietest som foregår i et afgrænset miljø (en sandkasse). 
Løsningen er hverken driftsklar eller skalerbar, der opereres med et afgrænset antal metrikker og der er hverken fokus på brugervenlighed eller fleksibel adgangsstyring.

Når POC'en er vel overstået og resultatet er efterbehandlet står KL derfor stadigt overfor arbejdet med manuelt at skabe raporten ud fra det tilvejebrgate datagrundlag, samt med at planlægge hvordan man eventuelt kommer videre i arbejdet med at etablere en blivende version af Helathanalyzeren.

Derudover står arbejdsgruppen overfor udfordringen med at skaffe opbakning omkring og midler til næste fase, MVP en hvor man implementerer en minimums løsning i et skalerbart og fremtidssikret driftsmiljø (MVP) og etablere en midlertidig forvaltningsorganisation, for derigennem at vurdere de juridiske, organisatoriske og økonomiske aspekter af en fremtidig driftssituation. MVP'en har således tol formål at vurdere løsningens realiserbarhed som reelt produkt i forhold til omkostningsniveau, drift og forvaltning, og vilkan først kunne estimeres i omfang og scope efter endt POC. 

## Prisen for en PO
Den samlede pris for afvikling af et PO forløb som både skaber engagement , involvering og håndgribeligt resultat  ligger på mellem 150.000 og 200.000 kr alt efter omfang og afregningsmodel for de deltagende leverandører.

**Den mest kosteffektive model** ville være et ***Micro Hackaton*** hvor man hyrer 2 tekniske ressourcer til at deltage sammen med arbejdsgruppen i e 2 dages workshop i KL's lokaler, afvikler POC'en i OS2's github miljø og afholder et virhuelt Snakathon som afslutning.
Et sådan arrangement vil koste omkring 80.000 til 100.000. Det vil kunne afvikles hurtigt, men alt kildekode og udviklet funktionalitet vil skulle flyttes over i et digitalt suverænt miljø inden en eventuel MVP vil kunne igangsættes. 

**Den mindst kosteffektive midel** ville være et ***Open-Soutce Hackaton** hvor man inviterer det danske Open-Source miljø ind til en to dages intens weekend hackaton, etablerer en digital suveræn platform til kildekode og POC afvikling og afholder en workshop for strategiske stakeholder som afslutning på processen. 
Et sådan arrangement vil koste omkring 400.000- 500.000. Det vil kræve meget forberedels, massiv markedsføring, dyre lokaler og en kendt keynote speaker. Modellen vil skabe massiv opmørksomhed og engagement i Opensource miljøet men vil ikke kunne gennemføres inden for de tidsmæssige rammer for udarbejdelse af KL rapporten. 

**Den anbefalede Model** er bygget om opmring et ***leverandør hackaton** hvor man beder 3-5 leverandører om at stille med kvalificerede tekniske ressourcer til en 2 dages workshop, etablerer en digital suveræn platform til kildekode og POC afvikling og begrænser den afsluttende snakatonnen til kun at omfatte arbejdsgruppen bag rapporten. 

Dette arrangement vil realistisk set kunne afvikles for mellem 150.000 og 200.000 kr alt efter hvormange leverandører man inviterret og hvilken afregningsmodel man anvender ( Honorar eller timebetaling).

***Hackaton:***
   1. 90.000 - 150.000  kr til Honorar afrgning til Komemrcielle aktører ( ved honorar afregning på 30.000 kr pr leverandør)
   2. 12.000 - 18.000 Kr til transport og accomondation til i forbindelse med POC aftestning ( 4-6 rejsende)
   3. 4.000 - 8.000 KR kr til møde forplejning
***POC***
   4. 15.000 - 25.000 til etablering og 2 måneders drift at et digital suveræn platform til kildekodeforvaltning, hackaton aktiviteter og POC afvikling
   5. 15.000  til tilpasninger under POC

***Snakathon***
   5. 12.000 - 18.000 Kr til transport og accomondation til deltagerne ( 4-6 rejsende)
   6. 2.000 - 3.000 KR kr til møde forplejning
   
  ***NB!*** platforms omkostningen er vurderet ud fra anvendelse af en europæisk løsning leveret Stackhero [https://www.stackhero.io/en-US/services/GitLab/pricing](https://www.stackhero.io/en-US/services/GitLab/pricing)
   Så fremt man ønsker den leveret af en dansk leverandør er det  erfaringen at prisen bliver langt højer.

## efterbehdnling af O

## Konklusion
En POC for en Open-source Health Analyzer er ikke alene vigtig for at opnå indsigt i open-source løsningers anvendelighed og modenhed, men det understøtter også en data-drevet beslutningsproces, som er essentiel for optimering og forbedring af open-source anvendelse i kommunal sammenhæng. Ved at følge en struktureret, iterativ metode kan man sikre, at løsningen er robust, skalerbar og økonomisk bæredygtig.

Da POC'en er en slags laboratorie test vil det kræve an man implementerer en minimums løsning i et skalerbart og fremtidssikret driftsmiljø (MVP) og etablere en midlertidig forvaltningsorganisation, for derigennem at vurdere de juridiske, organisatoriske og økonomiske aspekter af en fremtidig driftssituation.

