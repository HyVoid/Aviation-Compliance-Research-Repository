<!-- Language Navigation -->
<div align="center">

[English](#english) | [Français](#francais)

</div>

---

<a name="english"></a>

# Prevent Flight Duty Time Violations Before Dispatch

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)
![Language](https://img.shields.io/badge/lang-EN%20%7C%20FR-lightgrey)

**Designed for Canadian Part 702 and Part 705 operators who need to track flight time, duty time, fatigue exposure, and rolling compliance limits before a pilot is assigned.**

[Live Preview](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) | [Purchase Complete Excel](https://alexhasgreatestuff.gumroad.com/l/dutytracker)

</div>

Track rolling flight time limits, detect compliance risks in seconds, and maintain a single auditable source of truth for pilot duty records.

---

## Quick Preview

<!--
<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 11_47_04 AM" src="https://github.com/user-attachments/assets/cc792931-2477-40d4-9bd7-e92418817c77" />
-->


> View the interactive workbook preview: [pilot duty tracker demo](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)

---

## Why This Exists

Most flight and duty time violations are not caused by bad intentions.

They usually happen because rolling windows, mixed 702/705 activity, cumulative fatigue rules, reassigned duty, and fragmented records are difficult to monitor manually.

The risk is simple:

```text
Pilot assigned
-> Manual check
-> Prior records missed
-> Violation discovered after the flight
```

This workbook is designed to change the workflow:

```text
Pilot considered for assignment
-> Duty record entered once
-> Rolling limits checked automatically
-> Compliance risk flagged before dispatch
```

The commercial problem is not only regulation. It is operational visibility. Dispatchers and schedulers need to know whether a pilot can legally and safely take the next assignment before the flight is released.

---

## Three Compliance Traps That Catch Operators

### 1. Rolling windows are not calendar months

A 28-day, 90-day, or 365-day limit does not reset neatly when the month changes. Every proposed assignment creates a new lookback period.

If the proposed flight is on May 31, the relevant 28-day window may start on May 4. On June 1, the same check moves forward by one day. A manual month-end total can therefore look clean while the rolling window is already over the limit.

### 2. Mixed 702/705 operations hide cumulative exposure

Small and mid-size operators may use the same pilot across aerial work, charter, airline-style operations, positioning, reserve, or reassigned duty.

The compliance risk is not always inside one operation type. It often appears when records from multiple workflows are combined.

### 3. Manual checks fail at the relationship level

The error is rarely obvious in a single row.

It is usually hidden in the relationship between:

- today's planned duty
- the pilot's previous duty history
- report time
- sector count
- flight time accumulation
- required rest
- operator-specific procedures

That is why manual spreadsheet review often catches the issue late, or misses it entirely.

---

## Who This Tool Is For

| User | Practical Use Case |
|---|---|
| Flight dispatchers | Check pilot availability before issuing a dispatch release |
| Crew schedulers | Build rosters with visibility into remaining legal capacity |
| Chief pilots | Review pilot workload and cumulative exposure before approving assignments |
| Safety managers | Maintain structured records for internal review and audit preparation |
| Small AOC operators | Replace scattered manual tracking with one lightweight Excel workflow |

Best suited for Canadian operators with small to mid-size pilot groups, especially where full enterprise crew management software is too expensive or too heavy for daily operations.

---

## What The Workbook Does

### Duty Time Tracking

Record pilot duty, flight time, rest, operation type, report time, sectors, and assignment notes in a structured format.

### Rolling Window Monitoring

Monitor cumulative limits across rolling periods such as:

- 28 days
- 90 days
- 365 days

The workbook checks the relevant pilot history each time a new assignment is entered.

### Pre-dispatch Validation

Flag potential compliance risks before a pilot is assigned, instead of discovering the issue after the flight.

### Audit Reporting

Maintain a filterable record history that can support internal reviews, management reporting, and audit preparation.

### Single Source Of Truth

Keep dispatcher, scheduler, safety, and management views aligned around the same workbook data.

---

## Example Scenario

This is a simplified example, not a legal determination.

| Operator Profile | Situation |
|---|---|
| 12 pilots | Mixed Part 702 and Part 705 activity |
| Daily scheduling changes | Charter, aerial work, reassignment, and reserve coverage |
| Manual process | Dispatcher checks multiple spreadsheets and pilot records |
| Business risk | A rolling limit can be missed before morning dispatch |

### Before

- Manual checks every morning
- Separate dispatcher and pilot records
- Calendar-period summaries mistaken for rolling-window compliance
- Compliance conflicts discovered late

### After

- One workbook for pilot duty records
- Automatic rolling-window calculations
- Pre-dispatch warning status
- Filterable historical records for review

The value is not that Excel replaces compliance judgment. The value is that routine calculations stop depending on memory, copy-paste checks, and fragmented files.

---

## Why The Regulation Works This Way

Transport Canada regulates flight crew fatigue because fatigue is a safety hazard, not only an administrative issue. The rules are designed to control cumulative workload, duty timing, rest opportunity, and alertness risk.

That is why the regulations consider factors such as:

- total flight time across consecutive-day windows
- flight duty period limits
- report time and circadian timing
- number of flights or sectors
- rest periods and time free from duty
- operator monitoring and records

The operational logic is direct: two schedules can have the same number of duty hours but create different fatigue risk depending on timing, frequency, sector count, and prior accumulation.

Useful official references:

- [Transport Canada: Flight and duty time regulations](https://tc.canada.ca/en/aviation/commercial-air-services/fatigue-management-aviation/flight-duty-time-regulations-prescriptive-vs-performance-based-options)
- [Transport Canada Advisory Circular AC 700-047](https://tc.canada.ca/en/aviation/reference-centre/advisory-circulars/advisory-circular-ac-no-700-047)
- [Canadian Aviation Regulations SOR/96-433](https://tc.canada.ca/en/corporate-services/acts-regulations/list-regulations/canadian-aviation-regulations-sor-96-433)

---

## How Rolling Window Calculation Works

For a proposed assignment date `D` and a window length of `N` days:

```text
Window start = D - (N - 1)
Window end   = D

Included records =
all applicable records for the same pilot
between Window start and Window end

Remaining capacity =
regulatory limit
- prior included records
- proposed assignment
```

Example:

```text
Proposed assignment date: May 31
Rolling period: 28 days
Included window: May 4 through May 31
```

On June 1, the window becomes May 5 through June 1. The check moves every day. It does not reset because a new calendar month has started.

---

## Workbook Logic

The workbook is organized around a practical dispatch workflow:

1. Enter pilot and planned assignment data.
2. Identify the operation context.
3. Pull the relevant duty and flight history for that pilot.
4. Calculate rolling-window totals.
5. Compare planned assignment against configured limits.
6. Flag clear, warning, or risk status.
7. Preserve records for review and export.

The workbook is intended to be a decision-support and analysis tool. It does not replace the operator's legal responsibility to interpret and apply the current CARs, company operations manual, approved exemptions, or FRMS procedures.

---

## Purchase

Use the complete Excel workbook here:

[Purchase the complete Excel tracker](https://alexhasgreatestuff.gumroad.com/l/dutytracker)

---

## Limitations

This workbook is not legal advice and is not an official Transport Canada system.

Operators should verify the workbook configuration against:

- the current Canadian Aviation Regulations
- the operator's Air Operator Certificate
- company operations manual procedures
- approved FRMS, exemptions, or operations specifications
- Transport Canada guidance or inspector direction
- operator-specific treatment of reserve, standby, positioning, unforeseen operational circumstances, augmented crew, medevac, and other special cases

The workbook cannot correct inaccurate or missing source data. If flight time, duty time, rest periods, outside flying, or reassignment records are incomplete, the output may appear compliant while the real operation is not.

Regulatory references should be reviewed periodically because CARs provisions, advisory circulars, and Transport Canada guidance may change.

---

## About This Project

This workbook is part of a broader effort to translate complex operational and regulatory
requirements into lightweight tools that small and medium-sized organizations can actually use.

No ERP. No custom software project. No additional accounts.

Just clear business logic, structured data, and repeatable decision support —
delivered in software your team already has.

If your operation involves compliance, scheduling, or resource allocation problems
that currently live in someone's head or a disconnected spreadsheet,
[see what else is available →](https://alexhasgreatestuff.gumroad.com)

---

## License

Distributed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---

<div align="right"><a href="#english">Top (EN)</a> | <a href="#francais">Français</a></div>

---
---

<a name="francais"></a>

# Prévenir les infractions de temps de service de vol avant la répartition

<div align="center">

![Licence](https://img.shields.io/badge/licence-Apache%202.0-blue)
![Plateforme](https://img.shields.io/badge/plateforme-Microsoft%20Excel-217346)
![Réglementation](https://img.shields.io/badge/réglementation-RAC%20702%2F705-red)
![Langue](https://img.shields.io/badge/langue-EN%20%7C%20FR-lightgrey)

**Conçu pour les exploitants canadiens des Parties 702 et 705 qui doivent suivre le temps de vol, le temps de service, l'exposition à la fatigue et les limites de conformité glissantes avant d'assigner un pilote.**

[Aperçu en direct](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) | [Acheter le classeur Excel complet](https://alexhasgreatestuff.gumroad.com/l/dutytracker)

</div>

Suivre les limites glissantes de temps de vol, détecter les risques de conformité en quelques secondes et maintenir une source unique de vérité auditable pour les dossiers de service des pilotes.

---

## Aperçu rapide

<!--
<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 11_47_04 AM" src="https://github.com/user-attachments/assets/5b0a5f06-fea7-4a93-a64f-af0130e39ff1" />

-->


> Voir l'aperçu interactif du classeur : [démonstration du suivi de service pilote](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)

---

## Pourquoi cet outil existe

La plupart des infractions de temps de vol et de service ne viennent pas d'une mauvaise intention.

Elles surviennent souvent parce que les fenêtres glissantes, les activités mixtes 702/705, les calculs cumulatifs de fatigue, les réaffectations et les dossiers fragmentés sont difficiles à surveiller manuellement.

Le risque est simple :

```text
Pilote assigné
-> Vérification manuelle
-> Dossiers antérieurs oubliés
-> Infraction découverte après le vol
```

Ce classeur vise a modifier le flux de travail :

```text
Pilote envisagé pour une affectation
-> Données de service saisies une fois
-> Limites glissantes vérifiées automatiquement
-> Risque de conformité signalé avant la répartition
```

Le problème commercial n'est pas seulement la réglementation. C'est la visibilité opérationnelle. Les répartiteurs et planificateurs doivent savoir si un pilote peut légalement et raisonnablement accepter la prochaine affectation avant la libération du vol.

---

## Trois pièges de conformité qui touchent les exploitants

### 1. Les fenêtres glissantes ne sont pas des mois civils

Une limite de 28, 90 ou 365 jours ne se réinitialise pas proprement lorsque le mois change. Chaque affectation proposée crée une nouvelle période de recul.

Si le vol proposé est le 31 mai, la fenêtre pertinente de 28 jours peut commencer le 4 mai. Le 1er juin, la même vérification avance d'un jour. Un total de fin de mois peut donc paraître conforme alors que la fenêtre glissante dépasse déjà une limite.

### 2. Les opérations mixtes 702/705 cachent l'exposition cumulative

Les petits et moyens exploitants peuvent utiliser le même pilote pour du travail aérien, de l'affrètement, des opérations de type compagnie aérienne, de la mise en place, de la réserve ou des réaffectations.

Le risque de conformité n'est pas toujours visible dans un seul type d'exploitation. Il apparaît souvent lorsque les dossiers de plusieurs flux de travail sont combinés.

### 3. Les contrôles manuels échouent au niveau des relations entre données

L'erreur est rarement évidente dans une seule ligne.

Elle se cache souvent dans la relation entre :

- l'affectation prévue aujourd'hui
- l'historique de service du pilote
- l'heure de présentation
- le nombre de secteurs
- l'accumulation du temps de vol
- le repos requis
- les procédures propres à l'exploitant

C'est pourquoi la vérification manuelle par feuille de calcul détecte souvent le problème trop tard, ou ne le détecte pas.

---

## À qui s'adresse cet outil

| Utilisateur | Cas d'utilisation pratique |
|---|---|
| Répartiteurs | Vérifier la disponibilité d'un pilote avant l'autorisation de départ |
| Planificateurs d'équipage | Construire les horaires avec visibilité sur la capacité légale restante |
| Chefs pilotes | Examiner la charge et l'exposition cumulative avant d'approuver une affectation |
| Responsables sécurité | Maintenir des dossiers structurés pour revue interne et préparation d'audit |
| Petits exploitants AOC | Remplacer le suivi manuel dispersé par un flux Excel léger |

Particulièrement adapté aux exploitants canadiens avec des groupes de pilotes petits à moyens, surtout lorsque les logiciels de gestion d'équipage d'entreprise sont trop coûteux ou trop lourds pour les opérations quotidiennes.

---

## Ce que fait le classeur

### Suivi du temps de service

Consigner le service pilote, le temps de vol, le repos, le type d'exploitation, l'heure de présentation, les secteurs et les notes d'affectation dans un format structuré.

### Surveillance des fenêtres glissantes

Suivre les limites cumulatives sur des périodes glissantes telles que :

- 28 jours
- 90 jours
- 365 jours

Le classeur vérifie l'historique pertinent du pilote chaque fois qu'une nouvelle affectation est saisie.

### Validation avant répartition

Signaler les risques potentiels de conformité avant l'assignation du pilote, plutôt que découvrir le problème après le vol.

### Rapports d'audit

Conserver un historique filtrable pouvant soutenir les revues internes, les rapports de gestion et la préparation d'audit.

### Source unique de vérité

Aligner les vues répartition, planification, sécurité et direction autour des mêmes données de classeur.

---

## Scénario d'exemple

Il s'agit d'un exemple simplifié, et non d'une détermination juridique.

| Profil de l'exploitant | Situation |
|---|---|
| 12 pilotes | Activités mixtes Partie 702 et Partie 705 |
| Changements quotidiens | Affrètement, travail aérien, réaffectation et couverture de réserve |
| Processus manuel | Le répartiteur vérifie plusieurs feuilles de calcul et dossiers pilote |
| Risque commercial | Une limite glissante peut être oubliée avant la répartition du matin |

### Avant

- Vérifications manuelles chaque matin
- Dossiers répartiteur et pilote séparés
- Totaux par période civile confondus avec la conformité par fenêtre glissante
- Conflits de conformité découverts tardivement

### Après

- Un classeur unique pour les dossiers de service pilote
- Calculs automatiques de fenêtres glissantes
- Statut d'avertissement avant répartition
- Dossiers historiques filtrables pour revue

La valeur n'est pas qu'Excel remplace le jugement de conformité. La valeur est que les calculs répétitifs ne dépendent plus de la mémoire, des contrôles par copier-coller et des fichiers fragmentés.

---

## Pourquoi la réglementation fonctionne ainsi

Transports Canada encadre la fatigue des équipages de conduite parce que la fatigue est un risque de sécurité, pas seulement une question administrative. Les règles visent à contrôler la charge cumulative, le moment du service, l'occasion de repos et le risque de perte de vigilance.

C'est pourquoi la réglementation tient compte de facteurs tels que :

- le temps de vol total sur des périodes de jours consécutifs
- les limites de période de service de vol
- l'heure de présentation et le rythme circadien
- le nombre de vols ou secteurs
- les périodes de repos et le temps libre de service
- le suivi et les dossiers de l'exploitant

La logique opérationnelle est directe : deux horaires peuvent avoir le même nombre d'heures de service mais créer des risques de fatigue différents selon le moment, la fréquence, le nombre de secteurs et l'accumulation antérieure.

Références officielles utiles :

- [Transports Canada : réglementation sur le temps de vol et de service](https://tc.canada.ca/en/aviation/commercial-air-services/fatigue-management-aviation/flight-duty-time-regulations-prescriptive-vs-performance-based-options)
- [Circulaire d'information AC 700-047 de Transports Canada](https://tc.canada.ca/en/aviation/reference-centre/advisory-circulars/advisory-circular-ac-no-700-047)
- [Règlement de l'aviation canadien SOR/96-433](https://tc.canada.ca/en/corporate-services/acts-regulations/list-regulations/canadian-aviation-regulations-sor-96-433)

---

## Fonctionnement du calcul par fenêtre glissante

Pour une date d'affectation proposée `D` et une fenêtre de `N` jours :

```text
Début de fenêtre = D - (N - 1)
Fin de fenêtre   = D

Dossiers inclus =
tous les dossiers applicables du même pilote
entre le début et la fin de fenêtre

Capacité restante =
limite réglementaire
- dossiers antérieurs inclus
- affectation proposée
```

Exemple :

```text
Date d'affectation proposée : 31 mai
Période glissante : 28 jours
Fenêtre incluse : 4 mai au 31 mai
```

Le 1er juin, la fenêtre devient le 5 mai au 1er juin. La vérification avance chaque jour. Elle ne se réinitialise pas parce qu'un nouveau mois civil a commencé.

---

## Logique du classeur

Le classeur est organisé autour d'un flux pratique de répartition :

1. Saisir les données pilote et l'affectation prévue.
2. Identifier le contexte d'exploitation.
3. Extraire l'historique de vol et de service pertinent pour ce pilote.
4. Calculer les totaux par fenêtre glissante.
5. Comparer l'affectation prévue aux limites configurées.
6. Signaler un statut clair, avertissement ou risque.
7. Conserver les dossiers pour revue et export.

Le classeur est conçu comme un outil d'aide à la décision et d'analyse. Il ne remplace pas la responsabilité juridique de l'exploitant d'interpréter et d'appliquer le RAC en vigueur, le manuel d'exploitation de la compagnie, les exemptions approuvées ou les procédures SGRF.

---

## Achat

Utiliser le classeur Excel complet ici :

[Acheter le suivi Excel complet](https://alexhasgreatestuff.gumroad.com/l/dutytracker)

---

## Limites

Ce classeur n'est pas un avis juridique et n'est pas un systeme officiel de Transports Canada.

Les exploitants doivent vérifier la configuration du classeur avec :

- le Règlement de l'aviation canadien en vigueur
- le certificat d'exploitation aérienne de l'exploitant
- les procédures du manuel d'exploitation de la compagnie
- les SGRF, exemptions ou spécifications d'exploitation approuvés
- les lignes directrices ou instructions de Transports Canada
- le traitement propre à l'exploitant concernant réserve, attente, mise en place, circonstances opérationnelles imprévues, équipage renforcé, évacuation médicale et autres cas particuliers

Le classeur ne peut pas corriger des données sources inexactes ou manquantes. Si les temps de vol, temps de service, périodes de repos, vols externes ou réaffectations sont incomplets, le résultat peut paraître conforme alors que l'exploitation réelle ne l'est pas.

Les références réglementaires doivent être revues périodiquement, car les dispositions du RAC, les circulaires d'information et les lignes directrices de Transports Canada peuvent changer.

---

## À propos de ce projet

Ce classeur fait partie d'un effort plus large visant à traduire des exigences opérationnelles
et réglementaires complexes en outils légers que les organisations de taille petite et moyenne
peuvent réellement utiliser.

Pas d'ERP. Pas de projet logiciel sur mesure. Pas de comptes supplémentaires.

Juste une logique métier claire, des données structurées et un support de décision
reproductible — dans les outils que votre équipe utilise déjà.

Si vos opérations comportent des problèmes de conformité, de planification ou d'allocation
de ressources qui résident actuellement dans la tête de quelqu'un ou dans un tableur déconnecté,
[voir ce qui est disponible →](https://alexhasgreatestuff.gumroad.com/)

---

## Licence

Distribué sous la [licence Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---

<div align="right"><a href="#francais">Haut de page (FR)</a> | <a href="#english">English</a></div>
