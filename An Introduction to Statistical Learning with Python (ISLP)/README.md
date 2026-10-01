[🏠 **Main Repository**](../README.md) &nbsp;•&nbsp; [**Next module: ISLP PDF** ⏭️](../ISLP%20-%20direct%20PDF%20download/README.md)

---

# 📘 An Introduction to Statistical Learning with Python — ISLP (Weeks 9–11)

### *The exact sections to read, the labs to run, and what to skip*

[![Time](https://img.shields.io/badge/Time_budget-20_hrs-blue?style=flat-square)](#-the-study-path)
[![Edition](https://img.shields.io/badge/ISLP-Python_edition_2023-150458?style=flat-square)](https://www.statlearning.com/)
[![Labs](https://img.shields.io/badge/Labs-Ch_2_3_4_5_6-purple?style=flat-square)](https://islp.readthedocs.io/en/latest/labs.html)
[![Cost](https://img.shields.io/badge/Cost-Free_PDF-brightgreen?style=flat-square)](../ISLP%20-%20direct%20PDF%20download/README.md)

> [!NOTE]
> **Roadmap assignment:** Chapters **2, 3, 4 and 6**, read properly, with **every lab run**. From Chapter 5 only **5.1 Cross-Validation** (Week 10 needs it). **Skip:** Chapters 9–11, and Chapter 5 beyond cross-validation.
> **What you produce:** chapter notes in your own words, and every lab run and committed.
>
> The book is ~600 pages, so this file tells you **which numbered sections** to read, in which week, and which lab headings to run. Book section numbers are the ones printed in the Python edition (the free PDF — see the [PDF module](../ISLP%20-%20direct%20PDF%20download/README.md)).

> [!IMPORTANT]
> **The rule for this month:** read ISLP to *understand*, then close it and **derive on paper** before you write any NumPy. ISLP uses `statsmodels` and `sklearn` in its labs — that's fine for the labs, but your from-scratch code in this repo must not.
> Install the lab environment once: `pip install ISLP` (current version on PyPI: **0.4.1**). The labs load data with `from ISLP import load_data`.

---

## 🗺 The study path

| Part | Week | What | Time | Status |
| :-: | :-: | :--- | :-: | :-: |
| 1 | 9 | Ch 2 — Statistical Learning (+ lab, fast) | 3 h | ☐ |
| 2 | 9 | Ch 3 — Linear Regression (+ lab) | 5 h | ☐ |
| 3 | 10 | Ch 5.1 — Cross-Validation (+ CV part of the lab) | 2 h | ☐ |
| 4 | 10 | Ch 6 — Linear Model Selection and Regularization (+ lab) | 4 h | ☐ |
| 5 | 11 | Ch 4 — Classification (+ lab) | 6 h | ☐ |
| | | **Total** | **20 h** | |

📂 **Labs online (read-only view):** https://islp.readthedocs.io/en/latest/labs.html
📂 **Labs as notebooks (to run):** https://github.com/intro-stat-learning/ISLP_labs — clone it, or download the release zip (current tag **v2.2.2**).

---

### Part 1 — Ch 2: Statistical Learning · 3 h *(Week 9)*
📄 Book: read in the PDF · 🧪 Lab: [Ch02 — Introduction to Python](https://islp.readthedocs.io/en/latest/labs/Ch02-statlearn-lab.html)

- [ ] 1. **2.1 What Is Statistical Learning?** — 2.1.1 *Why estimate f?* (prediction vs inference, **reducible vs irreducible error**), 2.1.2 *How do we estimate f?* (parametric vs non-parametric), 2.1.3 *prediction accuracy vs interpretability*, 2.1.4 *supervised vs unsupervised*, 2.1.5 *regression vs classification*. · 45 min
- [ ] 2. ⭐ **2.2.1 Measuring the Quality of Fit** — training MSE vs test MSE; why training error always falls as flexibility grows. · 30 min
- [ ] 3. ⭐ **2.2.2 The Bias-Variance Trade-Off** — the U-shaped test-error curve. **Copy Figure 2.12's three panels by hand**; this is the picture behind Week 9's learning curves. · 30 min
- [ ] 4. **2.2.3 The Classification Setting** — error rate, the Bayes classifier, KNN. · 15 min
- [ ] 5. **Lab 2.3 — run it fast.** You already know Python from Months 1–2. Run every cell but only *read carefully*: [Introduction to Numerical Python](https://islp.readthedocs.io/en/latest/labs/Ch02-statlearn-lab.html#introduction-to-numerical-python), [Graphics](https://islp.readthedocs.io/en/latest/labs/Ch02-statlearn-lab.html#graphics) (it uses `fig, ax = subplots()` — same as your Week 7 style), and [Loading Data](https://islp.readthedocs.io/en/latest/labs/Ch02-statlearn-lab.html#loading-data). · 1 h

**Skip:** re-reading Python basics you already know ([Basic Commands](https://islp.readthedocs.io/en/latest/labs/Ch02-statlearn-lab.html#basic-commands), [For Loops](https://islp.readthedocs.io/en/latest/labs/Ch02-statlearn-lab.html#for-loops)) — run the cells, don't study them. Skip the Chapter 2 exercises except **conceptual exercise 2** (classify scenarios as regression/classification, inference/prediction) — 5 minutes, good warm-up.

---

### Part 2 — Ch 3: Linear Regression · 5 h *(Week 9, from-scratch #1)*
📄 Book: read in the PDF · 🧪 Lab: [Ch03 — Linear Regression](https://islp.readthedocs.io/en/latest/labs/Ch03-linreg-lab.html)

- [ ] 1. ⭐ **3.1.1 Estimating the Coefficients** — least squares. **Stop here and derive the closed form yourself** (squared error → derivative → set to zero). Then compare with the book's equation (3.4). · 45 min
- [ ] 2. **3.1.2 Assessing the Accuracy of the Coefficient Estimates** — standard errors, CIs for β, the t-statistic. (This is Month 1–2 statistics reappearing.) · 30 min
- [ ] 3. **3.1.3 Assessing the Accuracy of the Model** — RSE and R². · 15 min
- [ ] 4. ⭐ **3.2 Multiple Linear Regression** — 3.2.1 estimating the coefficients (the matrix form is what you code), 3.2.2 *Some important questions* (F-statistic, variable selection, model fit, prediction intervals vs confidence intervals). · 45 min
- [ ] 5. **3.3.1 Qualitative Predictors** (dummy variables) and **3.3.2 Extensions** (interactions, polynomial terms). · 30 min
- [ ] 6. ⭐ **3.3.3 Potential Problems** — non-linearity, correlated errors, heteroscedasticity, outliers, high-leverage points, **collinearity**. Collinearity is exactly the "matrix with no inverse" you break on purpose in Week 9 build task 4. · 40 min
- [ ] 7. **3.5 Comparison of Linear Regression with K-Nearest Neighbors** — parametric vs non-parametric in practice. · 15 min
- [ ] 8. **Lab 3.6** — run all of it. Read closely: [Simple Linear Regression](https://islp.readthedocs.io/en/latest/labs/Ch03-linreg-lab.html#simple-linear-regression), [Using Transformations: Fit and Transform](https://islp.readthedocs.io/en/latest/labs/Ch03-linreg-lab.html#using-transformations-fit-and-transform) (the `fit`/`transform` pattern you'll meet again in pipelines), [Multiple Linear Regression](https://islp.readthedocs.io/en/latest/labs/Ch03-linreg-lab.html#multiple-linear-regression), [Interaction Terms](https://islp.readthedocs.io/en/latest/labs/Ch03-linreg-lab.html#interaction-terms), [Non-linear Transformations of the Predictors](https://islp.readthedocs.io/en/latest/labs/Ch03-linreg-lab.html#non-linear-transformations-of-the-predictors), [Qualitative Predictors](https://islp.readthedocs.io/en/latest/labs/Ch03-linreg-lab.html#qualitative-predictors). · 1 h 20

**Skim:** 3.4 *The Marketing Plan* (a recap of the chapter as Q&A — 5 minutes, good for review). **Skip:** Lab [Inspecting Objects and Namespaces](https://islp.readthedocs.io/en/latest/labs/Ch03-linreg-lab.html#inspecting-objects-and-namespaces) and [List Comprehension](https://islp.readthedocs.io/en/latest/labs/Ch03-linreg-lab.html#list-comprehension) (Python basics).

**Do after the chapter:** applied exercise **8** (simple regression of `mpg` on `horsepower`, Auto data). Fit it with **your own** closed-form NumPy code and check it against the lab's `statsmodels` numbers to 8 decimal places.

---

### Part 3 — Ch 5.1: Cross-Validation · 2 h *(Week 10)*
📄 Book: read in the PDF · 🧪 Lab: [Ch05 — Cross-Validation and the Bootstrap](https://islp.readthedocs.io/en/latest/labs/Ch05-resample-lab.html)

- [ ] 1. **5.1.1 The Validation Set Approach** — and why its estimate is noisy. · 15 min
- [ ] 2. **5.1.2 Leave-One-Out Cross-Validation** — plus the shortcut formula (5.2) for least squares. · 20 min
- [ ] 3. ⭐ **5.1.3 k-Fold Cross-Validation** — the algorithm you implement yourself in Week 10 build task 4. · 20 min
- [ ] 4. ⭐ **5.1.4 Bias-Variance Trade-Off for k-Fold CV** — why k = 5 or 10. · 15 min
- [ ] 5. **5.1.5 Cross-Validation on Classification Problems.** · 10 min
- [ ] 6. **Lab 5.3 — CV parts only:** [The Validation Set Approach](https://islp.readthedocs.io/en/latest/labs/Ch05-resample-lab.html#the-validation-set-approach) and [Cross-Validation](https://islp.readthedocs.io/en/latest/labs/Ch05-resample-lab.html#cross-validation). · 40 min

**Skip:** 5.2 *The Bootstrap* and the lab's [The Bootstrap](https://islp.readthedocs.io/en/latest/labs/Ch05-resample-lab.html#the-bootstrap) section — you built the bootstrap from scratch in Month 1.

---

### Part 4 — Ch 6: Linear Model Selection and Regularization · 4 h *(Week 10)*
📄 Book: read in the PDF · 🧪 Lab: [Ch06 — Linear Models and Regularization Methods](https://islp.readthedocs.io/en/latest/labs/Ch06-varselect-lab.html)

- [ ] 1. **6.1 Subset Selection** — read 6.1.1 (best subset) and 6.1.2 (stepwise) for the idea only; read **6.1.3 Choosing the Optimal Model** properly (Cp, AIC, BIC, adjusted R², and *validation/CV instead*). · 40 min
- [ ] 2. ⭐ **6.2.1 Ridge Regression** — why ridge is least squares plus a penalty, and **why scaling is mandatory** (the book's own warning — Week 10 build task 3). · 40 min
- [ ] 3. ⭐ **6.2.2 The Lasso** — read *"Another Formulation for Ridge Regression and the Lasso"* and *"The Variable Selection Property of the Lasso"* twice. **Figure 6.7 (the diamond vs the circle) is the geometric reason lasso hits exactly zero.** Redraw it by hand. · 45 min
- [ ] 4. **6.2.3 Selecting the Tuning Parameter** — λ by cross-validation. · 15 min
- [ ] 5. **6.4 Considerations in High Dimensions** — why p > n breaks least squares (the same singular-matrix failure as Week 9). · 20 min
- [ ] 6. **Lab 6.5 — the regularization part:** [Ridge Regression](https://islp.readthedocs.io/en/latest/labs/Ch06-varselect-lab.html#ridge-regression) (the coefficient-path plot is **exactly** your Week 10 build task 2), [Estimating Test Error of Ridge Regression](https://islp.readthedocs.io/en/latest/labs/Ch06-varselect-lab.html#estimating-test-error-of-ridge-regression), [Fast Cross-Validation for Solution Paths](https://islp.readthedocs.io/en/latest/labs/Ch06-varselect-lab.html#fast-cross-validation-for-solution-paths), [Evaluating Test Error of Cross-Validated Ridge](https://islp.readthedocs.io/en/latest/labs/Ch06-varselect-lab.html#evaluating-test-error-of-cross-validated-ridge), [The Lasso](https://islp.readthedocs.io/en/latest/labs/Ch06-varselect-lab.html#the-lasso). · 1 h 10

**Skim:** 6.3 *Dimension Reduction Methods* (PCR and PLS) — 10 minutes; PCA comes properly in Month 4 (Ch 12). **Skip:** Lab [Subset Selection Methods](https://islp.readthedocs.io/en/latest/labs/Ch06-varselect-lab.html#subset-selection-methods) and [PCR and PLS Regression](https://islp.readthedocs.io/en/latest/labs/Ch06-varselect-lab.html#pcr-and-pls-regression).

---

### Part 5 — Ch 4: Classification · 6 h *(Week 11, from-scratch #2)*
📄 Book: read in the PDF · 🧪 Lab: [Ch04 — Logistic Regression, LDA, QDA, and KNN](https://islp.readthedocs.io/en/latest/labs/Ch04-classification-lab.html)

- [ ] 1. **4.1 An Overview of Classification** and **4.2 Why Not Linear Regression?** · 20 min
- [ ] 2. ⭐ **4.3.1 The Logistic Model** — the sigmoid and the **log-odds** (eqs. 4.2–4.4). · 30 min
- [ ] 3. ⭐ **4.3.2 Estimating the Regression Coefficients** — the likelihood function (4.5). **This is your Week 11 paper derivation:** write the likelihood, take the log, negate it, differentiate. The book stops at the likelihood; *you* finish the gradient. · 45 min
- [ ] 4. **4.3.3 Making Predictions**, **4.3.4 Multiple Logistic Regression** (read the confounding example — student vs balance — it's Simpson's paradox in miniature). · 30 min
- [ ] 5. ⭐ **4.3.5 Multinomial Logistic Regression** — the **softmax** coding (Week 11 build task 6). · 20 min
- [ ] 6. **4.4 Generative Models for Classification** — 4.4.1–4.4.3 LDA/QDA for the idea; **4.4.4 Naive Bayes** connects to your Month 1 classifier. · 1 h
- [ ] 7. **4.5 A Comparison of Classification Methods** — 4.5.1 analytical, 4.5.2 empirical. · 30 min
- [ ] 8. **4.6 Generalized Linear Models** — read 4.6.1–4.6.2 (Poisson regression) for the idea that linear and logistic regression are the same family. · 30 min
- [ ] 9. **Lab 4.7:** [The Stock Market Data](https://islp.readthedocs.io/en/latest/labs/Ch04-classification-lab.html#the-stock-market-data), ⭐ [Logistic Regression](https://islp.readthedocs.io/en/latest/labs/Ch04-classification-lab.html#logistic-regression) (note how its near-50% accuracy compares with a do-nothing baseline — that's Week 12's lesson early), [Naive Bayes](https://islp.readthedocs.io/en/latest/labs/Ch04-classification-lab.html#naive-bayes), [K-Nearest Neighbors](https://islp.readthedocs.io/en/latest/labs/Ch04-classification-lab.html#k-nearest-neighbors). · 1 h 35

**Skim:** Lab [Linear Discriminant Analysis](https://islp.readthedocs.io/en/latest/labs/Ch04-classification-lab.html#linear-discriminant-analysis), [Quadratic Discriminant Analysis](https://islp.readthedocs.io/en/latest/labs/Ch04-classification-lab.html#quadratic-discriminant-analysis) and [Linear and Poisson Regression on the Bikeshare Data](https://islp.readthedocs.io/en/latest/labs/Ch04-classification-lab.html#linear-and-poisson-regression-on-the-bikeshare-data) — run the cells, don't take notes. **Skip:** 4.6.3 (GLMs in greater generality).

---

## 🧪 Exercise on your own data (the "Apply" step)

Use the cleaned dataset from your Month 2 final analysis (or any real table with a numeric column and a yes/no column).

1. **Regression:** pick a numeric target. Fit it with (a) your NumPy closed-form, (b) your NumPy gradient descent, (c) `statsmodels` as in Lab 3.6. All three coefficients must agree.
2. **Diagnostics (3.3.3):** plot residuals vs fitted values, and compute leverage for every row. Write two sentences on whether a straight line is honest for this data.
3. **Regularization (Ch 6):** standardize, then draw the ridge **and** lasso coefficient paths side by side. Which columns does lasso switch off first? Does that match your domain sense?
4. **Classification (Ch 4):** pick a yes/no column. Fit logistic regression, read two coefficients as **odds ratios** in plain English, and compare the accuracy against "always predict the majority class".

---

## 🛠 What this module produces (from the roadmap)

- [ ] Chapter notes in your own words for Ch 2, 3, 4, 5.1, 6 — one file per chapter in this folder
- [ ] Every lab notebook run and committed (Ch02, Ch03, Ch04, Ch05 CV part, Ch06 ridge/lasso part)
- [ ] The own-data exercise above, as one notebook

**Where the videos are, if a section won't click:** the authors' free lectures are on the [statlearning.com online-courses page](https://www.statlearning.com/online-courses) (YouTube playlists + the edX *Statistical Learning with Python* course). **Don't do the course** — one primary resource per topic. Use a lecture only to unblock one section, then come back to the book.
