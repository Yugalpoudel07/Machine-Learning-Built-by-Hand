[🏠 **Main Repository**](../README.md) &nbsp;•&nbsp; [⏮️ **StatQuest**](../StatQuest%20-%20core%20ML%20set/README.md) &nbsp;•&nbsp; [**Next module: ML Specialization (optional)** ⏭️](../Machine%20Learning%20Specialization%20%28Andrew%20Ng%2C%20DeepLearning.AI%29/README.md)

---

# 📏 scikit-learn — Metrics and scoring (Week 12)

### *The headings to read on one very long page, plus two short pages Week 12 can't do without*

[![Time](https://img.shields.io/badge/Time_budget-4_hrs-blue?style=flat-square)](#-the-study-path)
[![Version](https://img.shields.io/badge/scikit--learn-1.9.x-F7931E?style=flat-square)](https://scikit-learn.org/stable/modules/model_evaluation.html)
[![Steps](https://img.shields.io/badge/Steps-6_parts-purple?style=flat-square)](#-the-study-path)

> [!NOTE]
> **Roadmap assignment:** the full model evaluation page, read properly, once. **Skip:** other sections of the user guide until Month 4.
> **What you produce:** the metrics implemented from scratch (Week 12, from-scratch #3), each checked against this page's definitions and the matching `sklearn.metrics` function.
>
> The page is section **3.4** of the user guide and has ~60 subsections — many are for multilabel ranking, clustering or exotic losses you won't touch this year. This file tells you **which headings** to read closely, which to skim and which to skip. Every link jumps straight to the heading.

> [!IMPORTANT]
> **Two additions to the roadmap card.** Week 12 also asks for a **reliability diagram** (calibration) and a **cost-based threshold**. Those aren't on the metrics page — they live on two short pages: *Probability calibration* (1.16) and *Tuning the decision threshold* (3.3). Parts 5–6 cover them, inside the same 4 hours. Docs are for **scikit-learn 1.9** (current stable, 1.9.1); check yours with `sklearn.__version__`.

---

## 🗺 The study path

| Part | Page / section | Time | Status |
| :-: | :--- | :-: | :-: |
| 1 | 3.4.1–3.4.3 Which metric, and the `scoring` API | 30 min | ☐ |
| 2 | ⭐ 3.4.4 Classification metrics (the core) | 1 h 45 | ☐ |
| 3 | 3.4.6 Regression metrics | 30 min | ☐ |
| 4 | 3.4.8 Dummy estimators — baselines | 15 min | ☐ |
| 5 | 1.16 Probability calibration *(bridge)* | 30 min | ☐ |
| 6 | 3.3 Tuning the decision threshold *(bridge)* | 30 min | ☐ |
| | **Total** | **4 h** | |

📄 Main page: https://scikit-learn.org/stable/modules/model_evaluation.html

---

### Part 1 — Which metric, and how sklearn scores models · 30 min

- [ ] 1. ⭐ [3.4.1 Which scoring function should I use?](https://scikit-learn.org/stable/modules/model_evaluation.html#which-scoring-function) — read slowly. The idea: first decide **what you want to predict** (a mean? a probability? a class?), *then* pick a metric that rewards exactly that. It's the "precision vs recall is a business decision" argument in its formal form. · 15 min
- [ ] 2. [3.4.2 Scoring API overview](https://scikit-learn.org/stable/modules/model_evaluation.html#scoring-api-overview) — the three places metrics appear (estimator `score`, `scoring=` in CV, `sklearn.metrics` functions). · 5 min
- [ ] 3. [3.4.3.1 String name scorers](https://scikit-learn.org/stable/modules/model_evaluation.html#scoring-string-names) — look at the table: note that losses are **negated** (`neg_log_loss`, `neg_mean_squared_error`) so that "higher is better" everywhere. · 10 min

**Skip:** [Callable scorers](https://scikit-learn.org/stable/modules/model_evaluation.html#scoring-callable) (`make_scorer`, custom scorer objects) and [Using multiple metric evaluation](https://scikit-learn.org/stable/modules/model_evaluation.html#multimetric-scoring) — useful in Month 4 tuning, not now.

---

### Part 2 — Classification metrics · 1 h 45 *(the core of Week 12)*

- [ ] 1. [3.4.4 Classification metrics](https://scikit-learn.org/stable/modules/model_evaluation.html#classification-metrics) — read the intro and scan the list of functions (binary-only vs multiclass-capable). · 5 min
- [ ] 2. [From binary to multiclass and multilabel](https://scikit-learn.org/stable/modules/model_evaluation.html#average) — `average="macro" / "micro" / "weighted"`. Know what each does to a rare class. · 10 min
- [ ] 3. [Accuracy score](https://scikit-learn.org/stable/modules/model_evaluation.html#accuracy-score) and ⭐ [Balanced accuracy score](https://scikit-learn.org/stable/modules/model_evaluation.html#balanced-accuracy-score) — balanced accuracy is the average recall per class; on a 99:1 dataset the do-nothing model drops from 0.99 to 0.50. · 10 min
- [ ] 4. ⭐ [Confusion matrix](https://scikit-learn.org/stable/modules/model_evaluation.html#confusion-matrix) — note the layout: **rows = true class, columns = predicted**, and `ravel()` gives `tn, fp, fn, tp`. Your from-scratch version must use the same layout. · 10 min
- [ ] 5. [Classification report](https://scikit-learn.org/stable/modules/model_evaluation.html#classification-report) · 5 min
- [ ] 6. ⭐ [Precision, recall and F-measures](https://scikit-learn.org/stable/modules/model_evaluation.html#precision-recall-f-measure-metrics) — the most important section. Read the part on `precision_recall_curve` and **`average_precision_score`**: AP is a step-wise sum, **not** the trapezoidal area — the page explains why trapezoidal PR-AUC is too optimistic. Then [Binary classification](https://scikit-learn.org/stable/modules/model_evaluation.html#binary-classification) (formulas) and [Multiclass and multilabel classification](https://scikit-learn.org/stable/modules/model_evaluation.html#multiclass-and-multilabel-classification) (skim). · 25 min
- [ ] 7. [Log loss](https://scikit-learn.org/stable/modules/model_evaluation.html#log-loss) — this **is** the negative log-likelihood you derived in Week 11. · 5 min
- [ ] 8. [Matthews correlation coefficient](https://scikit-learn.org/stable/modules/model_evaluation.html#matthews-corrcoef) — one number that stays honest under imbalance. · 5 min
- [ ] 9. ⭐ [Receiver operating characteristic (ROC)](https://scikit-learn.org/stable/modules/model_evaluation.html#roc-metrics) → [Binary case](https://scikit-learn.org/stable/modules/model_evaluation.html#roc-auc-binary). Skim [Multi-class case](https://scikit-learn.org/stable/modules/model_evaluation.html#roc-auc-multiclass) (one-vs-rest vs one-vs-one). · 15 min
- [ ] 10. ⭐ [Brier score loss](https://scikit-learn.org/stable/modules/model_evaluation.html#brier-score-loss) — the bridge to calibration (Part 5). · 10 min
- [ ] 11. **Implement while reading:** after each ⭐ section, write the NumPy version and assert it equals the sklearn function (`confusion_matrix`, `precision_score`, `recall_score`, `f1_score`, `roc_curve` + `auc`, `precision_recall_curve`, `average_precision_score`). · 5 min per metric, budgeted here: 5 min *(the full coding is Week 12 implementation time, not reading time)*

**Skip:** Top-k accuracy, Cohen's kappa, Hamming loss, Jaccard, Hinge loss, Multi-label confusion matrix, Multi-label ROC, Detection error tradeoff (DET), Zero one loss, Class likelihood ratios, D² score for classification. Glance at the headings so you know they exist.

---

### Part 3 — Regression metrics · 30 min

- [ ] 1. [3.4.6 Regression metrics](https://scikit-learn.org/stable/modules/model_evaluation.html#regression-metrics) — intro. · 3 min
- [ ] 2. ⭐ [R² score, the coefficient of determination](https://scikit-learn.org/stable/modules/model_evaluation.html#r2-score) — note that R² **can be negative** on test data (worse than predicting the mean). · 7 min
- [ ] 3. [Mean absolute error](https://scikit-learn.org/stable/modules/model_evaluation.html#mean-absolute-error) and [Mean squared error](https://scikit-learn.org/stable/modules/model_evaluation.html#mean-squared-error) (RMSE is `root_mean_squared_error`, in the same section). Tie them to Week 9: MSE → the mean, MAE → the median. · 7 min
- [ ] 4. [Mean absolute percentage error](https://scikit-learn.org/stable/modules/model_evaluation.html#mean-absolute-percentage-error) — read why it explodes near zero. · 3 min
- [ ] 5. [Visual evaluation of regression models](https://scikit-learn.org/stable/modules/model_evaluation.html#visualization-regression-evaluation) — `PredictionErrorDisplay` (actual vs predicted, residuals vs predicted). Use it on your Week 9 model. · 10 min

**Skip:** MSLE, median absolute error, max error, explained variance, Poisson/Gamma/Tweedie deviances, pinball loss, D² score. Also skip 3.4.5 [Multilabel ranking metrics](https://scikit-learn.org/stable/modules/model_evaluation.html#multilabel-ranking-metrics) and 3.4.7 [Clustering metrics](https://scikit-learn.org/stable/modules/model_evaluation.html#clustering-metrics) (Month 4).

---

### Part 4 — Baselines · 15 min

- [ ] 1. ⭐ [3.4.8 Dummy estimators](https://scikit-learn.org/stable/modules/model_evaluation.html#dummy-estimators) — `DummyClassifier(strategy="most_frequent")` **is** Week 12's "do-nothing model". `DummyRegressor(strategy="mean")` is the regression baseline. Roadmap rule: *every result is meaningless without one.*

---

### Part 5 — Probability calibration *(bridge)* · 30 min
📄 https://scikit-learn.org/stable/modules/calibration.html

- [ ] 1. Intro + the note on Brier score and log loss (why a lower Brier score doesn't prove better calibration). · 5 min
- [ ] 2. ⭐ [Calibration curves](https://scikit-learn.org/stable/modules/calibration.html#calibration-curve) — this *is* the reliability diagram: `CalibrationDisplay.from_estimator`. Note which models come out over- or under-confident, and why. · 10 min
- [ ] 3. [Calibrating a classifier](https://scikit-learn.org/stable/modules/calibration.html#calibrating-a-classifier) + [Usage](https://scikit-learn.org/stable/modules/calibration.html#usage) — `CalibratedClassifierCV`, fitted on data the model **didn't** train on. Then [Sigmoid](https://scikit-learn.org/stable/modules/calibration.html#sigmoid-regressor) vs [Isotonic](https://scikit-learn.org/stable/modules/calibration.html#isotonic) (isotonic needs more data). · 15 min

**Skip:** Multiclass support, Temperature Scaling. **Example to run:** [Probability Calibration curves](https://scikit-learn.org/stable/auto_examples/calibration/plot_calibration_curve.html).

---

### Part 6 — Tuning the decision threshold *(bridge)* · 30 min
📄 https://scikit-learn.org/stable/modules/classification_threshold.html

- [ ] 1. ⭐ Intro — read the tumour-detection example: 0.5 is a hard-coded default, not a decision. · 10 min
- [ ] 2. [Post-tuning the decision threshold](https://scikit-learn.org/stable/modules/classification_threshold.html#post-tuning-the-decision-threshold) + [Options to tune the decision threshold](https://scikit-learn.org/stable/modules/classification_threshold.html#options-to-tune-the-decision-threshold) — `TunedThresholdClassifierCV`. · 10 min
- [ ] 3. [Important notes regarding the internal cross-validation](https://scikit-learn.org/stable/modules/classification_threshold.html#important-notes-regarding-the-internal-cross-validation) — tuning a threshold on training data is a leak. · 5 min
- [ ] 4. Skim the example [Post-tuning the decision threshold for cost-sensitive learning](https://scikit-learn.org/stable/auto_examples/model_selection/plot_cost_sensitive_learning.html) — it's Week 12 build task 4 (cost-based threshold) done with real costs. **Read it after you've written your own version.** · 5 min

---

## 🧪 Exercise on your own data

Use the yes/no column from your own dataset (from the ISLP exercise). If it's balanced, make it imbalanced by down-sampling the positives to ~2%.

1. Fit logistic regression and a `DummyClassifier`. Report **accuracy, balanced accuracy, precision, recall, F1, ROC-AUC, average precision** for both — computed with *your* functions, checked against sklearn.
2. Plot ROC and PR curves side by side. Write two sentences on why ROC-AUC looks healthy while AP doesn't.
3. Draw a reliability diagram before and after `CalibratedClassifierCV`.
4. Invent a cost: a missed positive costs 10× a false alarm. Find the threshold that minimises total cost on a validation split and show it isn't 0.5.

---

## 🛠 What this module produces (from the roadmap)

- [ ] From-scratch `confusion_matrix`, `precision`, `recall`, `f1`, `roc_curve`, `auc`, `pr_curve` in this repo, **all tests passing against sklearn**
- [ ] The imbalance write-up (Week 12 build task 2) — a blog-post draft
- [ ] A reliability diagram, before and after calibration
- [ ] A cost-based threshold that isn't 0.5
