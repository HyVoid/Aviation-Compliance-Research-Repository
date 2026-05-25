<!-- Language Navigation -->
<div align="center">

[English](#english) · [Français](#français) · [简体中文](#简体中文)

</div>

---

<a name="english"></a>

# ✈️ CARs Part 702/705 — Flight & Duty Time Compliance Tracker

<div align="center">

![License](https://img.shields.io/badge/license-MIT-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)
![Language](https://img.shields.io/badge/lang-EN%20%7C%20FR%20%7C%20ZH-lightgrey)

**A compliance-grade Excel operations console for Canadian aviation operators  
holding dual AOC authority under Transport Canada CARs Part 702 and Part 705.**

</div>

---

## Table of Contents

- [Background](#background-en)
- [Problem Statement](#problem-en)
- [Solution Architecture](#architecture-en)
- [Core Modules](#modules-en)
- [Regulatory Scope](#regulatory-en)
- [Key Formulas](#formulas-en)
- [Business Outcomes](#outcomes-en)

---

<a name="background-en"></a>
## Background

This tool is designed for mixed-operation aviation companies simultaneously holding:

- **Part 702** authority — aerial work (pipeline patrol, survey, aerial firefighting)
- **Part 705** authority — commercial air transport (scheduled/charter passenger and cargo)

Dispatchers and crew schedulers operating under both subparts face a compounding compliance burden: they must apply two distinct regulatory frameworks concurrently, often for the same pilot on consecutive duty days.

Transport Canada has progressively tightened its **Flight Time and Duty Time (FTDT)** enforcement regime. CARs Part 702/705 carry mandatory legal force — not advisory status. A single infraction detected during a TC audit can result in:

- Fines of tens of thousands of Canadian dollars
- Suspension or revocation of the Air Operator Certificate (AOC)
- Suspension of individual pilot licences

---

<a name="problem-en"></a>
## Problem Statement

### Pain Points

| Pain Point | Description |
|---|---|
| Manual calculation overhead | Dispatchers manually tally 7/28/90-day rolling totals before every assignment — 20–30 min per pilot per check |
| Reactive compliance | Violations are often discovered post-flight during log entry, after the legal breach has already occurred |
| Audit preparation cost | Reconstructing compliant records from scattered spreadsheets takes 2–3 days per TC audit cycle |

### Technical Difficulties

- **Dual-subpart rule matrix** — Part 705 FDP limits follow a 9–13 hour tiered matrix indexed by report time window (e.g. `00:00–03:59`, `07:00–12:59`) and sector count; Part 702 applies a flatter but distinct standard
- **Rolling-window accumulation** — CARs mandates limits within *any* consecutive 28/90/365-day window, not calendar months; standard `SUM` functions cannot handle this
- **Cross-subpart hour pooling** — Hours flown under Part 702 consume Part 705 rolling quotas and vice versa; there is no separation between subpart totals

---

<a name="architecture-en"></a>
## Solution Architecture
