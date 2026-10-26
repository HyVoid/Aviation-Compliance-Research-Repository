[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)
# Canadese CARs 702 & 705 Vlucht- en Diensttijden Tracker (Excel-sjabloon) — Voorkom Pilootvermoeidheid & Indienststellingschendingen

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)

Een geautomatiseerde **Canadian Aviation Regulations (CARs) Part 702 en Part 705 Vlucht- en Diensttijdenregistratie Excel-spreadsheet** ontworpen voor commerciële luchtvaartexploitanten. Deze **piloot-diensttijdcalculator** en **Fatigue Risk Management (FRMS)-planningstool** helpt verkeersleiders, bemanningsplanners en hoofdpiloten bij het volgen van **rollende vluchttijdlimieten (vensters van 28/90/365 dagen)**, het berekenen van **maximale Flight Duty Periods (FDP)**, het monitoren van **verplichte rustperiodes** en het voorkomen van **Transport Canada nalevingsschendingen** vóór de vluchtindienststelling.

> [**Open de interactieve CARs 702/705 Vluchtdiensttijd Tracker webdemo (eenmalige proef)**](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)
>
> > [**Download de multi-piloot CARs Vlucht- & Diensttijden naleving Excel-werkmap**](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

Elimineer handmatige spreadsheetfouten, automatiseer **urenpooling voor CARs Subpart 702 luchtwerk en 705 luchtvaartmaatschappijvluchten**, detecteer **nalevingsrisico's door bemanningsvermoeidheid** binnen enkele seconden en onderhoud één **Transport Canada auditklare** bron van waarheid voor piloot-dienstregistraties.

---

## Interactieve preview: CARs 702/705 piloot-dienstcalculator

<img width="1672" height="941" alt="Canadian CARs 702 and 705 Flight Duty Time Tracker Excel Template Dashboard for Pilot Scheduling and Transport Canada Compliance" src="https://github.com/user-attachments/assets/cc792931-2477-40d4-9bd7-e92418817c77" />

> **Test de logica voordat u koopt:** [Probeer de interactieve Canadese piloot Vlucht- & Diensttijdcalculator webpreview](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)

---

## Waarom handmatige bemanningsplanning faalt bij Transport Canada-nalevingsaudits

De meeste **CARs schendingen van vlucht- en diensttijden** worden niet veroorzaakt door slechte intenties. Ze gebeuren omdat **rollende vluchttijdvensters**, gemengde **Subpart 702/705 vluchtactiviteiten**, cumulatieve **bemanningsvermoeidheidsregels**, split-duty-verlengingen en gefragmenteerde pilootlogboeken vrijwel onmogelijk handmatig te kruisverwijzen zijn tijdens een drukke ochtendindienststelling.

Het risico van traditionele handmatige planning ziet er zo uit:

```text
Pilot assigned to flight
-> Manual check across separate 702 and 705 spreadsheets
-> Rolling 28-day / 90-day boundary miscalculated
-> Violation discovered retroactively during a Transport Canada PVI / Audit
```

Deze **geautomatiseerde luchtvaartnaleving Excel-werkmap** ontwerpt de workflow vóór de indienststelling opnieuw:

```text
Pilot considered for flight assignment
-> Duty & sector details logged once in a unified tracker
-> Rolling CARs 702/705 limits & FDP matrix validated automatically
-> Non-compliant dispatch blocked BEFORE flight release
```

Het commerciële probleem is niet alleen regelgevingsafstemming—het is **operationele zichtbaarheid vóór de vlucht**. Verkeersleiders en bemanningsplanners hebben onmiddellijke zekerheid nodig over de vraag of een vluchtcrewlid de volgende sector legaal en veilig kan accepteren voordat het operationele vluchtplan (OFP) wordt vrijgegeven.

---

## Drie CARs 702 & 705 nalevingsvalkuilen in handmatige spreadsheets

### Valkuil 1 — Rollende vluchttijdvensters verkeerd gelezen als kalendermaanden
Onder **Transport Canada CARs** schuiven de **vluchttijdlimieten van 28, 90 en 365 opeenvolgende dagen** elke 24 uur vooruit, niet aan het einde van elke kalendermaand. Een commercieel piloot die tussen 1–28 mei 95 vluchturen logt en op 29 mei 8 uur vliegt, reset op 1 juni **niet**. Het rollende venster van 1 juni reikt nog terug tot 4 mei. Planners die pilooturen mentaal resetten bij maandgrenzen onderschatten routinematig de cumulatieve blootstelling.

### Valkuil 2 — Vluchturen niet gepoold over CARs Subpart 702 en 705
Wanneer hetzelfde vluchtcrewlid maandag een **luchtwerk-/survey-missie onder CARs Part 702** vliegt en woensdag een **commuter- of luchtvaartmaatschappij passagierscharter onder CARs Part 705**, moeten beide vluchttijden worden gepoold naar dezelfde **rollende cumulatieve dienstlimieten**. Luchtvaartexploitanten die aparte Excel-trackingbladen bijhouden voor elk AOC-subdeel onderschatten systematisch de totale vermoeidheidsblootstelling van piloten.

### Valkuil 3 — FDP- en rustschendingen ontdekt na de vlucht
Handmatige logboekverificatie gebeurt vaak pas nadat een vluchtvrijgave is uitgegeven of wanneer de maandelijkse salarisuren worden opgeteld. Tegen de tijd dat een overschrijding van de **maximale Flight Duty Period (FDP)** of **dienstvrije tijd (rustperiode)** wordt gemarkeerd, heeft de regelgevende overtreding al plaatsgevonden—waardoor de houder van het Air Operator Certificate (AOC) wordt blootgesteld aan **Transport Canada administratieve geldboetes (AMPs)**.

Echte **onderschepping vóór de indienststelling** vereist geautomatiseerde kruiscontrole van:
- de voor vandaag geplande **Flight Duty Period (FDP)** en lokale **meldtijd (geacclimatiseerd vs. niet-geacclimatiseerd)**
- de historische 28/90/365-daagse **vluchttijdaccumulatie** van de piloot
- gepland **aantal sectoren** en gemiddelde sectorlengte
- verplichte **rustintervallen vóór en na de vlucht** en **36 uur / 7 dagen dienstvrije tijd**

---

## Voor wie deze luchtvaartnaleving Excel-sjabloon is (rol- en use-casescenario's)

Als u op zoek bent naar een betaalbaar alternatief voor enterprise bemanningsbeheersoftware zonder regelgevingsnauwkeurigheid prijs te geven, dan is deze tool gebouwd voor uw dagelijkse operationele scenario's:

| Luchtvaartrol | Doelzoekschema & operationele workflow | Primaire nalevingsvoordeel |
|---|---|---|
| **Verkeersleiders** | Hebben een **piloot-legalitycalculator vóór de indienststelling** nodig om bemanningsbeschikbaarheid te verifiëren tijdens ochtendvluchtvrijgaven of last-minute charterverzoeken. | Directe **Go / No-Go nalevingsmarkeringen** voordat het operationele vluchtplan wordt ondertekend. |
| **Bemanningsplanners & planners** | Zoeken naar een **bemanningsrooster- en vermoeidheidstrackingspreadsheet** om maandschema's te bouwen zonder de rollende limieten van 28/90/365 dagen te overschrijden. | Realtime zicht op de **resterende legale vluchtcapaciteit** per piloot binnen de vloot. |
| **Hoofdpiloten & DFO's** | Vereisen een **hoofdpiloot vluchttijdmonitoringssjabloon** om crewwerklast te overzien, dienstverlengingen goed te keuren en systemische vermoeidheid te voorkomen. | Gecentraliseerd dashboard met **gepoolde uren over CARs 702/705** en waarschuwingen bij hoge benutting. |
| **Luchtvaart SMS & veiligheidsmanagers** | Zoeken naar een **auditklare Transport Canada nalevingslog** om zich voor te bereiden op Program Validation Inspections (PVIs) en SMS-audits. | Gestandaardiseerde, manipulatiebestendige historische registraties zonder enige nabewerking. |
| **Kleine tot middelgrote AOC-exploitanten** | Canadese regionale, medevac-, bush- en charterexploitanten (3–30 piloten) die **goedkope vluchtdiensttijdtrackingsoftware in Excel** nodig hebben. | Vervangt verspreide papieren logboeken en kwetsbare DIY-sheets door één deterministische **Microsoft Excel nalevingsengine**. |

---

## Wat het u helpt bij te houden: pijnpunt-naar-oplossing mapping

In plaats van te fungeren als een passief digitaal logboek, functioneert deze werkmap als een actieve **CARs 702/705 nalevingsregel-engine**:

| Operationeel pijnpunt (wat handmatig breekt) | Veelgevolgde nalevingsmetriek in de gaten gehouden | Geautomatiseerde werkmapoplossing (hoe het het oplost) |
|---|---|---|
| **Handmatige rollende vensterberekening:** Elke ochtend 28, 90 en 365 dagen terugtellen op een wandkalender voor 15+ piloten. | **Rollende cumulatieve vluchttijdlimieten** (`100h / 28d`, `300h / 90d`, `1,000h / 365d`) | Dynamische matrixformules schuiven de 28-, 90- en 365-daagse terugblikvensters elke dag automatisch vooruit en berekenen de exacte resterende legale uren. |
| **Complexe FDP-tabellen opzoeken:** Onder tijdsdruk meldtijden kruisverwijzen naar geplande landingen in de CARs-handleiding. | **CARs Part 705 Flight Duty Period (FDP)-matrix** (meldtijd × aantal sectoren) | Vooraf gecodeerde regelgevingsopzoektabellen passen het **maximale legale FDP** automatisch aan zodra u de meldtijd en het aantal sectoren invoert. |
| **Gescheiden multi-subdeel vluchten:** Vergeten om dinsdag's Part 702 brandpatrouilleuren op te tellen bij de limieten van vrijdag's Part 705 passagierscharter. | **Cross-subdeel (CARs 702 / 703 / 704 / 705) urenpooling** | Een uniforme dataschema tagt elke vlucht per subdeel maar aggregeert alle vlucht- en diensturen in één master nalevingsprofiel per piloot. |
| **Last-minute herindelingen:** Een klant voegt midden op de dag twee extra legs toe, en de verkeersleider weet niet of de crew de dienstlimieten overschrijdt. | **Go/No-Go legalitystatus vóór de indienststelling** | Realtime voorwaardelijke opmaak activeert visuele **Waarschuwing (dichtbij limiet)** en **Schending (geblokkeerd)** meldingen *voordat* de vlucht wordt ingezet. |
| **Door elkaar gegoede auditvoorbereiding:** Dagen besteden aan het opruimen van kapotte formules en ontbrekende datums vóór een Transport Canada-inspectie. | **Transport Canada auditklare historische logboeken** | Gestructureerd, filterbaar grootboek laat u schone nalevingshistorieën exporteren per piloot, vliegtuigregistratie, datumbereik of regelgevingsstatus in één klik. |

---

## De bedrijfslogica & methodologie

### Het kerncommerciële probleem: hoge-consequentie naleving vs. software-economie
Kleine en middelgrote Canadese luchtvaartexploitanten (met 3 tot 30 piloten) zitten in een structurele squeeze. Enerzijds dragen **Transport Canada's vermoeidheidsrisico- en vluchtdiensttijdregels** exact dezelfde strenge aansprakelijkheid voor een charteruitbater met 10 piloten als voor een grote luchtvaartmaatschappij. Anderzijds vereisen enterprise SaaS bemanningsplanningplatforms (zoals Navblue, Jeppesen of FL3XX enterprise modules) steile jaarlijkse licentiekosten, langdurige onboarding en dedicated IT-beheer. Gedwongen te kiezen, vallen kleinere AOC's terug op zelfgemaakte spreadsheets—met **stille formuleverval, kopieer-plakfouten en terugwerkend handhavingsrisico** tot gevolg.

### De methodologie: deterministische onderschepping vóór de indienststelling
Om dit op te lossen zonder enterprise-overhead, past deze werkmap een **Deterministische Pre-Dispatch Interceptiemethodologie** toe, native gebouwd binnen de rekenengine van Microsoft Excel:

1. **Single-entry relationele datanormalisatie:** In plaats van sheets te organiseren per maand of per CARs-subdeel (wat longitudinale tracking breekt), worden alle operationele invoeren vastgelegd in één genormaliseerd transactiegrootboek (`Flight & Duty Log`). Elke invoer is geïndexeerd op `Pilot_ID`, `UTC/Local_Date`, `Subpart_Tag`, `Report_Time` en `Sector_Count`.
2. **Schuivend tijdvenster temporele arraymodellering:** In plaats van statische maandelijkse sombereiken (`SUM(B2:B31)`) gebruikt de engine dynamische datumgebonden array-evaluatie (`[Current_Assignment_Date - N_Days, Current_Assignment_Date]`). Elke rij evalueert zijn eigen historische context over 28-, 90- en 365-daagse horizonnen tegelijk, waardoor historische schendingen en toekomstige schema-projecties worden berekend met 100% wiskundige consistentie.
3. **Tweedimensionale regelgevingsmatrixcodering:** De **CARs Part 705 FDP-tabel** (die maximale diensturen reguleert op basis van circadiane ritmes van het tijdstip en workloadsectoren) is hardgecodeerd in een onveranderlijke referentiematrix. Met multi-criteria index-matching (`INDEX/MATCH` over tijdbanddrempels en sectorbrackets) elimineert de werkmap menselijke opzoekfouten tijdens hoogstressvolle indienststellingsvensters.
4. **Shift-Left nalevingsbewaking:** Geleend van het "Shift-Left" testprincipe in softwareontwikkeling, wordt nalevingsvalidatie verplaatst van **post-flight auditing** naar de **pre-assignatiesimulatiefase**. Door `Projected_Accumulation = Historical_Rolling_Total + Planned_Duty_Input` te berekenen, fungeert het model als een preventieve stroomonderbreker—het markeert illegale toewijzingen terwijl ze nog hypothetisch zijn.

---

## Operationele workflowvergelijking: handmatige spreadsheets vs. geautomatiseerde CARs tracker

**Exploitantbenchmarkprofiel:** 12 commerciële piloten | Gemengde **CARs Part 702 (Luchtwerk)** en **Part 705 (Luchtvaartmaatschappij/Charter)** AOC | Eén centrale verkeersleiderspost.

**De operationele bottleneck:** Elke ochtend besteedt de verkeersleider 90 minuten aan het handmatig kruiscontroleren van rollende pilootdienstlimieten voordat het vluchtschema van de dag wordt vrijgegeven. Vluchturen zijn verdeeld over twee losgekoppelde Excel-bestanden—één voor 702-activiteiten, één voor 705. Wanneer een kapitein in dezelfde week onder beide subdelen vliegt, moeten gepoolde cumulatieve totalen met de hand worden berekend. Over een seizoenspiek van 90 dagen glippen twee rollende limietoverschrijdingen erdoorheen—beide ontdekt *nadat* het vliegtuig was vertrokken, wat onmiddellijke **Transport Canada nalevingsblootstelling** creëerde.

| Operationele & nalevingsdimensie | Voor: losgekoppelde handmatige spreadsheets | Na: uniforme CARs 702/705 nalevingswerkmap |
|---|---|---|
| **Vlucht- & dienstregistratiearchitectuur** | Gefragmenteerd over aparte CARs 702- en 705-bestanden; maandtabbladen breken rollende terugblikken | **Één uniforme Excel-database** met continue meerjarige longitudinale tracking |
| **Ochtend legalitycontrole vóór de indienststelling** | ~90 minuten handmatige datumtelling en rekenmachinecontroles over 12 piloten | **Onder 3 seconden per piloot** via geautomatiseerde pre-dispatch dashboardmarkeringen |
| **Multi-subdeel (702/705) urenpooling** | Foutgevoelig handmatig kopiëren en plakken tussen spreadsheets aan het einde van de week | **100% geautomatiseerde realtime pooling** over alle CARs-subdelen bij data-invoer |
| **FDP-tabel & sectorlimietvalidatie** | Handmatig opzoeken in PDF-regelgevingshandleidingen; hoog risico op verkeerd lezen van circadiane tijdbanden | **Directe dynamische FDP-berekening** op basis van pilootmeldtijd en geplande sectoren |
| **Schendingsdetectie & TC-auditriskico** | **Ontdekking na de vlucht**; terugwerkende Transport Canada-handhaving en AMP-blootstelling | **Onderschepping vóór de indienststelling**; niet-conforme crewtoewijzingen geblokkeerd vóór vluchtvrijgave |

---

## Quick start workflow: hoe u pilootlegality verifieert in 4 stappen

Wilt u zien hoe snel u de legale beschikbaarheid van een piloot kunt verifiëren? Volg deze 4-stappen workflow om nu een enkele vluchtindienststelling te testen en ga daarna over naar volledige vloottracking:

1. **Open de interactieve websandbox (stap 1 — gratis test voor één piloot):**
   Open de [**Live CARs 702/705 Vluchtdiensttijdcalculator webpreview**](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) in uw browser. Geen installatie nodig om één crewtoewijzingsscenario te testen.
2. **Voer geplande meldtijd & aantal sectoren in (stap 2 — FDP-matrixcontrole):**
   Voer de geplande **lokale meldtijd**, **geplande vluchturen** en **aantal vluchtsectoren** van uw piloot in en selecteer de toepasselijke regel (**CARs Part 702 of Part 705**). Zie hoe de calculator onmiddellijk de **maximale legale Flight Duty Period (FDP)** bepaalt.
3. **Verifieer de rollende cumulatieve limieten van 28 / 90 / 365 dagen (stap 3 — pre-dispatch poort):**
   Bekijk de geautomatiseerde **Pre-Dispatch Compliance Status Indicator**. De engine markeert onmiddellijk of de voorgestelde vlucht de piloot over de **100-uur (28-daagse)**, **300-uur (90-daagse)** of **1.000-uur (365-daagse)** Transport Canada regelgevingsplafonds duwt.
4. **Upgrade naar de volledige multi-piloot Excel-werkmap (stap 4 — continue vlootactiviteiten):**
   De webpreview is prima voor een eenmalige legalitycontrole, maar reset wanneer u uw browser sluit. Om historische pilootregistraties op te slaan, uren te poolen over **tot 30+ piloten** en permanente **Transport Canada auditlogs** bij te houden, [**download hier de complete herbruikbare CARs 702/705 Vlucht- & Diensttijden Excel-sjabloon**](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker).

---

*De operationele waarde is niet dat Microsoft Excel het nalevingsoordeel van een hoofdpiloot vervangt. De waarde is dat routinematige **CARs 702/705 regelgevingsberekeningen** niet langer afhangen van menselijk geheugen, handmatige kalendertelling en gefragmenteerde spreadsheets.*

---

## Waarom de regeling zo werkt

Transport Canada reguleert vermoeidheid van vluchtcrews omdat vermoeidheid een veiligheidsgevaar is, niet alleen een administratief probleem. De regels zijn ontworpen om cumulatieve werklast, diensttiming, rustmogelijkheid en alertheidsrisico te beheersen.

Daarom houden de regels rekening met factoren zoals:

- totale vluchttijd over vensters van opeenvolgende dagen
- limieten van vluchtdienstperiodes
- meldtijd en circadiane timing
- aantal vluchten of sectoren
- rustperiodes en dienstvrije tijd
- exploitantmonitoring en registraties

De operationele logica is direct: twee dienstroosters kunnen hetzelfde aantal diensturen hebben maar verschillende vermoeidheidsrisico's creëren, afhankelijk van timing, frequentie, aantal sectoren en eerdere accumulatie.

Nuttige officiële referenties:

- [Transport Canada: Flight and duty time regulations](https://tc.canada.ca/en/aviation/commercial-air-services/fatigue-management-aviation/flight-duty-time-regulations-prescriptive-vs-performance-based-options)
- [Transport Canada Advisory Circular AC 700-047](https://tc.canada.ca/en/aviation/reference-centre/advisory-circulars/advisory-circular-ac-no-700-047)
- [Canadian Aviation Regulations SOR/96-433](https://tc.canada.ca/en/corporate-services/acts-regulations/list-regulations/canadian-aviation-regulations-sor-96-433)

---

## Hoe de rollende vensters werken

De 28-daagse accumulatielimiet vereist dat de totale vluchttijd in elk opeenvolgend venster van 28 dagen
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
begint, is beperkt tot ongeveer 11 uur — omdat deze uitloopt in het circadiane venster 02:00–05:59 waar
door vermoeidheid veroorzaakte foutpercentages sterk toenemen. Een verschil van 30 minuten in meldtijd kan
het legale maximum met tot 2 uur veranderen. Het aantal sectoren voegt een tweede dimensie toe: elke extra
nadering en landing accumuleert meetbare cognitieve belasting, en de matrix vermindert de toegestane
FDP dienovereenkomstig.

---

## Werkmaplogica

De werkmap is georganiseerd rond een praktische indienststellingsworkflow:

1. Voer piloot- en geplande taakgegevens in.
2. Identificeer de operationele context.
3. Haal de relevante dienst- en vluchtgeschiedenis voor die piloot op.
4. Bereken totalen van rollende vensters.
5. Vergelijk de geplande taak met geconfigureerde limieten.
6. Markeer duidelijke, waarschuwings- of risicostatus.
7. Bewaar registraties voor review en export.

De werkmap is bedoeld als een tool voor besluitondersteuning en analyse. Het vervangt niet de wettelijke verantwoordelijkheid van de exploitant om de huidige CARs, het bedrijfsoperationshandboek, goedgekeurde vrijstellingen of FRMS-procedures te interpreteren en toe te passen.

---

## Aankoop

Gebruik hier de volledige Excel-werkmap:

[Koop de volledige Excel-tracker](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

---

## Beperkingen

- **Afhankelijkheid van gegevensintegriteit** — berekeningen zijn slechts zo nauwkeurig als de invoeren; late, ontbrekende of onjuiste registraties produceren een onjuiste nalevingsstatus zonder waarschuwing
- **Geen juridisch advies** — deze werkmap weerspiegelt de interpretatie van de auteur van de regelingen; de officiële positie van Transport Canada prevaleert, en toepassingen van randgevallen moeten worden gevalideerd met juridisch adviseurs of uw TC Principal Operations Inspector
- **Vertraging bij regelgevingwijzigingen** — CARs-wijzigingen worden niet automatisch weerspiegeld; exploitanten zijn verantwoordelijk voor het volgen van veranderingen in de TC-regelgeving en het dienovereenkomstig bijwerken van de werkmap
- **Bereik: alleen Part 702 en 705** — exploitanten onder Part 703 (air taxi) of Part 704 (commuter) werken onder andere specifieke limieten die in deze versie niet zijn gecodeerd
- **Schaalplafond** — ontworpen voor 3–30 piloten; boven ongeveer 30 kan de berekeningsdiepte de Excel-prestaties verslechteren
- **Gevoeligheid voor Excel-versie** — vereist Excel 2016 of later op Windows; gedrag in Excel voor Mac of Office 365 web kan afwijken
- **Randgevallen niet volledig geautomatiseerd** — bepalingen voor uitgebreide bemanning, split-duty-regels en bepaalde rustverlengingen omvatten regelgevingsvoorwaarden die het oordeel van de verkeersleider vereisen en in deze versie niet volledig zijn gecodeerd

---

## Over dit project

Deze werkmap is deel van een bredere inspanning om complexe operationele en regelgevende
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

