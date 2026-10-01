# ✍ Machine Learning, Built by Hand

Core ML algorithms derived on paper, then coded from scratch in NumPy and tested against scikit-learn: linear, ridge and logistic regression, softmax, cross-validation and evaluation metrics (ROC, PR, calibration). Includes the class-imbalance demo and the test-set tuning "lie" measured.

[![Modules with study guides](https://img.shields.io/badge/Study_guides-5%20of%205-brightgreen?style=flat-square)](#-learning-roadmap--curriculum-status)
[![From scratch](https://img.shields.io/badge/From--scratch_algorithms-0%20of%203-blue?style=flat-square)](#-what-this-repo-will-build--week-by-week)
[![Gate 3](https://img.shields.io/badge/Gate_3-not_attempted-lightgrey?style=flat-square)](#-gate-3--closed-book-75-minutes)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)](LICENSE)
[![Focus](https://img.shields.io/badge/Focus-Derive%20%C2%B7%20Implement%20%C2%B7%20Test%20%C2%B7%20Measure-purple?style=flat-square)](#)

**Month 3 of 12 · Weeks 9–13 · 150 hours** — Theory 7.5 h · Maths 4.5 h · Implementation 7.5 h · Project 7.5 h · Assessment 3 h per week.

---

## 🎯 The Goal, in Simple Words

This month I start building models — but **not by calling `sklearn`**. For every core algorithm I do the same three steps:

1. **Work out the maths on paper** (and photograph the page).
2. **Code it myself in NumPy.**
3. **Check that my version matches the library** — to 8 decimal places.

It's slower than watching a course. It's also the only way to actually *know* this material. When an interviewer asks *"why does logistic regression use that loss function?"*, the person who derived it answers in twenty seconds.

> [!IMPORTANT]
> **Why this is the highest-value month of the plan:** most paid data-science work is exactly this — tables of data, predictions, and someone asking whether they can trust your number. Not deep learning.

---

## 🔄 The Method

```text
   A FORMULA IN A BOOK                                             A THING I CAN DEFEND
        │                                                                   ▲
        ▼                                                                   │
  ┌───────────┐     ┌────────────┐     ┌────────────┐     ┌──────────────┐  │
  │  DERIVE   │ ──► │ IMPLEMENT  │ ──► │   TEST     │ ──► │  MEASURE     │ ─┘
  │  on paper │     │ NumPy only │     │ vs sklearn │     │  honestly    │
  │           │     │            │     │ (8 d.p.)   │     │              │
  └───────────┘     └────────────┘     └────────────┘     └──────────────┘
   ISLP chapters     no sklearn in       pytest, plus       right metric,
   StatQuest (after  the model code      Month 1's          a baseline,
   the derivation)                       gradient checker   calibration, cost
```

---

## 🗺 Learning Roadmap & Curriculum Status

Every module folder has a **study guide** (`README.md`): the exact sections to read with deep links, time per step adding up to the card's budget, what to skip, an exercise on my own data, and what the module produces.

| Week | Module | Tag | Primary Source | Core Focus | Budget | Status |
| :-: | :--- | :-: | :--- | :--- | :-: | :-: |
| 9–11 | **[An Introduction to Statistical Learning with Python (ISLP)](An%20Introduction%20to%20Statistical%20Learning%20with%20Python%20%28ISLP%29/README.md)** | MUST | James, Witten, Hastie, Tibshirani, Taylor | Ch 2, 3, 4, 5.1, 6 + labs | 20 h | 📋 Study guide ready |
| — | **[ISLP — direct PDF download](ISLP%20-%20direct%20PDF%20download/README.md)** | REFERENCE | Trevor Hastie (Stanford) | A local copy of the book | n/a | 📋 Study guide ready |
| 9–12 | **[StatQuest — core ML set](StatQuest%20-%20core%20ML%20set/README.md)** | MUST | Josh Starmer | 20 videos: regression, bias-variance, ridge/lasso, MLE, logistic, ROC | 6 h | 📋 Study guide ready |
| 12 | **[scikit-learn — Metrics and scoring](scikit-learn%20-%20Metrics%20and%20scoring/README.md)** | MUST | scikit-learn 1.9 docs | Classification & regression metrics, baselines, calibration, thresholds | 4 h | 📋 Study guide ready |
| 9–11 | **[Machine Learning Specialization (Andrew Ng)](Machine%20Learning%20Specialization%20%28Andrew%20Ng%2C%20DeepLearning.AI%29/README.md)** | OPTIONAL | DeepLearning.AI / Coursera | Course 1 at 1.5×, framing only | ≤ 8 h | 📋 Study guide ready |

**Resources ≈ 38 h across five weeks. Everything else is derivation, code and building.**

> [!NOTE]
> **Link changes found on 25 Sep 2026:** StatQuest's `video-index/` now redirects to `video_index.html`; Coursera's free audit has mostly become a first-module preview. Both are handled in the study guides.

---

## 🛠 What This Repo Will Build — week by week

### Week 9 — How ML works, and linear regression from scratch · **FROM-SCRATCH #1**

*Learn:* supervised vs unsupervised · regression vs classification · **train / validation / test — the test set is touched once** · data leakage · bias vs variance · MSE, MAE, Huber.

- [ ] **Paper first:** squared error → derivative → set to zero → the closed-form solution, on a blank page. Photograph it.
- [ ] Implement it in NumPy; test against `sklearn.LinearRegression` — **agree to 8 decimal places**
- [ ] The same model by **gradient descent**; plot the loss going down; confirm it reaches the formula's answer
- [ ] **Break it on purpose:** data with a non-invertible matrix — watch it fail, write down why
- [ ] Learning curves; diagnose bias vs variance from their shape

### Week 10 — Regularization and cross-validation

*Learn:* ridge (L2) as last week's formula plus a small addition · lasso (L1) and **the geometric reason** it hits exactly zero · why scaling is mandatory · k-fold, stratified, and why tuning on the test set is a lie.

- [ ] **Ridge from scratch** — derive, implement, test
- [ ] **Regularization path plot** — ridge and lasso side by side
- [ ] Ridge on unscaled vs scaled data — show the damage scaling prevents
- [ ] **k-fold cross-validation, written myself**
- [ ] **Measure the lie:** tune on the test set and record the score; then do it properly; **write down the gap**

### Week 11 — Logistic regression from scratch · **FROM-SCRATCH #2** · *the most important week of Month 3*

*Learn:* sigmoid and its derivative · log-odds and the linear decision boundary · **cross-entropy derived from maximum likelihood** · **the gradient, by hand** (predicted − actual) · softmax · coefficients as odds ratios.

- [ ] **Paper, before any code:** likelihood → log → negate → differentiate. Photograph the page.
- [ ] Implement in NumPy with gradient descent; test against sklearn
- [ ] **Check the hand-derived gradient with Month 1's numerical gradient checker** ([`mathkit/gradcheck`](https://github.com/Yugalpoudel07/Mathematics-for-Data-Science))
- [ ] Add L2 regularization; confirm the gradient changes the way the derivation predicts
- [ ] Plot the decision boundary on 2-D data
- [ ] **Softmax regression** for more than two classes

### Week 12 — Measuring models honestly · **FROM-SCRATCH #3** · ■ GATE 3

*Learn:* confusion matrix, precision, recall, specificity, F1 · **precision vs recall is a business decision** · ROC/AUC and **PR curves for rare classes** · threshold selection · **calibration** · class imbalance · RMSE, MAE, R² · **baselines**.

- [ ] From scratch: confusion matrix, precision, recall, F1, **ROC curve, AUC, PR curve** — all tested against sklearn
- [ ] **The imbalance demonstration** (99:1): do-nothing model = 99% accuracy, 0 recall; ROC-AUC healthy while PR-AUC collapses. **Write it up — first blog-post draft.**
- [ ] Reliability diagram for an uncalibrated model → fix calibration → show the improvement
- [ ] **Cost-based threshold:** price a false positive vs a false negative; find the optimal cut-off; show it isn't 0.5

### Week 13 — BUFFER WEEK

Unallocated on purpose. **Do not pre-spend it.** Use it for one of: repeating a week that didn't stick · retaking Gate 3 · rebuilding all three algorithms **from memory, no notes** · genuine rest.

---

## 🚧 Gate 3 — closed book, 75 minutes

1. Derive the logistic regression gradient from the likelihood. **No notes.**
2. Write logistic regression with gradient descent in an empty editor — 30 minutes, no internet.
3. Explain when PR-AUC beats ROC-AUC, and why.
4. Explain the difference between a model that **ranks** well and one that is **calibrated**.
5. Name three ways data leakage gets into a pipeline.

**Pass = 4 out of 5.** Result: `__ / 5` · Date: `____`

> This month has **no public project** — P1 shipped in Month 2, P2 ships in Month 4 ([The-Models-That-Win-Real-Problems](https://github.com/Yugalpoudel07/The-Models-That-Win-Real-Problems)).

---

## ✅ End of Month 3 — I must have

- [ ] Three algorithms in this repo (linear regression, logistic/softmax regression, evaluation metrics), **each with a passing test against sklearn**
- [ ] **Three photographed paper derivations** in the lab notebook
- [ ] The regularization path plot
- [ ] The test-set-tuning inflation measured and written down
- [ ] The class-imbalance demonstration written up
- [ ] **Gate 3 passed**
- [ ] 13 lab-notebook entries

> [!WARNING]
> **The trap this month:** reaching for scikit-learn before deriving the thing. The library call is two lines; the derivation is the year. **Skip Week 11's derivation and Week 19 (backpropagation) becomes impossible.**

---

## 🔗 How This Repo Connects to the Others

```text
   MONTH 1 · Mathematics-for-Data-Science        MONTH 3 · Machine-Learning-Built-by-Hand
   Matrix algebra, inverse, rank     ─────────►  Closed-form least squares; the singular-matrix failure
   Chain rule, gradient descent      ─────────►  Gradient descent for linear & logistic regression
   Numerical gradient checker        ─────────►  Checking the hand-derived logistic gradient (Week 11)
   Maximum likelihood, Bayes         ─────────►  Cross-entropy from the likelihood; naive Bayes vs logistic

   MONTH 2 · From-Raw-Data-to-a-Real-Answer
   Confidence intervals, power       ─────────►  Honest metrics; "one number is not a result"
   Type I / II errors                ─────────►  False positives / false negatives in the confusion matrix
   Cleaned real dataset              ─────────►  The "own data" exercise in every study guide

   NEXT · MONTH 4 · The-Models-That-Win-Real-Problems  (trees, forests, boosting, PCA, pipelines, A/B tests, P2)
   NEXT · MONTH 5 · Neural-Networks-With-Nothing-Hidden  (this month's logistic gradient flows backward through every layer)
```

---

## 📂 Repository Organization

```text
Machine-Learning-Built-by-Hand/
├── An Introduction to Statistical Learning with Python (ISLP)/   # Study guide: Ch 2, 3, 4, 5.1, 6 + labs (20 h)
├── ISLP - direct PDF download/                                   # Where to get the book (reference)
├── StatQuest - core ML set/                                      # 20 videos + one-line summaries (6 h)
├── scikit-learn - Metrics and scoring/                           # Metrics page + calibration + thresholds (4 h)
├── Machine Learning Specialization (Andrew Ng, DeepLearning.AI)/ # Optional, Course 1 only (≤ 8 h)
├── LICENSE                                                       # MIT License
└── README.md                                                     # You are here
```

From-scratch code, tests and the week-by-week notebooks get added as they're built.

---

## 🚀 Navigation & Study Guide

* Start each week with the **paper derivation**, then the reading, then the code. StatQuest comes **after** the derivation.
* ISLP is the primary text: read the sections listed in its study guide, run the labs, then close the book.
* Week 12 needs three pages, not one: [metrics](scikit-learn%20-%20Metrics%20and%20scoring/README.md#part-2--classification-metrics--1-h-45-the-core-of-week-12), [calibration](scikit-learn%20-%20Metrics%20and%20scoring/README.md#part-5--probability-calibration-bridge--30-min) and [thresholds](scikit-learn%20-%20Metrics%20and%20scoring/README.md#part-6--tuning-the-decision-threshold-bridge--30-min).
* **150% rule:** if any resource takes more than 1.5× its budget, stop — the resource is wrong or a prerequisite is missing.

---

*Authored as part of the Data Science Journey. Continuously updated as new modules are completed.*
