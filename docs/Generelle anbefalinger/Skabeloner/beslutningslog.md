---
layout: default
title: "Git template- beslutningslog"
author: "Anna-Lis Berg"
date: "31-01-2026"
status: "Final" 
parent: "Referat skabelon"
nav_order: 9
has_children: false
---

#Git template- beslutningslog"

📆 _sidst opdateret: {{ site.time | date: '%B %d, %Y' }}_

---
## Github - standard Issue metadata
name: Beslutningslog
about: Strukturert beskrivelse af en væsentlig beslutning i produktet
title: "[ADR/SDR/ODR][Tittle]"
labels: ''
assignees: ''
---

## Skabelon specifik Metadata:
- Dato: [ÅÅÅÅ-MM-DD]
- Status: [Forslag / Accepteret / Erstattet / Afvist]
- Beslutningstagere: [Beslutningsorgan, Navne  eller roller]
- Beslutningstype :   [Arkitekturbeslutning, Strategisk beslutning eller Operationel beslutning]

## Kontekst/ Årsag
Beskriv her det problem eller det behov, vi står overfor. Hvad er de tekniske, forretningsmæssige eller tidsmæssige faktorer, der tvinger os til at træffe en beslutning nu.
Beslutning
Her beskrives den Beslutning der er taget. Vær specifik omkring, hvad vi gør, og hvordan det implementeres. Inkluder eventuelt hvilke alternativer, der blev fravalgt og hvorfor.

## Konsekvenser
Beskriv hvad denne beslutning betyder fremadrettet (både godt og skidt):
- Positive: (f.eks. hurtigere performance, bedre sikkerhed).
- Negative: (f.eks. øget teknisk gæld, behov for ny viden i teamet).
- Neutral: (f.eks. ændret filstruktur).

## Effektuering
Beskriv hvad der skal til for at effektuere beslutningen når den er truffet, samt hvem der har ansvaret for dette.

## Risici:
Beskiv eventuelle risici forbundet med effektuering af den pågældende beslutning.

## Yderligere information:
- Henvis evt til hvor man kan finde yderligere information, inspiration eller baggrundsmateriale.
- Begrund eventuel afslag eller årsag til at beslutningen endnu ikke er taget.
