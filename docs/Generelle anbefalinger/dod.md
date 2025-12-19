---
layout: default
title: "Definition of Done"
author: "Lisbeth Wittendorff Lorentzen"
date: "19-12-2025"
status: "Udkast" 
parent: "Generelle anbefalinger"
nav_order: 1
has_children: false
---

# Definition of Done – OS2iot

**Målrettet leverandør**: Iterator IT ApS

## Udvikling og Dokumentation
- [ ] Funktionalitet er fuldt udviklet og opfylder kravspecifikationen
- [ ] Koden er peer-reviewed og godkendt
- [ ] Teknisk dokumentation er opdateret (API, datamodeller mv.)
- [ ] Ændringer i forretningslogik/datamodel er dokumenteret

## Test og Kvalitetssikring
- [ ] Enhedstest er skrevet og bestået (min. XX % dækningsgrad), anvend GitHub's CI/CD til unit test (?)
- [ ] Automatiseret test og integrationstest er gennemført og bestået
- [ ] Brugertest er udført
- [ ] Acceptkriterier fra user story er opfyldt og testet (der skal ligge beskrivelser for, hvordan der testes)
- [ ] Inputvalidering og fejlscenarier er testet
- [ ] Performance test er udført (hvis relevant for funktionens belastning)
- [ ] Regressionstest (gentest) er udført på berørte områder – dette gennemføres af koordinationsgruppemedlemmer i PROD
- [ ] Sikkerhedstest og persondatahåndtering er valideret

## Lovgivning og Compliance
- [ ] Funktion overholder GDPR-krav – ligger i drift
- [ ] Offentlige it-standarder (fx WCAG 2.1) er overholdt. NIS2
- [ ] Logging og audit trail er implementeret og testet – ligger i drift
- [ ] Retention og sletning af persondata er dokumenteret
  - *Automatisk sletning*

## Deployment & Drift
- [ ] Funktionalitet er deploybar gennem CI/CD pipeline **
- [ ] Rollback-plan er dokumenteret
- [ ] Overvågning/logning er opdateret med nye hændelser/fejl

## Godkendelse og Kommunikation
- [ ] Udvalgte medlemmer af koordinationsgruppen har godkendt funktionaliteten
- [ ] Release notes er opdateret

* "Retention" betyder, hvor længe oplysninger må opbevares i systemet, og hvornår de skal slettes – fx af hensyn til GDPR. Retention-regler er implementeret: Persondata slettes eller arkiveres automatisk efter gældende opbevaringsperiode.

**Er klar til at blive sat i drift.** Funktionaliteten er så færdig og testet, at den kan installeres og aktiveres i den version af systemet, som brugerne har adgang til.
```
