[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | 🇪🇸 [ Español ](README.sp.md) | [ 🇬🇧 English ](README.md)

# Verhindern Sie Verstöße gegen Flug- und Dienstzeiten vor der Disposition

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)

**Entwickelt für kanadische Betreiber nach Part 702 und Part 705, die Flugzeit, Dienstzeit, Ermüdungsexposition und rollierende Compliance-Grenzen verfolgen müssen, bevor ein Pilot zugewiesen wird.**

[Live-Vorschau](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) | [Komplette Excel kaufen](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

Verfolgen Sie rollierende Flugzeitgrenzen, erkennen Sie Compliance-Risiken in Sekunden und pflegen Sie eine einzige prüfbare Quelle der Wahrheit für Piloten-Dienstdatensätze.

---

## Schnelle Vorschau

<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 11_47_04 AM" src="https://github.com/user-attachments/assets/cc792931-2477-40d4-9bd7-e92418817c77" />

> Sehen Sie sich die interaktive Arbeitsmappen-Vorschau an: [Pilot-Duty-Tracker-Demo](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)

---

## Warum dies existiert

Die meisten Verstöße gegen Flug- und Dienstzeiten werden nicht durch böse Absichten verursacht.

Sie passieren meist, weil rollierende Fenster, gemischte 702/705-Aktivitäten, kumulative Ermüdungsregeln, neu zugewiesene Dienste und fragmentierte Aufzeichnungen manuell schwer zu überwachen sind.

Das Risiko ist einfach:

```text
Pilot assigned
-> Manual check
-> Prior records missed
-> Violation discovered after the flight
```

Diese Arbeitsmappe wurde entwickelt, um den Workflow zu ändern:

```text
Pilot considered for assignment
-> Duty record entered once
-> Rolling limits checked automatically
-> Compliance risk flagged before dispatch
```

Das kommerzielle Problem ist nicht nur Regulierung. Es ist operative Transparenz. Disponenten und Planer müssen wissen, ob ein Pilot die nächste Zuweisung legal und sicher übernehmen kann, bevor der Flug freigegeben wird.

---

## Drei Compliance-Fallen, die Betreiber fangen

### Falle 1 — Rollierende Fenster werden als Kalenderzeiträume missverstanden

Die 28-, 90- und 365-Tage-Grenzen rutschen jeden Tag vor, nicht jeden Monat.
Ein Pilot, der zwischen dem 1. und 28. Mai 95 Stunden flog und dann am 29. Mai 8 Stunden flog,
hat zu Beginn des Juni **nicht** zurückgesetzt. Das Fenster vom 1. Juni reicht noch bis zum 4. Mai zurück.

Planer, die Grenzen geistig an Monatsgrenzen zurücksetzen, unterschätzen routinemäßig die Exposition.
Dies ist die strukturell unsichtbarste Falle: das mentale Modell fühlt sich richtig an; die Berechnung ist falsch.

### Falle 2 — Stunden werden nicht über 702 und 705 gebündelt

Wenn derselbe Pilot am Montag eine Luftbefliegung unter Part 702 und am Mittwoch einen Passagier-Charter
unter Part 705 durchführt, zählen beide Stundensätze für dieselben rollierenden Akkumulationsgrenzen.

Betreiber, die getrennte Tracking-Blätter für jeden Unterteil führen — eine natürliche Workflow-Teilung —
unterschätzen systematisch. Die Verordnung erkennt diese operative Grenze nicht an.

### Falle 3 — Verstöße werden nach dem Flug entdeckt

Manuelle Verifizierung erfolgt typischerweise, nachdem eine Dienstezuweisung ausgegeben wurde, oder nachdem der Flug
abgeflogen ist. Bis ein Verstoß identifiziert wird, ist der Verstoß bereits eingetreten.
Die Durchsetzung durch Transport Canada gilt rückwirkend.

Die Abfangung vor dem Flug erfordert, dass der Compliance-Status sichtbar ist, *bevor* ein Pilot zugewiesen wird —
was erfordert, dass alle historischen Daten aktuell sind und alle Berechnungen automatisch zum
Zeitpunkt der Disposition laufen.

Sie steckt normalerweise in der Beziehung zwischen:

- der für heute geplanten Dienstzeit
- der vorherigen Diensthistorie des Piloten
- der Meldezeit
- der Sektoranzahl
- der Flugzeitakkumulation
- der erforderlichen Ruhezeit
- betreiberspezifischen Verfahren

Deshalb entdeckt die manuelle Tabellenkalkulationsprüfung das Problem oft spät oder übersieht es ganz.

---

## Für wen dieses Tool ist

| Benutzer | Praktischer Anwendungsfall |
|---|---|
| Flugdisponenten | Pilotenverfügbarkeit vor Ausgabe einer Dispositionsfreigabe prüfen |
| Crew-Planer | Dienstpläne mit Sichtbarkeit der verbleibenden legalen Kapazität erstellen |
| Chefpiloten | Pilotenarbeitslast und kumulative Exposition vor Genehmigung von Zuweisungen prüfen |
| Sicherheitsmanager | Strukturierte Aufzeichnungen für interne Überprüfung und Audit-Vorbereitung pflegen |
| Kleine AOC-Betreiber | Verstreutes manuelles Tracking durch einen leichten Excel-Workflow ersetzen |

Am besten geeignet für kanadische Betreiber mit 3–30 Piloten, die gemischte 702/705-Operationen betreiben,
wo dedizierte Crew-Management-Software kostspielig ist, manuelle Ansätze aber nicht mehr skalieren.

---

## Was die Arbeitsmappe tut

### Dienstzeiterfassung
Ein einziger Dateneingabepunkt für alle Piloten-Dienstdatensätze. Disponenten erfassen grundlegende Flug- und Dienstinformationen
einmal; Berechnungen laufen automatisch im Hintergrund.

### Rollierende Fensterüberwachung
Automatische Berechnung der Part 705-Akkumulationsgrenzen über alle drei regulatorischen Fenster gleichzeitig:
- 100 Stunden in beliebigen 28 aufeinanderfolgenden Tagen
- 300 Stunden in beliebigen 90 aufeinanderfolgenden Tagen
- 1.000 Stunden in beliebigen 365 aufeinanderfolgenden Tagen

### Compliance-Status vor der Disposition
Der Compliance-Status jedes Piloten ist sichtbar, bevor die Zuweisung ausgegeben wird.
Kein manuelles Abgleichen. Keine Entdeckung nach dem Flug.

### FDP-Matrix-Validierung
Die Flight-Duty-Period-Grenzen von Part 705 — eine zweivariable Matrix aus Meldezeit × Sektoranzahl —
sind vorcodiert. Das legale FDP-Maximum aktualisiert sich automatisch basierend darauf, wann der Pilot sich meldet
und wie viele Sektoren geplant sind.

### Audit-fertige Berichterstattung
Jeder Eintrag ist von Tag eins an strukturiert und nachverfolgbar. Historische Compliance-Aufzeichnungen können nach
Pilot, Datumsbereich oder Status gefiltert und ohne Nachbearbeitung exportiert werden.

---

## Beispielszenario

**Betreiberprofil:** 12 Piloten. Gemischte Operationen nach Part 702 und Part 705. Ein Dispositionsbüro.

**Das Problem:** Jeden Morgen verbringt der Disponent 90 Minuten mit der manuellen Überprüfung rollierender
Dienstgrenzen, bevor er den Flugbetrieb des Tages zuweist. Flugstunden werden in zwei getrennten
Tabellenkalkulationen verfolgt — eine für 702-Operationen, eine für 705. Wenn ein Pilot unter beiden Unterteilen
in derselben Woche fliegt, werden gebündelte Summen von Hand konsolidiert.

Über drei Betriebsmonate hinweg wurden zwei Grenzüberschreitungen entdeckt — beide nachdem der Flug
bereits abgeflogen war.

| | Vorher | Nachher |
|---|---|---|
| Aufzeichnungsstruktur | Zwei getrennte Blätter, eines pro Unterteil | Eine einheitliche Arbeitsmappe |
| Morgenprüfzeit | ~90 Min. über alle Piloten | Unter 3 Sekunden pro Pilot |
| 702/705-Stundenbündelung | Manuelle Konsolidierung | Automatisch über beide Unterteile |
| Verstoßentdeckung | Nach dem Flug; rückwirkende TC-Exposition | Vor der Disposition; vor Zuweisung blockiert |

---

Der Wert liegt nicht darin, dass Excel das Compliance-Urteil ersetzt. Der Wert liegt darin, dass routinemäßige Berechnungen nicht mehr von Gedächtnis, Copy-Paste-Prüfungen und fragmentierten Dateien abhängen.

---

## Warum die Verordnung so funktioniert

Transport Canada reguliert die Ermüdung von Flugbesatzungen, weil Ermüdung ein Sicherheitsrisiko ist, nicht nur ein administratives Thema. Die Regeln sind darauf ausgelegt, kumulative Arbeitslast, Dienstzeitplanung, Ruhegelegenheit und Wachsamkeitsrisiko zu kontrollieren.

Deshalb berücksichtigen die Verordnungen Faktoren wie:

- Gesamtflugzeit über Fenster aufeinanderfolgender Tage
- Grenzen der Flugdienstperioden
- Meldezeit und zirkadianes Timing
- Anzahl der Flüge oder Sektoren
- Ruhezeiten und dienstfreie Zeit
- Betreiberüberwachung und Aufzeichnungen

Die operative Logik ist direkt: zwei Dienstpläne können die gleiche Anzahl von Dienststunden haben, aber je nach Timing, Häufigkeit, Sektoranzahl und vorheriger Akkumulation unterschiedliches Ermüdungsrisiko erzeugen.

Nützliche offizielle Referenzen:

- [Transport Canada: Flight and duty time regulations](https://tc.canada.ca/en/aviation/commercial-air-services/fatigue-management-aviation/flight-duty-time-regulations-prescriptive-vs-performance-based-options)
- [Transport Canada Advisory Circular AC 700-047](https://tc.canada.ca/en/aviation/reference-centre/advisory-circulars/advisory-circular-ac-no-700-047)
- [Canadian Aviation Regulations SOR/96/433](https://tc.canada.ca/en/corporate-services/acts-regulations/list-regulations/canadian-aviation-regulations-sor-96-433)

---

## Wie die rollierenden Fenster funktionieren

Die 28-Tage-Akkumulationsgrenze erfordert, dass die Gesamtflugzeit in beliebigen 28 aufeinanderfolgenden Tagen
100 Stunden nicht überschreitet. Das Fenster rutscht jeden Tag vor — es ist kein Kalendermonat.

| Datum | Fenster deckt ab | Nettoeffekt |
|---|---|---|
| 15. Juni | 19. Mai – 15. Juni | 92 h im Fenster |
| 16. Juni | 20. Mai – 16. Juni | − Stunden geflogen am 19. Mai + Stunden geflogen am 16. Juni |
| 17. Juni | 21. Mai – 17. Juni | rutscht weiter |

**Die Falle in Zahlen:**  
Der Pilot hat 92 Stunden im Fenster. Für 10 Stunden am 16. Juni eingeplant.

- Wenn er am 19. Mai 4 Stunden flog: 92 − 4 + 10 = **98 h** — legal.  
- Wenn er am 19. Mai 0 Stunden flog: 92 − 0 + 10 = **102 h** — Verstoß.

Ein mentales Modell mit monatlichem Zurücksetzen genehmigt beides. Das rollierende Fenster nicht.

Jeder Pilot trägt drei dieser Berechnungen gleichzeitig: 28-Tage, 90-Tage und 365-Tage.
Bei 15 Piloten sind das 45 live rollierende Berechnungen pro Dispositionszyklus, jede erfordert bis zu
365 Tage historische Nachschau. Die Mathematik erfordert kein Urteil. Automatisierung eliminiert die Fehlerklasse vollständig.

**Warum auch die Meldezeit FDP bestimmt:** Die FDP-Grenzen von Part 705 hängen vom Dienstbeginn ab.
Ein Dienst, der um 09:00 beginnt, darf legal bis zu 13 Stunden laufen; derselbe Dienst, der um 01:00
beginnt, ist auf nahe 11 Stunden begrenzt — weil er in das zirkadiane Fenster 02:00–05:59 reicht, wo
ermüdungsbedingte Fehlerraten stark ansteigen. Ein 30-minütiger Unterschied in der Meldezeit kann
das legale Maximum um bis zu 2 Stunden ändern. Die Sektoranzahl fügt eine zweite Dimension hinzu: jeder zusätzliche
Anflug und jede Landung akkumuliert messbare kognitive Last, und die Matrix reduziert die erlaubte
FDP entsprechend.

---

## Arbeitsmappen-Logik

Die Arbeitsmappe ist um einen praktischen Dispositions-Workflow organisiert:

1. Pilot- und geplante Zuweisungsdaten eingeben.
2. Den Operationskontext identifizieren.
3. Die relevante Dienst- und Flughistorie für diesen Piloten abrufen.
4. Rollierende Fenstersummen berechnen.
5. Geplante Zuweisung mit konfigurierten Grenzen vergleichen.
6. Klaren, Warn- oder Risikostatus markieren.
7. Aufzeichnungen für Überprüfung und Export bewahren.

Die Arbeitsmappe soll ein Entscheidungsunterstützungs- und Analysewerkzeug sein. Sie ersetzt nicht die rechtliche Verantwortung des Betreibers, die aktuellen CARs, das Firmenoperationshandbuch, genehmigte Ausnahmen oder FRMS-Verfahren zu interpretieren und anzuwenden.

---

## Kauf

Verwenden Sie hier die komplette Excel-Arbeitsmappe:

[Den kompletten Excel-Tracker kaufen](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

---

## Einschränkungen

- **Abhängigkeit der Datenintegrität** — Berechnungen sind nur so genau wie die Eingaben; verspätete, fehlende oder falsche Aufzeichnungen erzeugen ohne Warnung einen falschen Compliance-Status
- **Keine rechtliche Meinung** — diese Arbeitsmappe spiegelt die Interpretation des Autors der Verordnungen wider; die offizielle Position von Transport Canada gilt, und Grenzfallanwendungen sollten mit Rechtsberatern oder Ihrem TC Principal Operations Inspector validiert werden
- **Verzögerung bei Verordnungsänderungen** — CARs-Änderungen werden nicht automatisch übernommen; Betreiber sind dafür verantwortlich, TC-Verordnungsänderungen zu überwachen und die Arbeitsmappe entsprechend zu aktualisieren
- **Umfang: nur Part 702 und 705** — Betreiber unter Part 703 (Air Taxi) oder Part 704 (Commuter) arbeiten unter anderen spezifischen Grenzen, die in dieser Version nicht codiert sind
- **Skalierungsgrenze** — für 3–30 Piloten ausgelegt; jenseits von etwa 30 kann die Berechnungstiefe die Excel-Leistung beeinträchtigen
- **Empfindlichkeit der Excel-Version** — erfordert Excel 2016 oder höher unter Windows; das Verhalten in Excel für Mac oder Office 365 Web kann abweichen
- **Grenzfälle nicht vollständig automatisiert** — Bestimmungen für erweiterte Crew, Split-Duty-Regeln und bestimmte Ruhezeitverlängerungen beinhalten regulatorische Bedingungen, die Disponentenurteil erfordern und in dieser Version nicht vollständig codiert sind

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

## License

Verbreitet unter der [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---
