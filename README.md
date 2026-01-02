# **Housing Affordability Intelligence: Rent-to-Price Decision Signals**

## **Project Overview**
This project analyzes **housing affordability dynamics across California metropolitan areas** using the **Rent-to-House Price Ratio** as a decision signal rather than a raw prediction target.

Instead of optimizing for model accuracy alone, the focus is on **analytical judgment**:
- Why specific variables matter
- Where linear assumptions break
- How non-linear market forces distort affordability signals

The goal is to surface **decision-grade insights** relevant to policymakers, lenders, developers, and housing platforms.

---

## **Business Problem**
Housing affordability is often discussed using isolated metrics such as house prices or mortgage rates. These metrics fail to capture:
- Social risk (crime, unemployment)
- Supply signals (permits, schools)
- Market behavior (price cuts, market heat)

This project reframes affordability as a **system outcome**, not a single-variable problem.

---

## **Key Questions Addressed**
- **Which factors materially influence the rent-to-price ratio?**
- **Do cities naturally segment into affordability tiers?**
- **Why do linear models fail in real housing markets?**
- **When does high predictive accuracy become misleading?**

---

## **Data & Features**
- **Target Variable:** RentHousePrice_Ratio
- **Economic Factors:** Mortgage rates, unemployment
- **Social Indicators:** Crime rate, school density
- **Market Signals:** Price cuts, building permits
- ~200 city-level observations across California metros

---

## **Analytical Approach**
### **1. Exploratory Analysis**
- Identified skewed and multimodal distributions
- Confirmed non-normality across most economic indicators
- Validated rent-to-price ratio stability with narrow variance bands

### **2. Dimensionality Reduction (PCA)**
- **3 principal components explain ~72% of total variance**
- Reduced complexity while preserving system-level structure
- Demonstrated that affordability is driven by combined forces, not isolated variables

### **3. Market Segmentation (K-Means Clustering)**
- Optimal clustering at **k = 3**
- Segmented cities into:
  - **Affordability-stable markets**
  - **Risk-adjusted moderate markets**
  - **High-cost, supply-constrained markets**
- Used for **strategic classification**, not prediction

### **4. Predictive Modeling**
#### Linear Regression (Baseline)
- **R² ≈ 0.18**
- Demonstrates failure of linear assumptions in housing systems
- Useful as a diagnostic, not a decision tool

#### Random Forest Regression
- **R² ≈ 0.95**
- Captures non-linear thresholds and interactions
- Feature importance highlights:
  - **Crime rate as the dominant affordability signal**
  - Social factors outweigh pure financial variables

> High accuracy is treated cautiously and discussed as a **risk of overconfidence**, not a success metric alone.

---

## **Key Insights**
- **Affordability is driven more by social risk than mortgage rates**
- **Supply signals (permits, schools) act as early indicators**
- **Linear models systematically underrepresent real market behavior**
- **High-accuracy models require governance and interpretability to be decision-safe**

---

## **Limitations & Judgment Calls**
- Cross-sectional analysis (no panel causality)
- City-level aggregation masks micro-neighborhood effects
- Random Forest accuracy may reflect structural correlations rather than causal truth

These limitations are documented intentionally to avoid false confidence.

---

## **Why This Project Matters**
This project demonstrates:
- Analytical trade-off awareness
- Model selection discipline
- Ability to translate ML outputs into business and policy decisions

It is designed to signal **decision-making maturity**, not just technical execution.
