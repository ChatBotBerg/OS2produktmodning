---
layout: default
title: "Open-Source Healthanalyzer"
author: "Anna-Lis Berg"
date: "19-09-2025"
status: "Udkast" 
parent: "Produktspecifikke anvisninger"
nav_order: 4
has_children: true
---

# "Open-Source Healthanalyzer"

Herunder findes en række anbefalinger til hvordan man organisere  og orkestrerer etableringen en open-source helath analyzer på en effektiv, iterativ og målrettet måde.

**Formålet** er at etablere et genbrugeligt værktøj der måler open-source produkters modehed på en kvantitativ, effektiv og indiskutabel måde.

**Visionen** er at etablere et værktøj der kan bruges på tværs at det danske Open-Source Økosystem til at evaluere og udstille kvalitet og udbredelse af danske Open-Source produkter.

- **Evalueringskriteriterierne** tager udgangspunkt i de klassiske betingelser for at kategorisere software som open-source.
  
- **Målingerne** skal være baseret på automatiseret dataindsamling og kvalitetsbærende metrikker
- **Processen** er bygget op omkring open-source metodik og praksis

## Hvorfor skal vi have en Health Analyzer og hvad skal den bruges til 

Ideen til at implementere Open-Source Healthanalyser udspringer af flg:

Behovet for let at kunne evalueret:
- produktfællesskabets aktivitetsniveau og engagement
- produktudviklingsprocessens stabilitet, sikkerhed og transperans
- kildekodens aktualitet kvalitet og compliance
- produktets anvendelse af open-source standarder og bestpraksis. 

Tidligere erfaringer med selvevalueringeringer og ekspertvurderinger så som:
- de er tidskrævende og omkostningstunge
- de er udtryk for et øjebliksbillede
- de kan ikke eftervises kvantitativt
- de er ikke nødvendigvis hverken upartiske og absolut retvisende

Ønsket og at få værktøj der kontinuerligt kan bruges til at vurdere "helbredstilstanden" på:
- OS2's produkt portefølje
- Open-source produkter som anvendes i dansk offentlig sektor
- Open-source upstream komponenter som kunne være af interesse for den danske offentlige sektor

## Arkitektur, løsningsdesign og software komponenter

 principper, arkitektur og gevinstpotentiale bag healthanaluzeren firnder du her: 
[https://janhalen.github.io/enterprise-architecture-patterns/proposals/2025-10-02-health-analyzer.html](https://janhalen.github.io/enterprise-architecture-patterns/proposals/2025-10-02-health-analyzer.html)-


## Forløb og faser

Det anbefales at dele etableringsforløbet op i flg faser: 
1. Afklaring, afprøvning og afgrænsning 
2. Etablering af en referencearkitektur
3. Implementering af "det gode eksempel" / (fyrtårns implementering)"
4. Etablering og udbredelse af en af en skalerbar og produktionsklar løsning

![Visionen for forløbet](Assets\images\Skærmbillede 2026-01-15 132215.png)
