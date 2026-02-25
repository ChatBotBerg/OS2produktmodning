---
layout: default
title: "UDKAST: Krav til OS2BorgerPC 3"
author: "Agnete Moos"
date: "01-02-2025"
status: "Udkast" 
parent: "OS2borgerPc V3"
nav_order: 4
has_children: false
---

## UDKAST: Krav til OS2BorgerPC 3

{:toc}

#### Interessenter
- Bruger: Borger, der bruger en BorgerPC til digital selvbetjening, print mv.
- Superbruger: Medarbejder i en kommune, der installerer nye BorgerPC'er, overvåger driftsstatus på BorgerPC'er, definerer konfigurationsprofiler, løser mindre driftsproblemer.
- Beslutningstager: Herfra kommer typisk krav om energisparefunktionalitet, genbrug af hardware, sikkerhedskrav mv.

#### Miljø
- BorgerPC'er står i åbne offentlige rum, hvor der ikke er personale til stede.
- Brugeren har sjældent adgang til hjælp i forhold til betjening af maskinen.
- Der er ingen teknisk personale til stede på lokaliteten. Tekniske problemer, der kræver fysisk adgang til maskinen, kan være vanskelige at få løst.
- BorgerPC'erne står på stærkt sikrede netværk, hvor der kun er adgang til udadgående kommunikation på port 80 og 443. Det kan også være begrænset, hvilke domæner, der kan kommunikeres med.
- BorgerPC'erne kan i perioder være slukkede. Det skal systemet tage højde for i forhold til softwareopdateringer og andet.

#### Hardware
Behovet for hardwarekompatibilitet for BorgerPC'er går i to retninger:
- Nogle kommuner indkøber billige små computere til formålet. Det har historisk været Intel NUCs, men på det seneste er Raspberry Pi's blevet populære. Det kræver, at både x86- og ARM-arkitektur understøttes.
- Andre kommuner prioriterer genbrug af hardware. Typisk genbruges PC'er fra administrationen som BorgerPC'er.



## 1. Privacy og datasikkerhed for brugeren af en BorgerPC
**Baggrund**: Når brugere benytter BorgerPC'er til digital selvbetjening, indtaster de fortrolige oplysninger som CPR-numre, brugernavne og adgangskoder og tilgår private data og dokumenter. Det er afgørende vigtigt, at alle spor efter deres brugersession slettes automatisk fra computeren, når de forlader den, så private data ikke kompromitteres.

Ikke alle brugere er opmærksomme på at værne om egen datasikkerhed. De kan finde på at forlade en computer, mens de stadig er logget ind i digitale platforme.

Hacking er også en problemstilling, der skal indtænkes. Der har været eksempler på hacking af PC'er på biblioteker via USB-keyloggere. Systemet skal designes med henblik på, at der er ondsindede personer, der aktivt leder efter sikkerhedshuller, som de kan udnytte til at skaffe sig adgang til private data fra andre brugere.

### 1.1 PC, der altid er sikkerhedsopdateret
**Krav**: BorgerPC'en skal automatisk hente og installere sikkerhedsopdateringer til operativsystem og applikationer.

### 1.2 Oprydningsfunktion ved ny brugersession
**Krav**: Der skal være en automatisk oprydningsrutine, der sletter alle brugerens data, når en bruger er færdig med computeren.
- Oprydningsrutinen må ikke kunne manipuleres ved at tage strømmen til computeren eller på anden måde gribe ind i log ud og ind.
- Oprydningsproceduren skal tage højde for, at spor af en brugersession også ligger uden for brugerens hjemmemappe, som i /tmp/, /var/tmp/ og /var/spool/cron/. Samt evt. personfølsomme oplysninger i systemlogs.
- Det bør overvejes, om det udgør en sikkerhedsrisiko at genbruge det samme brugerid i hver ny brugersession.

### 1.3 Automatisk log ud, hvis computeren forlades
Det sker desværre, at brugere går fra PC'en uden at logge ud. Dermed får den næste bruger af computeren adgang til den første brugers private data. Det kan f.eks. være cachede logins til email-konti eller lignende. Problemet kan ikke fjernes helt, men minimeres ved, at computeren automatisk logger brugeren ud efter en periode med inaktivitet.

**Krav**: Efter en konfigurerbar periode med inaktivitet skal der automatisk logges ud. Log ud skal varsles til brugeren gennem f.eks. et pop-up-vindue, hvor brugeren kan nå at stoppe log ud-proceduren ved indgriben, f.eks. ved klik på en knap.

