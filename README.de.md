[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)
# Kanadischer CARs 702 & 705 Flug- und Dienstzeit-Tracker (Excel-Vorlage) — Verhindern Sie Pilotenübermüdung & Dispositionsverstöße

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)

Eine automatisierte **Excel-Tabelle zur Verfolgung von Flug- und Dienstzeiten gemäß den Canadian Aviation Regulations (CARs) Part 702 und Part 705** für kommerzielle Luftfahrtbetreiber. Dieser **Dienstzeitrechner für Piloten** und **Planungstool für das Fatigue Risk Management (FRMS)** hilft Flugdisponenten, Crew-Planern und Chefpiloten, **rollierende Flugzeitgrenzen (28-/90-/365-Tage-Fenster)** zu verfolgen, **maximale Flight Duty Periods (FDP)** zu berechnen, **obligatorische Ruhezeiten** zu überwachen und **Compliance-Verstöße gegen Transport Canada** vor der Flugfreigabe zu verhindern.

> [**Starten Sie die interaktive Web-Demo des CARs 702/705 Flug- und Dienstzeit-Trackers (einmalige Testnutzung)**](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)
>
> > [**Laden Sie die Multi-Piloten-CARs-Excel-Arbeitsmappe für Flug- und Dienstzeit-Compliance herunter**](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

Beseitigen Sie manuelle Tabellenkalkulationsfehler, automatisieren Sie **das Bündeln der Flugzeiten über CARs Subpart 702 (Luftarbeit) und Subpart 705 (Fluglinienbetrieb)**, erkennen Sie **Compliance-Risiken durch Crew-Ermüdung** in Sekunden und pflegen Sie eine einzige, **prüfungsfähige Quelle der Wahrheit für Transport Canada** für Piloten-Dienstdatensätze.

---

## Interaktive Vorschau: CARs 702/705 Piloten-Dienstzeitrechner

<img width="1672" height="941" alt="Canadian CARs 702 and 705 Flight Duty Time Tracker Excel Template Dashboard for Pilot Scheduling and Transport Canada Compliance" src="https://github.com/user-attachments/assets/cc792931-2477-40d4-9bd7-e92418817c77" />

> **Testen Sie die Logik, bevor Sie kaufen:** [Probieren Sie die interaktive Web-Vorschau des kanadischen Piloten-Flug- und Dienstzeitrechners aus](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)

---

## Warum manuelle Crew-Planung bei Compliance-Audits von Transport Canada scheitert

Die meisten **Verstöße gegen Flug- und Dienstzeiten nach den CARs** entstehen nicht durch böse Absichten. Sie entstehen, weil **rollierende Flugzeitfenster**, gemischte **Flugbetriebe nach Subpart 702/705**, kumulative **Ermüdungsregeln für Besatzungen**, Split-Duty-Verlängerungen und fragmentierte Piloten-Flugbücher während einer geschäftigen morgendlichen Disposition beinahe unmöglich manuell gegenüberzustellen sind.

Das Risiko der traditionellen manuellen Planung sieht so aus:

```text
Pilot assigned to flight
-> Manual check across separate 702 and 705 spreadsheets
-> Rolling 28-day / 90-day boundary miscalculated
-> Violation discovered retroactively during a Transport Canada PVI / Audit
```

Diese **automatisierte Excel-Arbeitsmappe für Luftfahrt-Compliance** gestaltet den Arbeitsablauf vor der Disposition neu:

```text
Pilot considered for flight assignment
-> Duty & sector details logged once in a unified tracker
-> Rolling CARs 702/705 limits & FDP matrix validated automatically
-> Non-compliant dispatch blocked BEFORE flight release
```

Das kommerzielle Problem ist nicht nur die regulatorische Ausrichtung — es ist **die operative Transparenz vor dem Flug**. Flugdisponenten und Crew-Planer brauchen unmittelbare Gewissheit, ob ein Besatzungsmitglied den nächsten Streckenabschnitt legal und sicher übernehmen kann, bevor der Operationsflugplan (OFP) freigegeben wird.

---

## Drei Compliance-Fallen der CARs 702 & 705 in manuellen Tabellenkalkulationen

### Falle 1 — Rollierende Flugzeitfenster werden als Kalendermonate missverstanden
Nach den **CARs von Transport Canada** rutschen die **28-, 90- und 365-Tage-Grenzen für aufeinanderfolgende Tage** alle 24 Stunden weiter, nicht am Ende eines jeden Kalendermonats. Ein kommerzieller Pilot, der zwischen dem 1. und 28. Mai 95 Flugstunden verzeichnet und am 29. Mai 8 Stunden fliegt, setzt am 1. Juni **nicht** zurück. Das rollierende Fenster des 1. Juni reicht noch bis zum 4. Mai zurück. Planer, die die Pilotenstunden gedanklich an Monatsgrenzen zurücksetzen, unterschätzen routinemäßig die kumulative Exposition.

### Falle 2 — Flugstunden werden nicht über CARs Subpart 702 und 705 gebündelt
Wenn dasselbe Besatzungsmitglied am Montag einen **Luftarbeits-/Vermessungseinsatz unter CARs Part 702** und am Mittwoch einen **Pendler- oder Passagiercharter unter CARs Part 705** fliegt, müssen beide Flugzeiten auf dieselben **rollierenden kumulativen Dienstgrenzen** angerechnet werden. Luftfahrtbetreiber, die für jeden AOC-Subpart getrennte Excel-Tracking-Blätter führen, unterschätzen systematisch die gesamte Ermüdungsexposition ihrer Piloten.

### Falle 3 — FDP- & Ruhezeitverstöße werden erst nach dem Flug entdeckt
Die manuelle Überprüfung des Flugbuchs erfolgt oft erst, nachdem eine Flugfreigabe erteilt wurde oder wenn die Monatslöhne abgerechnet werden. Bis eine Überschreitung der **maximalen Flight Duty Period (FDP)** oder der **dienstfreien Zeit (Ruhezeit)** markiert wird, ist der Regelverstoß bereits geschehen — und stellt den Inhaber des Air Operator Certificate (AOC) **administrativen Geldbußen (AMPs) von Transport Canada** aus.

Die echte **Abfangung vor der Disposition** erfordert automatisierte Gegenprüfung von:
- der heute geplanten **Flight Duty Period (FDP)** und der lokalen **Meldezeit (akklimatisiert vs. nicht akklimatisiert)**
- der historischen **Flugzeitakkumulation** des Piloten über 28/90/365 Tage
- der geplanten **Anzahl der Streckenabschnitte (Sektoren)** und der durchschnittlichen Abschnittslänge
- obligatorischen **Ruhezeiten vor und nach dem Flug** sowie der **36-stündigen / 7-tägigen dienstfreien Zeit**

---

## Für wen diese Excel-Vorlage zur Luftfahrt-Compliance gedacht ist (Rollen & Anwendungsszenarien)

Wenn Sie eine günstige Alternative zu Enterprise-Crew-Management-Software suchen, ohne regulatorische Genauigkeit einzubüßen, ist dieses Tool für Ihre täglichen betrieblichen Szenarien gebaut:

| Luftfahrt-Rolle | Zielsuchszenario & Betriebsablauf | Wichtigster Compliance-Nutzen |
|---|---|---|
| **Flugdisponenten** | Benötigen einen **Dienstbarkeitsrechner für Piloten vor der Disposition**, um die Crew-Verfügbarkeit bei morgendlichen Flugfreigaben oder kurzfristigen Charteranfragen zu prüfen. | Sofortige **Go / No-Go-Compliance-Markierungen**, bevor der Operationsflugplan unterzeichnet wird. |
| **Crew-Planer & Scheduler** | Suchen eine **Crew-Einsatzplanungs- und Ermüdungs-Tracking-Tabelle**, um Monatspläne ohne Überschreitung der rollierenden 28/90/365-Tage-Obergrenzen zu erstellen. | Echtzeit-Sichtbarkeit der **verbleibenden legalen Flugkapazität** pro Pilot in der gesamten Flotte. |
| **Chefpiloten & DFOs** | Benötigen eine **Überwachungsvorlage für Flugzeiten des Chefpiloten**, um die Arbeitslast der Crew zu überwachen, Dienstverlängerungen zu genehmigen und systematische Übermüdung zu verhindern. | Zentrales Dashboard mit **Stundenbündelung über gemischte CARs 702/705** und Warnhinweisen bei hoher Auslastung. |
| **Luftfahrt-SMS- & Sicherheitsmanager** | Suchen ein **prüfungsfertiges Compliance-Protokoll für Transport Canada** zur Vorbereitung auf Program Validation Inspections (PVIs) und SMS-Audits. | Standardisierte, manipulationssichere historische Aufzeichnungen ohne jegliche Nachbearbeitung. |
| **Kleine bis mittlere AOC-Betreiber** | Kanadische Regional-, Medevac-, Bush- und Charterbetreiber (3–30 Piloten), die **günstige Software zur Verfolgung der Flugdienstzeiten in Excel** benötigen. | Ersetzt verstreute Papier-Flugbücher und fehleranfällige Eigenbau-Tabellen durch eine deterministische **Microsoft-Excel-Compliance-Engine**. |

---

## Was es Ihnen hilft zu verfolgen: Zuordnung von Problempunkten zu Lösungen

Statt als passives digitales Flugbuch zu dienen, funktioniert diese Arbeitsmappe als aktive **Regel-Engine für CARs 702/705**:

| Operativer Problempunkt (Was manuell scheitert) | Häufig verfolgte Compliance-Kennzahl | Automatisierte Lösung der Arbeitsmappe (Wie sie das Problem löst) |
|---|---|---|
| **Manuelles Rechnen mit rollierenden Fenstern:** Jeden Morgen für 15+ Piloten 28, 90 und 365 Tage auf einer Wandkalender zurückzählen. | **Rollierende kumulative Flugzeitgrenzen** (`100h / 28d`, `300h / 90d`, `1,000h / 365d`) | Dynamische Array-Formeln schieben die 28-, 90- und 365-Tage-Betrachtungsfenster jeden Tag automatisch weiter und berechnen die exakt verbleibenden legalen Stunden. |
| **Komplexe FDP-Tabellennachschläge:** Piloten-Meldezeiten unter Zeitdruck gegen geplante Landungen im CARs-Handbuch abgleichen. | **CARs-Part-705-Flight-Duty-Period-(FDP)-Matrix** (Meldezeit × Sektoranzahl) | Voreingebettete regulatorische Nachschlagetabellen passen das **maximale legale FDP** automatisch an, sobald Sie die Meldezeit und die Anzahl der Sektoren eingeben. |
| **Getrennte Flüge über mehrere Subparts:** Die Part-702-Feuerwachstunden vom Dienstag vergessen, zu den Part-705-Passagierchartergrenzen vom Freitag hinzuzurechnen. | **Stundenbündelung über Subparts hinweg (CARs 702 / 703 / 704 / 705)** | Ein einheitliches Datenschema markiert jeden Flug nach Subpart, aggregiert aber alle Flug- und Dienststunden in einem einzigen zentralen Compliance-Profil pro Pilot. |
| **Kurzfristige Umplanungen:** Ein Kunde fügt mittags zwei zusätzliche Streckenabschnitte hinzu, und die Disposition weiß nicht, ob die Crew die Dienstgrenzen sprengt. | **Go/No-Go-Legalitätsstatus vor der Disposition** | Echtzeit-Bedingungsformatierung löst visuelle Warnungen **Warnung (Grenze nahe)** und **Verstoß (Blockiert)** aus, *bevor* der Flug freigegeben wird. |
| **Zerrüttete Audit-Vorbereitung:** Tage mit der Bereinigung kaputter Formeln und fehlender Daten vor einer Transport-Canada-Inspektion verbringen. | **Prüfungsfertige historische Protokolle für Transport Canada** | Ein strukturiertes, filterbares Verzeichnis ermöglicht den Export sauberer Compliance-Historien nach Pilot, Luftfahrzeugkennzeichen, Datumsbereich oder Regulator-Status mit einem Klick. |

---

## Geschäftslogik & Methodik

### Das kommerzielle Kernproblem: Hochriskante Compliance vs. Softwareökonomie
Kleine und mittelgroße kanadische Luftfahrtbetreiber (mit 3 bis 30 Piloten) stehen unter strukturellem Druck. Auf der einen Seite tragen die **Ermüdungsrisiko- und Flugdienstzeitvorschriften von Transport Canada** für einen Charterbetrieb mit 10 Piloten genau dieselbe strenge Haftung wie für eine große Fluggesellschaft. Auf der anderen Seite verlangen Enterprise-SaaS-Crew-Planungsplattformen (wie Navblue, Jeppesen oder FL3XX-Enterprise-Module) hohe jährliche Lizenzgebühren, langwierige Einführungen und eine eigene IT-Verwaltung. Vor diese Wahl gestellt, greifen kleinere AOCs auf selbstgebaute Tabellen zurück — mit **stille Formelverfall, Copy-Paste-Fehlern und rückwirkendem Vollstreckungsrisiko**.

### Die Methodik: Deterministische Abfangung vor der Disposition
Um dies ohne Enterprise-Aufwand zu lösen, wendet diese Arbeitsmappe eine **deterministische Methodik zur Abfangung vor der Disposition** an, die nativ in der Berechnungs-Engine von Microsoft Excel verankert ist:

1. **Eingabe normalisierter relationaler Daten an einer einzigen Stelle:** Statt Tabellen nach Monat oder CARs-Subpart zu organisieren (was die longitudinale Verfolgung zerstört), werden alle operativen Eingaben in einem einzigen normalisierten Transaktionsverzeichnis (`Flight & Duty Log`) erfasst. Jeder Eintrag wird über `Pilot_ID`, `UTC/Local_Date`, `Subpart_Tag`, `Report_Time` und `Sector_Count` indiziert.
2. **Zeitliche Array-Modellierung mit gleitenden Fenstern:** Statt statischer monatlicher Summenbereiche (`SUM(B2:B31)`) verwendet die Engine eine dynamische, datumsbegrenzte Array-Auswertung (`[Current_Assignment_Date - N_Days, Current_Assignment_Date]`). Jede Zeile wertet ihren eigenen historischen Kontext gleichzeitig über 28-, 90- und 365-Tage-Horizonte aus, sodass historische Verstöße und Zukunftsprojektionen mit 100 % mathematischer Konsistenz berechnet werden.
3. **Zweidimensionale Kodierung der regulatorischen Matrix:** Die **CARs-Part-705-FDP-Tabelle** (die die maximalen Dienststunden auf Grundlage tageszeitlicher zirkadianer Rhythmen und Arbeitslastsektoren regelt) ist als unveränderliche Referenzmatrix fest verdrahtet. Mittels Mehrkriterien-Indexsuche (`INDEX/MATCH` über Zeitband-Schwellen und Sektorbereiche) eliminiert die Arbeitsmappe menschliche Nachschlagefehler in stressigen Dispositionsfenstern.
4. **Shift-Left-Compliance-Kontrolle:** Entlehnt aus dem „Shift-Left“-Testprinzip der Softwaretechnik wird die Compliance-Validierung von der **Prüfung nach dem Flug** in die **Simulationsphase vor der Zuweisung** verlegt. Durch die Berechnung von `Projected_Accumulation = Historical_Rolling_Total + Planned_Duty_Input` fungiert das Modell als präventiver Schutzschalter — es markiert illegale Zuweisungen, solange sie noch hypothetisch sind.

---

## Vergleich der Betriebsabläufe: Manuelle Tabellen vs. automatisierter CARs-Tracker

**Betreiber-Benchmark-Profil:** 12 kommerzielle Piloten | gemischter AOC nach **CARs Part 702 (Luftarbeit)** und **Part 705 (Fluglinie/Charter)** | eine zentrale Dispositionsstelle.

**Der betriebliche Engpass:** Jeden Morgen verbringt der Flugdisponent 90 Minuten mit der manuellen Gegenprüfung rollierender Dienstgrenzen der Piloten, bevor er den Tagesflugplan freigibt. Die Flugstunden verteilen sich auf zwei getrennte Excel-Dateien — eine für 702-Betrieb, eine für 705. Wenn ein Kapitän in derselben Woche unter beiden Subparts fliegt, müssen die gebündelten Kumulativsummen von Hand berechnet werden. Während eines saisonalen 90-Tage-Höhepunkts schlüpften zwei rollierende Grenzüberschreitungen durch — beide erst *nach* dem Abflug entdeckt, was eine unmittelbare **Compliance-Exposition gegenüber Transport Canada** schuf.

| Betriebs- & Compliance-Dimension | Vorher: getrennte manuelle Tabellen | Nachher: einheitliche CARs-702/705-Compliance-Arbeitsmappe |
|---|---|---|
| **Architektur der Flug- & Dienstaufzeichnungen** | Zersplittert über getrennte CARs-702- und 705-Dateien; monatliche Register brechen rollierende Rückblicke | **Eine einheitliche Excel-Datenbank** mit kontinuierlicher mehrjähriger Langzeitverfolgung |
| **Morgendliche Legalitätsprüfung vor der Disposition** | ~90 Minuten manuelles Datenzählen und Rechnerkontrollen über 12 Piloten | **Unter 3 Sekunden pro Pilot** durch automatisierte Dashboard-Markierungen vor der Disposition |
| **Stundenbündelung über Subparts (702/705)** | Fehleranfälliges manuelles Copy-Paste zwischen den Tabellen am Wochenende | **100 % automatisierte Echtzeit-Bündelung** über alle CARs-Subparts bei der Dateneingabe |
| **FDP-Tabellen- & Sektorgrenzen-Validierung** | Manueller Nachschlag in PDF-Vorschriften; hohes Risiko, zirkadiane Zeitbänder falsch zu lesen | **Sofortige dynamische FDP-Berechnung** auf Basis der Meldezeit und der geplanten Sektoren |
| **Verstoßerkennung & TC-Auditrisiko** | **Entdeckung nach dem Flug**; rückwirkende Vollstreckung durch Transport Canada und AMP-Exposition | **Abfangen vor der Disposition**; nicht konforme Crew-Zuweisungen werden vor der Flugfreigabe blockiert |

---

## Schnellstart-Workflow: Pilotenlegalität in 4 Schritten prüfen

Möchten Sie sehen, wie schnell Sie die legale Verfügbarkeit eines Piloten prüfen können? Folgen Sie diesem 4-Schritte-Workflow, um jetzt eine einzelne Flugfreigabe zu testen, und wechseln Sie dann zur vollständigen Flottenverfolgung:

1. **Starten Sie die interaktive Web-Sandbox (Schritt 1 — kostenloser Einzeltest):** Öffnen Sie die [**Live-Web-Vorschau des CARs 702/705 Flug- und Dienstzeitrechners**](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) in Ihrem Browser. Für den Test eines einzelnen Besatzungsszenarios ist keine Installation erforderlich.
2. **Eingabe der geplanten Meldezeit & Sektoranzahl (Schritt 2 — FDP-Matrixprüfung):** Geben Sie die geplante **lokale Meldezeit** des Piloten, die **geplanten Flugstunden** und die **Anzahl der Flugsektoren** ein und wählen Sie die anwendbare Vorschrift (**CARs Part 702 oder Part 705**). Beobachten Sie, wie der Rechner sofort das **maximale legale Flight Duty Period (FDP)** bestimmt.
3. **Rollierende kumulative Grenzen über 28 / 90 / 365 Tage prüfen (Schritt 3 — Gate vor der Disposition):** Prüfen Sie den automatisierten **Compliance-Statusindikator vor der Disposition**. Die Engine markiert sofort, ob der vorgeschlagene Flug den Piloten über die regulatorischen Obergrenzen von **100 Stunden (28 Tage)**, **300 Stunden (90 Tage)** oder **1.000 Stunden (365 Tage)** von Transport Canada hinausdrängt.
4. **Upgrade auf die vollständige Multi-Piloten-Excel-Arbeitsmappe (Schritt 4 — kontinuierlicher Flottenbetrieb):** Die Web-Vorschau eignet sich hervorragend für eine einmalige Legalitätsprüfung, setzt sich aber beim Schließen des Browsers zurück. Um historische Pilotendatensätze zu speichern, Stunden über **bis zu 30+ Piloten** hinweg zu bündeln und dauerhafte **Transport-Canada-Auditprotokolle** zu führen, [**laden Sie hier die vollständige wiederverwendbare CARs-702/705-Excel-Vorlage für Flug- und Dienstzeiten herunter**](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker).

---

*Der operative Wert liegt nicht darin, dass Microsoft Excel das Compliance-Urteil eines Chefpiloten ersetzt. Der Wert liegt darin, dass die routinemäßige **Regel-Mathematik der CARs 702/705** nicht mehr vom menschlichen Gedächtnis, dem manuellen Kalenderzählen und zersplitterten Tabellen abhängt.*

---

## Warum die Vorschrift so funktioniert

Transport Canada reguliert die Ermüdung von Flugbesatzungen, weil Ermüdung ein Sicherheitsrisiko ist, nicht nur ein administratives Thema. Die Regeln sind darauf ausgelegt, kumulative Arbeitslast, Dienstzeitplanung, Ruhegelegenheit und Wachsamkeitsrisiko zu kontrollieren.

Deshalb berücksichtigen die Vorschriften Faktoren wie:

- Gesamtflugzeit über Fenster aufeinanderfolgender Tage
- Grenzen der Flugdienstperioden
- Meldezeit und zirkadianes Timing
- Anzahl der Flüge oder Sektoren
- Ruhezeiten und dienstfreie Zeit
- Betreiberüberwachung und Aufzeichnungen

Die operative Logik ist direkt: Zwei Dienstpläne können die gleiche Anzahl von Dienststunden haben, aber je nach Timing, Häufigkeit, Sektoranzahl und vorheriger Akkumulation unterschiedliche Ermüdungsrisiken erzeugen.

Nützliche offizielle Referenzen:

- [Transport Canada: Flight and duty time regulations](https://tc.canada.ca/en/aviation/commercial-air-services/fatigue-management-aviation/flight-duty-time-regulations-prescriptive-vs-performance-based-options)
- [Transport Canada Advisory Circular AC 700-047](https://tc.canada.ca/en/aviation/reference-centre/advisory-circulars/advisory-circular-ac-no-700-047)
- [Canadian Aviation Regulations SOR/96-433](https://tc.canada.ca/en/corporate-services/acts-regulations/list-regulations/canadian-aviation-regulations-sor-96-433)

---

## Wie die rollierenden Fenster funktionieren

Die 28-Tage-Akkumulationsgrenze erfordert, dass die Gesamtflugzeit in einem beliebigen Zeitfenster von 28 aufeinanderfolgenden Tagen 100 Stunden nicht überschreitet. Das Fenster rutscht jeden Tag vor — es ist kein Kalendermonat.

| Datum | Fenster deckt ab | Nettoeffekt |
|---|---|---|
| 15. Juni | 19. Mai – 15. Juni | 92 h im Fenster |
| 16. Juni | 20. Mai – 16. Juni | − Stunden geflogen am 19. Mai + Stunden geflogen am 16. Juni |
| 17. Juni | 21. Mai – 17. Juni | rutscht weiter |

**Die Falle in Zahlen:**  
Pilot hat 92 Stunden im Fenster. Für 10 Stunden am 16. Juni eingeplant.

- Wenn er am 19. Mai 4 Stunden flog: 92 − 4 + 10 = **98 h** — legal.  
- Wenn er am 19. Mai 0 Stunden flog: 92 − 0 + 10 = **102 h** — Verstoß.

Ein mentales Modell mit monatlichem Zurücksetzen genehmigt beides. Das rollierende Fenster nicht.

Jeder Pilot führt drei dieser Berechnungen gleichzeitig: 28-Tage, 90-Tage und 365-Tage.
Bei 15 Piloten sind das 45 live rollierende Berechnungen pro Dispositionszyklus, jede erfordert bis zu
365 Tage historischer Nachschau. Die Mathematik erfordert kein Urteil. Automatisierung eliminiert diese Fehlerklasse vollständig.

**Warum auch die Meldezeit die FDP bestimmt:** Die FDP-Grenzen von Part 705 hängen vom Dienstbeginn ab.
Ein Dienst, der um 09:00 beginnt, darf legal bis zu 13 Stunden laufen; derselbe Dienst, der um 01:00
beginnt, ist auf nahezu 11 Stunden begrenzt — weil er in das zirkadiane Fenster 02:00–05:59 reicht, in dem
ermüdungsbedingte Fehlerraten stark ansteigen. Ein Unterschied von 30 Minuten in der Meldezeit kann
das legale Maximum um bis zu 2 Stunden ändern. Die Sektoranzahl fügt eine zweite Dimension hinzu: Jeder zusätzliche
Anflug und jede Landung akkumuliert messbare kognitive Last, und die Matrix reduziert die erlaubte
FDP entsprechend.

---

## Arbeitsmappen-Logik

Die Arbeitsmappe ist um einen praktischen Dispositions-Workflow organisiert:

1. Piloten- und geplante Zuweisungsdaten eingeben.
2. Den Operationskontext identifizieren.
3. Die relevante Dienst- und Flughistorie für diesen Piloten abrufen.
4. Rollierende Fenstersummen berechnen.
5. Die geplante Zuweisung mit den konfigurierten Grenzen vergleichen.
6. Klaren, Warn- oder Risikostatus markieren.
7. Aufzeichnungen für Überprüfung und Export aufbewahren.

Die Arbeitsmappe ist als Entscheidungsunterstützungs- und Analysetool gedacht. Sie ersetzt nicht die rechtliche Verantwortung des Betreibers, die aktuellen CARs, das Firmenoperationshandbuch, genehmigte Ausnahmen oder FRMS-Verfahren zu interpretieren und anzuwenden.

---

## Kauf

Verwenden Sie hier die komplette Excel-Arbeitsmappe:

[Den kompletten Excel-Tracker kaufen](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

---

## Einschränkungen

- **Abhängigkeit von der Datenintegrität** — Berechnungen sind nur so genau wie die Eingaben; verspätete, fehlende oder falsche Aufzeichnungen erzeugen ohne Warnung einen falschen Compliance-Status
- **Keine rechtliche Stellungnahme** — diese Arbeitsmappe spiegelt die Interpretation des Autors der Vorschriften wider; die offizielle Position von Transport Canada ist maßgeblich, und Grenzfallanwendungen sollten mit Rechtsberatern oder Ihrem TC Principal Operations Inspector validiert werden
- **Verzögerung bei Vorschriftenänderungen** — CARs-Änderungen werden nicht automatisch übernommen; Betreiber sind dafür verantwortlich, TC-Vorschriftenänderungen zu überwachen und die Arbeitsmappe entsprechend zu aktualisieren
- **Umfang: nur Part 702 und 705** — Betreiber unter Part 703 (Air Taxi) oder Part 704 (Commuter) unterliegen anderen spezifischen Grenzen, die in dieser Version nicht kodiert sind
- **Skalierungsgrenze** — für 3–30 Piloten ausgelegt; jenseits von etwa 30 kann die Berechnungstiefe die Excel-Leistung beeinträchtigen
- **Abhängigkeit von der Excel-Version** — erfordert Excel 2016 oder höher unter Windows; das Verhalten in Excel für Mac oder Office 365 Web kann abweichen
- **Grenzfälle nicht vollständig automatisiert** — Bestimmungen für erweiterte Besatzungen, Split-Duty-Regeln und bestimmte Ruhezeitverlängerungen beinhalten regulatorische Bedingungen, die das Urteil des Disponenten erfordern und in dieser Version nicht vollständig kodiert sind

---

## Über dieses Projekt

Diese Arbeitsmappe ist Teil einer breiteren Anstrengung, komplexe betriebliche und regulatorische
Anforderungen in leichte Werkzeuge zu übersetzen, die kleine und mittlere Organisationen tatsächlich nutzen können.

Kein ERP. Kein individuelles Softwareprojekt. Keine zusätzlichen Konten.

Nur klare Geschäftslogik, strukturierte Daten und wiederholbare Entscheidungsunterstützung —
geliefert in Software, die Ihr Team bereits hat.

Wenn Ihre Operation Compliance-, Planungs- oder Ressourcenzuteilungsprobleme beinhaltet,
die derzeit im Kopf von jemandem oder in einer getrennten Tabelle leben,
[sehen Sie, was sonst verfügbar ist →](https://www.theseusworkshop.com)

---

## Lizenz

Verbreitet unter der [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---

