# Modeling Car Insurance Claim Outcomes  
**Logistic Regression Feature Evaluation | DataCamp Data Science Project**

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=plastic&logo=python)](https://www.python.org/)
[![Statsmodels](https://img.shields.io/badge/Statsmodels-Statistical%20ML-lightgrey?style=plastic)](https://www.statsmodels.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-purple?style=plastic&logo=pandas)](https://pandas.pydata.org/)
[![Status](https://img.shields.io/badge/Status-Completed-success?style=plastic)](#)
[![Experience](https://img.shields.io/badge/Experience-DataCamp%20Project-blueviolet?style=plastic)](#)

---

## 📑 Table of Contents
- [Project Overview](#project-overview)
- [Business Context & Objective](#business-context--objective)
- [Dataset Overview](#dataset-overview)
- [Methodology](#methodology)
- [Evaluation & Analysis](#evaluation--analysis)
- [Results](#results)
- [Key Insights](#key-insights)
- [Tools & Technologies](#tools--technologies)
- [Repository Structure](#repository-structure)
- [How to Run the Project](#how-to-run-the-project)
- [Author](#author)
- [License / Disclaimer](#license--disclaimer)

---

## Project Overview

- Developed a simple and interpretable machine learning solution to predict whether a customer will file a car insurance claim.  
- Evaluated individual customer features using logistic regression to identify the strongest single predictor.  
- Designed a low-complexity approach suitable for insurers with limited ML infrastructure.  
- Focused on accuracy, transparency, and ease of deployment.

---

## Business Context & Objective

Car insurance is a highly competitive and data-driven industry where accurate risk assessment directly impacts pricing and profitability.

**On the Road Car Insurance** required a model that could be deployed quickly without maintaining complex machine learning pipelines.

**Objective:**  
Identify the **single customer feature** that produces the most accurate prediction of whether a policyholder will make an insurance claim, enabling a simple and production-ready model.

---

## Dataset Overview

- **Source:** DataCamp project dataset  
- **File:** `car_insurance.csv`  
- **Target Variable:** `outcome`  
  - `0` → No claim  
  - `1` → Claim made  

### Feature Categories
- **Demographics:** age, gender, marital status, children  
- **Driving Behavior:** driving experience, speeding violations, DUIs, past accidents  
- **Vehicle Information:** ownership status, vehicle year, vehicle type  
- **Financial Indicators:** income level, credit score  
- **Usage Patterns:** annual mileage  

### Data Considerations
- Missing values in continuous features were handled using mean imputation.  
- Categorical variables were encoded numerically.  
- The `id` column was excluded from modeling.

---

## Methodology

### Data Preprocessing
- Converted relevant fields to numeric types.
- Filled missing values in continuous variables using mean imputation.
- Removed non-predictive identifiers.

### Modeling Approach
- Built **one logistic regression model per feature** using `statsmodels`.
- Each model predicted insurance claim outcomes using a single independent variable.
- Logistic regression was selected due to its interpretability and industry acceptance.

### Evaluation Strategy
- Generated confusion matrices for each model.
- Calculated accuracy for performance comparison.
- Selected the feature associated with the highest accuracy score.

---

## Evaluation & Analysis

- Accuracy calculated as:
    - (True Positives + True Negatives) / Total Observations
- Each feature was evaluated independently to isolate predictive power.

### Strengths
- High interpretability
- Minimal model complexity
- Business-aligned evaluation metric

### Limitations
- Accuracy alone does not address class imbalance
- No multivariate interactions considered
- No threshold optimization applied

---

## Results

| Best Feature         | Accuracy |
|----------------------|----------|
| driving_experience   | 0.7771   |

**Driving experience** was identified as the most predictive individual feature for insurance claim outcomes.

---

## Key Insights

- Driving experience is a stronger predictor of claim risk than demographic or vehicle attributes.
- A single-feature logistic regression model can deliver solid baseline performance.
- Simple models can be effective when interpretability and fast deployment are priorities.

---

## Tools & Technologies

- **Programming Language:** Python  
- **Libraries:** pandas, numpy, statsmodels  
- **Environment:** Jupyter Notebook  

---

## Repository Structure
```
Task-4-Modeling-Car-Insurance-Claim-Outcomes/
│── data/
│ └── car_insurance.csv
│── notebooks/
│ └── notebook.ipynb
│── car.jpg
│── requirements.txt
│── README.md
```

---

## How to Run the Project
1. Clone the repository
   ```bash
    git clone https://github.com/x3loox/DataCamp-Data-Science-Projects.git
   ```

2. Navigate to the project folder
   ```bash
   cd Modeling-Car-Insurance-Claim-Outcomes
   ```

3. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

4. Run the notebook
   ```bash
   jupyter notebook
   ```


---

## Author
**AlaEldin Ali**  

_Aspiring Data Scientist | Machine Learning Enthusiast_  

🔗 [LinkedIn](https://www.linkedin.com/in/x3loox) | [GitHub](https://github.com/x3loox)

---

## License / Disclaimer
This project was completed as part of a **DataCamp Data Science program** and is intended for **educational and portfolio demonstration purposes only**.
