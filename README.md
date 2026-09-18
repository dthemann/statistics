# Statistics Deep Dive

A hands-on statistics course in **13 Jupyter notebooks** (plus a start-here notebook and 13 solution notebooks).
Every concept is explained in detail in the markdown cells, made visible with simulations and plots
(about 120 figures in the lessons, 60 more in the solutions), and applied in **65 real-world use-case exercises**
with fully worked, interpreted solutions.

## Quick start

```bash
pip install -r requirements.txt
jupyter lab            # then open 00_start_here.ipynb
```

* Python ≥ 3.9 with numpy, pandas, scipy, matplotlib, seaborn, statsmodels, scikit-learn (`ipywidgets` is optional).
* **No internet connection needed**: data are simulated inside the notebooks (seeded, reproducible) or bundled with
  scikit-learn / statsmodels; small classic data sets are typed in directly.
* All notebooks are delivered **already executed**, so every plot is visible immediately — also in VS Code, GitHub or nbviewer.
  Use *Run ▸ Restart Kernel and Run All Cells* to reproduce them.

## Contents

| # | Notebook | Core concepts | Real-world exercises |
|---|---|---|---|
| 0 | `00_start_here` | course map, environment check, how to study | — |
| 1 | `01_descriptive_statistics` | measurement scales, centre, spread, quantiles, shape, outliers, Anscombe | salaries in a job ad · courier service levels · cold-chain sensor log · wine profiling *(real data)* |
| 2 | `02_probability_foundations` | probability rules, conditional probability, Bayes' theorem, expectation, Monte Carlo | spam filter · server reliability · fraud false alarms · warranty pricing · project-deadline risk |
| 3 | `03_probability_distributions` | binomial, Poisson, normal, exponential, log-normal, t/χ²/F, Q–Q plots, fitting | acceptance sampling · call-centre staffing · tolerances · pump failures · insurance tail risk |
| 4 | `04_sampling_lln_clt` | sampling designs & bias, sampling distributions, standard error, LLN, CLT | poll sample size · inventory audit · bottling line · latency alerts · biased survey |
| 5 | `05_estimation_confidence_intervals` | bias/variance/MSE, maximum likelihood, confidence intervals, Wilson, bootstrap | German tank problem · subscriber lifetimes (censoring) · basket value · zero defects · revenue lift |
| 6 | `06_hypothesis_testing` | p-values, type I/II errors, power, t-tests, proportions, permutation tests, effect size | filling machine · blood-pressure trial · fuel additive · checkout A/B test · physiotherapy pilot |
| 7 | `07_anova_nonparametric_chisquare` | one-/two-way ANOVA, Tukey HSD, rank tests, χ² tests, Fisher, RR/OR/NNT | fertiliser trial · channel × discount · app ratings · Benford's law · plan vs. age · migraine trial |
| 8 | `08_experimental_design_power_pitfalls` | randomisation, Simpson's paradox, power, winner's curse, multiple testing, peeking, CUPED, regression to the mean | Berkeley admissions *(real data)* · A/B test duration · 25 segments · optional stopping · CUPED · speed cameras |
| 9 | `09_correlation_simple_regression` | Pearson/Spearman, confounding, least squares, R², confidence vs. prediction bands, diagnostics | ad spend · firefighters · price per m² · gas demand · stopping distance |
| 10 | `10_multiple_regression` | partial effects, omitted-variable bias, dummies, interactions, VIF, influence, robust SEs, cross-validation, ridge/lasso | house prices · pay-gap audit · marketing mix · insurance charges · diabetes progression *(real data)* |
| 11 | `11_logistic_regression_glm` | odds & logit, odds ratios, confusion matrix, ROC/AUC, calibration, cost-based thresholds, Poisson regression | telecom churn · credit scoring · breast-cancer diagnosis *(real data)* · motor-insurance claims |
| 12 | `12_bayesian_statistics` | prior/posterior, conjugate models, credible intervals, Bayesian A/B testing, shrinkage, Metropolis MCMC | product launch · e-mail subject lines · on-call sizing · marketplace ranking · Challenger O-rings *(real data)* |
| 13 | `13_time_series` | trend/seasonality, ACF/PACF, smoothing, STL, stationarity, spurious regression, SARIMA, rolling-origin evaluation | daily orders · tourism seasonality · share prices · electricity demand · retail sales |

## How a module works

1. **Concept** in prose → formula → pitfalls (⚠️).
2. **🤔 Predict first** prompts: commit to an answer before running the next cell.
3. **Visual demonstration**: nearly every idea is simulated and plotted — change the numbers and re-run.
4. **✍️ Exercises — real-world use cases**: one for every core method; each creates its own data and has an empty cell for your work.
5. **Solutions** in `solutions/NN_*_solutions.ipynb`: executed code, plots and a written interpretation.
6. **🔑 Key takeaways + cheat sheet** of the relevant function calls.

Plan 3–5 hours per module and work through them in order.

## Conventions

* Every notebook starts with the same setup cell. `C` is the colour palette (`C[0]` blue, `C[1]` orange, …) and `rng`
  a seeded NumPy generator. Because the name `C` is taken, model formulas avoid patsy's `C(...)`; categorical
  columns are stored as text or pandas categoricals instead.
* Exercise data use their own seeded generators, so your results match the solution notebooks exactly.
* Interactive explorers (modules 3 and 4) use `ipywidgets` if installed and fall back to static plots otherwise.
