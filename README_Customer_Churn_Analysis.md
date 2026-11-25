# Customer Churn Analysis: Segmentation, Insights & Recommendations

A data analysis project completed during the **Business Analysis Internship at SaiKet Systems**. The project explores customer churn in a telecommunications dataset, identifies customer groups with higher churn rates, and translates the findings into practical retention recommendations.

**Author:** Odetunde Olumide Temitope  
**Project date:** 28 October 2026  
**Role:** Business Analysis Intern, SaiKet Systems

---

## Project Overview

Customer churn occurs when customers stop using a company's products or services. Understanding which customers are more likely to leave can help a business improve retention and make better decisions.

This project analyzes the Telco Customer Churn dataset to understand the overall churn rate, explore customer behaviour, segment customers by tenure, compare churn across customer groups, and identify patterns that may inform retention strategies.

The analysis is exploratory and statistical. It does **not** include a trained or deployed machine-learning churn prediction model.

## Objectives

- Inspect and clean the telecommunications customer dataset.
- Explore customer demographics, services, contracts, tenure, and billing characteristics.
- Segment customers by tenure and compare churn across lifecycle groups.
- Identify customer categories associated with higher or lower churn.
- Apply statistical analysis to assess selected relationships.
- Develop evidence-based recommendations for improving customer retention.

## Dataset

The project uses the **Telco Customer Churn** dataset.

| Dataset characteristic | Details |
|---|---:|
| Customer records | 7,043 |
| Columns | 21 |
| Target field | `Churn` |
| Target values | Yes / No |

The dataset contains information about customer demographics, subscribed services, contract arrangements, payment methods, tenure, and charges.

> The CSV included in this repository is the dataset used for this analysis. Please retain its original attribution and usage terms when redistributing it.

## Tools and Technologies

- **Python** – analysis and data processing
- **Pandas** – data loading, cleaning, manipulation, and grouping
- **NumPy** – numerical operations
- **Matplotlib** – data visualization
- **Seaborn** – statistical visualization
- **SciPy** – statistical testing
- **Jupyter Notebook** – documented analysis workflow

## Project Workflow

1. **Data loading and inspection:** Loaded the CSV file and reviewed its dimensions, data types, and missing values.
2. **Data cleaning:** Standardized column names, handled whitespace and blank values, converted `TotalCharges` to a numeric field, checked duplicates, and encoded churn as a binary variable for analysis.
3. **Exploratory data analysis:** Examined summary statistics and distributions, and compared customers who churned with those who stayed.
4. **Customer segmentation:** Grouped customers into tenure-based lifecycle segments.
5. **Advanced analysis:** Compared churn across contract types, payment methods, service categories, and demographic groups, and conducted selected statistical tests.
6. **Recommendations:** Translated the findings into practical retention actions.

### Data Cleaning Notes

- The dataset contained 11 blank `TotalCharges` values. These belonged to customers with zero tenure and were filled with `0`.
- No duplicate records were identified.
- `TotalCharges` was converted from text to a numeric data type.
- The final cleaned dataset contained no missing values.

## Key Findings

### 1. Overall churn

- **26.5%** of customers churned (1,869 customers).
- **73.5%** stayed (5,174 customers).

### 2. Tenure and customer lifecycle

Churn was highest among newer customers and declined as tenure increased:

| Customer tenure | Churn rate |
|---|---:|
| 0–12 months | 47.4% |
| 13–36 months | 25.5% |
| More than 36 months | 11.9% |

This highlights the first year of the customer relationship as an important period for retention efforts.

### 3. Contract type

| Contract type | Churn rate |
|---|---:|
| Month-to-month | 42.7% |
| One year | 11.3% |
| Two year | 2.8% |

Month-to-month customers represented 55.0% of the customer base and 88.6% of all churners.

### 4. Payment method

Customers paying by electronic check had a churn rate of **45.3%**, compared with **15.2%–19.1%** for the other payment methods.

### 5. Service and customer characteristics

Higher churn rates were also observed among:

- Fiber optic customers: **41.9%**
- Customers without tech support: **41.6%**
- Senior citizens: **41.7%**
- Customers without a partner: **33.0%**
- Customers without dependents: **31.3%**
- Customers using paperless billing: **33.6%**

### 6. Monthly charges and gender

- Churned customers had higher monthly charges than retained customers across the tenure segments examined.
- The median monthly charge was **79.65** for churned customers and **64.43** for customers who stayed.
- Gender showed no statistically significant difference in churn in the analysis: 26.9% for female customers and 26.2% for male customers.

These results describe associations in the dataset; they do not establish that any single characteristic causes churn.

## Business Recommendations

Based on the analysis, the following actions were recommended:

1. **Strengthen first-year onboarding:** Introduce early check-ins and targeted support during the first 12 months.
2. **Encourage longer contracts:** Develop clear incentives that encourage suitable month-to-month customers to consider one-year or two-year plans.
3. **Review electronic-check payments:** Encourage customers to use automatic payment options and investigate whether payment experience contributes to churn.
4. **Investigate fiber optic experience:** Review service quality, customer feedback, and pricing for fiber optic customers.
5. **Promote technical support:** Make support options more visible and accessible, particularly to customers who do not currently subscribe to tech support.
6. **Offer relevant customer support:** Consider tailored assistance for senior customers and relevant household-focused offers.

A churn-risk scoring model was identified as a possible next step. It was not built as part of the analysis documented in this repository.

## Repository Structure

The repository can be organized as follows:

```text
customer-churn-analysis/
│
├── Customer_Churn_Analysis_Documented.ipynb
├── Customer_Churn_Analysis_Report.pdf
├── Telco_Customer_Churn_Dataset.csv
└── README.md
```

If you retain the original dataset filename, update the filename shown above to match it exactly.

## How to Explore the Project

1. Clone or download this repository.
2. Ensure Python and Jupyter Notebook are installed.
3. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scipy jupyter
   ```

4. Open `Customer_Churn_Analysis_Documented.ipynb` in Jupyter Notebook or JupyterLab.
5. Run the notebook cells in order. Ensure the dataset CSV is in the location referenced by the notebook.

The accompanying PDF report provides a written summary of the analysis, findings, and recommendations.

## Limitations

- The analysis uses a single customer dataset snapshot and does not provide a calendar-based view of churn over time.
- Tenure is used to examine customer lifecycle patterns.
- The findings identify associations, not proven causes of churn.
- No predictive model was trained or evaluated in this project.
- Further analysis would be needed to isolate the effects of overlapping customer characteristics and validate retention interventions.

## Author

**Odetunde Olumide Temitope**  
Data Analyst | Data Scientist

- **Portfolio:** https://olumideodetunde.netlify.app
- **LinkedIn:** https://www.linkedin.com/in/olumide-temitope-odetunde-209924201
- **GitHub:** https://github.com/odetundeolumide

---

*This project demonstrates an end-to-end exploratory data analysis workflow: data preparation, customer segmentation, statistical exploration, visualization, interpretation, and business recommendations.*