### 1.4 Forebyggelse af hacking via USB-keyloggere
I flere kommuner har der været eksempler på hacking via USB-keyloggere. USB-indgange på PC'erne udgør derfor en særlig sikkerhedsrisiko, som skal håndteres.

**Krav**: Der skal udvikles en løsning for, hvordan hacking via USB-loggere kan forebygges.



## 2. Brugervenlighed i desktop

**Baggrund**: BorgerPC'er bruges af helt almindelige mennesker med gennemsnitlige eller svage IT-færdigheder. Der er kun sjældent adgang til hjælp eller rådgivning fra personale. Brugeroplevelsen skal derfor konstrueres, så den er overskuelig, selvforklarende og intuitiv.

### 2.1 Computeren skal stå med tændt skærm
En tændt skærm viser brugeren, at PC'en er klar til brug. En sort skærm tolkes af brugere som, at den ikke er i drift eller i stykker.

**Krav**: Automatisk dvale ved inaktivitet skal deaktiveres. (modsatrettet krav findes under de strømesparende funktioner - kommuner prioriterer ikke ens)

### 2.2 Computeren skal være sat op til automatisk indlogning som borger-bruger
**Krav**: Når PC'en tænder/efter log out skal der automatisk logges ind i en ny borger-bruger-session. Der skal ikke tastes passwords eller brugernavne for at komme ind i systemet.

### 2.3 NumLock skal være aktiveret
Det forvirrer brugere og giver anledning til henvendelser, hvis det nummeriske tastatur ikke virker.
**Krav**: NumLock skal være aktiv.

### 2.4 Fjerne menupunkter vedr. power off, sleep mode, lock og change user fra systemmenuen
Brugere skal afslutte deres session ved at logge af – ikke ved power off eller sleep mode. Power off og visse sleep modes sætter PC'en i en ubrugelig tilstand, som kræver, at personale får fysisk adgang til PC'en og genstarter den. Lock og change user er heller ikke relevante. Det kan brugere ikke forventes at kunne regne ud.

**Krav**: Fjern menupunkter vedr. power off, sleep, lock og change user.

### 2.5 Menubjælke, der synliggør tilgængelige applikationer
**Krav**: Brugerens desktop skal have en menubjælke, der altid er synlig. Den viser brugeren, hvilke applikationer de har adgang til. Brugerne kan ikke finde ud af at fremsøge applikationer gennem søgefelter eller diskrete små menuknapper. Det skal være konfigurerbart, hvilke applikationer, der skal være genveje til fra menuen. Der bør altid ligge et genvejsikon til Log out.

### 2.6 Genveje på skrivebord
**Krav**: Det skal være muligt at oprette genveje på skrivebordet i brugerens desktop. Det kan være genveje til filer, mapper, URL'er og applikationer.

### 2.7 Synliggør tilgængelighedsfunktioner
**Krav**: Tilgængelighedsfunktioner (hjælp til handicappede) skal være synlige i GUI, evt. som ikon i systemmenuen.

### 2.8 Skjul systembeskeder
**Krav**: Systembeskeder fra operativsystemet omkring opdateringer og lignende skal undertrykkes. De gør brugerne utrygge og forvirrede.



## 3. Systemadministration af BorgerPC'er ude i kommunerne
**Baggrund**: Det er superbrugere i hver kommune, der installerer BorgerPC-systemet på computerne. Superbrugere definerer også lokale konfigurationsprofiler, så f.eks. wifi-opsætning, print-konfiguration og browser-startside passer til de lokale forhold. De laver driftsovervågning og griber ind, hvis maskiner går offline eller på anden måde fejler.

I større kommuner er ansvaret for BorgerPC-flåden delegeret til forskellige superbrugere. En gruppe superbrugere har f.eks. ansvaret for bibliotekernes PC'er, mens en anden servicerer jobcenter og borgerservice. Af den grund er der brug for opdeling af flåden under adskilte tenants. Af hensyn til IT-sikkerheden skal superbruger kun have rettigheder til at administrere de maskiner, der hører under den tenant, som de er tilknyttet.

### 3.1 Installation af ny BorgerPC
Installation af en ny BorgerPC skal være nem og hurtig. I forhold til en standard Linux-installationswizard bør flere trin kunne prækonfigureres, så de springes over.

### 3.2 System til fleet overview under adskilte tenants
Superbrugere har brug for en grafisk brugergrænseflade, der giver dem et overblik over status på de computere, som de har driftsansvar for.

Pr. tenant skal der vises:
- Oversigt over alle PC'er i flåden
- Hurtigt overblik over maskiner, der er offline
- Overblik over konfigurationsgrupper og hvilke PC'er, der er medlem i dem

