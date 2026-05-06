# BRSM Project: Selective Attention Game Validation

## Overview
This project focuses on a validation study for a newly developed **"Selective Attention Game"**, comparing its effectiveness against a standard **"Lab Task"** (gold standard) based on PsychoPy. Selective attention is the cognitive capacity to concentrate on task-relevant stimuli while filtering out competing distractors. 

The study utilizes a **2 × 2 Mixed Factorial Design** involving 37 participants to investigate the effects of:
- **Target Load** (Between-Subjects): Single Target vs. Multiple Targets
- **Modality** (Within-Subjects): Game (Smartphone) vs. Lab Task (Desktop)

### Research Questions
The analysis aims to answer the following core research questions:
- **RQ1 (Concurrent Validity)**: Is there a significant positive correlation between performance (Reaction Time/Accuracy) in the Game and the Lab Task?
- **RQ2 (Target Load Effect)**: Is performance significantly worse in the Multiple Target condition compared to the Single Target condition?
- **RQ3 (Modality Effect)**: Does the gamified interface significantly alter performance compared to the standard lab interface?
- **RQ4 (Level Effect)**: What is the effect of progression across different levels in the game?

---

## Notebooks and Datasets

The project's analysis is split across three Jupyter notebooks, mapping to different research questions, tests, and dataset structures.

### 1. `Notebooks/Start EDA RQ1 to RQ3.ipynb`
This notebook handles Exploratory Data Analysis (EDA), Descriptive Statistics, Normality Testing, and Non-Parametric Hypothesis Tests for the first three research questions (RQ1 to RQ3). 
* **Tests applied:** Spearman Correlation (RQ1), Mann–Whitney U Test (RQ2), Wilcoxon Signed-Rank Test (RQ3).
* **Datasets used:** 
  * `datasets/participant_rt_by_group.csv`
  * `datasets/participant_accuracy_by_group.csv`

### 2. `Notebooks/RQ4 to OLS.ipynb`
This notebook addresses RQ4 and performs more complex parametric testing, focusing on the interaction between conditions and predictive modeling.
* **Tests applied:** 2×2 Mixed Factorial ANOVA, Friedman Test (RQ4), and Ordinary Least Squares (OLS) Regression for Reaction Time and Complexity Level.
* **Dataset used:** 
  * `datasets/cleaned_all_conditions.csv`

### 3. `Notebooks/Paired Sample t tests.ipynb`
This notebook specifically analyzes the learning effect and complexity through targeted tests on specific participant groupings. 
* **Tests applied:** Paired Sample t-tests for Learning Effect (Multiple Phone vs Lab Modality) and Complexity (Single Phone vs Game Modality).
* **Dataset used:** 
  * *Data is embedded directly inside the `.ipynb` file itself.*

---

## Technical Details

- **Language:** Python
- **Libraries:** pandas, numpy, matplotlib, seaborn, scipy, statsmodels (for OLS and ANOVA)
