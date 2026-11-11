---
title: "Predicting the Time to Finish a Can of Beer"
excerpt: "Does each can take longer to finish as the evening goes on? A small-sample prediction exercise comparing linear, regularised and robust regression with leave-one-out cross-validation. Python."
collection: portfolio
date: 2026-10-02 12:00:00 +0000
---

**Data Science for Business I course project, Aalto University, 2026 (grade 20/20)**<br>
[View the code and report on GitHub](https://github.com/nooavon/Predicting-the-Time-to-Finish-a-Can-of-Beer-from-Cumulative-Consumption){: .btn .btn--primary}

## Question

Does it take longer to finish a can of beer as the evening goes on, and can the number of cans already consumed be used to predict how long the next one will take?

## Approach

- A small dataset of 16 cans from two people on one evening.
- Compared ordinary least squares, feature selection, Ridge and Lasso, and robust methods (Huber, median and Theil-Sen regression).
- Evaluated every model with **leave-one-out cross-validation**.

## Key findings

- The can number is the most useful predictor. The other recorded features resulted in overfitting due to how tiny the dataset was.
- Two of the cans were outliers in terms of time to finish, which resulted in models that aren't resistant to outliers such as OLS to perform poorly.
- The recommended model, **Theil-Sen regression** on can number alone, predicts about 6.9 more minutes per additional can.
- The best models improve on simple baselines by roughly 16–22%.

*Tools: Python, pandas, scikit-learn, Jupyter.*
