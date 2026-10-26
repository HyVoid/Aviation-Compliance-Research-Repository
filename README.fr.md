[ 🌐 عربي ](README.ar.md) | [ 🇩🇪 Deutsch ](README.de.md) | [ 🇫🇷 Français ](README.fr.md) | [ 🇳🇱 Nederlands ](README.nl.md) | [ 🇪🇸 Español ](README.sp.md) | [ 🇬🇧 English ](README.md)
# Suiveur des temps de vol et de service CARs 702 & 705 du Canada (modèle Excel) — Prévenez la fatigue des pilotes et les violations de mise en service

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)

Un **tableur Excel automatisé de suivi des temps de vol et de service du Règlement de l'aviation canadien (CARs), parties 702 et 705** conçu pour les exploitants aériens commerciaux. Ce **calculateur de temps de service des pilotes** et cet **outil de planification FRMS (gestion des risques de fatigue)** aide les répartiteurs de vol, les planificateurs d'équipage et les pilotes en chef à suivre les **limites glissantes de temps de vol (fenêtres de 28/90/365 jours)**, à calculer les **maximums de période de service de vol (FDP)**, à surveiller les **périodes de repos obligatoires** et à prévenir les **violations de conformité Transport Canada** avant la mise en service du vol.

> [**Lancez la démo web interactive du suiveur des temps de service CARs 702/705 (essai à usage unique)**](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)
>
> > [**Téléchargez le classeur Excel de conformité multi-pilotes des temps de vol et de service CARs**](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker)

Éliminez les erreurs manuelles de tableur, automatisez la **mutualisation des temps de vol des sous-parties 702 (travail aérien) et 705 (transport aérien) des CARs**, détectez les **risques de non-conformité liés à la fatigue de l'équipage** en quelques secondes et conservez une source de vérité unique et **prête pour l'audit Transport Canada** des dossiers de service des pilotes.

---

## Aperçu interactif : calculateur de temps de service des pilotes CARs 702/705

<img width="1672" height="941" alt="Canadian CARs 702 and 705 Flight Duty Time Tracker Excel Template Dashboard for Pilot Scheduling and Transport Canada Compliance" src="https://github.com/user-attachments/assets/cc792931-2477-40d4-9bd7-e92418817c77" />

> **Essayez la logique avant d'acheter :** [Essayez l'aperçu web interactif du calculateur canadien des temps de vol et de service des pilotes](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/)

---

## Pourquoi la planification manuelle des équipages échoue aux audits de conformité de Transport Canada

La plupart des **violations de temps de vol et de service des CARs** ne sont pas causées par de mauvaises intentions. Elles surviennent parce que les **fenêtres glissantes de temps de vol**, les **opérations mixtes des sous-parties 702/705**, les **règles cumulatives de fatigue de l'équipage**, les extensions de service fractionné et les carnets de vol fragmentés des pilotes sont presque impossibles à recouper manuellement lors d'une mise en service matinale chargée.

Le risque traditionnel de la planification manuelle ressemble à ceci :

```text
Pilot assigned to flight
-> Manual check across separate 702 and 705 spreadsheets
-> Rolling 28-day / 90-day boundary miscalculated
-> Violation discovered retroactively during a Transport Canada PVI / Audit
```

Ce **classeur Excel automatisé de conformité aéronautique** réorganise le flux de travail préalable à la mise en service :

```text
Pilot considered for flight assignment
-> Duty & sector details logged once in a unified tracker
-> Rolling CARs 702/705 limits & FDP matrix validated automatically
-> Non-compliant dispatch blocked BEFORE flight release
```

Le problème commercial n'est pas seulement l'alignement réglementaire — c'est la **visibilité opérationnelle avant le vol**. Les répartiteurs de vol et les planificateurs d'équipage ont besoin d'une certitude immédiate quant à savoir si un membre d'équipage de conduite peut légalement et en toute sécurité accepter le prochain secteur avant que le plan de vol opérationnel (OFP) ne soit libéré.

---

## Trois pièges de conformité CARs 702 & 705 dans les tableurs manuels

