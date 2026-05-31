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

Transport Canada's CARs Part 702 (aerial work) and Part 705 (commercial air transport) impose legally binding limits on pilot flight time and duty time. These are not advisory guidelines — violations can result in heavy fines, suspension of the Air Operator Certificate (AOC), and individual licence penalties.

These regulations are rooted in decades of accident investigation linking crew fatigue to controlled-flight-into-terrain (CFIT), approach-and-landing accidents, and loss-of-control events. Their structure reflects three underlying principles:

**Circadian alignment.** The human body is not equally alert at all hours. Duty periods that begin during the circadian trough (approximately 02:00–05:59 local time) carry significantly higher fatigue risk than those starting mid-morning. Part 705's Flight Duty Period (FDP) matrix encodes this directly: the same pilot who may legally fly a 13-hour FDP starting at 09:00 is capped at approximately 11 hours starting at 01:00. The rules are not arbitrary — they reflect the physiological window in which fatigue-induced error rates sharply increase.

**Cumulative fatigue management.** A single-day limit is insufficient to capture chronic under-rest. Regulations therefore layer rolling accumulation caps — 100 hours in any 28 consecutive days, 300 hours in any 90 consecutive days, 1,000 hours in any 365 consecutive days — on top of daily FDP limits. A pilot can be within their daily limit and simultaneously in violation of the 28-day rolling cap.

**Differential risk calibration.** Part 705 applies stricter limits than Part 702 because scheduled commercial air transport carries higher passenger density, complex IFR operations, and multi-sector duty cycles. Operators holding dual 702/705 authority must pool flight hours across both subparts when computing rolling totals — which is where most manual tracking approaches fail.

---

## Industry Problem

### The three most common violation sources

**1. Rolling windows misread as calendar periods**

The 28-, 90-, and 365-day limits slide daily, not monthly. A pilot who flew 95 hours between May 1–28 and then flew 8 hours on May 29 has not "reset" when June begins. The June 1 window still reaches back to May 4 — those 95 hours remain fully in scope. Schedulers who mentally reset limits at month boundaries routinely undercount exposure. This is the most structurally invisible violation source: the mental model feels correct, the math is wrong.

**2. Hours not pooled across 702 and 705**

When the same pilot performs aerial survey under Part 702 on Monday and a passenger charter under Part 705 on Wednesday, both sets of hours count toward the same rolling accumulation limits. Operators who maintain separate logbooks or separate tracking sheets for each subpart — a natural workflow separation — systematically undercount. The regulation does not recognize the operational boundary between subparts; the pilot's body accumulates fatigue regardless.

**3. Post-flight rather than pre-flight discovery**

Manual verification typically happens after a duty assignment is issued, or after the flight has departed. By the time a violation is identified, the breach has already occurred and TC enforcement can be applied retroactively. Pre-flight interception requires that compliance status be visible before a pilot is assigned — which requires that all historical entries are current and all calculations run without manual input at the moment of dispatch.

---

## Compliance Logic

### Why report time governs maximum FDP

Part 705's FDP limits are a two-variable matrix: **report time** × **number of flight sectors**. Report time proxies circadian phase. A duty starting at 09:00 covers daylight hours when alertness is naturally higher; the same duration starting at 01:00 extends into 03:00–06:00, the window of maximum circadian vulnerability. A 30-minute difference in report time can cross a matrix band boundary and change the legal FDP maximum by up to two hours.

This has real operational consequences. Flights are routinely scheduled around slot availability, weather, and aircraft routing — not pilot biology. An operation that "just moves departure 45 minutes earlier" may unknowingly shift the pilot into a stricter FDP band.

### Why sector count matters

Each approach and landing is the highest-workload phase of flight. The research underpinning the FDP matrix quantified cognitive load accumulation across sectors: completing six sectors in a day produces measurably greater fatigue than two sectors over the same elapsed time, independent of total flight hours. The matrix reflects this by reducing maximum FDP as sector count increases — an operator who schedules "light flying days" measured only in hours-aloft, without counting sector count, may be scheduling fatigue without knowing it.

### The rest period trap

Minimum rest between duty periods must equal at least the preceding FDP duration, or the regulatory minimum, whichever is greater. The trap: rest must be *free from all duty* — positioning flights, pre-flight briefing, and standby obligations are duty, not rest. An operator who schedules a "rest window" between two duties without accounting for these bookend obligations under-rests the crew without the records showing it.

