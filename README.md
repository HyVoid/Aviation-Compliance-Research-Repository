<!-- Language Navigation -->
<div align="center">

[English](#english) · [Français](#français)

</div>

---

<a name="english"></a>

# ✈️ CARs Part 702/705 — Flight & Duty Time Compliance Tracker

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)
![Language](https://img.shields.io/badge/lang-EN%20%7C%20FR-lightgrey)

**A compliance-grade Excel tool for Canadian aviation operators under Transport Canada CARs Part 702 and Part 705.**

[Purchase for complete Excel](https://alexhasgreatestuff.gumroad.com/l/dutytracker)
</div>

---

## Regulatory Background

Transport Canada’s flight and duty time limits are **not optional guidelines** — they are legally binding rules designed to prevent fatigue‑related accidents. Under CARs Part 702 (aerial work) and Part 705 (commercial air transport), exceeding prescribed flight time or duty time can lead to:

- Heavy monetary penalties
- Suspension of the Air Operator Certificate (AOC)
- Individual licence sanctions

### Why the regulation exists

Decades of accident investigation data show that pilot fatigue impairs judgement, reaction time, and decision‑making at a level comparable to alcohol intoxication. The prescriptive limits — maximum flight hours per rolling window, maximum flight duty period (FDP) based on start time and number of sectors — are the regulator’s way of embedding fatigue science directly into operational boundaries. Every constraint you see in the rules is there because a fatigue‑related incident has happened before.

### Most common sources of non‑compliance

In practice, violations rarely come from a single extreme event. They usually accumulate silently through:

1. **Mixed 702/705 operations** – A pilot flies aerial work in the morning and a charter flight in the evening. Hours from both subparts are pooled; forgetting to aggregate them causes an unseen breach.
2. **Overlapping rolling windows** – A flight that is legal inside the 28‑day window may push the 90‑day or 365‑day total over the limit, but manual checks often only look at the most immediate window.
3. **Incorrect FDP determination** – The Part 705 FDP matrix changes based on report time and number of sectors. A dispatcher who relies on memory or a static cheat sheet easily picks the wrong maximum duty period.
4. **Post‑facto discovery** – Without a pre‑flight compliance gate, violations are found days or weeks later during a manual audit, when the damage is already done.

---

## Industry Problem

Small to mid‑size AOC holders operating under both Part 702 and Part 705 face a disproportionate compliance burden:

- **A single pilot can change roles daily**, blending flight time and duty time across two regulatory subparts.
- **Manual tracking is fragile.** A dispatcher must remember or re‑calculate multiple accumulation windows (28 days, 90 days, 365 days) for every pilot, every assignment.
- **Human error is the norm, not the exception.** A forgotten early‑morning sector, a missed day of recurrent training credited as duty, or an incorrect FDP matrix lookup — any one of these can trigger a violation.
- **Audit preparation is reactive.** When Transport Canada requests records, teams often spend 2–3 days reconstructing logbook entries, flight reports, and dispatch notes, hoping nothing is inconsistent.

### Why manual checks systematically miss violations

- **Mental arithmetic under time pressure** — Dispatchers frequently make scheduling decisions in under a minute. Calculating three separate rolling window totals (each requiring a review of up to 365 days of history) is cognitively unrealistic.
- **No unified view** — Flight time and duty time are often kept in separate silos (pilot logbooks, dispatch software, spreadsheets). Gaps between these records are invisible until reconciliation.
- **Window “edge effects”** — A flight that drops out of the 28‑day window on day 29 might suddenly make a pilot legal again, while simultaneously pushing the 90‑day window to its limit. These interdependencies are almost impossible to track by hand.

For operators with 3–30 pilots, enterprise crew management systems costing hundreds of thousands of dollars are out of reach, yet spreadsheet‑only approaches break down as complexity grows.

---

## Compliance Logic

This Excel workbook acts as a **pre‑flight compliance gate**, not a post‑flight recorder. Its core principle: *the moment a dispatcher enters a proposed duty, all regulatory limits are checked instantly — before the pilot is assigned.*

### How rolling time windows are calculated

The tool continuously maintains three sliding windows — 28 days, 90 days, and 365 days — based on the date of the proposed flight. For any given pilot:

1. All past flights and duties are stored as dated records.
2. When a new assignment is entered, the workbook uses `SUMIFS` formulas to sum flight time and duty time where `Date ≥ (ProposedDate − WindowLength)`.
3. The result is compared against the CARs limits (e.g., 100 hours in 28 days, 300 hours in 90 days, 1,200 hours in 365 days for Part 705).
4. If the addition of the new assignment would exceed any window, the cell turns red and blocks the assignment — before any operational commitment is made.

### Pre‑encoded regulation engine

- **Part 705 FDP matrix** (report time × number of sectors) is fully built into the logic. The dispatcher does not need to look up a table; the tool automatically selects the correct maximum FDP.
- **Part 702 limits** are embedded alongside Part 705, and hours accumulate across both subparts in a single view.
- **Real‑time remaining legality** is displayed for every pilot, so schedulers building rosters 7–14 days out can see exactly how many hours remain before a limit is breached.

### Operational impact

| Dimension | Before | After |
|---|---|---|
| Violation risk | Discovered post‑flight; TC penalties applied retroactively | Blocked before dispatch; 100% pre‑flight interception |
| Scheduling check time | 20–30 min per pilot, per check | Under 3 seconds |
| Audit preparation | 2–3 days to reconstruct records | Filter and export in under 5 seconds |
| Crew utilisation | 1–2 hour manual buffer routinely wasted | Minute‑level precision; every legal minute accounted for |
| Data consistency | Dispatcher and pilot copies frequently diverge | Single source of truth across all records and reports |

---

## Calculation Method

Without exposing proprietary formulas, here is how the workbook automates what is otherwise a manual minefield:

- **Flight Duty Period (FDP)**: The dispatcher enters the pilot’s report time and the number of sectors. The workbook retrieves the maximum allowable FDP from the encoded matrix (e.g., 14 hours for a 0600 report with 1–4 sectors, reducing to 9 hours for certain late‑night reports). The actual duty end time is validated against this limit.
- **Cumulative flight time**: Each flight’s block time is logged. The workbook sums these values across the three rolling windows using date‑conditional aggregation. As the calendar advances, older flights automatically fall out of the summation range — giving a true sliding‑window calculation.
- **Duty time accumulation**: Separate from flight time, total duty hours (including pre‑ and post‑flight duties, standby, and training) are tracked and checked against the same 28/90/365‑day rolling windows where applicable.
- **Cross‑subpart pooling**: A pilot’s records are tagged by subpart (702/705), but all hours flow into the same accumulation pools, exactly as required by the regulation. There is no risk of double‑counting or omission.

This method replaces what would otherwise be a tedious, multi‑spreadsheet reconciliation — a process that, when done manually, is the single largest source of late‑discovered non‑compliance.

---

## Workbook Demo

> 🔗 **[View live preview →](https://hyvoid.github.io/pilot-duty-tracker-designed-for-Part-702-and-Part-705-operations/)**

The preview demonstrates the pre‑flight validation flow, colour‑coded legality indicators, and the dispatch‑ready dashboard. No sign‑up, no installation — see exactly how a duty entry becomes an instant compliance check.

---

## Limitations

- **Excel‑based**: Requires Microsoft Excel (desktop or compatible). It is not a web application and does not offer real‑time multi‑user synchronisation.
- **Manual data entry**: Flight and duty records must be entered by the dispatcher or scheduler. The tool does not ingest data directly from ACARS, crew scheduling platforms, or electronic logbooks.
- **Regulatory scope**: Covers Part 702 and Part 705 only. It does not address Part 703, 704, or non‑Canadian regulations (EASA, FAA). Operators with split‑authority operations outside these subparts should verify supplementary rules separately.
- **Interpretative responsibility**: The workbook encodes published limits and standard interpretations, but ultimate compliance remains the operator’s responsibility. Updates to regulations or company‑specific exemptions (e.g., fatigue risk management system adjustments) must be validated by the user.
- **No fatigue modelling**: It enforces prescriptive limits, not predictive fatigue science (e.g., SAFE model). It is a compliance tracking tool, not a biomathematical fatigue management system.

---

## Purchase

> 🛒 **[Get the complete Excel workbook on Gumroad →](https://alexhasgreatestuff.gumroad.com/l/njeyey)**

---

## License

Distributed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---

<br>
<div align="right"><a href="#english">↑ Top (EN)</a> · <a href="#français">Français →</a></div>

---
---

<a name="français"></a>

# ✈️ RAC Parties 702/705 — Outil de suivi de conformité temps de vol et de service

<div align="center">

![Licence](https://img.shields.io/badge/licence-Apache%202.0-blue)
![Plateforme](https://img.shields.io/badge/plateforme-Microsoft%20Excel-217346)
![Réglementation](https://img.shields.io/badge/réglementation-RAC%20702%2F705-red)
![Langue](https://img.shields.io/badge/langue-EN%20%7C%20FR-lightgrey)

**Un outil Excel de niveau conformité pour les exploitants aériens canadiens assujettis aux Parties 702 et 705 du RAC de Transports Canada.**

[Acheter le classeur complet](https://alexhasgreatestuff.gumroad.com/l/dutytracker)
</div>

---

## Contexte réglementaire

Les limites de temps de vol et de service imposées par Transports Canada **ne sont pas de simples recommandations** — ce sont des obligations légales conçues pour prévenir les accidents liés à la fatigue. En vertu de la Partie 702 (travail aérien) et de la Partie 705 (transport aérien commercial) du RAC, tout dépassement peut entraîner :

- De lourdes amendes
- La suspension du certificat d’exploitation aérienne (CEA)
- Des sanctions sur les licences individuelles

### Pourquoi une telle réglementation

Des décennies de données d’accidents montrent que la fatigue des pilotes altère le jugement, les réflexes et la prise de décision, à un niveau comparable à l’intoxication alcoolique. Les limites prescriptives — heures de vol maximales par fenêtre glissante, période de service de vol (PSV) maximale selon l’heure de présentation et le nombre de secteurs — sont le moyen par lequel le régulateur intègre la science de la fatigue directement dans les opérations. Chaque contrainte présente dans la réglementation existe parce qu’un incident lié à la fatigue s’est déjà produit.

### Sources les plus fréquentes de non‑conformité

En pratique, les infractions résultent rarement d’un seul événement extrême. Elles s’accumulent silencieusement :

1. **Opérations mixtes 702/705** – Un pilote effectue du travail aérien le matin et un vol affrété le soir. Les heures des deux sous‑parties sont cumulées; oublier de les agréger conduit à un dépassement invisible.
2. **Fenêtres glissantes superposées** – Un vol qui est légal sur la fenêtre de 28 jours peut faire dépasser le cumul 90 ou 365 jours, mais les vérifications manuelles ne regardent souvent que la fenêtre la plus immédiate.
3. **Détermination incorrecte de la PSV** – La matrice PSV de la Partie 705 varie selon l’heure de présentation et le nombre de secteurs. Un répartiteur qui se fie à sa mémoire ou à un aide‑mémoire statique choisit facilement la mauvaise limite.
4. **Découverte a posteriori** – Sans contrôle de conformité avant le vol, les infractions sont découvertes des jours ou des semaines plus tard, lors d’un audit manuel, quand le mal est déjà fait.

---

## Problématique sectorielle

Les petits et moyens exploitants détenant une double autorisation 702/705 subissent une pression de conformité disproportionnée :

- **Un même pilote peut changer de rôle quotidiennement**, mélangeant temps de vol et temps de service entre deux sous‑parties réglementaires.
- **Le suivi manuel est fragile.** Un répartiteur doit mémoriser ou recalculer plusieurs fenêtres d’accumulation (28, 90, 365 jours) pour chaque pilote, à chaque affectation.
- **L’erreur humaine est la norme, pas l’exception.** Un secteur tôt le matin oublié, une journée de formation périodique comptabilisée comme service, ou une mauvaise lecture de la matrice PSV — un seul de ces éléments peut entraîner une infraction.
- **La préparation aux audits est réactive.** Lorsque Transports Canada demande les dossiers, les équipes passent souvent 2 à 3 jours à reconstituer des carnets de vol, des rapports de vol et des notes de répartition, en espérant qu’il n’y ait pas d’incohérence.

### Pourquoi les vérifications manuelles laissent passer des infractions

- **Calcul mental sous pression** — Les répartiteurs prennent souvent des décisions en moins d’une minute. Additionner trois totaux de fenêtres glissantes (nécessitant l’examen d’un historique pouvant aller jusqu’à 365 jours) est cognitivement irréaliste.
- **Absence de vue unifiée** — Le temps de vol et le temps de service sont souvent conservés dans des silos distincts (carnets de vol pilotes, logiciels de répartition, tableurs). Les écarts entre ces sources restent invisibles jusqu’à la réconciliation.
- **Effets de bord des fenêtres** — Un vol qui sort de la fenêtre de 28 jours au 29ᵉ jour peut soudainement rendre un pilote à nouveau légal, tout en poussant la fenêtre de 90 jours à sa limite. Ces interdépendances sont quasi impossibles à suivre manuellement.

Pour les exploitants de 3 à 30 pilotes, les logiciels de gestion d’équipage d’entreprise coûtant des centaines de milliers de dollars sont inaccessibles, tandis que les approches purement tableur ne suffisent plus.

---

## Logique de conformité

Ce classeur Excel fonctionne comme un **poste de contrôle de conformité avant le vol**, et non comme un simple enregistreur a posteriori. Son principe fondamental : *dès qu’un répartiteur saisit un service proposé, toutes les limites réglementaires sont vérifiées instantanément — avant que le pilote ne soit assigné.*

### Comment les fenêtres glissantes sont calculées

L’outil maintient en continu trois fenêtres glissantes — 28 jours, 90 jours et 365 jours — basées sur la date du vol proposé. Pour un pilote donné :

1. Tous les vols et services antérieurs sont stockés sous forme d’enregistrements datés.
2. Lorsqu’une nouvelle affectation est saisie, le classeur utilise des formules `SUMIFS` pour additionner le temps de vol et le temps de service lorsque `Date ≥ (DateProposée − DuréeFenêtre)`.
3. Le résultat est comparé aux limites du RAC (par ex., 100 heures en 28 jours, 300 heures en 90 jours, 1 200 heures en 365 jours pour la Partie 705).
4. Si l’ajout de la nouvelle affectation dépasse l’une des fenêtres, la cellule passe au rouge et bloque l’affectation — avant tout engagement opérationnel.

### Moteur réglementaire pré‑encodé

- **La matrice PSV de la Partie 705** (heure de présentation × nombre de secteurs) est entièrement intégrée. Le répartiteur n’a pas besoin de consulter une table ; l’outil sélectionne automatiquement la PSV maximale correcte.
- **Les limites de la Partie 702** sont intégrées aux côtés de celles de la Partie 705, et les heures s’accumulent dans une vue unique, toutes sous‑parties confondues.
- **Le temps restant légal** est affiché en temps réel pour chaque pilote, permettant aux planificateurs de construire des tableaux de service sur 7 à 14 jours avec une visibilité parfaite.

### Impact opérationnel

| Dimension | Avant | Après |
|---|---|---|
| Risque d’infraction | Détecté après le vol ; pénalités TC appliquées rétroactivement | Bloqué avant la répartition ; interception pré‑vol à 100 % |
| Durée de vérification | 20–30 min par pilote, par vérification | Moins de 3 secondes |
| Préparation aux audits | 2–3 jours pour reconstituer les dossiers | Filtrer et exporter en moins de 5 secondes |
| Utilisation des équipages | Tampon manuel de 1–2 heures régulièrement gaspillé | Précision à la minute ; chaque minute légale comptabilisée |
| Cohérence des données | Copie répartiteur et copie pilote fréquemment divergentes | Source unique de vérité pour tous les dossiers et rapports |

---

## Méthode de calcul

Sans dévoiler les formules propriétaires, voici comment le classeur automatise ce qui constitue autrement un terrain miné manuel :

- **Période de service de vol (PSV)** : Le répartiteur saisit l’heure de présentation du pilote et le nombre de secteurs. Le classeur extrait la PSV maximale autorisée de la matrice encodée (par ex., 14 heures pour une présentation à 06h00 avec 1–4 secteurs, réduite à 9 heures pour certaines présentations nocturnes). L’heure de fin de service réelle est validée par rapport à cette limite.
- **Temps de vol cumulé** : Le temps bloc de chaque vol est enregistré. Le classeur additionne ces valeurs sur les trois fenêtres glissantes en utilisant une agrégation conditionnelle à la date. Au fil du calendrier, les vols plus anciens sortent automatiquement de la plage de sommation — réalisant un véritable calcul de fenêtre glissante.
- **Cumul du temps de service** : Distinct du temps de vol, le temps de service total (incluant les tâches avant et après vol, la mise en place et la formation) est suivi et vérifié sur les mêmes fenêtres de 28, 90 et 365 jours lorsque la réglementation l’exige.
- **Cumul inter‑sous‑parties** : Les enregistrements d’un pilote sont étiquetés par sous‑partie (702/705), mais toutes les heures alimentent les mêmes bassins d’accumulation, exactement comme l’exige la réglementation. Il n’y a aucun risque de double comptage ou d’omission.

Cette méthode remplace ce qui serait autrement une réconciliation fastidieuse sur plusieurs feuilles de calcul — un processus qui, effectué manuellement, constitue la principale source d’infractions découvertes tardivement.

---

## Démonstration du classeur

> 🔗 **[Voir l’aperçu en direct →](https://hyvoid.github.io/pilot-duty-tracker-designed-for-Part-702-and-Part-705-operations/)**

L’aperçu montre le flux de validation avant vol, les indicateurs de légalité par code couleur et le tableau de bord prêt pour la répartition. Aucune inscription, aucune installation — voyez comment une saisie de service devient instantanément une vérification de conformité.

---

## Limitations

- **Basé sur Excel** : Nécessite Microsoft Excel (bureau ou compatible). Il ne s’agit pas d’une application web et il n’offre pas de synchronisation multi‑utilisateurs en temps réel.
- **Saisie manuelle des données** : Les enregistrements de vol et de service doivent être saisis par le répartiteur ou le planificateur. L’outil ne récupère pas les données directement d’un système ACARS, d’une plateforme de gestion d’équipage ou de carnets de vol électroniques.
- **Portée réglementaire** : Couvre uniquement les Parties 702 et 705. Il ne traite pas les Parties 703, 704 ni les réglementations non canadiennes (EASA, FAA). Les exploitants ayant des opérations mixtes en dehors de ces sous‑parties doivent vérifier les règles supplémentaires séparément.
- **Responsabilité d’interprétation** : Le classeur encode les limites publiées et les interprétations standard, mais la conformité ultime relève de la responsabilité de l’exploitant. Les mises à jour réglementaires ou les exemptions spécifiques à l’entreprise (p. ex., ajustements liés à un système de gestion des risques de fatigue) doivent être validées par l’utilisateur.
- **Pas de modélisation de la fatigue** : Il applique des limites prescriptives, et non une science prédictive de la fatigue (comme le modèle SAFE). C’est un outil de suivi de conformité, pas un système de gestion de la fatigue biomathématique.

---

## Achat

> 🛒 **[Obtenir le classeur Excel complet sur Gumroad →](https://alexhasgreatestuff.gumroad.com/l/njeyey)**

---

## Licence

Distribué sous la [licence Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---

<br>
<div align="right"><a href="#français">↑ Haut de page (FR)</a> · <a href="#english">← English</a></div>
