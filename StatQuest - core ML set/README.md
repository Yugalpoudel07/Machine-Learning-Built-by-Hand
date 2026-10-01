[🏠 **Main Repository**](../README.md) &nbsp;•&nbsp; [⏮️ **ISLP PDF**](../ISLP%20-%20direct%20PDF%20download/README.md) &nbsp;•&nbsp; [**Next module: scikit-learn metrics** ⏭️](../scikit-learn%20-%20Metrics%20and%20scoring/README.md)

---

# 🎥 StatQuest with Josh Starmer — Core ML Set (Weeks 9–12)

### *20 videos, in the order the weeks need them — watched **after** your derivation, not before*

[![Time](https://img.shields.io/badge/Time_budget-6_hrs-blue?style=flat-square)](#-the-study-path)
[![Videos](https://img.shields.io/badge/Videos-20_(~4_h_runtime)-red?style=flat-square&logo=youtube)](https://statquest.org/video_index.html)
[![Channel](https://img.shields.io/badge/StatQuest-Josh_Starmer-red?style=flat-square&logo=youtube)](https://www.youtube.com/@statquest)

> [!NOTE]
> **Roadmap assignment:** linear regression · bias-variance trade-off · ridge and lasso · the logistic regression series · maximum likelihood · ROC and AUC · confusion matrix. **Skip everything else this month.**
> **What you produce:** a one-line summary per video, in your own words (fill the **My one line** column below).

> [!IMPORTANT]
> **Order of work:** attempt the derivation on paper **first**, then watch. The video is a check on your understanding, not a substitute for it. If the video shows a step you couldn't do, redo that step on paper with the video closed.
>
> **Link change:** the roadmap's `statquest.org/video-index/` now **redirects** to **https://statquest.org/video_index.html**. All video links below come from that page (checked 25 Sep 2026). Runtimes are approximate.

---

## 🗺 The study path

| Part | Week | Topic | Videos | Time | Status |
| :-: | :-: | :--- | :-: | :-: | :-: |
| 1 | 9 | Linear regression + bias-variance | 5 | 1 h 30 | ☐ |
| 2 | 10 | Cross-validation + ridge and lasso | 4 | 1 h 15 | ☐ |
| 3 | 11 | Maximum likelihood, odds, logistic regression | 8 | 2 h 15 | ☐ |
| 4 | 12 | Confusion matrix, sensitivity/specificity, ROC and AUC | 3 | 1 h | ☐ |
| | | **Total** | **20** | **6 h** | |

*Time = runtime + pausing to work the numbers + writing the one-liner.*

---

### Part 1 — Week 9: linear regression and bias-variance · 1 h 30
*Do first: derive the least-squares closed form on paper (Week 9 build task 1).*

| ✓ | Video | ≈ min | My one line |
| :-: | :--- | :-: | :--- |
| ☐ | [Linear Models Part 0: Fitting a line to data, aka Least Squares, aka Linear Regression](https://youtu.be/PaFPbb66DxQ) | 9 | |
| ☐ | ⭐ [Linear Models Part 1: Linear Regression](https://youtu.be/7ArmBVF2dCs) | 27 | |
| ☐ | [Linear Models Part 1.5: Multiple Regression](https://youtu.be/zITIFTsivN8) | 5 | |
| ☐ | [R-squared explained](https://youtu.be/2AQKmw14mHM) | 11 | |
| ☐ | ⭐ [Machine Learning Fundamentals: Bias and Variance](https://youtu.be/EuBBz3bI-aA) | 7 | |

**Watch for:** R² as "fraction of variance explained", and why the p-value for R² needs the F-distribution. In *Bias and Variance*, the "squiggly line" is overfitting — sketch it next to your learning curves.

---

### Part 2 — Week 10: cross-validation, ridge and lasso · 1 h 15
*Do first: derive ridge on paper (Week 10 build task 1).*

| ✓ | Video | ≈ min | My one line |
| :-: | :--- | :-: | :--- |
| ☐ | [Machine Learning Fundamentals: Cross Validation](https://youtu.be/fSytzGwwBVw) | 6 | |
| ☐ | ⭐ [Regularization Part 1: L2, Ridge Regression](https://youtu.be/Q81RR3yKn30) | 20 | |
| ☐ | [Regularization Part 2: L1, Lasso Regression](https://youtu.be/NGf0voTMlcs) | 8 | |
| ☐ | ⭐ [Regularization Part 2.5: Ridge vs Lasso Visualized (or why Lasso can set parameters to 0 and Ridge can't)](https://youtu.be/Xm2C_gTAl8c) | 9 | |

**Watch for:** Part 2.5 is the *curve-picture* version of ISLP Figure 6.7 (the diamond vs the circle). After it, you should be able to say in one sentence why lasso reaches exactly zero and ridge doesn't.

**Skip:** *Regularization Part 3: Elastic-Net Regression* — not needed until you use it.

---

### Part 3 — Week 11: maximum likelihood and logistic regression · 2 h 15
*Do first: the full paper derivation — likelihood → log → negate → gradient (Week 11 build task 1).*

| ✓ | Video | ≈ min | My one line |
| :-: | :--- | :-: | :--- |
| ☐ | ⭐ [Maximum Likelihood](https://youtu.be/XepXtl9YKwc) | 7 | |
| ☐ | [Maximum Likelihood: A worked out example for the normal distribution](https://youtu.be/Dn6b9fCIUpM) | 18 | |
| ☐ | [Odds and Log(Odds)](https://youtu.be/ARfXDSkQf1Y) | 9 | |
| ☐ | [Odds Ratios and Log(Odds Ratios)](https://youtu.be/8nm0G-1uJzA) | 16 | |
| ☐ | ⭐ [Logistic Regression](https://youtu.be/yIYKR4sgzI8) | 9 | |
| ☐ | [Logistic Regression, Details Part 1: Coefficients](https://youtu.be/vN5cNN2-HWE) | 19 | |
| ☐ | ⭐ [Logistic Regression, Details Part 2: Maximum Likelihood](https://youtu.be/BfKanl1aSG0) | 11 | |
| ☐ | [Logistic Regression, Details Part 3: R-squared and its p-value](https://youtu.be/xxFYro8QuXA) | 15 | |

**Watch for:** the normal-distribution MLE video is the same move you make for logistic regression — take the log so a product becomes a sum, then differentiate. The *Odds Ratios* video is what you need for "reading coefficients as odds ratios".
**If short on time:** Details Part 3 is the one to drop.

---

### Part 4 — Week 12: measuring classifiers · 1 h
*Do first: implement the confusion matrix and ROC curve yourself (Week 12 build task 1).*

| ✓ | Video | ≈ min | My one line |
| :-: | :--- | :-: | :--- |
| ☐ | [Machine Learning Fundamentals: The Confusion Matrix](https://youtu.be/Kdsp6soqA7o) | 7 | |
| ☐ | [Machine Learning Fundamentals: Sensitivity and Specificity](https://youtu.be/vP06aMoz4v8) | 12 | |
| ☐ | ⭐ [ROC and AUC](https://youtu.be/4jRBRDbJemM) | 16 | |

**Watch for:** near the end of the ROC video he swaps the false-positive rate for **precision** — that's the PR curve, and the reason it wins when one class is rare (Week 12 build task 2). StatQuest has **no** video on calibration or PR-AUC, so for those use the [scikit-learn metrics guide](../scikit-learn%20-%20Metrics%20and%20scoring/README.md).

---

## ⏭ Deliberately skipped this month

| Video | Why skip | When it comes back |
| :--- | :--- | :--- |
| Regularization Part 3: Elastic-Net | Not in any Month 3 build task | Only if P2 needs it |
| Linear Models Part 2 / Part 3 (t-tests & ANOVA, design matrices) | You met Part 2 in Month 2 | Optional refresher |
| Neural Networks Part 5 (SoftMax) / Part 6 (Cross Entropy) | Same maths as Week 11, but neural-network framing | Month 5 |
| Decision trees, random forests, boosting, PCA, k-means | Next month's material | [Month 4 repo](https://github.com/Yugalpoudel07/The-Models-That-Win-Real-Problems) |

---

## 🧪 Exercise on your own data

After Part 3, take the yes/no column you used in the ISLP exercise and **reproduce the StatQuest logistic regression walkthrough with your numbers**: pick 8 rows, write down the log(odds) of each fitted value, turn them into probabilities, and compute the log-likelihood by hand on paper. Then check it against `-log_loss(y, p, normalize=False)` from scikit-learn.

---

## 🛠 What this module produces

- [ ] 20 one-line summaries (the **My one line** column above)
- [ ] A one-paragraph note after Part 3: *"Where my derivation and the video disagreed, and who was right"*
