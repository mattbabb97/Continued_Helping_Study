# README: Capuchin Partner-Directed Helping and Reciprocity: Data & Statistical Analysis

## Project Overview

This project examines whether capuchin monkeys (*Sapajus spp*) continue to help a partner in a cooperative barpull task after they have already received their own reward, and whether that helping depends on reciprocity over short (trial-to-trial) and long (cumulative) time frames or on relationship quality (Composite Sociality Index, CSI).

**Species:** Brown capuchin monkeys (*Sapajus spp*)  

**N:** 7 subjects across 5 dyads 

**Task:** Manual cooperative barpull task with removable blockers

---

## Repository Structure

```
project/
├── README.md
├── Study_3_Analysis_v8.Rmd     # Full analysis pipeline: data prep, GLMMs, LMM, post-hoc tests, diagnostics, figures
├── Study_3_Final_Data.csv      # Trial-by-trial data used in the primary models
├── long_data_final.csv         # Long-format data (one row per subject per trial, used for the reciprocity models)
├── CSI_Values.csv              # Dyadic Composite Sociality Index values
└── Figure_S1 [FINAL].png       # Supplementary Figure S1
```

---

## Task Design

### Apparatus

Pairs of capuchins worked together on a loose string barpull apparatus. Once the tray was within reach, two barriers blocked access to the food (hereafter, blockers). Both capuchins needed to work together (again) to each remove their blocker so the food could be accessed.

### Trial Types

| Trial type  | Description |
|-------------|-------------|
| Early/End   | Subject's reward available early; partner's reward available only if subject moved their blocker. Helping occurs after the subject has already been rewarded. |
| Early/Early | Both rewards available early. Blocker movement is not needed by the partner or subject. This controls for general blocker movement. |
| End/End     | Both rewards available only after tray is pulled within reach and both blockers are removed. This obtained baseline rates of coordination for a dyad |

### Conditions

| Condition   | Description |
|-------------|-------------|
| Unilateral  | Roles fixed, so the partner could never return help within the session. Serves as the no-contingency baseline. |
| Alternating | Roles alternate within a session, so helping can be returned within the session. |

---

## Statistical Analysis

### Software

- **Language:** R
- **IDE:** RStudio
- **Key packages:**
  - `lme4`: binomial GLMMs (`glmer()`)
  - `glmmTMB`: Gaussian LMM for latency
  - `emmeans`: post-hoc contrasts (`emmeans()`, `emtrends()`, `pairs()`)
  - `car`: Wald Type III chi-square tests (`Anova()`)
  - `DHARMa`: residual diagnostics
  - `splines`: natural spline on session for the latency model
  - 'ggplot2': creating visualizations

### Running the Code

1. Place all CSV files in the same folder as `Study_3_Analysis_v8.Rmd`.
2. Update the `setwd()` path at the top of the Rmd, or open the folder as an RStudio project.
3. Knit the Rmd or run chunks in order.

## Contact

For questions about the data or analysis, contact the corresponding author at matthew.h.babb@gmail.com.


