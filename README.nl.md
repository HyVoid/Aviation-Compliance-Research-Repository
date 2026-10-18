[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | 🇪🇸 [ Español ](README.sp.md) | [ 🇬🇧 English ](README.md)

# Voorkom schendingen van vlucht- en diensttijden vóór de indienststelling

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)

**Ontworpen voor Canadese exploitanten onder Part 702 en Part 705 die vluchttijd, diensttijd, vermoeidheidsblootstelling en rollende nalevingslimieten moeten volgen voordat een piloot wordt toegewezen.**

[Live voorbeeld](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) | [Koop volledige Excel](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

Volg rollende vluchttijdlimieten, detecteer nalevingsrisico's binnen enkele seconden en behoud één auditeerbare bron van waarheid voor piloot-dienstregistraties.

---

## Snelle voorbeeld

<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 11_47_04 AM" src="https://github.com/user-attachments/assets/cc792931-2477-40d4-9bd7-e92418817c77" />

> Bekijk het interactieve werkmappenvoorbeeld: [piloot-diensttracker-demo](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)

---

## Waarom dit bestaat

De meeste schendingen van vlucht- en diensttijden worden niet veroorzaakt door slechte intenties.

Ze gebeuren meestal omdat rollende vensters, gemengde 702/705-activiteiten, cumulatieve vermoeidheidsregels, hertoegewezen diensten en gefragmenteerde registraties moeilijk handmatig te volgen zijn.

Het risico is simpel:

```text
Pilot assigned
-> Manual check
-> Prior records missed
-> Violation discovered after the flight
```

Deze werkmappen is ontworpen om de workflow te veranderen:

```text
Pilot considered for assignment
-> Duty record entered once
-> Rolling limits checked automatically
-> Compliance risk flagged before dispatch
```

Het commerciële probleem is niet alleen regelgeving. Het is operationeel zicht. Verkeersleiders en planners moeten weten of een piloot de volgende taak legaal en veilig kan aanvoeren voordat de vlucht wordt vrijgegeven.

---

## Drie nalevingsvalkuilen die exploitanten vangen

### Valkuil 1 — Rollende vensters verkeerd gelezen als kalenderperioden

De limieten van 28, 90 en 365 dagen schuiven elke dag vooruit, niet elke maand.
Een piloot die tussen 1 en 28 mei 95 uur vloog en toen op 29 mei 8 uur vloog,
is bij het begin van juni **niet** gereset. Het venster van 1 juni reikt nog terug tot 4 mei.

Planners die limieten mentaal resetten bij maandgrenzen onderschatten routinematig de blootstelling.
Dit is de structureel onzichtbaarste valkuil: het mentale model voelt correct; de berekening is verkeerd.

### Valkuil 2 — Uren niet gepoold over 702 en 705

Wanneer dezelfde piloot maandag een luchtopname uitvoert onder Part 702 en woensdag een passagierscharter
onder Part 705, tellen beide sets uren mee voor dezelfde rollende accumulatielimieten.

Exploitanten die separate trackingbladen bijhouden voor elk subdeel — een natuurlijke workflowverdeling —
onderschatten systematisch. De regeling erkent die operationele grens niet.

### Valkuil 3 — Schendingen ontdekt na de vlucht

Handmatige verificatie gebeurt meestal nadat een diensttoewijzing is uitgegeven, of nadat de vlucht
is vertrokken. Tegen de tijd dat een schending wordt geïdentificeerd, is de overtreding al plaatsgevonden.
Handhaving door Transport Canada geldt terugwerkend.

Onderschepping vóór de vlucht vereist dat de nalevingsstatus zichtbaar is *voordat* een piloot wordt toegewezen —
wat vereist dat alle historische gegevens actueel zijn en alle berekeningen automatisch draaien op
het moment van indienststelling.

Het zit meestal verborgen in de relatie tussen:

- de voor vandaag geplande dienst
- de eerdere dienstgeschiedenis van de piloot
- de meldtijd
- het aantal sectoren
- de accumulatie van vluchttijd
- de vereiste rust
- exploitantspecifieke procedures

Daarom vindt handmatig spreadsheetonderzoek het probleem vaak laat, of mist het volledig.

---

## Voor wie deze tool is

| Gebruiker | Praktische use case |
|---|---|
| Verkeersleiders | Controleer pilootbeschikbaarheid voordat een indienststellingsvergunning wordt uitgegeven |
| Bemanningplanners | Bouw roosters met zicht op resterende legale capaciteit |
| Hoofdpiloten | Beoordeel pilootwerklast en cumulatieve blootstelling voordat toewijzingen worden goedgekeurd |
| Veiligheidsmanagers | Behoud gestructureerde registraties voor interne review en auditvoorbereiding |
| Kleine AOC-exploitanten | Vervang verspreide handmatige tracking door één lichte Excel-workflow |

Het meest geschikt voor Canadese exploitanten met 3–30 piloten die gemengde 702/705-operaties uitvoeren,
waar speciale bemanningsoftware te kostbaar is maar handmatige benaderingen niet meer schalen.

---

## Wat de werkmappen doet

### Registratie van diensttijd
Één gegevensinvoerpunt voor alle piloot-dienstregistraties. Verkeersleiders loggen basisvlucht- en dienstinformatie
eenmaal; berekeningen draaien automatisch op de achtergrond.

### Monitoring van rollende vensters
Automatische berekening van Part 705-accumulatielimieten over alle drie de regelgevingsvensters tegelijk:
- 100 uur in elke 28 opeenvolgende dagen
- 300 uur in elke 90 opeenvolgende dagen
- 1.000 uur in elke 365 opeenvolgende dagen

### Nalevingsstatus vóór indienststelling
De nalevingsstatus van elke piloot is zichtbaar voordat de toewijzing wordt uitgegeven.
Geen handmatige kruisverwijzing. Geen ontdekking na de vlucht.

### FDP-matrixvalidatie
De Flight Duty Period-limieten van Part 705 — een tweevariabele matrix van meldtijd × aantal sectoren —
zijn vooraf gecodeerd. Het legale FDP-maximum werkt automatisch bij op basis van wanneer de piloot zich meldt
en hoeveel sectoren zijn gepland.

### Auditklare rapportage
Elke invoer is vanaf dag één gestructureerd en traceerbaar. Historische nalevingsregistraties kunnen worden
gefilterd op piloot, datumbereik of status en geëxporteerd zonder nabewerking.

---

## Voorbeeldscenario

**Exploitantprofiel:** 12 piloten. Gemengde operaties onder Part 702 en Part 705. Één verkeersleiderskantoor.

**Het probleem:** Elke ochtend besteedt de verkeersleider 90 minuten aan het handmatig verifiëren van rollende
dienstlimieten voordat de vluchten van de dag worden toegewezen. Vluchturen worden bijgehouden in twee
gescheiden spreadsheets — één voor 702-operaties, één voor 705. Wanneer een piloot onder beide subdelen
in dezelfde week vliegt, worden gepoold totalen met de hand geconsolideerd.

Gedurende drie maanden operaties werden twee limietoverschrijdingen ontdekt — beide nadat de vlucht
al was vertrokken.

| | Voor | Na |
|---|---|---|
| Registratestructuur | Twee gescheiden bladen, één per subdeel | Één uniforme werkmappen |
| Ochtendcontroletijd | ~90 min over alle piloten | Onder 3 seconden per piloot |
| 702/705-urenpooling | Handmatige consolidatie | Automatisch over beide subdelen |
| Ontdekking van schendingen | Na de vlucht; terugwerkende TC-blootstelling | Vóór indienststelling; geblokkeerd vóór toewijzing |

---

De waarde is niet dat Excel nalevingsoordeel vervangt. De waarde is dat routinematige berekeningen niet langer afhangen van geheugen, kopieer-plakcontroles en gefragmenteerde bestanden.

---

## Waarom de regeling zo werkt

Transport Canada reguleert vermoeidheid van vliegtuigbemanningen omdat vermoeidheid een veiligheidsgevaar is, niet alleen een administratief probleem. De regels zijn ontworpen om cumulatieve werklast, dienstplanning, rustmogelijkheid en alertheidrisico te controleren.

Daarom houden de regelingen rekening met factoren zoals:

- totale vluchttijd over vensters van opeenvolgende dagen
- limieten van vluchtdienstperioden
- meldtijd en circadian ritme
- aantal vluchten of sectoren
- rustperioden en dienstvrije tijd
- exploitantenmonitoring en registraties

De operationele logica is direct: twee dienstroosters kunnen hetzelfde aantal diensturen hebben maar verschillende vermoeidheidsrisico's creëren afhankelijk van timing, frequentie, aantal sectoren en eerdere accumulatie.

Nuttige officiële referenties:

- [Transport Canada: Flight and duty time regulations](https://tc.canada.ca/en/aviation/commercial-air-services/fatigue-management-aviation/flight-duty-time-regulations-prescriptive-vs-performance-based-options)
- [Transport Canada Advisory Circular AC 700-047](https://tc.canada.ca/en/aviation/reference-centre/advisory-circulars/advisory-circular-ac-no-700-047)
- [Canadian Aviation Regulations SOR/96-433](https://tc.canada.ca/en/corporate-services/acts-regulations/list-regulations/canadian-aviation-regulations-sor-96-433)

---

## Hoe de rollende vensters werken

De 28-daags accumulatielimiet vereist dat de totale vluchttijd in elk opeenvolgend venster van 28 dagen
100 uur niet overschrijdt. Het venster schuift elke dag vooruit — het is geen kalendermaand.

| Datum | Venster dekt | Netto effect |
|---|---|---|
| 15 juni | 19 mei – 15 juni | 92 u in venster |
| 16 juni | 20 mei – 16 juni | − uren gevlogen op 19 mei + uren gevlogen op 16 juni |
| 17 juni | 21 mei – 17 juni | blijft schuiven |

**De valkuil in cijfers:**  
De piloot heeft 92 uur in het venster. Ingepland voor 10 uur op 16 juni.

- Als hij 4 uur vloog op 19 mei: 92 − 4 + 10 = **98 u** — legaal.  
- Als hij 0 uur vloog op 19 mei: 92 − 0 + 10 = **102 u** — schending.

Een mentaal model met maandelijkse reset keurt beide goed. Het rollende venster niet.

Elke piloot draagt drie van deze berekeningen tegelijk: 28-daags, 90-daags en 365-daags.
Voor 15 piloten zijn dat 45 live rollende berekeningen per indienststellingscyclus, elk vereist tot
365 dagen historische opzoekingen. De wiskunde vereist geen oordeel. Automatisering elimineert de foutklasse volledig.

**Waarom meldtijd ook FDP bepaalt:** De FDP-limieten van Part 705 hangen af van wanneer de dienst begint.
Een dienst die om 09:00 begint, mag legaal tot 13 uur duren; dezelfde dienst die om 01:00
begint, is beperkt tot ongeveer 11 uur — omdat deze uitloopt in het circadian venster 02:00–05:59 waar
door vermoeidheid veroorzaakte foutpercentages sterk toenemen. Een verschil van 30 minuten in meldtijd kan
het legale maximum met tot 2 uur veranderen. Het aantal sectoren voegt een tweede dimensie toe: elke extra
nadering en landing accumuleert meetbare cognitieve belasting, en de matrix vermindert de toegestane
FDP dienovereenkomstig.

---

## Werkmappenlogica

De werkmappen is georganiseerd rond een praktische indienststellingsworkflow:

1. Voer piloot- en geplande taakgegevens in.
2. Identificeer de operationele context.
3. Haal de relevante dienst- en vluchtgeschiedenis voor die piloot op.
4. Bereken totalen van rollende vensters.
5. Vergelijk de geplande taak met geconfigureerde limieten.
6. Markeer duidelijke, waarschuwings- of risicostatus.
7. Bewaar registraties voor review en export.

De werkmappen is bedoeld als een tool voor besluitondersteuning en analyse. Het vervangt niet de wettelijke verantwoordelijkheid van de exploitant om de huidige CARs, het bedrijfsoperationshandboek, goedgekeurde vrijstellingen of FRMS-procedures te interpreteren en toe te passen.

---

## Aankoop

Gebruik hier de volledige Excel-werkmappen:

[Koop de volledige Excel-tracker](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

---

## Beperkingen

- **Afhankelijkheid van gegevensintegriteit** — berekeningen zijn slechts zo nauwkeurig als de invoeren; late, ontbrekende of onjuiste registraties produceren een onjuiste nalevingsstatus zonder waarschuwing
- **Geen juridisch advies** — deze werkmappen weerspiegelt de interpretatie van de auteur van de regelingen; de officiële positie van Transport Canada prevaleert, en toepassingen van randgevallen moeten worden gevalideerd met juridisch adviseurs of uw TC Principal Operations Inspector
- **Vertraging bij regelgevingwijzigingen** — CARs-wijzigingen worden niet automatisch weerspiegeld; exploitanten zijn verantwoordelijk voor het volgen van veranderingen in de TC-regelgeving en het dienovereenkomstig bijwerken van de werkmappen
- **Bereik: alleen Part 702 en 705** — exploitanten onder Part 703 (air taxi) of Part 704 (commuter) werken onder andere specifieke limieten die in deze versie niet zijn gecodeerd
- **Schaalplafond** — ontworpen voor 3–30 piloten; boven ongeveer 30 kan de berekeningsdiepte de Excel-prestaties verslechteren
- **Gevoeligheid voor Excel-versie** — vereist Excel 2016 of later op Windows; gedrag in Excel voor Mac of Office 365 web kan afwijken
- **Randgevallen niet volledig geautomatiseerd** — bepalingen voor uitgebreide bemanning, split-duty-regels en bepaalde rustverlengingen omvatten regelgevingsvoorwaarden die het oordeel van de verkeersleider vereisen en in deze versie niet volledig zijn gecodeerd

---

## Over dit project

Deze werkmappen is deel van een bredere inspanning om complexe operationele en regelgevende
vereisten te vertalen naar lichte tools die kleine en middelgrote organisaties echt kunnen gebruiken.

Geen ERP. Geen aangepast softwareproject. Geen extra accounts.

Alleen duidelijke bedrijfslogica, gestructureerde gegevens en herhaalbare besluitondersteuning —
geleverd in software die je team al heeft.

Als je operatie nalevings-, plannings- of resourceallocatieproblemen kent
die momenteel in het hoofd van iemand leven of in een losgekoppeld spreadsheet,
[bekijk wat er nog meer beschikbaar is →](https://www.theseusworkshop.com)

---

## License

Gedistribueerd onder de [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---
