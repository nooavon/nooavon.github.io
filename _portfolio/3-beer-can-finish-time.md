---
title: "Predicting the Time to Finish a Can of Beer"
excerpt: "Does each can take longer to finish as the evening goes on? A small-sample prediction exercise comparing linear, regularised and robust regression with leave-one-out cross-validation. Python."
collection: portfolio
---

[View the code and report on GitHub](https://github.com/nooavon/Predicting-the-Time-to-Finish-a-Can-of-Beer-from-Cumulative-Consumption){: .btn .btn--primary}

## Question

Does it take longer to finish a can of beer as the evening goes on, and can the number of cans already consumed be used to predict how long the next one will take?

## Approach

- A small dataset of 16 cans from two people on one evening, with the finish time in minutes, the can number, can size and who bought it.
- Compared ordinary least squares, feature selection, Ridge and Lasso, and robust methods (Huber, median and Theil-Sen regression).
- Evaluated every model with **leave-one-out cross-validation**, with all tuning and feature selection done inside each training fold so that the held-out can was never used.

## Key findings

- The can number is the most useful predictor. The other recorded features did not improve out-of-sample predictions.
- Two unusually long finish times (235 and 174 minutes) have a large effect on ordinary least squares, which is why robust methods matter here.
- The recommended model, **Theil-Sen regression** on can number alone, predicts about 6.9 more minutes per additional can, with a mean absolute error of 27.7 minutes.
- The best models improve on simple baselines by roughly 16–22%.

With only 16 observations, the results are exploratory. The project is mainly an exercise in careful model evaluation with very little data.

*Tools: Python, pandas, scikit-learn, Jupyter.*