### Piège 1 — Les fenêtres glissantes de temps de vol sont lues comme des mois calendaires
Sous le régime des **CARs de Transport Canada**, les **limites de temps de vol de 28, 90 et 365 jours consécutifs** glissent vers l'avant toutes les 24 heures, pas à la fin de chaque mois calendaire. Un pilote commercial qui cumule 95 heures de vol entre le 1er et le 28 mai et vole 8 heures le 29 mai ne se remet **pas** à zéro au 1er juin. La fenêtre glissante du 1er juin remonte encore jusqu'au 4 mai. Les planificateurs d'équipage qui réinitialisent mentalement les heures des pilotes aux frontières mensuelles sous-estiment systématiquement l'exposition cumulée.

### Piège 2 — Les heures de vol ne sont pas mutualisées entre les sous-parties 702 et 705 des CARs
Lorsque le même membre d'équipage de conduite effectue une **mission de travail aérien / de levé sous la partie 702 des CARs** le lundi et un **vol charter passagers de navetteur ou de compagnie aérienne sous la partie 705 des CARs** le mercredi, les deux temps de vol doivent être mutualisés vers les mêmes **limites cumulées de service glissantes**. Les exploitants aériens qui tiennent des feuilles de suivi Excel séparées pour chaque sous-partie AOC sous-estiment systématiquement l'exposition totale à la fatigue des pilotes.

### Piège 3 — Les violations de FDP et de repos découvertes après le vol
La vérification manuelle des carnets de vol se produit souvent après l'émission d'une mise en service de vol ou lors du calcul mensuel des heures de paie. Au moment où un dépassement de la **période de service de vol (FDP) maximale** ou du **temps libre de service (période de repos)** est signalé, la brèche réglementaire s'est déjà produite — exposant le titulaire du certificat d'exploitant aérien (AOC) aux **sanctions administratives pécuniaires (AMPs) de Transport Canada**.

Une véritable **interception avant la mise en service** exige un recoupement automatisé de :
- la **période de service de vol (FDP)** prévue du jour et l'**heure de présentation locale (adapté vs. non adapté)**
- l'**accumulation de temps de vol** historique du pilote sur 28/90/365 jours
- le **nombre de secteurs** prévu et la durée moyenne des secteurs
- les **intervalles de repos avant et après le vol** obligatoires et le **temps libre de service de 36 heures / 7 jours**

---

## À qui est destiné ce modèle Excel de conformité aéronautique (rôles et scénarios d'usage)

Si vous cherchez une alternative abordable aux logiciels d'entreprise de gestion des équipages sans sacrifier l'exactitude réglementaire, cet outil est conçu pour vos scénarios opérationnels quotidiens :

| Rôle aéronautique | Scénario de recherche visé et flux opérationnel | Avantage principal de conformité |
|---|---|---|
| **Répartiteurs de vol** | Besoin d'un **calculateur de légalité des pilotes avant mise en service** pour vérifier la disponibilité de l'équipage lors des mises en service matinales ou des demandes de charter de dernière minute. | Drapeaux de conformité **Go / No-Go instantanés** avant la signature du plan de vol opérationnel. |
| **Planificateurs et gestionnaires d'équipage** | À la recherche d'un **tableur de roulement d'équipage et de suivi de la fatigue** pour construire des horaires mensuels sans dépasser les plafonds glissants de 28/90/365 jours. | Visibilité en temps réel sur la **capacité de vol légale restante** de chaque pilote dans la flotte. |
| **Pilotes en chef et DFO** | Exigent un **modèle de suivi du temps de vol du pilote en chef** pour superviser la charge de travail de l'équipage, approuver les extensions de service et prévenir la fatigue systémique. | Tableau de bord centralisé montrant la **mutualisation des heures mixtes CARs 702/705** et des alertes d'utilisation élevée. |
| **Responsables SMS et sécurité aérienne** | À la recherche d'un **journal de conformité Transport Canada prêt pour l'audit** pour préparer les inspections de validation de programme (PVI) et les audits SMS. | Dossiers historiques standardisés, à l'épreuve des falsifications, sans post-traitement requis. |
| **Petits et moyens exploitants AOC** | Exploitants canadiens régionaux, medevac, brousse et charter (3 à 30 pilotes) ayant besoin d'un **logiciel de suivi des temps de service à faible coût sous Excel**. | Remplace les journaux papier dispersés et les feuilles DIY fragiles par un **moteur de conformité Microsoft Excel** déterministe unique. |

