<!-- Language Navigation -->
<div align="center">

[English](#english)

</div>

---

<a name="english"></a>

# Prevent Flight Duty Time Violations Before Dispatch

<div align="center">

![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Platform](https://img.shields.io/badge/platform-Microsoft%20Excel-217346)
![Regulation](https://img.shields.io/badge/regulation-CARs%20702%2F705-red)

**Designed for Canadian Part 702 and Part 705 operators who need to track flight time, duty time, fatigue exposure, and rolling compliance limits before a pilot is assigned.**

[Live Preview](https://hyvoid.github.io/Aviation-Compliance-Research-Repository/) | [Purchase Complete Excel](https://alexhasgreatestuff.gumroad.com/l/dutytracker)

</div>

Track rolling flight time limits, detect compliance risks in seconds, and maintain a single auditable source of truth for pilot duty records.

---

## Quick Preview

<img width="1672" height="941" alt="ChatGPT Image May 25, 2026, 11_47_04 AM" src="https://github.com/user-attachments/assets/cc792931-2477-40d4-9bd7-e92418817c77" />



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
[see what else is available →](https://alexhasgreatestuff.gumroad.com)

---

## License

Distributed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

---



---
---

