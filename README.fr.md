[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | 🇪🇸 [ Español ](README.sp.md) | [ 🇬🇧 English ](README.md)

# Prévenez les violations de temps de vol et de service avant la mise en service

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)

**Conçu pour les exploitants canadiens des parties 702 et 705 qui doivent suivre le temps de vol, le temps de service, l'exposition à la fatigue et les limites de conformité glissantes avant qu'un pilote ne soit affecté.**

[Aperçu en direct](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) | [Acheter l'Excel complet](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

Suivez les limites glissantes de temps de vol, détectez les risques de non-conformité en quelques secondes et conservez une source de vérité unique et auditable pour les dossiers de service des pilotes.

---

## Aperçu rapide

<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 11_47_04 AM" src="https://github.com/user-attachments/assets/cc792931-2477-40d4-9bd7-e92418817c77" />

> Consultez l'aperçu interactif du classeur : [démo du suivi de service des pilotes](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)

---

## Pourquoi cela existe

La plupart des violations de temps de vol et de service ne sont pas causées par de mauvaises intentions.

Elles surviennent généralement parce que les fenêtres glissantes, les activités mixtes 702/705, les règles cumulatives de fatigue, les services réaffectés et les dossiers fragmentés sont difficiles à surveiller manuellement.

Le risque est simple :

```text
Pilot assigned
-> Manual check
-> Prior records missed
-> Violation discovered after the flight
```

Ce classeur est conçu pour changer le flux de travail :

```text
Pilot considered for assignment
-> Duty record entered once
-> Rolling limits checked automatically
-> Compliance risk flagged before dispatch
```

Le problème commercial n'est pas seulement la réglementation. C'est la visibilité opérationnelle. Les répartiteurs et les planificateurs doivent savoir si un pilote peut légalement et en toute sécurité prendre la prochaine affectation avant que le vol ne soit libéré.

---

## Trois pièges de conformité qui surprennent les exploitants

### Piège 1 — Les fenêtres glissantes sont lues comme des périodes calendaires

Les limites de 28, 90 et 365 jours glissent vers l'avant chaque jour, pas chaque mois.
Un pilote qui a volé 95 heures entre le 1er et le 28 mai puis a volé 8 heures le 29 mai
n'a **pas** été remis à zéro au début de juin. La fenêtre du 1er juin remonte encore jusqu'au 4 mai.

Les planificateurs qui réinitialisent mentalement les limites aux frontières mensuelles sous-estiment systématiquement l'exposition.
C'est le piège le plus structurellement invisible : le modèle mental semble correct ; le calcul est faux.

### Piège 2 — Les heures ne sont pas mutualisées entre 702 et 705

Lorsque le même pilote effectue un levé aérien en vertu de la partie 702 le lundi et une location charter passagers
en vertu de la partie 705 le mercredi, les deux ensembles d'heures comptent pour les mêmes limites d'accumulation glissantes.

Les exploitants qui tiennent des feuilles de suivi séparées pour chaque sous-partie — une division naturelle du flux de travail —
sous-estiment systématiquement. La réglementation ne reconnaît pas cette frontière opérationnelle.

### Piège 3 — Les violations sont découvertes après le vol

La vérification manuelle se produit généralement après l'émission d'une affectation de service, ou après le départ
du vol. Au moment où une violation est identifiée, la brèche s'est déjà produite.
L'application par Transport Canada s'applique rétroactivement.

L'interception avant le vol exige que le statut de conformité soit visible *avant* qu'un pilote ne soit affecté —
ce qui exige que toutes les données historiques soient à jour et que tous les calculs s'exécutent automatiquement au
moment de la mise en service.

Il se cache généralement dans la relation entre :

- le service prévu du jour
- l'historique de service précédent du pilote
- l'heure de présentation
- le nombre de secteurs
- l'accumulation de temps de vol
- le repos requis
- les procédures spécifiques de l'exploitant

C'est pourquoi l'examen manuel par tableur attrape souvent le problème tardivement, ou le manque entièrement.

---

## À qui cet outil est destiné

| Utilisateur | Cas d'usage pratique |
|---|---|
| Répartiteurs de vol | Vérifier la disponibilité des pilotes avant d'émettre une autorisation de mise en service |
| Planificateurs d'équipage | Construire des roulements avec visibilité sur la capacité légale restante |
| Pilotes en chef | Examiner la charge de travail des pilotes et l'exposition cumulée avant d'approuver les affectations |
| Gestionnaires de sécurité | Maintenir des dossiers structurés pour l'examen interne et la préparation aux audits |
| Petits exploitants AOC | Remplacer le suivi manuel dispersé par un flux de travail Excel léger unique |

Convient le mieux aux exploitants canadiens de 3 à 30 pilotes menant des opérations mixtes 702/705,
où un logiciel de gestion d'équipage dédié est prohibitif en coût mais les approches manuelles n'évoluent plus.

---

## Ce que fait le classeur

### Enregistrement du temps de service
Un point d'entrée de données unique pour tous les dossiers de service des pilotes. Les répartiteurs enregistrent les informations de vol et de service
de base une seule fois ; les calculs s'exécutent automatiquement en arrière-plan.

### Surveillance des fenêtres glissantes
Calcul automatique des limites d'accumulation de la partie 705 sur les trois fenêtres réglementaires simultanément :
- 100 heures sur toute période de 28 jours consécutifs
- 300 heures sur toute période de 90 jours consécutifs
- 1 000 heures sur toute période de 365 jours consécutifs

### Statut de conformité avant mise en service
Le statut de conformité de chaque pilote est visible avant l'émission de l'affectation.
Aucun recoupement manuel. Aucune découverte après le vol.

### Validation de la matrice FDP
Les limites de période de service de vol (FDP) de la partie 705 — une matrice à deux variables d'heure de présentation × nombre de secteurs —
sont pré-encodées. Le maximum FDP légal se met à jour automatiquement en fonction du moment où le pilote se présente
et du nombre de secteurs programmés.

### Rapports prêts pour l'audit
Chaque entrée est structurée et traçable dès le premier jour. Les dossiers de conformité historiques peuvent être
filtrés par pilote, plage de dates ou statut et exportés sans post-traitement.

---

## Scénario d'exemple

**Profil de l'exploitant :** 12 pilotes. Opérations mixtes des parties 702 et 705. Un seul bureau de répartition.

**Le problème :** Chaque matin, le répartiteur passe 90 minutes à vérifier manuellement les limites
de service glissantes avant d'attribuer les vols du jour. Les heures de vol sont suivies dans deux
tableurs séparés — un pour les opérations 702, un pour les opérations 705. Lorsqu'un pilote vole en vertu des deux sous-parties
la même semaine, les totaux mutualisés sont consolidés à la main.

Sur trois mois d'exploitation, deux dépassements de limites ont été détectés — tous deux après le départ
du vol.

| | Avant | Après |
|---|---|---|
| Structure des dossiers | Deux feuilles séparées, une par sous-partie | Un classeur unifié unique |
| Temps de vérification matinale | ~90 min pour tous les pilotes | Moins de 3 secondes par pilote |
| Mutualisation des heures 702/705 | Consolidation manuelle | Automatique sur les deux sous-parties |
| Découverte des violations | Après le vol ; exposition rétroactive TC | Avant mise en service ; bloquée avant affectation |

---

La valeur n'est pas qu'Excel remplace le jugement de conformité. La valeur est que les calculs de routine cessent de dépendre de la mémoire, des vérifications par copier-coller et des fichiers fragmentés.

---

## Pourquoi la réglementation fonctionne ainsi

Transport Canada réglemente la fatigue des équipages de vol parce que la fatigue est un danger pour la sécurité, pas seulement une question administrative. Les règles sont conçues pour contrôler la charge de travail cumulée, le calendrier de service, les possibilités de repos et le risque de baisse de vigilance.

C'est pourquoi les réglementations prennent en compte des facteurs tels que :

- le temps de vol total sur des fenêtres de jours consécutifs
- les limites de période de service de vol
- l'heure de présentation et le rythme circadien
- le nombre de vols ou de secteurs
- les périodes de repos et le temps libre de service
- la surveillance de l'exploitant et les dossiers

La logique opérationnelle est directe : deux horaires peuvent avoir le même nombre d'heures de service mais créer des risques de fatigue différents selon le calendrier, la fréquence, le nombre de secteurs et l'accumulation antérieure.

Références officielles utiles :

- [Transport Canada : Flight and duty time regulations](https://tc.canada.ca/en/aviation/commercial-air-services/fatigue-management-aviation/flight-duty-time-regulations-prescriptive-vs-performance-based-options)
- [Transport Canada Advisory Circular AC 700-047](https://tc.canada.ca/en/aviation/reference-centre/advisory-circulars/advisory-circular-ac-no-700-047)
- [Canadian Aviation Regulations SOR/96-433](https://tc.canada.ca/en/corporate-services/acts-regulations/list-regulations/canadian-aviation-regulations-sor-96-433)

---

## Comment fonctionnent les fenêtres glissantes

La limite d'accumulation de 28 jours exige que le temps de vol total sur toute fenêtre consécutive de 28 jours
ne dépasse pas 100 heures. La fenêtre glisse vers l'avant chaque jour — ce n'est pas un mois calendaire.

| Date | La fenêtre couvre | Effet net |
|---|---|---|
| 15 juin | 19 mai – 15 juin | 92 h dans la fenêtre |
| 16 juin | 20 mai – 16 juin | − heures volées le 19 mai + heures volées le 16 juin |
| 17 juin | 21 mai – 17 juin | continue de glisser |

**Le piège en chiffres :**  
Le pilote a 92 heures dans la fenêtre. Programmées pour 10 heures le 16 juin.

- S'il a volé 4 heures le 19 mai : 92 − 4 + 10 = **98 h** — légal.  
- S'il a volé 0 heure le 19 mai : 92 − 0 + 10 = **102 h** — violation.

Un modèle mental de remise à zéro mensuelle approuve les deux. La fenêtre glissante ne l'approuve pas.

Chaque pilote porte trois de ces calculs simultanément : 28 jours, 90 jours et 365 jours.
Pour 15 pilotes, cela fait 45 calculs glissants en direct par cycle de mise en service, chacun nécessitant jusqu'à
365 jours de recherche historique. Les mathématiques ne nécessitent aucun jugement. L'automatisation élimine entièrement la classe d'erreurs.

**Pourquoi l'heure de présentation régit aussi la FDP :** Les limites FDP de la partie 705 dépendent du début du service.
Un service commençant à 09h00 peut légalement durer jusqu'à 13 heures ; le même service commençant à 01h00
est plafonné près de 11 heures — parce qu'il s'étend dans la fenêtre circadienne 02h00–05h59 où
les taux d'erreur dus à la fatigue augmentent fortement. Une différence de 30 minutes dans l'heure de présentation peut changer
le maximum légal de jusqu'à 2 heures. Le nombre de secteurs ajoute une deuxième dimension : chaque approche
et atterrissage supplémentaire accumule une charge cognitive mesurable, et la matrice réduit la FDP
autorisée en conséquence.

---

## Logique du classeur

Le classeur est organisé autour d'un flux de travail de mise en service pratique :

1. Saisir les données du pilote et de l'affectation prévue.
2. Identifier le contexte opérationnel.
3. Extraire l'historique de service et de vol pertinent pour ce pilote.
4. Calculer les totaux des fenêtres glissantes.
5. Comparer l'affectation prévue aux limites configurées.
6. Signaler un statut clair, d'avertissement ou de risque.
7. Conserver les dossiers pour examen et exportation.

Le classeur est destiné à être un outil d'aide à la décision et d'analyse. Il ne remplace pas la responsabilité légale de l'exploitant d'interpréter et d'appliquer les CARs actuels, le manuel d'exploitation de l'entreprise, les exemptions approuvées ou les procédures FRMS.

---

## Achat

Utilisez ici le classeur Excel complet :

[Acheter le suiveur Excel complet](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

---

## Limites

- **Dépendance de l'intégrité des données** — les calculs sont aussi précis que les saisies ; des dossiers tardifs, manquants ou incorrects produisent un statut de conformité incorrect sans avertissement
- **Pas un avis juridique** — ce classeur reflète l'interprétation de l'auteur des réglementations ; la position officielle de Transport Canada prévaut, et les applications de cas limites devraient être validées avec un conseiller juridique ou votre inspecteur principal des opérations TC
- **Retard des amendements réglementaires** — les amendements des CARs ne sont pas automatiquement reflétés ; les exploitants sont responsables de la surveillance des changements réglementaires TC et de la mise à jour du classeur en conséquence
- **Portée : parties 702 et 705 uniquement** — les exploitants sous la partie 703 (taxi aérien) ou la partie 704 (navette) travaillent sous des limites spécifiques différentes non encodées dans cette version
- **Plafond d'échelle** — conçu pour 3 à 30 pilotes ; au-delà d'environ 30, la profondeur de calcul peut dégrader les performances d'Excel
- **Sensibilité à la version d'Excel** — nécessite Excel 2016 ou version ultérieure sous Windows ; le comportement dans Excel pour Mac ou Office 365 web peut différer
- **Cas limites non entièrement automatisés** — les dispositions d'équipage augmenté, les règles de service fractionné et certaines extensions de repos impliquent des conditions réglementaires qui nécessitent le jugement du répartiteur et ne sont pas entièrement encodées dans cette version

---

## À propos de ce projet

Ce classeur fait partie d'un effort plus large visant à traduire des exigences opérationnelles et réglementaires complexes
en outils légers que les petites et moyennes organisations peuvent réellement utiliser.

Pas d'ERP. Pas de projet logiciel sur mesure. Pas de comptes supplémentaires.

Juste une logique métier claire, des données structurées et un support décisionnel reproductible —
livré dans un logiciel que votre équipe possède déjà.

Si votre exploitation implique des problèmes de conformité, de planification ou d'allocation de ressources
qui vivent actuellement dans la tête de quelqu'un ou dans un tableur déconnecté,
[voyez ce qui est disponible →](https://www.theseusworkshop.com)

---

## License

Distribué sous la [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---
