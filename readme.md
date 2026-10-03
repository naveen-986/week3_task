# Statistical Analysis and Hypothesis Testing in Python

## Week 3 Assignment

A comprehensive statistical analysis project using Python to investigate the relationship between **passenger gender and survival status** in the Titanic dataset. The project demonstrates data preprocessing, exploratory data analysis, hypothesis testing, confidence intervals, visualization, and statistical interpretation.

---

## 📌 Project Overview

This project focuses on applying statistical methods to a real-world dataset and answering a research question through hypothesis testing.

### Research Question

> **Was passenger gender statistically associated with survival status in the Titanic dataset?**

The analysis uses the Titanic passenger dataset and applies multiple statistical techniques to evaluate this question.

The primary statistical methods used are:

- Chi-Square Test of Independence
- Two-Proportion Z-Test
- 95% Confidence Interval
- One-Way ANOVA
- Descriptive Statistics
- Exploratory Data Analysis (EDA)

---

## 🎯 Objectives

The main objectives of this project are:

1. Understand and inspect the Titanic dataset.
2. Identify and handle missing values.
3. Perform exploratory data analysis.
4. Calculate descriptive statistics.
5. Formulate statistical hypotheses.
6. Apply the Chi-Square Test of Independence.
7. Apply a Two-Proportion Z-Test.
8. Calculate a 95% confidence interval for the difference in survival proportions.
9. Perform an additional ANOVA analysis.
10. Visualize important statistical patterns.
11. Interpret p-values and confidence intervals.
12. Draw statistically justified conclusions.
13. Document the complete analysis in a professional report.

---

## 🧪 Hypothesis

### Null Hypothesis (H₀)

Passenger gender and survival status are independent.

In other words, there is **no statistically significant association** between gender and survival status.

### Alternative Hypothesis (H₁)

Passenger gender and survival status are not independent.

In other words, there **is a statistically significant association** between gender and survival status.

### Significance Level

```text
α = 0.05
```

### Decision Rule

- If `p-value < 0.05` → Reject H₀
- If `p-value ≥ 0.05` → Do not reject H₀

---

## 📊 Dataset

The project uses the Titanic passenger dataset.

### Dataset Information

| Property | Value |
|---|---:|
| Total Records | 891 |
| Total Variables | 15 |
| Records Analyzed | 891 |
| Target Variable | `survived` |
| Main Feature | `sex` |

### Important Variables

| Variable | Description |
|---|---|
| `survived` | Survival status: 0 = No, 1 = Yes |
| `pclass` | Passenger class: 1, 2, or 3 |
| `sex` | Passenger gender |
| `age` | Passenger age |
| `sibsp` | Number of siblings/spouses aboard |
| `parch` | Number of parents/children aboard |
| `fare` | Passenger ticket fare |
| `embarked` | Port of embarkation |

---

## 🔧 Data Preprocessing

Before statistical analysis, the dataset was cleaned and prepared.

### Preprocessing steps

- Inspected dataset dimensions and data types.
- Checked missing values.
- Filled missing `age` values using the median.
- Filled missing `embarked` values using the mode.
- Removed records missing `sex` or `survived`.
- Verified categorical and numerical variables.
- Prepared contingency tables for hypothesis testing.

The final analytical dataset contained:

```text
891 observations
```

---

## 📈 Exploratory Data Analysis

Several visualizations were created to understand the dataset.

### Visualizations

1. Passenger survival counts by gender
2. Survival rate by gender
3. Gender × Survival contingency heatmap
4. Survival counts by passenger class
5. Age distribution by survival status

These visualizations help identify patterns before performing formal statistical tests.

---

## 🧮 Statistical Analysis

### 1. Chi-Square Test of Independence

The Chi-Square Test was selected because both variables in the primary hypothesis are categorical:

```text
Gender → Categorical
Survival → Categorical
```

### Results

```text
Chi-Square Statistic = 260.7170
Degrees of Freedom   = 1
p-value              = 1.197357 × 10⁻⁵⁸
```

Since:

```text
p-value < 0.05
```

the null hypothesis is rejected.

### Interpretation

There is strong statistical evidence of an association between passenger gender and survival status in the Titanic dataset.

---

## 2. Two-Proportion Z-Test

The Two-Proportion Z-Test was used to directly compare survival proportions between female and male passengers.

### Results

```text
Z Statistic = 16.2188
p-value     = 3.711748 × 10⁻⁵⁹
```

The p-value is significantly below 0.05.

Therefore, the null hypothesis of equal survival proportions is rejected.

---

## 3. Survival Rate Comparison

The observed survival rates were:

| Gender | Survival Rate |
|---|---:|
| Female | 74.20% |
| Male | 18.89% |

The observed difference was approximately:

```text
55.31 percentage points
```

This is a descriptive difference, while the statistical tests determine whether the difference is statistically significant.

---

## 4. 95% Confidence Interval

A 95% confidence interval was