I detaljer for en PC skal vises:
- Hvilke konfigurationsgrupper en PC er med i
- Driftsstatus (online/offline)
- Opdateringsstatus
- PC's MAC-adresse

### 3.3 System til management af konfigurationsprofiler under adskilte tenants
**Baggrund**: Superbrugere skal, evt. med hjælp fra driftsleverandør, kunne opbygge konfigurationsprofiler for grupper af PC'er under deres tenant.

Eksempler på typisk konfiguration er wifi-opsætning, browserens startside, installation af printer og valg af standardprinter.

Eksempel 1:
En konfigurationsprofil med navnet "Borgerservice Rådhusgade", der sætter browserens startside til borger.dk, en bestemt Konica Minolta BizHub-printer installeres og sættes som standardprinter, og wifi deaktiveres.

Eksempel 2:
En konfigurationsprofil med navnet "Broager Bibliotek", hvor browserens startside sættes til bibliotekets hjemmeside, print opsættes til Princh-printservice og wifi opsættes, så PC'en automatisk kobler på et bestemt SSID.

### 3.4 Tilknytning af PC til konfigurationsgruppe
Det skal være muligt at knytte en PC til en bestemt konfigurationsprofil via konfigurationsgrupper.

### 3.5 Deployment af konfiguration til PC
- Når en PC knyttes til en konfigurationsgruppe, skal konfigurationsprofilene automatisk rulles ud på PC'en.
- Ændringer i konfigurationsprofilen skal automatisk rulles ud til PC'er i konfigurationsgruppen.
- Er PC'en slukket, skal konfigurationen automatisk rulles på, når PC'en tændes.



## 4. Print og skanning
**Baggrund**: En stor andel af BorgerPC-brugerne kommer for at printe. Det er et meget benyttet tilbud på bibliotekerne.
Følgende skal kunne konfigureres:
- Netværksprinter med/uden angivelse af PPD-fil
- Princh Cloud Printer
- Standardprinter
- Standard printerindstillinger



## 5. Programmer
Borgere har først og fremmest brug for en webbrowser. Derudover er der brug for PDF-læsning og evt. redigering i forhold til at udfylde formularer. Der er også brug for tekstbehandling.

### 5.1 Browsere
BorgerPC'er er for nogle personer deres primære adgang til digital selvbetjening og kontakt. Det er et alvorligt problem, hvis vigtige hjemmesider ikke fungerer i løsningen – herunder formularer, instruktionsvideoer og lign. Rigide principper om at udelukke proprietære formater og teknologier må ikke prioriteres over brugbarhed. Løsningen skal fungere i en uperfekt verden, hvor kritisk vigtige hjemmesider kan være bundet op på proprietær teknologi. Hvis ideologi prioriteres over funktion, tager vi samfundets svageste borgere og frontpersonalet i kommunerne som gidsel i en...

Det kan være en fordel at have to forskellige browsere, hvis der er en hjemmeside, der ikke virker i den ene, så kan man prøve med den anden.

### 5.2 LibreOffice
LibreOffice fungerer fint til tekstbehandling. Tip of the day skal deaktiveres. Microsoft-dokumentformater skal være understøttet.



## 6. Strømbesparende funktioner og genbrug af hardware
I mange kommuner er der stort fokus på den grønne dagsorden i forhold til genbrug og energibesparelser. Computerskærme, der står unødig tændt i offentlige institutioner, kan fremprovokere stærke reaktioner fra både borgere og politikere og bør undgås.

### 6.1 Planlagt dvale-funktionalitet
Beslutningstagere ønsker ikke skærme, der står tændt om natten. Det sender et uheldigt signal om ressourcespild og miljøsvineri. Derfor er der behov for planlagt dvalefunktion. Dvs., at PC'en efter en fast tidsplan dagligt går i dvale eftermiddag/aften og vågner igen, når det bliver morgen. Der er som minimum brug for at kunne differentiere på hverdage/weekend og tidspunktet for dvale/vågn op.

### 6.2 Dvale ved inaktivitet
Nogle kommuner prioriterer strømbesparelser meget højt. De ønsker, at deres BorgerPC'er skal gå i dvale efter en periode med inaktivitet. Det betyder, at deres BorgerPC'er ofte står med sort skærm, og borgerne skal vække dem ved tryk på tastatur eller mus.

### 6.3 Understøttelse af ældre hardware
Nogle kommuner genbruger ældre administrative PC'er som BorgerPC'er. Det er altid x86-maskiner. Systemet skal kunne fungere på en bred palette af hardware – også af lidt ældre dato.
```
