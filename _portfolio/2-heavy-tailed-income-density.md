---
title: "Predicting a Heavy-Tailed Income Density"
excerpt: "How much data does it take to learn the top of an income distribution? Compares spline regression, k-nearest neighbours and gradient boosting on simulated incomes. Python."
collection: portfolio
date: 2026-10-11 12:00:00 +0000
---

[View the code and report on GitHub](https://github.com/nooavon/Predicting-a-Heavy-Tailed-Income-Density){: .btn .btn--primary}

## Question

Most people's incomes follow a fairly regular pattern, but a small group of very high earners creates a long "tail". How much data does a model need to learn that tail, and what breaks a model first?

## Approach

- Simulated incomes from a mix of a lognormal distribution (most people) and a heavy-tailed Lomax distribution (very high earners).
- Trained three models to predict the density from income alone: **spline regression (OLS)**, **k-nearest neighbours** and **gradient boosting**.
- Scored the models against the true density, which they never saw during training.
- Varied the sample size (1,000 to 1,000,000), the noise level and the share of high earners, with 10 fresh datasets per setting.

## Key findings

- **The middle is easy, the tail is hard.** With 10,000 observations, all three models predict typical incomes to within about 2–8%.
- **More data does not fix the wrong model.** Gradient boosting stays about 7 times off for incomes above €1M even with a million observations, because tree models cannot extrapolate. k-nearest neighbours keeps improving.
- **Splines are the most robust with small or noisy data.** With 1,000 observations the spline is off by about 2.6 times in the far tail, compared with about 100 times for k-nearest neighbours.

Far-tail error (incomes €1M–€10M; 1.0 = perfect), median of 10 runs:

| Model             | n = 1,000 | n = 10,000 | n = 100,000 | n = 1,000,000 |
|-------------------|----------:|-----------:|------------:|--------------:|
| Spline OLS        |      2.64 |       1.40 |        1.39 |          1.38 |
| k-NN              |    103.64 |       3.51 |        1.14 |          1.02 |
| Gradient boosting |    231.92 |       6.31 |        7.06 |          7.12 |

*Tools: Python, NumPy, pandas, scikit-learn, Jupyter.*
