---
layout: default
title: "Git understøttet beslutningsprocesser"
author: "Anna-Lis Berg"
date: "19-12-2025"
status: "final" 
parent: "Git understøttet processer"
nav_order: 1
has_children: true
---
📆 _sidst opdateret: {{ site.time | date: '%B %d, %Y' }}_

# Diskusion og dokumentation af arkitekturprincipper, produktstrategi og samarbejdsmodel

Alle beslutninger vedrørende arkitektur principper, produkt strategier og forvaltningsprincipper foretages, eller ratificeres af produkternes koordinations og styregrupper.

Diskussionerne har traditionelt set foregået bilateralt på møder eller via mails og dokumenteres sjældent på en struktureret måde.

Såfremt diskutionerne udmyntes i en formel beslutning foretaget af produktets styre eller koordinations gruppe dokumenteres dette ofte udelukkende i et mødereferat eller en rundsendt mail.

Denne praksis medførere at såvel beslutningen som beslutningsrationale og beslutningsgrundlage, er skjult for alle andre stakeholdere end dem der sidder i produktets styrende organer.

## Fordele ved Git understøttede beslutningsprocesser

Git understøttede besluntingsprocesser, kan eliminere dette problem helt eller detlvist, alt efter hvordan processerne impelenteres i praksis. 


1. Såfremt et produkt går all ind på anvendelse af GIT ISsues som bærende element i beslutningsprocessen, vil beslutnings loggen ikke alene give et entydigt billede af hvad der er besluttet hvornår, den vil også give produktets interessenter direkte adgang til de rationaler og diskussioner der liggger til grund for beslutningen. 
2. Såfremt diskussioner og aftaler stadig foregår på formelle møder eller via mails, vil der være forbundet en del administrativt overhead på at dokumentere essensen af disse diskusioner i beslutningsloggen. Gevinst potentialet er stadigt ikke ubetydeligt da man stadig har fået etableret både kontekst, historik, overblik og transperans for hele beslutningsprocessen. 
4. Såfremt der ikke kan afsættes de nødvendige ressourcer til at dokiumentere beslutningens rationaler og diskussioner, vil anvendelse af GIT Issues som dokumentationsværktøj stadig skabe både troværdighed, udbredelse og overblik over hvad der er besluttet hvornår.

Ved at flytte beslutningskomumentaion over i Git Issues det bliver det ikke alene letteere at fastholde et overblik over hvad der er besluttet hvornår og af hvem, det bliver også lettere at koble udviklingønsker, dokumentationskravv og acceptkriterier direkte til disse beslutninger. 

# Implementering af Gir understøttede beslutningsprocesser

Implementering af git understøttet beslutningsprocesser, behøver hverken at være udviklingstung eller kompliceret,

Man starter ved at:
1. etablere et forvaltnings repository i produktorganisationen 
2. Uddeleger ansvar for vedligehold af dette repository til produktets daglige ledelse (PProdukt koordinator, Product Owner. Produkt Administrator, community mangger eller lignende)
3. Oprette et Forvaltningsteam i organisationen
4. Invitere alle styre- og koordinationsgruppemedlemmerne, samt produktets daglige ledelse ind i dette team
5. Implementere en standardiseret Issue template ( se eksempel) 
6. etablere de labels  der er nødvendige for at sikre at man kan fremfinde de nødvendige beslutninger. 