---

## Calculation Method

### Rolling window: worked example

The 28-day accumulation limit requires that a pilot's total flight time in any consecutive 28-day window not exceed 100 hours.

**How the window slides:**

| Date | Window covers | Hours in window |
|---|---|---|
| June 15 | May 19 – June 15 | 92 h |
| June 16 | May 20 – June 16 | 92 − (hours flown May 19) + (hours flown June 16) |
| June 17 | May 21 – June 17 | continues sliding |

**Scenario A:** Pilot flew 4 hours on May 19. Scheduled for 10 hours on June 16.
Window total = 92 − 4 + 10 = **98 hours** — legal.

**Scenario B:** Pilot flew 0 hours on May 19. Same 10-hour schedule on June 16.
Window total = 92 − 0 + 10 = **102 hours** — a violation. A monthly-reset mental model produces the same approval decision in both scenarios. The rolling window produces different results.

The same sliding logic runs simultaneously for the 90-day (300-hour) and 365-day (1,000-hour) windows. Every pilot carries three live rolling calculations at all times, each with a different lookback horizon.

### Why manual verification fails at scale

For an operator with 15 pilots, verifying all three rolling windows before every dispatch requires:

- 15 pilots × 3 windows = **45 live calculations per dispatch cycle**
- Each calculation requires scanning up to **365 days of historical records** per pilot
- The check must be completed in **real time**, before a dispatch release is issued

Under favourable conditions, manual cross-referencing takes 20–30 minutes per pilot. The calculations themselves are deterministic — they require no judgment, only accurate data and arithmetic. The human error introduced at this stage is not interpretive; it is mechanical. Automation eliminates the error class entirely.

---

## Workbook Preview