---

## Ce que l'outil vous aide à suivre : correspondance entre points de douleur et solutions

Au lieu d'agir comme un carnet de vol numérique passif, ce classeur fonctionne comme un **moteur de règles réglementaires CARs 702/705** actif :

| Point de douleur opérationnel (ce qui casse en manuel) | Indicateur de conformité à haute fréquence suivi | Solution automatisée du classeur (comment elle le résout) |
|---|---|---|
| **Calcul manuel des fenêtres glissantes :** compter à rebours 28, 90 et 365 jours sur un calendrier mural pour plus de 15 pilotes chaque matin. | **Limites glissantes cumulées de temps de vol** (`100h / 28d`, `300h / 90d`, `1,000h / 365d`) | Les formules de tableaux dynamiques font glisser les fenêtres de rétrospection de 28, 90 et 365 jours vers l'avant chaque jour et calculent les heures légales restantes exactes. |
| **Recherches complexes dans la table FDP :** recouper les heures de présentation des pilotes avec les atterrissages prévus dans le manuel des CARs sous pression temporelle. | **Matrice des périodes de service de vol (FDP) de la partie 705 des CARs** (heure de présentation × nombre de secteurs) | Les tables de recherche réglementaires pré-encodées ajustent automatiquement la **FDP légale maximale** du pilote dès que vous saisissez l'heure de présentation et le nombre de secteurs. |
| **Vols multi-sous-parties cloisonnés :** oublier d'ajouter les heures de patrouille incendie de la partie 702 du mardi aux limites de charter passagers de la partie 705 du vendredi. | **Mutualisation des heures inter-sous-parties (CARs 702 / 703 / 704 / 705)** | Un schéma de données unifié étiquette chaque vol par sous-partie mais agrège toutes les heures de vol et de service dans un profil de conformité maître unique par pilote. |
| **Réaffectations de dernière minute :** un client ajoute deux segments supplémentaires en cours de journée, et la répartition ne sait pas si l'équipage dépassera les limites de service. | **Statut de légalité Go/No-Go avant mise en service** | La mise en forme conditionnelle en temps réel déclenche des alertes visuelles **Avertissement (proche de la limite)** et **Violation (bloqué)** *avant* que le vol ne soit mis en service. |
| **Préparation d'audit chaotique :** passer des jours à nettoyer les formules cassées et les dates manquantes avant une inspection de Transport Canada. | **Journaux historiques prêts pour l'audit Transport Canada** | Un registre structuré et filtrable permet d'exporter des historiques de conformité propres par pilote, immatriculation d'aéronef, plage de dates ou statut réglementaire en un clic. |

---

## Logique métier et méthodologie

