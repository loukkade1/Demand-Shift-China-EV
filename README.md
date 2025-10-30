# Policy Shocks and Structural Demand Shifts in China’s Automobile Market  
### Difference-in-Differences Analysis of the 2020 Electric Vehicle Subsidy Reform

---

## Overview
This project analyzes the causal impact of **China’s April 2020 Electric Vehicle (EV) Subsidy Reform** on the demand for electric vehicles versus gasoline cars.  
Using a **Difference-in-Differences (DiD)** framework, the study evaluates how this policy—launched during the COVID-19 pandemic—reshaped consumer behavior, revealing a structural shift toward electric mobility.

---

## Research Objective
**Question:**  
How did China’s extension of the EV subsidy policy in April 2020 affect electric vehicle demand compared to gasoline vehicles?

**Hypotheses:**  
1. Extending pro-EV policies positively affected EV sales despite the pandemic’s economic impact.  
2. There is a substitution effect where EV demand rises while gasoline demand declines, indicating a structural shift.

---

## Dataset
The dataset used in this analysis originates from Kaggle:

> **China Automobile Monthly Sales Data (2018–2024)** by *Felix Zhao*  
> [https://www.kaggle.com/datasets/felixzhao/china-automobile-monthly-sales-data-2018-2024-4](https://www.kaggle.com/datasets/felixzhao/china-automobile-monthly-sales-data-2018-2024-4)

The original dataset was released under the **MIT License**.  
This project uses a cleaned and transformed version (`Analysis_china_automobile.csv`), where:
- Numeric and date columns were standardized.  
- Vehicles were categorized as *EV* or *Gasoline*.  
- Monthly aggregation was applied.  
- A binary variable `post_policy` was defined for months after April 2020.

---

## Methodology
The analysis applies a **Difference-in-Differences (DiD)** model:
$$
\[
Y_{it} = \beta_0 + \beta_1 EV_i + \beta_2 Post_t + \beta_3 (EV_i \times Post_t) + \epsilon_{it}
\]
$$
Where:
- $$\(Y_{it}\)$$: monthly units sold for vehicle type *i* at time *t*  
- \(EV_i\): 1 if electric vehicle, 0 if gasoline  
- \(Post_t\): 1 for months after April 2020  
- \(EV_i \times Post_t\): interaction term capturing the treatment effect  

The coefficient \( \beta_3 \) measures the causal impact of the policy.

---

## Key Findings
- **EV sales** increased from ~64,000 to **361,000 units/month** post-policy.  
- **Gasoline sales** declined from 1.7 million to 1.45 million units/month.  
- The estimated DiD effect is **+555,000 EV units per month**.  
- Results confirm a **policy-driven demand shift** from ICE to EVs, even under COVID-induced economic uncertainty.

---

## Citation & License
Dataset: *China Automobile Monthly Sales Data (2018–2024)* by Felix Zhao  
Released under the [MIT License](https://opensource.org/licenses/MIT).  
© 2013 Mark Otto, © 2017 Andrew Fong. Used under MIT terms.  

This repository and analysis are for educational and research purposes only.

---

## Author
**Sunicha Mahamad**  
MSc Business Analytics & Technology Management, Concordia University (Montréal)
