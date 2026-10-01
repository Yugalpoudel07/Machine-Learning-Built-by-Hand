[🏠 **Main Repository**](../README.md) &nbsp;•&nbsp; [⏮️ **scikit-learn metrics**](../scikit-learn%20-%20Metrics%20and%20scoring/README.md)

---

# 🎓 Machine Learning Specialization — Andrew Ng, DeepLearning.AI (optional)

### *Course 1 only, at 1.5× speed, for framing — never as the main activity*

[![Tag](https://img.shields.io/badge/Tag-OPTIONAL-lightgrey?style=flat-square)](#)
[![Time](https://img.shields.io/badge/Time_budget-8_hrs_max-blue?style=flat-square)](#-the-study-path)
[![Course](https://img.shields.io/badge/Course_1-3_modules-purple?style=flat-square)](https://www.coursera.org/learn/machine-learning)

> [!NOTE]
> **Roadmap assignment:** Course 1 only, at 1.5× speed, for framing. **Skip:** Courses 2 and 3 entirely. **What you produce:** nothing — supplement only.
> **Warning from the roadmap:** this plan covers the same ground *with derivations*. If this course becomes your main activity, you are consuming instead of building. **Only do it in spare capacity — never at the expense of a MUST.**

> [!WARNING]
> **Access check (25 Sep 2026) — the card said "CHECK before use", and something did change.**
> - The specialization page is live, and Course 1 is still **"Supervised Machine Learning: Regression and Classification"** (~33 h listed, 3 modules): https://www.coursera.org/learn/machine-learning
> - **Free "audit" is no longer reliable on Coursera.** Since about Aug 2025 many courses offer only a free **preview of the first module**, with the rest locked behind a subscription or a 7-day trial ([OSSU report, Aug 2025](https://github.com/ossu/computer-science/issues/1352); [Class Central guide](https://www.classcentral.com/report/coursera-signup-for-free/)). The course page still says "Enroll for free" and offers financial aid.
> - **What to do:** open the **course** page (not the specialization page — audit/preview options only appear there) and see what you get. If only Module 1 is free, **do Module 1 and stop.** It covers linear regression and gradient descent, which is the part worth your framing time. Don't pay for this — it's optional.

---

## 🗺 The study path

| Part | Week | Module | Video runtime (1×) | Time | Status |
| :-: | :-: | :--- | :-: | :-: | :-: |
| 1 | 9 | Module 1 — Introduction to Machine Learning | 147 min | 1 h 45 | ☐ |
| 2 | 10 | Module 2 — Regression with multiple input variables | 66 min | 1 h 15 | ☐ |
| 3 | 11 | Module 3 — Classification | 98 min *(after skipping the interview)* | 2 h | ☐ |
| 4 | 9–11 | Optional labs, only where they test something you built | — | 2 h | ☐ |
| 5 | 12 | One-page framing note | — | 1 h | ☐ |
| | | **Total (a ceiling, not a target)** | | **8 h** | |

---

### Part 1 — Module 1: Introduction to Machine Learning · 1 h 45 *(Week 9)*

Watch at 1.5×. **After** you've done Week 9's paper derivation.

- [ ] 1. *What is machine learning?*, *Supervised learning part 1–2*, *Unsupervised learning part 1–2* — the vocabulary. · 20 min
- [ ] 2. ⭐ *Linear regression model part 1–2*, *Cost function formula*, *Cost function intuition*, *Visualizing the cost function*, *Visualization examples* — the contour-plot pictures are the best part of this course. · 40 min
- [ ] 3. ⭐ *Gradient descent*, *Implementing gradient descent*, *Gradient descent intuition*, *Learning rate*, *Gradient descent for linear regression*, *Running gradient descent* — compare with your Month 1 gradient-descent code. · 35 min
- [ ] 4. Write 3 lines: what did his framing add that ISLP didn't? · 10 min

**Skip:** *Welcome*, *Applications of machine learning*, *Jupyter Notebooks*.

---

### Part 2 — Module 2: Regression with multiple input variables · 1 h 15 *(Week 10)*

- [ ] 1. *Multiple features*, *Vectorization part 1–2*, *Gradient descent for multiple linear regression*. · 20 min
- [ ] 2. ⭐ *Feature scaling part 1–2* — then **rerun your own gradient descent on unscaled vs scaled data** and count iterations to converge. This is the gradient-descent side of Week 10 build task 3. · 35 min
- [ ] 3. *Checking gradient descent for convergence*, *Choosing the learning rate*. · 10 min
- [ ] 4. *Feature engineering*, *Polynomial regression*. · 10 min

---

### Part 3 — Module 3: Classification · 2 h *(Week 11)*

**Do the Week 11 paper derivation first.** This module hands you the gradient without deriving it from the likelihood — your derivation is the part it leaves out.

- [ ] 1. *Motivations*, *Logistic regression*, ⭐ *Decision boundary*. · 25 min
- [ ] 2. ⭐ *Cost function for logistic regression*, *Simplified Cost Function for Logistic Regression*, *Gradient Descent Implementation* — check his final gradient against the one on your paper. They must match. · 25 min
- [ ] 3. *The problem of overfitting*, *Addressing overfitting*, *Cost function with regularization*, *Regularized linear regression*, *Regularized logistic regression* — cross-check with your Week 11 L2 build task 4. · 30 min
- [ ] 4. Note where his "why" is weaker than your derivation (he motivates the log loss by its shape; you derived it from maximum likelihood). · 40 min

**Skip:** *Andrew Ng and Fei-Fei Li on Human-Centered AI* (42 min — interesting, not this month).

---

### Part 4 — Optional labs · 2 h *(only if accessible)*

Each module has ungraded Jupyter labs. Open **only** the ones that test something you've already built — gradient descent (Module 1), feature scaling (Module 2), logistic cost and gradient (Module 3) — and compare their numbers with your code. **Skip** the graded programming assignments: your from-scratch repo is the better exercise.

---

### Part 5 — One-page framing note · 1 h *(Week 12)*

- [ ] Write `framing-notes.md` in this folder: the 5 pictures or phrases from this course you'll reuse when *explaining* linear and logistic regression in an interview.

---

## 🧪 Exercise on your own data

Take your own dataset's numeric target. Run your gradient descent with learning rates `[1e-4, 1e-3, 1e-2, 1e-1, 1]` on **unscaled** and **scaled** features and plot cost vs iteration for all 10 runs on one figure (`fig, ax = plt.subplots(1, 2)`). Mark which runs diverge. That picture is Module 2 applied to your data.

---

## 🛠 What this module produces

Nothing required — it's a supplement. If you do it: `framing-notes.md` (Part 5).
