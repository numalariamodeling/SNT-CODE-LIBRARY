# CODE LIBRARY for SUB-NATIONAL TAILORING

**Version**: 13 September 2024  
**Authors**: Mohamed Sillah Kanu, Sammy Oppong, Jaline Gerardin

## Table of Contents
<details>
<summary>Click to expand</summary>

- [Overview](#overview)
- [Motivation](#motivation)
- [Objectives](#objectives)
- [Target audience](#target-audience)
- [Scope](#scope)
- [Library elements](#library-elements)
  - [A. DATA ASSEMBLY AND MANAGEMENT](#a-data-assembly-and-management)
    - [A.1 Shapefiles](#a1-shapefiles)
    - [A.2 Health Facilities](#a2-health-facilities)
    - [A.3 Routine case data from DHIS2](#a3-routine-case-data-from-dhis2)
    - [A.4 DHS data](#a4-dhs-data)
    - [A.5 Climate data](#a5-climate-data)
    - [A.6 LMIS data](#a6-lmis-data)
    - [A.7 Modeled data](#a7-modeled-data)
    - [A.8 Population data](#a8-population-data)
  - [B. EPIDEMIOLOGICAL STRATIFICATION](#b-epidemiological-stratification)
    - [B.1 Reporting Rate per Variable](#b1-reporting-rate-per-variable)
    - [B.2 Group and merge data frame](#b2-group-and-merge-data-frame)
    - [B.3 Crude Incidence by Year](#b3-crude-incidence-by-year)
    - [B.4 Adjusted Incidence by Year](#b4-adjusted-incidence-by-year)
    - [B.5 Option to Select Incidence](#b5-option-to-select-incidence)
    - [B.6 Risk Categorization](#b6-risk-categorization)
  - [C. STRATIFICATION OF OTHER DETERMINANTS](#c-stratification-of-other-determinants)
  - [D. REVIEW OF PAST INTERVENTIONS](#d-review-of-past-interventions)
  - [E. Targeting of interventions](#e-targeting-of-interventions)
  - [F. Retrospective analysis](#f-retrospective-analysis)
  - [G. Urban microstratification](#g-urban-microstratification)

</details>

---

## Overview

### Motivation
SNT is here to stay: many NMCPs have found it useful and are continuing to embrace it and further develop it for their analytical needs. Since 2019, multiple individuals have supported the analysis portions of SNT. In most cases, individuals have built their own code in a variety of languages (Stata, R, and Python), sometimes building on others’ previous code and sometimes re-developing independently.

As SNT matures, more quality assurance is needed so that NMCPs can be confident that the analysis used to inform their decisions is of high quality, regardless of the individual supporting the analyst. Continued rollout also means that analysis can become more efficient if analysts are better able to build on each other’s work, rather than tempted to reinvent what has already been developed. Lastly, SNT analysis can become much more accessible if there is a common resource available to help those with intermediate coding skills quickly access the collective knowledge of the SNT analyst community.

### Objectives
We will build a code library for SNT analysis to:
- Ensure that SNT analysts are using similar, correct approaches
- Improve efficiency of SNT analysis by minimizing duplication of effort
- Promote accessibility of SNT analysis by lowering barriers to entry

### Target audience
Anyone doing this kind of work. We assume some basic knowledge of R, some understanding of the data, and a strong connection to the NMCP.

### Scope
All analysis steps of SNT up to but not including mathematical modeling; some related analysis.

The code library will be in R and publicly available. It will be quality-assured and well-commented.

When multiple algorithmic options could be used, strengths and limitations of each one, along with discussion of when to use each option, as possible.

Framing text, and when possible the code comments, will be available in both English and French.

---

## Library elements

### A. DATA ASSEMBLY AND MANAGEMENT
<details>
<summary>Click to expand A. DATA ASSEMBLY AND MANAGEMENT</summary>

#### A.1 Shapefiles
- **A.1.1** Import shapefiles
- **A.1.2** Rename and match names
- **A.1.3** Link shapefiles to relevant scales
- **A.1.4** Visualizing shapefiles and making basic maps
```r
HOW TO DO IT (THE CODE)

