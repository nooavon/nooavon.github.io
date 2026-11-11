---
title: "Evaluating \"Fair Chance\" Employment: Ban the Box and Minority Employment"
excerpt: "Bachelor's thesis (2026, grade 5/5). Replicates and extends a difference-in-differences study of Ban the Box laws using American Community Survey data, 2004–2019. Stata."
collection: portfolio
date: 2026-08-19 12:00:00 +0000
---

**Bachelor's thesis in Economics, Aalto University, 2026 (grade 5/5)**<br>
[View the code and thesis on GitHub](https://github.com/nooavon/Evaluating-Fair-Chance-Employment-Replication-Package){: .btn .btn--primary}

## Question

Ban the Box (BTB) laws stop employers from asking about criminal records early in the hiring process. Earlier research found that these laws may have reduced employment for young Black and Hispanic men, because some employers may guess at criminal records based on race. Burton and Wasser (2025) revisited this finding. My thesis asks whether their results still hold when the sample is extended by five more years.

## Data and method

- Annual **American Community Survey (ACS)** microdata from IPUMS, 2004–2019.
- Sample: U.S.-citizen men aged 25–34 without a bachelor's degree, split into non-Hispanic Black, Hispanic and non-Hispanic White groups.
- **Difference-in-differences** design, with BTB treatment assigned at the metropolitan area level.
- The sample ends in 2019 to avoid mixing the study period with the COVID-19 pandemic.

## What I added

- Reproduced the original 2004–2014 results, then extended the data to 2019 and updated the annual BTB law coding.
- Event-study tests for pre-existing trends, and checks for sensitivity to the 2008–2009 recession.
- Tests of whether pre-policy conditions predicted BTB adoption, whether BTB was linked to migration, and whether effects changed after 2014.
- Goodman–Bacon decompositions for the staggered treatment timing.

## Result

Across the three groups, the thesis finds **no robust employment effects** of Ban the Box. Some specifications produce statistically significant estimates, which the thesis interprets alongside the pre-trend diagnostics and multiple-testing concerns.

*Tools: Stata. This is an independent extension of Burton and Wasser's study, not a release by the original authors.*