> 🔗 **[View live preview →](https://hyvoid.github.io/pilot-duty-tracker-designed-for-Part-702-and-Part-705-operations/)**

**Who it's for:**

| User | Scenario |
|---|---|
| **Flight dispatchers** | Verify pilot availability in seconds before issuing a dispatch release |
| **Crew schedulers** | Build rosters 7–14 days out with real-time visibility of each pilot's remaining legal hours |
| **Safety managers** | Maintain an auditable, single source of truth for all duty records |
| **Small AOC operators** | Affordable alternative to enterprise crew management systems costing hundreds of thousands of dollars |

Best suited for Canadian operators with 3–30 pilots running mixed 702/705 operations, where dedicated crew management software is cost-prohibitive but spreadsheet-only approaches no longer scale.

**Management outcomes:**

| Dimension | Before | After |
|---|---|---|
| Violation risk | Discovered post-flight; TC penalties applied retroactively | Blocked before dispatch; 100% pre-flight interception |
| Scheduling check time | 20–30 min per pilot, per check | Under 3 seconds |
| Audit preparation | 2–3 days to reconstruct records | Filter and export in under 5 seconds |
| Crew utilisation | 1–2 hour manual buffer routinely wasted | Minute-level precision; every legal minute accounted for |
| Data consistency | Dispatcher and pilot copies frequently diverge | Single source of truth across all records and reports |

> 🛒 **[Get it on Gumroad →](https://alexhasgreatestuff.gumroad.com/l/njeyey)**

---

## Limitations

This tool is designed for operational clarity. The following boundaries are known and should be evaluated before deployment:

- **Data integrity dependency** — all calculations are only as accurate as the duty entries. Entries not logged, logged late, or entered incorrectly will produce incorrect compliance status without any automatic warning
- **Not a legal opinion** — this workbook implements the regulations as the author interprets them. Transport Canada's official interpretation governs in all enforcement contexts; operators should validate edge-case rule applications with legal counsel or their TC Principal Operations Inspector
- **Regulatory amendment lag** — CARs amendments are not automatically reflected in the workbook. Operators are responsible for monitoring TC regulatory changes and updating the tool accordingly
- **Scope: Part 702 and 705 only** — operators under Part 703 (air taxi) or Part 704 (commuter operations) are subject to different specific limits; this workbook does not encode those subparts
- **Scale ceiling** — the single-workbook architecture is sized for 3–30 pilots; beyond approximately 30 pilots, row volume and rolling-window calculation depth may degrade Excel performance
- **Excel version sensitivity** — formulas require Excel 2016 or later on Windows; behaviour in Excel for Mac or Office 365 web may differ
- **Edge cases not fully automated** — augmented crew provisions, split duty rules, and certain rest extensions involve regulatory conditions that require dispatcher judgment and are not fully encoded in this version

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

[Aperçu](#apercu-fr) · [Acheter](https://alexhasgreatestuff.gumroad.com/l/dutytracker)

</div>

---

## Contexte réglementaire

Les Parties 702 (travail aérien) et 705 (transport aérien commercial) du RAC imposent des limites légalement contraignantes sur le temps de vol et le temps de service des pilotes. Il ne s'agit pas de lignes directrices — les infractions peuvent entraîner de lourdes amendes, la suspension du certificat d'exploitation aérienne (CEA) et des sanctions sur les licences individuelles.

Ces réglementations découlent de décennies d'enquêtes sur les accidents liant la fatigue des équipages aux accidents de vol contrôlé en relief (CFIT), aux accidents à l'approche et à l'atterrissage et aux pertes de contrôle. Leur structure reflète trois principes fondamentaux :

**Alignement circadien.** Le corps humain n'est pas également alerte à toutes les heures. Les périodes de service débutant pendant le creux circadien (environ 02h00–05h59 heure locale) présentent un risque de fatigue nettement plus élevé que celles débutant en milieu de matinée. La matrice de Période de Service en vol (PDS) de la Partie 705 intègre directement ce facteur : le même pilote pouvant légalement effectuer une PDS de 13 heures débutant à 09h00 est limité à environ 11 heures débutant à 01h00. Ces règles ne sont pas arbitraires — elles reflètent la fenêtre physiologique dans laquelle les taux d'erreur liés à la fatigue augmentent fortement.

**Gestion de la fatigue cumulative.** Une limite journalière seule est insuffisante pour rendre compte du déficit chronique de repos. Les réglementations superposent donc des plafonds d'accumulation glissants — 100 heures sur 28 jours consécutifs, 300 heures sur 90 jours consécutifs, 1 000 heures sur 365 jours consécutifs — aux limites journalières de PDS. Un pilote peut être dans les limites quotidiennes tout en étant simultanément en infraction avec le plafond glissant de 28 jours.

**Calibration différentielle du risque.** La Partie 705 applique des limites plus strictes que la Partie 702, car le transport aérien commercial régulier implique une densité de passagers plus élevée, des opérations IFR dans un espace aérien complexe et des cycles de service multi-secteurs. Les exploitants détenant une double autorisation 702/705 doivent cumuler les heures des deux sous-parties lors du calcul des totaux glissants — c'est là que la plupart des suivis manuels s'effondrent.

---

## Problème sectoriel

### Les trois principales sources d'infraction

**1. Fenêtres glissantes confondues avec des périodes calendaires**

Les limites de 28, 90 et 365 jours glissent quotidiennement, non mensuellement. Un pilote ayant volé 95 heures entre le 1er et le 28 mai, puis 8 heures le 29 mai, ne repart pas à zéro le 1er juin — la fenêtre du 1er juin remonte toujours au 4 mai. Les planificateurs qui réinitialisent mentalement les limites en début de mois sous-estiment systématiquement l'exposition. C'est la source d'infraction la plus structurellement invisible : le modèle mental paraît correct, le calcul est faux.

**2. Heures non cumulées entre les Parties 702 et 705**

Lorsqu'un même pilote effectue un relevé aérien sous la Partie 702 le lundi et un vol charter passagers sous la Partie 705 le mercredi, les deux ensembles d'heures comptent vers les mêmes limites d'accumulation glissantes. Les exploitants qui maintiennent des carnets de vol ou des feuilles de suivi séparés pour chaque sous-partie — séparation opérationnelle naturelle — sous-comptent systématiquement. La réglementation ne reconnaît pas la frontière opérationnelle entre sous-parties ; le corps du pilote accumule la fatigue indépendamment de cette distinction.

**3. Découverte après le vol plutôt qu'avant**

La vérification manuelle a généralement lieu après qu'une affectation de service est émise, voire après le départ du vol. Au moment où une infraction est identifiée, le manquement a déjà eu lieu et Transports Canada peut appliquer des sanctions rétroactivement. L'interception pré-vol exige que le statut de conformité soit visible avant l'affectation d'un pilote — ce qui implique que toutes les entrées historiques soient à jour et que tous les calculs s'exécutent automatiquement au moment de la répartition.

---

## Logique de conformité

### Pourquoi l'heure de présentation détermine la PDS maximale

Les limites de PDS de la Partie 705 constituent une matrice à deux variables : **heure de présentation** × **nombre de secteurs de vol**. L'heure de présentation sert de proxy pour la phase circadienne. Un service débutant à 09h00 couvre des heures de lumière où l'éveil est naturellement plus élevé ; la même durée débutant à 01h00 s'étend jusqu'à 03h00–06h00, la fenêtre de vulnérabilité circadienne maximale. Une différence de 30 minutes dans l'heure de présentation peut franchir une limite de bande matricielle et modifier la PDS légale maximale jusqu'à deux heures.

Cela a des conséquences opérationnelles concrètes. Les vols sont couramment planifiés en fonction des créneaux disponibles, des conditions météorologiques et du routage des appareils — non en fonction de la biologie des pilotes. Une opération dont le départ est « simplement avancé de 45 minutes » peut placer le pilote dans une bande PDS plus restrictive sans que personne ne s'en rende compte.

### Pourquoi le nombre de secteurs est important

Chaque approche et atterrissage représente la phase de charge de travail la plus élevée du vol. La recherche ayant établi les limites de PDS a quantifié l'accumulation de charge cognitive sur plusieurs secteurs : compléter six secteurs dans une journée produit une fatigue mesurément plus grande que deux secteurs sur la même durée écoulée, indépendamment du total d'heures de vol. La matrice en tient compte en réduisant la PDS maximale à mesure que le nombre de secteurs augmente. Un exploitant qui planifie des « journées légères » mesurées uniquement en heures-vol, sans comptabiliser les secteurs, peut planifier de la fatigue sans le savoir.

### Le piège de la période de repos

Le repos minimal entre les périodes de service doit être au moins égal à la PDS précédente, ou au minimum réglementaire, selon ce qui est plus élevé. Le piège : le repos doit être *exempt de tout service* — les vols de positionnement, les briefings pré-vol et les périodes d'astreinte constituent du temps de service, pas du repos. Un exploitant qui planifie une « fenêtre de repos » entre deux services sans comptabiliser ces obligations périphériques sous-repose les équipages sans que les dossiers l'indiquent.

---

## Méthode de calcul

### Fenêtre glissante : exemple concret

La limite d'accumulation sur 28 jours exige que le temps de vol total d'un pilote dans toute fenêtre de 28 jours consécutifs n'excède pas 100 heures.

**Comment la fenêtre se déplace :**

| Date | Fenêtre couverte | Heures dans la fenêtre |
|---|---|---|
| 15 juin | 19 mai – 15 juin | 92 h |
| 16 juin | 20 mai – 16 juin | 92 − (heures du 19 mai) + (heures du 16 juin) |
| 17 juin | 21 mai – 17 juin | continue de glisser |

**Scénario A :** Le pilote a volé 4 heures le 19 mai. Prévu pour 10 heures le 16 juin.
Total de la fenêtre = 92 − 4 + 10 = **98 heures** — légal.

**Scénario B :** Le pilote a volé 0 heure le 19 mai. Même planning de 10 heures le 16 juin.
Total de la fenêtre = 92 − 0 + 10 = **102 heures** — une infraction. Un modèle mental de réinitialisation mensuelle produit la même décision d'approbation dans les deux scénarios. La fenêtre glissante produit des résultats différents.

La même logique glissante s'applique simultanément aux fenêtres de 90 jours (300 heures) et de 365 jours (1 000 heures). Chaque pilote porte en permanence trois calculs glissants actifs, chacun avec un horizon de lookback différent.

### Pourquoi la vérification manuelle échoue à l'échelle

Pour un exploitant de 15 pilotes, vérifier les trois fenêtres glissantes avant chaque répartition nécessite :

- 15 pilotes × 3 fenêtres = **45 calculs actifs par cycle de répartition**
- Chaque calcul exige l'examen de jusqu'à **365 jours d'historique** par pilote
- La vérification doit être complétée **en temps réel**, avant d'émettre l'autorisation de répartition

Dans des conditions favorables, la consultation manuelle prend 20 à 30 minutes par pilote. Les calculs sont déterministes — ils ne requièrent aucun jugement, seulement des données exactes et de l'arithmétique. L'erreur humaine introduite à ce stade n'est pas interprétative ; elle est mécanique. L'automatisation élimine entièrement cette classe d'erreur.

---

<a name="apercu-fr"></a>
## Aperçu du classeur

> 🔗 **[Voir l'aperçu en direct →](https://hyvoid.github.io/pilot-duty-tracker-designed-for-Part-702-and-Part-705-operations/)**

**À qui s'adresse cet outil :**

| Utilisateur | Scénario |
|---|---|
| **Répartiteurs** | Vérifier la disponibilité d'un pilote en quelques secondes avant d'émettre une autorisation de départ |
| **Coordinateurs d'équipage** | Construire des tableaux de service 7 à 14 jours à l'avance avec visibilité en temps réel des heures légales restantes |
| **Responsables sécurité** | Maintenir une source unique de vérité auditable pour tous les dossiers de service |
| **Petits exploitants AOC** | Alternative abordable aux systèmes de gestion d'équipage d'entreprise coûtant des centaines de milliers de dollars |

Particulièrement adapté aux exploitants canadiens de 3 à 30 pilotes menant des opérations mixtes 702/705, pour lesquels les logiciels dédiés sont trop coûteux mais les approches tableur seules ne sont plus suffisantes.

**Résultats de gestion :**

| Dimension | Avant | Après |
|---|---|---|
| Risque d'infraction | Détecté après le vol ; pénalités TC appliquées rétroactivement | Bloqué avant la répartition ; interception pré-vol à 100 % |
| Durée de vérification | 20–30 min par pilote, par vérification | Moins de 3 secondes |
| Préparation aux audits | 2–3 jours pour reconstituer les dossiers | Filtrer et exporter en moins de 5 secondes |
| Utilisation des équipages | Tampon manuel de 1–2 heures régulièrement gaspillé | Précision à la minute ; chaque minute légale comptabilisée |
| Cohérence des données | Copie répartiteur et copie pilote fréquemment divergentes | Source unique de vérité pour tous les dossiers et rapports |

> 🛒 **[Disponible sur Gumroad →](https://alexhasgreatestuff.gumroad.com/l/dutytracker)**

---

## Limitations

Cet outil est conçu dans un souci de clarté et de transparence. Les limites suivantes sont connues et doivent être évaluées avant tout déploiement :

- **Dépendance à l'intégrité des données** — tous les calculs ne sont exacts qu'à condition que les données de service saisies le soient également. Les entrées non enregistrées, enregistrées tardivement ou incorrectement produiront un statut de conformité erroné sans avertissement automatique
- **Pas un avis juridique** — ce classeur implémente les règlements tels que l'auteur les interprète. L'interprétation officielle de Transports Canada prévaut dans tout contexte d'application ; les exploitants doivent valider les cas limites avec un conseil juridique ou leur Inspecteur principal des opérations TC
- **Délai de mise à jour réglementaire** — les modifications du RAC ne sont pas automatiquement reflétées dans le classeur ; il incombe aux exploitants de surveiller les changements réglementaires et de mettre à jour l'outil en conséquence
- **Périmètre : Parties 702 et 705 uniquement** — les exploitants sous la Partie 703 (taxi aérien) ou la Partie 704 (exploitation de navettes) sont soumis à des limites spécifiques différentes ; ce classeur ne couvre pas ces sous-parties
- **Plafond d'échelle** — l'architecture à classeur unique est dimensionnée pour 3 à 30 pilotes ; au-delà d'environ 30 pilotes, le volume de lignes et la profondeur des calculs glissants peuvent dégrader les performances Excel
- **Sensibilité à la version Excel** — les formules nécessitent Excel 2016 ou une version ultérieure sur Windows ; le comportement dans Excel pour Mac ou Office 365 en ligne peut différer
- **Cas limites non entièrement automatisés** — les dispositions relatives aux équipages renforcés, les règles de service fractionné et certaines extensions de repos impliquent des conditions réglementaires nécessitant le jugement du répartiteur et ne sont pas entièrement encodées dans cette version

---

## Licence

Distribué sous la [licence Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---

<br>
<div align="right"><a href="#français">↑ Haut de page (FR)</a> · <a href="#english">← English</a></div>
