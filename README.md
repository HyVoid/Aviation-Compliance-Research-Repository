**Design principle:** Strict separation of data storage, calculation logic, and display layer. Entry is standardised; computation is fully automated; the presentation layer is read-only.

---

<a name="modules-en"></a>
## Core Modules

### Module 1 — Dashboard *(Decision Layer)*

- **Live Crew Status Board** — All pilots listed with colour-coded compliance state:
  - 🟢 Available
  - 🟡 Approaching limit (warning threshold)
  - 🔴 Blocked — fatigue or hours exhausted
  - 🔵 In mandatory rest (countdown to legal availability)
- **Pre-Flight Compliance Checker** — Dispatcher selects pilot, inputs report time and planned sectors; system immediately returns maximum permissible FDP and a compliant/non-compliant verdict

### Module 2 — `tbl_Pilots` *(Configuration Layer)*

| Field | Description |
|---|---|
| `Pilot ID` | Unique primary key |
| `Full Name` | Display name |
| `Primary Subpart` | Part 702 / Part 705 |
| `Home Base` | Base timezone (for acclimatisation calculation) |
| `Roster Option` | Part 705 scheduling option (Option 1 / Option 2) |

### Module 3 — `tbl_DutyLogs` *(Data Entry Layer)*

| Field | Description |
|---|---|
| `Record ID` | Auto-generated entry ID |
| `Pilot ID` | Foreign key to `tbl_Pilots` |
| `Duty Date` | Date of duty |
| `Operational Subpart` | Applicable regulation for this duty (702 / 705) |
| `Duty Start Local` | Report / check-in time |
| `Duty End Local` | Release time |
| `Flight Time (Block Hours)` | Actual block hours flown |
| `Sectors Flown` | Sector count (required for Part 705 FDP matrix) |
| `Split Duty Break (hrs)` | Rest break taken during split duty, if applicable |
| `Rest Period Provided (hrs)` | Actual rest received before this duty |

### Module 4 — `Engine_CARs` *(Calculation Engine — protected)*