### Le problème commercial central : conformité à fort enjeu contre économie du logiciel
Les petits et moyens exploitants aériens canadiens (exploitant 3 à 30 pilotes) font face à une contrainte structurelle. D'un côté, la **réglementation de Transport Canada sur les risques de fatigue et les temps de service** entraîne exactement la même responsabilité stricte pour une entreprise de charter de 10 pilotes que pour une grande compagnie aérienne. De l'autre, les plateformes SaaS d'entreprise de planification d'équipage (telles que Navblue, Jeppesen ou les modules d'entreprise FL3XX) exigent des frais de licence annuels élevés, une intégration longue et une administration informatique dédiée. Contraints de choisir, les petits AOC retombent sur des tableurs faits maison — introduisant **décroissance silencieuse des formules, erreurs de copier-coller et risque d'application rétroactive**.

### La méthodologie : interception déterministe avant mise en service
Pour résoudre ce problème sans les coûts d'une solution d'entreprise, ce classeur applique une **méthodologie d'interception déterministe avant mise en service** construite nativement dans le moteur de calcul de Microsoft Excel :

1. **Normalisation relationnelle des données à saisie unique :** au lieu d'organiser les feuilles par mois ou par sous-partie des CARs (ce qui casse le suivi longitudinal), toutes les entrées opérationnelles sont capturées dans un registre transactionnel normalisé unique (`Flight & Duty Log`). Chaque entrée est indexée par `Pilot_ID`, `UTC/Local_Date`, `Subpart_Tag`, `Report_Time` et `Sector_Count`.
2. **Modélisation par tableaux temporels à fenêtre glissante :** plutôt que d'utiliser des plages de sommation mensuelles statiques (`SUM(B2:B31)`), le moteur utilise une évaluation dynamique de tableaux bornés par dates (`[Current_Assignment_Date - N_Days, Current_Assignment_Date]`). Chaque ligne évalue son propre contexte historique simultanément sur les horizons de 28, 90 et 365 jours, garantissant que les violations historiques et les projections d'horaires futures soient calculées avec une cohérence mathématique de 100 %.
3. **Encodage de matrice réglementaire bidimensionnelle :** la **table FDP de la partie 705 des CARs** (qui régit les heures de service maximales selon les rythmes circadiens de l'heure de la journée et les secteurs de charge de travail) est codée en dur dans une matrice de référence immuable. Grâce à la correspondance multi-critères (`INDEX/MATCH` sur les seuils de bandes horaires et les tranches de secteurs), le classeur élimine l'erreur de recherche humaine pendant les fenêtres de mise en service à fort stress.
4. **Contrôle de conformité décalé en amont :** emprunté au principe de test « Shift-Left » du génie logiciel, la validation de conformité est déplacée de l'**audit après le vol** vers la **phase de simulation avant affectation**. En calculant `Projected_Accumulation = Historical_Rolling_Total + Planned_Duty_Input`, le modèle agit comme un disjoncteur préventif — signalant les affectations illégales tant qu'elles sont encore hypothétiques.

---

## Comparaison des flux opérationnels : tableurs manuels contre suiveur CARs automatisé

**Profil de référence de l'exploitant :** 12 pilotes commerciaux | AOC mixte **partie 702 (travail aérien)** et **partie 705 (compagnie aérienne / charter)** | Un seul bureau de répartition central.

**Le goulot d'étranglement opérationnel :** chaque matin, le répartiteur de vol passe 90 minutes à recouper manuellement les limites de service glissantes des pilotes avant de libérer l'horaire des vols du jour. Les heures de vol sont réparties entre deux fichiers Excel déconnectés — un pour les opérations 702, un pour les opérations 705. Lorsqu'un commandant de bord vole sous les deux sous-parties la même semaine, les totaux cumulés mutualisés doivent être calculés à la main. Sur un pic saisonnier de 90 jours, deux dépassements de limites glissantes ont passé au travers — tous deux découverts *après* le départ de l'aéronef, créant une **exposition immédiate à la conformité Transport Canada**.

| Dimension opérationnelle et de conformité | Avant : tableurs manuels déconnectés | Après : classeur de conformité CARs 702/705 unifié |
|---|---|---|
| **Architecture des dossiers de vol et de service** | Fragmentée entre fichiers CARs 702 et 705 séparés ; les onglets mensuels cassent les rétrospections glissantes | **Base de données Excel unifiée unique** avec suivi longitudinal continu pluriannuel |
| **Vérification de légalité matinale avant mise en service** | ~90 minutes de comptage manuel de dates et de vérifications à la calculatrice pour 12 pilotes | **Moins de 3 secondes par pilote** via des drapeaux automatisés du tableau de bord pré-mise en service |
| **Mutualisation des heures multi-sous-parties (702/705)** | Copier-coller manuel sujet aux erreurs entre tableurs en fin de semaine | **Mutualisation en temps réel 100 % automatisée** entre toutes les sous-parties des CARs dès la saisie des données |
| **Validation de la table FDP et des limites de secteurs** | Recherche manuelle dans des manuels réglementaires PDF ; risque élevé de mal lire les bandes horaires circadiennes | **Calcul FDP dynamique instantané** basé sur l'heure de présentation du pilote et les secteurs prévus |
| **Détection des violations et risque d'audit TC** | **Découverte après le vol** ; application rétroactive de Transport Canada et exposition aux AMP | **Interception avant mise en service** ; affectations d'équipage non conformes bloquées avant la libération du vol |

---

## Flux de démarrage rapide : comment valider la légalité d'un pilote en 4 étapes

Vous voulez voir à quelle vitesse vous pouvez vérifier la disponibilité légale d'un pilote ? Suivez ce flux en 4 étapes pour tester dès maintenant une mise en service de vol unique, puis passez au suivi complet de la flotte :

1. **Lancez le bac à sable web interactif (étape 1 — test gratuit mono-pilote) :**
   Ouvrez l'[**aperçu web en direct du calculateur des temps de vol et de service CARs 702/705**](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) dans votre navigateur. Aucune installation n'est requise pour tester un scénario d'affectation d'équipage unique.
2. **Saisissez l'heure de présentation prévue et le nombre de secteurs (étape 2 — vérification de la matrice FDP) :**
   Entrez l'**heure de présentation locale** prévue de votre pilote, les **heures de vol planifiées** et le **nombre de secteurs de vol**, puis sélectionnez la règle applicable (**partie 702 ou partie 705 des CARs**). Regardez le calculateur déterminer instantanément la **période de service de vol (FDP) légale maximale**.
3. **Vérifiez les limites cumulées glissantes de 28 / 90 / 365 jours (étape 3 — barrière pré-mise en service) :**
   Consultez l'**indicateur de statut de conformité pré-mise en service** automatisé. Le moteur signale immédiatement si le vol proposé pousse le pilote au-delà des plafonds réglementaires de Transport Canada de **100 heures (28 jours)**, **300 heures (90 jours)** ou **1 000 heures (365 jours)**.
4. **Passez au classeur Excel complet multi-pilotes (étape 4 — opérations de flotte continues) :**
   L'aperçu web est parfait pour une vérification de légalité ponctuelle, mais il se réinitialise lorsque vous fermez votre navigateur. Pour conserver les dossiers historiques des pilotes, mutualiser les heures sur **jusqu'à plus de 30 pilotes** et tenir des **journaux d'audit Transport Canada** permanents, [**téléchargez ici le modèle Excel complet et réutilisable des temps de vol et de service CARs 702/705**](https://www.theseusworkshop.com/l/dutytracker?utm_source=github&utm_medium=GitHub%20README&utm_campaign=readme%20new%20launch&utm_content=cars-flight-duty-tracker).

---

*La valeur opérationnelle n'est pas que Microsoft Excel remplace le jugement de conformité d'un pilote en chef. La valeur est que les **calculs réglementaires CARs 702/705** de routine cessent de dépendre de la mémoire humaine, du comptage manuel du calendrier et des tableurs fragmentés.*

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
Le pilote a 92 heures dans la fenêtre. 10 heures programmées le 16 juin.

- S'il a volé 4 heures le 19 mai : 92 − 4 + 10 = **98 h** — légal.  
- S'il a volé 0 heure le 19 mai : 92 − 0 + 10 = **102 h** — violation.

Un modèle mental de remise à zéro mensuelle approuve les deux. La fenêtre glissante ne l'approuve pas.

Chaque pilote porte trois de ces calculs simultanément : 28 jours, 90 jours et 365 jours.
Pour 15 pilotes, cela fait 45 calculs glissants en direct par cycle de mise en service, chacun nécessitant jusqu'à
365 jours de recherche historique. Les mathématiques ne nécessitent aucun jugement. L'automatisation élimine entièrement la classe d'erreurs.

**Pourquoi l'heure de présentation régit aussi la FDP :** Les limites FDP de la partie 705 dépendent du début du service.
Un service commençant à 09:00 peut légalement durer jusqu'à 13 heures ; le même service commençant à 01:00
est plafonné près de 11 heures — parce qu'il s'étend dans la fenêtre circadienne 02:00–05:59 où
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
- **Portée : parties 702 et 705 uniquement** — les exploitants sous la partie 703 (taxi aérien) ou la partie 704 (navetteur) travaillent sous des limites spécifiques différentes non encodées dans cette version
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

