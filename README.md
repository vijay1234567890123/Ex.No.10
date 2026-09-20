#  AI-Based Smart Traffic Signal Optimization Integrated with Road Safety Audit

**Exp 10 — Capstone Mini Project: Prompt Engineering for Real-World Engineering Application**
*Subject: 19TD608 — Prompt Engineering*

[![Domain](https://img.shields.io/badge/Domain-Civil%20Engineering-blue)]()
[![Focus](https://img.shields.io/badge/Focus-Intelligent%20Transportation%20Systems-orange)]()
[![Model](https://img.shields.io/badge/ML%20Model-Random%20Forest%20Regression-green)]()
[![Status](https://img.shields.io/badge/Status-Phase%201%20Report-yellow)]()

---

##  Aim

To apply prompt engineering techniques to design, generate, and validate a real-world civil engineering deliverable — an AI-based traffic signal optimization model integrated with a Road Safety Audit — for Chettipedu Junction on the Chennai–Bengaluru National Highway.

---

##  Overview

This experiment applies **prompt engineering** as a working method to solve a real-world civil engineering problem: reducing traffic delay and improving safety at **Chettipedu Junction**, a four-leg at-grade intersection on the Chennai–Bengaluru National Highway (Kancheepuram district, Tamil Nadu).

Structured prompting was used to (a) design the field-survey framework, (b) drive a Random Forest regression model for AI-based signal-timing prediction, and (c) generate a formal, IRC-consistent Road Safety Audit — combining efficiency optimization and safety evaluation into one framework, a gap identified across 20 reviewed studies.

| | |
|---|---|
| **Name** | Anangi Vijay Vishal (212223030001)|
| **Guide** | Dr. P. Raghunatha Pandian |
| **Institution** | Saveetha Engineering College, Anna University |
| **Report Type** | Project Phase-1 Report, Sep 2026 |

---

##  Problem Statement

Chettipedu Junction runs on a **fixed-time signal** that ignores real-time demand. The Chennai–Bengaluru through movement carries ~65% of total traffic but received under half the green time — causing heavy delay on the highway approaches, while local diversion behavior (service-road merge + an informal heavy-vehicle shortcut toward Nemam) compounds congestion and safety risk.

##  Objectives

- Collect and analyze peak-hour traffic volume across all 4 approaches
- Convert mixed traffic into Passenger Car Units (PCU) for standardized comparison
- Conduct a Stage-3 Road Safety Audit against IRC:SP:88 criteria
- Train an AI regression model to predict optimized signal green times
- Compare existing vs. AI-optimized performance (delay, queue, LOS)
- Recommend geometric/operational safety fixes

---

##  Prompt Engineering Methodology

The core engineering artifacts of this project — literature synthesis, methodology design, data-consistency checks, and the results narrative — were produced through iterative, structured prompting rather than one-shot generation.

**Prompting techniques applied:**

| Technique | Where it was used |
|---|---|
| **Role + format-locking prompts** | Replicating a fixed IRC-style report structure (chapters, table/caption formatting) across all sections |
| **Few-shot exemplars** | Matching a reference literature-review paragraph pattern: `Author et al. (year) investigated X... found Y... However, limitation Z` across 20 real, verified citations |
| **Constraint-based prompts** | Enforcing a fixed 105-second cycle length and 14-second minimum green time in every optimization output |
| **Iterative refinement** | Moving from a simplified 4-phase signal assumption to a more realistic 3-phase (N-S combined, East, West) model |
| **Self-consistency checks** | Ensuring turning-movement totals, PCU totals, and signal-timing entries stayed internally consistent across a 192-record interval-level dataset |
| **Trade-off surfacing prompts** | Explicitly prompting for *both* improvements and regressions, rather than accepting only favorable results |

---

##  Technical Approach

```
Field Traffic Data Collection (Peak-Hour Vehicle Counts)
        ↓
Traffic Volume Analysis (PCU Conversion)
        ↓
Road Safety Audit (Geometric & Operational Review — IRC:SP:88)
        ↓
AI Model Development (Random Forest — Signal Timing Prediction)
        ↓
Signal Timing Optimization (Green Time & Cycle Length)
        ↓
Performance Evaluation (Delay & Level of Service Comparison)
```

**Model:** Random Forest Regression
**Inputs:** phase-wise PCU volume, time-of-day period, vehicle-type composition ratio
**Output:** optimized green time (seconds) per phase
**Constraints:** 105 s fixed cycle length, 14 s minimum green time per phase

---

##  Key Results

| Metric | Existing Signal | AI-Optimized | Change |
|---|---|---|---|
| R² Score (model fit) | — | **0.91** | — |
| MAE | — | **1.8 sec** | — |
| North approach delay | 40 s | 26 s | **−35%** |
| South approach delay | 39 s | 25 s | **−36%** |
| East approach delay | 29 s | 32 s | +10% (trade-off) |
| West approach delay | 29 s | 34 s | +17% (trade-off) |
| Volume-weighted avg. delay | 36.0 s (LOS D) | **27.9 s (LOS C)** | Improved |

The optimization reallocates green time proportionally to demand (+12 s to North–South, −6 s each to East/West) — cutting highway delay substantially, at an explicit, disclosed cost to the minor cross-road approaches.

**Road Safety Audit:** 20 field observations logged; 7 flagged high-priority, including a missing pedestrian crossing, absent right-turn channelization, missing signage, and an unsignalized service-road merge conflict.

---

##  Repository Structure

```
├── Chettipedu_Traffic_Report.docx              # Full 31-page Phase-1 report
├── Chettipedu_Traffic_Data_Collection_Filled.xlsx  # 8-sheet interval-level dataset
├── Chettipedu_Traffic_PPT.pptx                 # 24-slide presentation deck
└── README.md                                   # This file
```

---

##  Limitations & Future Scope

- Field data is **limited**, not a multi-day survey — flagged for field validation before implementation
- Optimization uses simple proportional allocation; a **constrained/weighted objective** capping the minor-approach delay increase is proposed as future work
- No real-time sensor deployment yet — an IoT/RFID-based density-sensing path is noted as a plausible incremental upgrade

---

##  Result

Prompt engineering techniques (role/format-locking, few-shot exemplars, constraint-based prompting, iterative refinement, and self-consistency checks) were successfully applied to generate a complete, internally consistent civil engineering deliverable for Chettipedu Junction.

The AI-optimized signal plan, produced through this prompting workflow, reduced the volume-weighted average intersection delay from **36.0 s (LOS D)** to **27.9 s (LOS C)** — a **~22% overall improvement** — with the trade-off on minor approaches explicitly surfaced rather than hidden. The Random Forest model achieved **R² = 0.91** with **MAE = 1.8 s**, confirming the approach is practically viable.

**Thus, prompt engineering was successfully used to model, optimize, and document a real-world traffic signal engineering problem, and the desired output (an AI-optimized signal plan with an integrated Road Safety Audit) was achieved.**

---

##  References

20 peer-reviewed sources spanning DRL-based signal control, Road Safety Audit methodology (incl. IRC:SP:88-2019), PCU/mixed-traffic characterization, ML-based delay prediction (Random Forest, XGBoost), and route-diversion/pedestrian-safety literature. Full list in the report's References section.

---

*Prepared as part of Exp 10 (Capstone Mini Project) for the Prompt Engineering course, demonstrating structured prompting applied to a real civil engineering deliverable.*