Hidden/protected sheet containing all regulatory logic. See [Key Formulas](#formulas-en).

### Module 5 — `Audit_Reporter` *(Export Layer)*

Filter by pilot and date range; output a clean, TC-formatted compliance log suitable for direct PDF export. Designed to require zero post-processing before submission to a Transport Canada inspector.

---

<a name="regulatory-en"></a>
## Regulatory Scope

### Flight Time Limits (all subparts, rolling windows)

| Window | Limit |
|---|---|
| 24 hours (single-pilot) | ≤ 8 hours |
| Any 28 consecutive days | ≤ 112 hours |
| Any 90 consecutive days | ≤ 300 hours |
| Any 365 consecutive days | ≤ 1,000 hours |

### Duty Time Limits

| Window | Limit |
|---|---|
| Any 28 consecutive days | ≤ 192 hours |
| Any 365 consecutive days | ≤ 2,200 – 2,400 hours (schedule-dependent) |

### Part 705 Maximum FDP Matrix

Maximum FDP is determined by a two-dimensional lookup:
- **Axis 1** — Report time window (e.g. `04:00–06:59`, `07:00–12:59`, `13:00–17:59`, etc.)
- **Axis 2** — Number of sectors planned

The resulting value ranges from 9 to 13 hours and may be extended under augmented crew or split-duty provisions.

---

<a name="formulas-en"></a>
## Key Formulas

**Part 705 — Maximum FDP (two-dimensional matrix lookup)**

```excel
=XLOOKUP(
  StartTimeHour,
  CARs_TimeRange_Column,
  XLOOKUP(Sectors, CARs_Sectors_Header_Row, FDP_Matrix)
)
```

**28-day rolling flight time accumulation**

```excel
=SUMIFS(
  [Flight Time],
  [Pilot ID], [@Pilot ID],
  [Duty Date], ">="&([@Duty Date]-27),
  [Duty Date], "<="&[@Duty Date]
)
```

Replace `-27` with `-89` and `-364` for 90-day and 365-day windows respectively. Compare output against `112`, `300`, and `1000` hour thresholds.

---

<a name="outcomes-en"></a>
## Business Outcomes

| Dimension | Before | After |
|---|---|---|
| Violation risk | Discovered post-flight; TC penalties applied retroactively | 100% pre-flight interception; non-compliant dispatch is blocked |
| Scheduling check time | 20–30 min per pilot per check (manual) | < 3 seconds |
| Audit preparation | 2–3 days to reconstruct records | Instant — filter and export in < 5 seconds |
| Crew utilisation | Conservative 1–2 hour manual buffer wasted | Minute-level precision; every legal minute utilised |
| Data integrity | Dispatcher copy vs. pilot copy frequently diverge | Single source of truth across all calculations and reports |

---

<br>
<div align="right"><a href="#english">↑ Back to top (EN)</a> · <a href="#français">Français →</a> · <a href="#简体中文">中文 →</a></div>

---
---

<a name="français"></a>

# ✈️ CARs Parties 702/705 — Outil de suivi de conformité temps de vol et de service

<div align="center">

![Licence](https://img.shields.io/badge/licence-MIT-blue)
![Plateforme](https://img.shields.io/badge/plateforme-Microsoft%20Excel-217346)
![Réglementation](https://img.shields.io/badge/réglementation-CARs%20702%2F705-red)
![Langue](https://img.shields.io/badge/langue-EN%20%7C%20FR%20%7C%20ZH-lightgrey)

**Console opérationnelle Excel de niveau conformité pour les exploitants aériens canadiens  
détenant une autorisation mixte AOC en vertu des Parties 702 et 705 du RAC de Transports Canada.**

</div>

---

## Table des matières

- [Contexte](#contexte-fr)
- [Définition du problème](#probleme-fr)
- [Architecture de la solution](#architecture-fr)
- [Modules principaux](#modules-fr)
- [Portée réglementaire](#reglementaire-fr)
- [Formules clés](#formules-fr)
- [Résultats opérationnels](#resultats-fr)

---

<a name="contexte-fr"></a>
## Contexte

Cet outil est conçu pour les entreprises d'aviation à opérations mixtes détenant simultanément :

- Une autorisation **Partie 702** — travail aérien (patrouille de pipelines, levés, lutte aérienne contre les incendies)
- Une autorisation **Partie 705** — transport aérien commercial (vols réguliers ou affrétés, passagers et fret)

Les répartiteurs et coordinateurs d'équipages opérant sous ces deux sous-parties font face à une charge de conformité cumulative : ils doivent appliquer deux référentiels réglementaires distincts en parallèle, souvent pour le même pilote sur des jours de service consécutifs.

Transports Canada a progressivement renforcé son régime d'application des **limites de temps de vol et de service (FTDT)**. Les Parties 702/705 du RAC ont force de loi obligatoire — elles ne constituent pas de simples lignes directrices. Une seule infraction détectée lors d'un audit TC peut entraîner :

- Des amendes de dizaines de milliers de dollars canadiens
- La suspension ou le retrait du certificat d'exploitation aérienne (CEA)
- La suspension des licences de pilotes individuels

---

<a name="probleme-fr"></a>
## Définition du problème

### Points de douleur

| Point de douleur | Description |
|---|---|
| Surcharge de calcul manuel | Les répartiteurs calculent manuellement les totaux glissants sur 7/28/90 jours avant chaque assignation — 20 à 30 min par pilote par vérification |
| Conformité réactive | Les infractions sont souvent détectées après le vol lors de la saisie des journaux, une fois le manquement légal déjà survenu |
| Coût de préparation aux audits | Reconstituer des dossiers conformes à partir de feuilles de calcul dispersées nécessite 2 à 3 jours par cycle d'audit TC |

### Difficultés techniques

- **Matrice de règles à double sous-partie** — Les limites de PDS de la Partie 705 suivent une matrice étagée de 9 à 13 heures indexée par plage horaire de présentation (p. ex. `00:00–03:59`, `07:00–12:59`) et par nombre de secteurs ; la Partie 702 applique un standard distinct bien que plus simple
- **Accumulation sur fenêtre glissante** — Le RAC impose des limites dans *tout* intervalle consécutif de 28/90/365 jours, et non par mois civil ; les fonctions `SOMME` standard ne peuvent pas gérer cela
- **Mutualisation des heures entre sous-parties** — Les heures effectuées sous la Partie 702 consomment les quotas glissants de la Partie 705 et vice versa ; aucune séparation n'existe entre les totaux par sous-partie

---


**Principe de conception :** Séparation stricte entre stockage des données, logique de calcul et couche d'affichage. La saisie est normalisée ; le calcul est entièrement automatisé ; la couche de présentation est en lecture seule.

---

<a name="modules-fr"></a>
## Modules principaux

### Module 1 — Tableau de bord *(Couche décisionnelle)*

- **Tableau de statut d'équipage en temps réel** — Tous les pilotes listés avec état de conformité codé par couleur :
  - 🟢 Disponible
  - 🟡 Approche de la limite (seuil d'avertissement)
  - 🔴 Bloqué — fatigue ou heures épuisées
  - 🔵 En repos réglementaire obligatoire (compte à rebours jusqu'à disponibilité légale)
- **Vérificateur de conformité pré-vol** — Le répartiteur sélectionne le pilote, saisit l'heure de présentation et les secteurs prévus ; le système retourne immédiatement le PDS maximal autorisé et un verdict conforme / non conforme

### Module 2 — `tbl_Pilotes` *(Couche de configuration)*

| Champ | Description |
|---|---|
| `ID Pilote` | Clé primaire unique |
| `Nom complet` | Nom d'affichage |
| `Sous-partie principale` | Partie 702 / Partie 705 |
| `Base d'attache` | Fuseau horaire de base (pour calcul d'acclimatation) |
| `Option de tableau de service` | Option de planification Partie 705 (Option 1 / Option 2) |

### Module 3 — `tbl_JournauxService` *(Couche de saisie)*

| Champ | Description |
|---|---|
| `ID Enregistrement` | Identifiant auto-généré |
| `ID Pilote` | Clé étrangère vers `tbl_Pilotes` |
| `Date de service` | Date du service |
| `Sous-partie opérationnelle` | Réglementation applicable à ce service (702 / 705) |
| `Début service (heure locale)` | Heure de présentation / enregistrement |
| `Fin service (heure locale)` | Heure de libération |
| `Temps de vol (heures bloc)` | Heures bloc réellement effectuées |
| `Secteurs effectués` | Nombre de secteurs (requis pour la matrice PDS Partie 705) |
| `Pause service fractionné (h)` | Durée de la pause en cas de service fractionné, le cas échéant |
| `Repos accordé (h)` | Repos effectivement obtenu avant ce service |

### Module 4 — `Moteur_RAC` *(Moteur de calcul — protégé)*

Feuille masquée/protégée contenant toute la logique réglementaire. Voir [Formules clés](#formules-fr).

### Module 5 — `Rapport_Audit` *(Couche d'export)*

Filtrer par pilote et plage de dates ; exporter un journal de conformité propre et formaté selon les normes TC, directement prêt pour l'exportation PDF. Conçu pour ne nécessiter aucun post-traitement avant soumission à un inspecteur de Transports Canada.

---

<a name="reglementaire-fr"></a>
## Portée réglementaire

### Limites de temps de vol (toutes sous-parties, fenêtres glissantes)

| Fenêtre | Limite |
|---|---|
| 24 heures (pilote unique) | ≤ 8 heures |
| Tout intervalle de 28 jours consécutifs | ≤ 112 heures |
| Tout intervalle de 90 jours consécutifs | ≤ 300 heures |
| Tout intervalle de 365 jours consécutifs | ≤ 1 000 heures |

### Limites de temps de service

| Fenêtre | Limite |
|---|---|
| Tout intervalle de 28 jours consécutifs | ≤ 192 heures |
| Tout intervalle de 365 jours consécutifs | ≤ 2 200 – 2 400 heures (selon le programme) |

### Matrice de PDS maximum — Partie 705

Le PDS maximum est déterminé par une recherche bidimensionnelle :
- **Axe 1** — Plage horaire de présentation (p. ex. `04:00–06:59`, `07:00–12:59`, `13:00–17:59`, etc.)
- **Axe 2** — Nombre de secteurs planifiés

La valeur résultante varie de 9 à 13 heures et peut être prolongée en cas d'équipage augmenté ou de service fractionné.

---

<a name="formules-fr"></a>
## Formules clés

**Partie 705 — PDS maximum (recherche matricielle bidimensionnelle)**

```excel
=XLOOKUP(
  HeureDePresentation,
  ColonnePlagesHoraires_RAC,
  XLOOKUP(Secteurs, LigneEnTeteSecteurs_RAC, Matrice_PDS)
)
```

**Accumulation glissante du temps de vol sur 28 jours**

```excel
=SOMME.SI.ENS(
  [Temps de vol],
  [ID Pilote], [@ID Pilote],
  [Date de service], ">="&([@Date de service]-27),
  [Date de service], "<="&[@Date de service]
)
```

Remplacer `-27` par `-89` et `-364` pour les fenêtres de 90 et 365 jours respectivement. Comparer la sortie aux seuils de `112`, `300` et `1 000` heures.

---

<a name="resultats-fr"></a>
## Résultats opérationnels

| Dimension | Avant | Après |
|---|---|---|
| Risque d'infraction | Détecté après le vol ; pénalités TC appliquées rétroactivement | Interception pré-vol à 100 % ; les dispatches non conformes sont bloqués |
| Durée de vérification de planification | 20–30 min par pilote par vérification (manuel) | < 3 secondes |
| Préparation aux audits | 2–3 jours pour reconstituer les dossiers | Instantanée — filtrer et exporter en < 5 secondes |
| Utilisation des équipages | Tampon manuel conservateur de 1–2 heures gaspillé | Précision à la minute ; chaque minute légale est utilisée |
| Intégrité des données | Copie répartiteur vs copie pilote fréquemment divergentes | Source unique de vérité pour tous les calculs et rapports |

---

<br>
<div align="right"><a href="#français">↑ Haut de page (FR)</a> · <a href="#english">← English</a> · <a href="#简体中文">中文 →</a></div>

---
---

<a name="简体中文"></a>

# ✈️ CARs 第702/705部 — 飞行与值勤时间合规追踪工具

<div align="center">

![许可证](https://img.shields.io/badge/许可证-MIT-blue)
![平台](https://img.shields.io/badge/平台-Microsoft%20Excel-217346)
![法规](https://img.shields.io/badge/法规-CARs%20702%2F705-red)
![语言](https://img.shields.io/badge/语言-EN%20%7C%20FR%20%7C%20ZH-lightgrey)

**面向同时持有加拿大交通部 CARs 第702部与第705部双重 AOC 权限的航空运营商  
所设计的合规级 Excel 运营控制台。**

</div>

---

## 目录

- [背景](#background-zh)
- [问题定义](#problem-zh)
- [解决方案架构](#architecture-zh)
- [核心模块](#modules-zh)
- [法规范围](#regulatory-zh)
- [核心公式](#formulas-zh)
- [业务成效](#outcomes-zh)

---

<a name="background-zh"></a>
## 背景

本工具面向同时持有以下运营资质的混合运营航空公司：

- **第702部**授权 — 空中作业（巡线、测绘、空中消防等）
- **第705部**授权 — 商业航空运输（定期/不定期客货包机）

在双授权体系下运营的签派员和排班协调员面临叠加的合规负担：他们必须在同一套体系内并行应用两套完全不同的法规标准，且同一飞行员在连续值勤日内可能频繁跨部切换。

加拿大交通部（TC）近年来持续收紧**飞行与值勤时间限制（FTDT）**的执法力度。CARs 第702/705部具有强制法律效力，并非指导性意见。一旦在审计中发现任何违规，可能面临：

- 数万加元的高额罚款
- 暂停或吊销航空营运人证书（AOC）
- 飞行员个人执照受罚

---

<a name="problem-zh"></a>
## 问题定义

### 痛点

| 痛点 | 描述 |
|---|---|
| 人工计算负荷高 | 签派员在每次排班前需手动汇总7/28/90天滚动累计值，每人每次耗时20–30分钟 |
| 合规管理滞后 | 违规往往在飞行完成后的日志录入环节才被发现，法律风险已经发生 |
| 审计准备成本高 | 从分散的纸质记录或基础表格中重建合规档案，每次 TC 审计需耗费2–3天 |

### 技术难点

- **双部矩阵规则** — 第705部最大飞行值勤期（FDP）遵循9至13小时的阶梯矩阵，以报到时间区间（如`00:00–03:59`、`07:00–12:59`）和扇区数量为双轴索引；第702部采用不同但更简单的标准
- **滚动窗口累积** — CARs 要求计算*任意*连续28/90/365天内的累计时间，而非按自然月；标准 `SUM` 函数无法处理此逻辑
- **跨部时间共用** — 第702部执勤消耗第705部的滚动额度，反之亦然；两套法规下的时间没有独立计算空间

---

**设计原则：** 数据存储、计算逻辑与展示层严格分离。录入端规范化，计算端全自动，展示层只读。

---

<a name="modules-zh"></a>
## 核心模块

### 模块一 — Dashboard（可视化看板 · 决策层）

- **机组状态实时监控** — 全员列表配合色块编码合规状态：
  - 🟢 正常可用
  - 🟡 临界预警（接近限额阈值）
  - 🔴 严禁排班（疲劳 / 时间耗尽）
  - 🔵 法定休息中（倒计时显示距离合法可用还剩多少小时）
- **起飞前合规推演器** — 签派员选择飞行员、输入预计报到时间与扇区数，系统即时反馈最大允许 FDP 及合规/不合规判定

### 模块二 — `tbl_Pilots`（飞行员主数据 · 配置层）

| 字段 | 描述 |
|---|---|
| `Pilot ID` | 唯一主键 |
| `Full Name` | 显示名称 |
| `Primary Subpart` | 主运营法规：第702部 / 第705部 |
| `Home Base` | 基地时区（用于时区适应性计算） |
| `Roster Option` | 第705部排班方案（选项1 / 选项2） |

### 模块三 — `tbl_DutyLogs`（值勤日志 · 录入层）

| 字段 | 描述 |
|---|---|
| `Record ID` | 自动生成的记录ID |
| `Pilot ID` | 关联 `tbl_Pilots` 的外键 |
| `Duty Date` | 值勤日期 |
| `Operational Subpart` | 本次值勤适用法规（702 / 705） |
| `Duty Start Local` | 报到/开始值勤时间（本地时间） |
| `Duty End Local` | 释放/结束值勤时间（本地时间） |
| `Flight Time (Block Hours)` | 实际执行的轮挡飞行小时数 |
| `Sectors Flown` | 扇区数（第705部 FDP 矩阵必要输入） |
| `Split Duty Break (hrs)` | 拆分值勤中的休息时长（如适用） |
| `Rest Period Provided (hrs)` | 本次值勤前实际获得的休息时间 |

### 模块四 — `Engine_CARs`（计算引擎 · 保护页）

隐藏/保护工作表，承载所有法规计算逻辑。详见[核心公式](#formulas-zh)。

### 模块五 — `Audit_Reporter`（审计报告 · 导出层）

按飞行员与时间段筛选，输出排版规范、符合 TC 格式要求的合规日志，支持直接 PDF 导出，提交审计前无需任何二次处理。

---

<a name="regulatory-zh"></a>
## 法规范围

### 飞行时间限制（全部子法规 · 滚动窗口）

| 滚动窗口 | 限制 |
|---|---|
| 任意24小时（单飞行员） | ≤ 8小时 |
| 任意连续28天 | ≤ 112小时 |
| 任意连续90天 | ≤ 300小时 |
| 任意连续365天 | ≤ 1,000小时 |

### 值勤时间限制

| 滚动窗口 | 限制 |
|---|---|
| 任意连续28天 | ≤ 192小时 |
| 任意连续365天 | ≤ 2,200 – 2,400小时（取决于调休方案） |

### 第705部最大飞行值勤期矩阵

最大 FDP 通过二维查找确定：
- **轴一** — 报到时间区间（如`04:00–06:59`、`07:00–12:59`、`13:00–17:59` 等）
- **轴二** — 计划扇区数量

结果值介于9至13小时之间，扩编机组或拆分值勤情况下可依规延长。

---

<a name="formulas-zh"></a>
## 核心公式

**第705部 — 最大 FDP（二维矩阵检索）**

```excel
=XLOOKUP(
  报到时间小时值,
  CARs时间区间列,
  XLOOKUP(扇区数, CARs扇区表头行, FDP矩阵)
)
```

**28天滚动飞行时间累积**

```excel
=SUMIFS(
  [Flight Time],
  [Pilot ID], [@Pilot ID],
  [Duty Date], ">="&([@Duty Date]-27),
  [Duty Date], "<="&[@Duty Date]
)
```

90天与365天窗口分别将 `-27` 替换为 `-89` 和 `-364`，并与 `112`、`300`、`1000` 小时限额进行比对。

---

<a name="outcomes-zh"></a>
## 业务成效

| 评估维度 | 采用前 | 采用后 |
|---|---|---|
| 违规风险控制 | 飞行后发现；TC 罚款追溯施加 | 起飞前100%拦截；不合规签派被系统阻断 |
| 排班校验效率 | 人工计算20–30分钟/人/次 | 3秒内完成 |
| 审计准备时间 | 重建记录需2–3天 | 即时导出，全程<5秒 |
| 机组运力挖掘 | 人工保守预留1–2小时缓冲造成运力浪费 | 分钟级精度；合法可用时间全部利用 |
| 数据一致性 | 签派记录与飞行员记录频繁对不上 | 单一数据源，计算与报表全部基于同一表格 |

---

<br>
<div align="right"><a href="#简体中文">↑ 返回顶部</a> · <a href="#english">← English</a> · <a href="#français">← Français</a></div>
