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

### Prevent flight duty time violations before dispatch.

Track rolling flight time limits, detect compliance risks in real time,  
and maintain a single auditable source of truth — all inside Microsoft Excel.

**Built for Canadian Part 702 and Part 705 operators.**

[Purchase for complete Excel](https://alexhasgreatestuff.gumroad.com/l/dutytracker)

</div>

---

## Why This Exists

Most duty time violations are not caused by bad intentions.

They happen because the regulations require tracking three simultaneous rolling windows —
28, 90, and 365 consecutive days — across pilots who may fly under both Part 702 and Part 705,
in real time, before every dispatch decision.

Manual tracking cannot reliably do this. The math is deterministic. The window slides daily.
The error is structural, not human.
---

## Three Compliance Traps That Catch Operators

### Trap 1 — Rolling windows misread as calendar periods

The 28-, 90-, and 365-day limits slide forward every day, not every month.
A pilot who flew 95 hours between May 1–28 and then flew 8 hours on May 29
has **not** reset when June begins. The June 1 window still reaches back to May 4.

Schedulers who mentally reset limits at month boundaries routinely undercount exposure.
This is the most structurally invisible trap: the mental model feels correct; the calculation is wrong.

### Trap 2 — Hours not pooled across 702 and 705

When the same pilot performs aerial survey under Part 702 on Monday and a passenger charter
under Part 705 on Wednesday, both sets of hours count toward the same rolling accumulation limits.

Operators who maintain separate tracking sheets for each subpart — a natural workflow division —
systematically undercount. The regulation does not recognise that operational boundary.

### Trap 3 — Violations discovered after the flight

Manual verification typically happens after a duty assignment is issued, or after the flight
has departed. By the time a violation is identified, the breach has already occurred.
Transport Canada enforcement applies retroactively.

Pre-flight interception requires that compliance status be visible *before* a pilot is assigned —
which requires all historical data to be current and all calculations to run automatically at
the moment of dispatch.

---

## Who This Tool Is For

✓ **Flight dispatchers** — verify pilot availability in seconds before issuing a dispatch release

✓ **Crew schedulers** — build rosters 7–14 days out with real-time visibility of each pilot's remaining legal hours

✓ **Chief pilots** — maintain fleet-wide oversight of duty exposure without waiting for safety reports

✓ **Safety managers** — hold a single auditable source of truth for all duty records

✓ **Small AOC operators** — an affordable alternative to enterprise crew management systems costing hundreds of thousands of dollars

Best suited for Canadian operators with 3–30 pilots running mixed 702/705 operations,
where dedicated crew management software is cost-prohibitive but manual approaches no longer scale.

---

## What The Workbook Does

### Duty Time Logging
A single data entry point for all pilot duty records. Dispatchers log basic flight and duty
information once; calculations run automatically in the background.

### Rolling Window Monitoring
Automatic calculation of Part 705 accumulation limits across all three regulatory windows simultaneously:
- 100 hours in any 28 consecutive days
- 300 hours in any 90 consecutive days
- 1,000 hours in any 365 consecutive days

### Pre-Dispatch Compliance Status
Each pilot's compliance status is visible before assignment is issued.
No manual cross-referencing. No post-flight discovery.

### FDP Matrix Validation
Part 705's Flight Duty Period limits — a two-variable matrix of report time × sector count —
are pre-encoded. Legal FDP maximum updates automatically based on when the pilot reports
and how many sectors are scheduled.

### Audit-Ready Reporting
Every entry is structured and traceable from day one. Historical compliance records can be
filtered by pilot, date range, or status and exported without post-processing.

---

## Workbook Preview

> 🔗 **[View live preview →](https://hyvoid.github.io/pilot-duty-tracker-designed-for-Part-702-and-Part-705-operations/)**

| Dimension | Before | After |
|---|---|---|
| Violation risk | Discovered post-flight; TC penalties applied retroactively | Blocked before dispatch; 100% pre-flight interception |
| Scheduling check time | 20–30 min per pilot, per check | Under 3 seconds |
| Audit preparation | 2–3 days to reconstruct records | Filter and export in under 5 seconds |
| Crew utilisation | 1–2 hour manual buffer routinely wasted | Minute-level precision; every legal minute accounted for |
| Data consistency | Dispatcher and pilot copies frequently diverge | Single source of truth across all records and reports |

> 🛒 **[Get it on Gumroad →](https://alexhasgreatestuff.gumroad.com/l/njeyey)**

---

## Example Scenario

**Operator profile:** 12 pilots. Mixed Part 702 and Part 705 operations. Single dispatch office.

**The problem:** Every morning, the dispatcher spends 90 minutes manually verifying rolling
duty limits before assigning the day's flying. Flight hours are tracked in two separate
spreadsheets — one for 702 operations, one for 705. When a pilot flies under both subparts
in the same week, pooled totals are consolidated by hand.

Over three months of operations, two limit exceedances were caught — both after the flight
had already departed.

| | Before | After |
|---|---|---|
| Record structure | Two separate sheets, one per subpart | Single unified workbook |
| Morning check time | ~90 min across all pilots | Under 3 seconds per pilot |
| 702/705 hour pooling | Manual consolidation | Automatic across both subparts |
| Violation discovery | Post-flight; retroactive TC exposure | Pre-dispatch; blocked before assignment |

---

## How The Rolling Windows Work

The 28-day accumulation limit requires that total flight time in any consecutive 28-day window
not exceed 100 hours. The window slides forward every day — it is not a calendar month.

| Date | Window covers | Net effect |
|---|---|---|
| June 15 | May 19 – June 15 | 92 h in window |
| June 16 | May 20 – June 16 | − hours flown May 19 + hours flown June 16 |
| June 17 | May 21 – June 17 | continues sliding |

**The trap in numbers:**  
Pilot has 92 hours in window. Scheduled for 10 hours on June 16.

- If they flew 4 hours on May 19: 92 − 4 + 10 = **98 h** — legal.  
- If they flew 0 hours on May 19: 92 − 0 + 10 = **102 h** — violation.

A monthly-reset mental model approves both. The rolling window does not.

Every pilot carries three of these calculations simultaneously: 28-day, 90-day, and 365-day.
For 15 pilots, that is 45 live rolling calculations per dispatch cycle, each requiring up to
365 days of historical lookup. The math requires no judgment. Automation eliminates the error class entirely.

**Why report time also governs FDP:** Part 705's FDP limits depend on when duty starts.
A duty beginning at 09:00 may legally run up to 13 hours; the same duty beginning at 01:00
is capped near 11 hours — because it extends into the 02:00–05:59 circadian window where
fatigue-driven error rates sharply increase. A 30-minute difference in report time can change
the legal maximum by up to 2 hours. Sector count adds a second dimension: each additional
approach and landing accumulates measurable cognitive load, and the matrix reduces permitted
FDP accordingly.

---

## Limitations

- **Data integrity dependency** — calculations are only as accurate as the entries; late, missing, or incorrect records produce incorrect compliance status without warning
- **Not a legal opinion** — this workbook reflects the author's interpretation of the regulations; Transport Canada's official position governs, and edge-case applications should be validated with legal counsel or your TC Principal Operations Inspector
- **Regulatory amendment lag** — CARs amendments are not automatically reflected; operators are responsible for monitoring TC regulatory changes and updating the workbook accordingly
- **Scope: Part 702 and 705 only** — operators under Part 703 (air taxi) or Part 704 (commuter) work under different specific limits not encoded in this version
- **Scale ceiling** — designed for 3–30 pilots; beyond approximately 30, calculation depth may degrade Excel performance
- **Excel version sensitivity** — requires Excel 2016 or later on Windows; behaviour in Excel for Mac or Office 365 web may differ
- **Edge cases not fully automated** — augmented crew provisions, split duty rules, and certain rest extensions involve regulatory conditions that require dispatcher judgment and are not fully encoded in this version

---

## About This Project

This workbook is part of a broader effort to translate complex operational and regulatory
requirements into lightweight tools that small and medium-sized organizations can actually use.

No ERP. No custom software project. No additional accounts.

Just clear business logic, structured data, and repeatable decision support —
delivered in software your team already has.

If your operation involves compliance, scheduling, or resource allocation problems
that currently live in someone's head or a disconnected spreadsheet,
[see what else is available →](https://alexhasgreatestuff.gumroad.com/l/dutytracker)

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

### Prévenir les infractions au temps de service avant la répartition.

Suivez les limites glissantes de temps de vol, détectez les risques de non-conformité en temps réel,  
et maintenez une source unique de vérité auditable — entièrement dans Microsoft Excel.

**Conçu pour les exploitants canadiens des Parties 702 et 705.**

[Aperçu](#apercu-fr) · [Acheter](https://alexhasgreatestuff.gumroad.com/l/njeyey)

</div>

---

## Pourquoi cet outil existe

La plupart des infractions au temps de service ne sont pas causées par de mauvaises intentions.

Elles surviennent parce que les réglementations exigent le suivi de trois fenêtres glissantes
simultanées — 28, 90 et 365 jours consécutifs — pour des pilotes pouvant voler sous la Partie 702
et la Partie 705, en temps réel, avant chaque décision de répartition.

Le suivi manuel ne peut pas faire cela de manière fiable. Le calcul est déterministe.
La fenêtre glisse quotidiennement. L'erreur est structurelle, pas humaine.
---

## Trois pièges de conformité qui piègent les exploitants

### Piège 1 — Fenêtres glissantes confondues avec des périodes calendaires

Les limites de 28, 90 et 365 jours glissent quotidiennement, pas mensuellement.
Un pilote ayant volé 95 heures entre le 1er et le 28 mai, puis 8 heures le 29 mai,
ne repart **pas** à zéro le 1er juin. La fenêtre du 1er juin remonte toujours au 4 mai.

Les planificateurs qui réinitialisent mentalement les limites en début de mois sous-estiment
systématiquement l'exposition. C'est le piège le plus invisible structurellement :
le modèle mental paraît correct ; le calcul est faux.

### Piège 2 — Heures non cumulées entre les Parties 702 et 705

Lorsqu'un même pilote effectue un relevé aérien sous la Partie 702 le lundi et un vol charter
passagers sous la Partie 705 le mercredi, les deux ensembles d'heures comptent vers les mêmes
limites d'accumulation glissantes.

Les exploitants qui maintiennent des feuilles de suivi séparées pour chaque sous-partie —
séparation opérationnelle naturelle — sous-comptent systématiquement.
La réglementation ne reconnaît pas cette frontière opérationnelle.

### Piège 3 — Infractions découvertes après le vol

La vérification manuelle a généralement lieu après qu'une affectation est émise,
voire après le départ du vol. Au moment où l'infraction est identifiée, le manquement
a déjà eu lieu. Transports Canada peut appliquer des sanctions rétroactivement.

L'interception pré-vol exige que le statut de conformité soit visible *avant* l'affectation
d'un pilote — ce qui implique que toutes les données historiques soient à jour et que tous
les calculs s'exécutent automatiquement au moment de la répartition.

---

## À qui s'adresse cet outil

✓ **Répartiteurs** — vérifier la disponibilité d'un pilote en quelques secondes avant d'émettre une autorisation de départ

✓ **Coordinateurs d'équipage** — construire des tableaux de service 7 à 14 jours à l'avance avec visibilité en temps réel des heures légales restantes

✓ **Pilotes en chef** — maintenir une visibilité complète de l'exposition au temps de service à l'échelle de la flotte sans attendre les rapports sécurité

✓ **Responsables sécurité** — détenir une source unique de vérité auditable pour tous les dossiers de service

✓ **Petits exploitants AOC** — une alternative abordable aux systèmes de gestion d'équipage d'entreprise coûtant des centaines de milliers de dollars

Particulièrement adapté aux exploitants canadiens de 3 à 30 pilotes menant des opérations
mixtes 702/705, pour lesquels les logiciels dédiés sont trop coûteux mais les approches
manuelles ne sont plus viables.

---

## Ce que fait le classeur

### Enregistrement du temps de service
Un seul point de saisie pour tous les dossiers de service des pilotes. Les répartiteurs
enregistrent une fois les informations de base ; les calculs s'exécutent automatiquement
en arrière-plan.

### Suivi des fenêtres glissantes
Calcul automatique des limites d'accumulation de la Partie 705 sur les trois fenêtres
réglementaires simultanément :
- 100 heures sur 28 jours consécutifs
- 300 heures sur 90 jours consécutifs
- 1 000 heures sur 365 jours consécutifs

### Statut de conformité avant répartition
Le statut de conformité de chaque pilote est visible avant l'émission de l'affectation.
Aucune consultation manuelle. Aucune découverte post-vol.

### Validation de la matrice PDS
Les limites de Période de Service en vol (PDS) de la Partie 705 — une matrice à deux variables
heure de présentation × nombre de secteurs — sont pré-encodées. La PDS maximale légale
se met à jour automatiquement selon l'heure de présentation du pilote et le nombre de secteurs prévus.

### Rapports prêts pour l'audit
Chaque saisie est structurée et traçable dès le premier jour. Les dossiers de conformité
historiques peuvent être filtrés par pilote, période ou statut et exportés sans post-traitement.

---

<a name="apercu-fr"></a>
## Aperçu du classeur

> 🔗 **[Voir l'aperçu en direct →](https://hyvoid.github.io/pilot-duty-tracker-designed-for-Part-702-and-Part-705-operations/)**

| Dimension | Avant | Après |
|---|---|---|
| Risque d'infraction | Détecté après le vol ; pénalités TC appliquées rétroactivement | Bloqué avant la répartition ; interception pré-vol à 100 % |
| Durée de vérification | 20–30 min par pilote, par vérification | Moins de 3 secondes |
| Préparation aux audits | 2–3 jours pour reconstituer les dossiers | Filtrer et exporter en moins de 5 secondes |
| Utilisation des équipages | Tampon manuel de 1–2 heures régulièrement gaspillé | Précision à la minute ; chaque minute légale comptabilisée |
| Cohérence des données | Copie répartiteur et copie pilote fréquemment divergentes | Source unique de vérité pour tous les dossiers et rapports |

> 🛒 **[Disponible sur Gumroad →](https://alexhasgreatestuff.gumroad.com/l/njeyey)**

---

## Exemple concret

**Profil de l'exploitant :** 12 pilotes. Opérations mixtes Parties 702 et 705. Bureau de répartition unique.

**Le problème :** Chaque matin, le répartiteur passe 90 minutes à vérifier manuellement les
limites de temps de service glissantes avant d'affecter les vols de la journée. Les heures de vol
sont consignées dans deux tableurs séparés — un pour les opérations 702, un pour les opérations 705.
Lorsqu'un pilote vole sous les deux sous-parties la même semaine, le cumul est consolidé manuellement.

Sur trois mois d'opérations, deux dépassements de limite ont été identifiés — les deux après
le départ du vol.

| | Avant | Après |
|---|---|---|
| Structure des dossiers | Deux tableurs séparés, un par sous-partie | Classeur unique unifié |
| Durée de vérification matinale | ~90 min pour tous les pilotes | Moins de 3 secondes par pilote |
| Cumul des heures 702/705 | Consolidation manuelle | Automatique sur les deux sous-parties |
| Découverte des infractions | Post-vol ; exposition TC rétroactive | Pré-répartition ; bloqué avant affectation |

---

## Comment fonctionnent les fenêtres glissantes

La limite d'accumulation sur 28 jours exige que le temps de vol total dans toute fenêtre
de 28 jours consécutifs n'excède pas 100 heures. La fenêtre avance chaque jour —
ce n'est pas un mois calendaire.

| Date | Fenêtre couverte | Effet net |
|---|---|---|
| 15 juin | 19 mai – 15 juin | 92 h dans la fenêtre |
| 16 juin | 20 mai – 16 juin | − heures du 19 mai + heures du 16 juin |
| 17 juin | 21 mai – 17 juin | continue de glisser |

**Le piège en chiffres :**  
Le pilote a 92 heures dans la fenêtre. Prévu pour 10 heures le 16 juin.

- S'il a volé 4 heures le 19 mai : 92 − 4 + 10 = **98 h** — légal.  
- S'il a volé 0 heure le 19 mai : 92 − 0 + 10 = **102 h** — infraction.

Un modèle mental de réinitialisation mensuelle approuve les deux. La fenêtre glissante, non.

Chaque pilote porte trois de ces calculs simultanément : 28, 90 et 365 jours.
Pour 15 pilotes, cela représente 45 calculs glissants actifs par cycle de répartition,
chacun nécessitant jusqu'à 365 jours d'historique. Le calcul ne requiert aucun jugement.
L'automatisation élimine entièrement cette classe d'erreur.

**Pourquoi l'heure de présentation détermine aussi la PDS :** Les limites de PDS de la Partie 705
dépendent de l'heure de début du service. Un service débutant à 09h00 peut légalement durer
jusqu'à 13 heures ; le même service débutant à 01h00 est limité à environ 11 heures — car il
s'étend dans la fenêtre circadienne 02h00–05h59 où les taux d'erreur liés à la fatigue augmentent
fortement. Une différence de 30 minutes dans l'heure de présentation peut modifier le maximum
légal jusqu'à 2 heures. Le nombre de secteurs ajoute une deuxième dimension : chaque approche
et atterrissage supplémentaire accumule une charge cognitive mesurable, et la matrice réduit
la PDS autorisée en conséquence.

---

## Limitations

- **Dépendance à l'intégrité des données** — les calculs ne sont exacts qu'à condition que les saisies le soient ; les entrées manquantes, tardives ou incorrectes produisent un statut de conformité erroné sans avertissement
- **Pas un avis juridique** — ce classeur reflète l'interprétation de l'auteur ; l'interprétation officielle de Transports Canada prévaut, et les cas limites doivent être validés avec un conseil juridique ou l'Inspecteur principal des opérations TC
- **Délai de mise à jour réglementaire** — les modifications du RAC ne sont pas automatiquement reflétées ; les exploitants sont responsables du suivi des changements réglementaires et de la mise à jour du classeur
- **Périmètre : Parties 702 et 705 uniquement** — les exploitants sous la Partie 703 (taxi aérien) ou la Partie 704 (navettes) sont soumis à des limites spécifiques différentes non encodées dans cette version
- **Plafond d'échelle** — conçu pour 3 à 30 pilotes ; au-delà d'environ 30, la profondeur des calculs peut dégrader les performances Excel
- **Sensibilité à la version Excel** — nécessite Excel 2016 ou une version ultérieure sur Windows ; le comportement dans Excel pour Mac ou Office 365 en ligne peut différer
- **Cas limites non entièrement automatisés** — les dispositions relatives aux équipages renforcés, les règles de service fractionné et certaines extensions de repos nécessitent le jugement du répartiteur et ne sont pas entièrement encodées dans cette version

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
[voir ce qui est disponible →](https://alexhasgreatestuff.gumroad.com/l/njeyey)

---

## Licence

Distribué sous la [licence Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---

<br>
<div align="right"><a href="#français">↑ Haut de page (FR)</a> · <a href="#english">← English</a></div>
