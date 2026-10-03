# Codveda Data Analytics Internship Projects

This repository contains six data analytics projects completed as part of my **Data Analytics Internship at Codveda Technologies**.

The projects progress from exploratory data analysis and visualization to regression, clustering, classification, model evaluation, and interactive business intelligence dashboard development.

Throughout the internship, I applied Python, Pandas, Matplotlib, Seaborn, scikit-learn, and Power BI to analyze data, build predictive models, and communicate actionable insights.

## Project Overview

| Level | Task | Project | Main Tools |
|---|---|---|---|
| Level 1 | Task 2 | Iris Exploratory Data Analysis | Python, Pandas, Matplotlib, Seaborn |
| Level 1 | Task 3 | Apple Stock Data Visualization | Python, Pandas, Matplotlib, Seaborn |
| Level 2 | Task 1 | House Price Regression Analysis | Python, Pandas, scikit-learn |
| Level 2 | Task 3 | Iris K-Means Clustering | Python, Pandas, scikit-learn |
| Level 3 | Task 1 | Customer Churn Classification | Python, Pandas, scikit-learn |
| Level 3 | Task 2 | Customer Churn Power BI Dashboard | Power BI, DAX, Power Query |

---
## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Power BI
- Power Query
- DAX
- Git
- GitHub


---

## Level 1 — Exploratory Data Analysis & Visualization

### Task 2: Iris Exploratory Data Analysis

**File:** [Level1_Task2_Iris_EDA.ipynb](01_level_task_projects/Level1_Task2_Iris_EDA.ipynb)

#### Objective

Perform exploratory data analysis on the Iris dataset to understand the dataset structure, distributions, differences between species, feature relationships, and correlations.

#### Techniques Used

- Data inspection and data-quality checks
- Descriptive statistics
- Species-level aggregation
- Histograms
- Boxplots
- Scatter plots
- Correlation analysis
- Correlation heatmap
- Pandas, Matplotlib, and Seaborn

#### Key Findings

- Petal measurements provide clearer separation between Iris species than sepal measurements.
- Setosa is distinctly separated from Versicolor and Virginica, particularly in petal length and petal width.
- Versicolor and Virginica show greater overlap in their measurements.
- Petal length and petal width have a strong positive relationship.
- The analysis demonstrated how exploratory visualization can reveal patterns that are not immediately visible from summary statistics alone.

---

### Task 3: Apple Stock Data Visualization

**File:** [Level1_Task3_Stock_Data_Visualization.ipynb](01_level_task_projects/Level1_Task3_Stock_Data_Visualization.ipynb)

#### Objective

Visualize Apple historical stock-price data and identify trends, yearly differences, and relationships between opening and closing prices.

#### Techniques Used

- Data filtering for Apple (`AAPL`)
- Data-quality checks
- Date conversion and time-based analysis
- Line chart
- Grouped bar chart
- Scatter plot
- Matplotlib and Seaborn
- Exporting visualizations as image files

#### Key Findings

- Apple opening and closing prices moved closely together throughout the observed period.
- The overall stock-price trend increased from 2014 to 2017 despite short-term fluctuations.
- Average opening and closing prices were very similar within each year.
- Average prices increased from 2014 to 2015, declined in 2016, and reached their highest yearly average in 2017.
- Opening and closing prices showed a strong positive relationship.

---

## Level 2 — Regression & Clustering

### Task 1: House Price Regression Analysis

**File:** [Level2_Task1_Regression_Analysis.ipynb](02_level_task_projects/Level2_Task1_Regression_Analysis.ipynb)

#### Objective

Build a simple linear regression model to examine the relationship between the average number of rooms (`RM`) and median house value (`MEDV`) and use the model to predict house values.

#### Techniques Used

- Data inspection and preprocessing
- Correlation analysis
- Feature and target selection
- Train/test split
- Simple Linear Regression
- Model prediction
- Regression-line visualization
- R² evaluation
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Scikit-learn

#### Model Results

| Metric | Result |
|---|---:|
| RM–MEDV Correlation | 0.695 |
| Coefficient | 8.639 |
| Intercept | -32.058 |
| R² | 0.564 |
| MSE | 45.602 |
| RMSE | ~6.75 |

#### Regression Equation

`MEDV = -32.058 + 8.639 × RM`

#### Key Findings

- `RM` and `MEDV` have a moderately strong positive relationship.
- The positive coefficient indicates that houses with more rooms tend to have higher predicted median values.
- The model explains approximately **56.4% of the variation** in median house value.
- Room count alone provides useful predictive information but does not explain all variation in housing prices.
- Additional variables would likely be needed for a more comprehensive prediction model.

---

### Task 3: Iris K-Means Clustering

**File:** [Level2_Task3_KMeans_Clustering.ipynb](02_level_task_projects/Level2_Task3_KMeans_Clustering.ipynb)

#### Objective

Apply unsupervised machine learning to group Iris flowers into clusters based only on their numerical measurements and compare the discovered clusters with the known species.

#### Techniques Used

- Numerical feature selection
- Feature standardization with `StandardScaler`
- K-Means clustering
- Elbow method
- Inertia / SSE comparison
- Cluster centroid analysis
- Cluster visualization
- Cluster-to-species comparison
- Scikit-learn

#### Method

The four numerical Iris features were standardized before clustering:

- Sepal Length
- Sepal Width
- Petal Length
- Petal Width

The elbow method was used to determine the appropriate number of clusters, and **K = 3** was selected.

#### Key Findings

- The elbow method indicated that three clusters were an appropriate choice.
- K-Means successfully identified three meaningful groups without using the species labels during training.
- One cluster completely separated the Setosa observations.
- Versicolor and Virginica showed some overlap because their measurements are more similar.
- Petal length and petal width provided particularly useful visual separation between the discovered clusters.
- The results demonstrate how unsupervised learning can identify natural structure in numerical data.

---

## Level 3 — Predictive Modeling & Business Intelligence

### Task 1: Customer Churn Classification

**File:** [Level3_Task1_Churn_Classification.ipynb](03_level_task_projects/Level3_Task1_Churn_Classification.ipynb)

#### Objective

Build, compare, and optimize multiple classification models to predict whether a telecommunications customer will churn.

#### Techniques Used

- Training and testing dataset inspection
- Missing-value and duplicate checks
- Categorical feature encoding
- Feature scaling
- Logistic Regression
- Decision Tree
- Random Forest
- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Hyperparameter tuning with `GridSearchCV`
- Model-performance comparison

#### Dataset

The provided data was already divided into:

- **Training set:** 2,666 customers
- **Testing set:** 667 customers

The churn target was imbalanced, with approximately **14.5% churn customers** in the training data.

#### Baseline Model Performance

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression | 85.91% | 51.06% | 25.26% | 33.80% |
| Decision Tree | 93.40% | 78.02% | 74.74% | 76.34% |
| Random Forest | 94.15% | 98.28% | 60.00% | 74.51% |

#### Tuned Model Performance

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Decision Tree (Tuned) | **94.90%** | 85.06% | **77.89%** | **81.32%** |
| Random Forest (Tuned) | 94.75% | **100.00%** | 63.16% | 77.42% |

#### Final Model

**Tuned Decision Tree**

The Tuned Decision Tree was selected because it provided the strongest overall balance between precision, recall, and F1-score for identifying churn customers.

#### Key Findings

- The churn dataset is imbalanced, making accuracy alone insufficient for model evaluation.
- Logistic Regression achieved relatively poor recall for churn customers.
- The baseline Decision Tree achieved stronger recall and F1-score than the baseline Random Forest.
- Hyperparameter tuning improved the performance of both tree-based models.
- The Tuned Random Forest achieved perfect precision but missed more actual churners.
- The Tuned Decision Tree achieved the highest F1-score and stronger recall, making it the preferred model for this task.

---

### Task 2: Customer Churn Power BI Dashboard

**File:** [Level3_Task2_Build_BI_Dashboard.pbix](03_level_task_projects/Level3_Task2_Build_BI_Dashboard.pbix)

#### Objective

Develop an interactive business intelligence dashboard to analyze customer churn, identify important behavioral and segment patterns, and communicate findings through an executive-friendly Power BI report.

#### Techniques Used

- Power Query
- Data preparation and transformation
- DAX measures
- KPI development
- Bar and column charts
- Scatter plots
- Geographic mapping
- Slicers and filters
- Page navigation
- Interactive cross-filtering
- Dashboard design and business reporting

#### Key KPIs

| KPI | Result |
|---|---:|
| Total Customers | 3,333 |
| Churned Customers | 483 |
| Churn Rate | 14.49% |
| Retention Rate | 85.51% |

#### Dashboard Pages

**1. Customer Churn Executive Overview**

Provides a high-level view of:

- Total customers
- Churned customers
- Churn rate
- Retention rate
- Churn by International Plan
- Churn by Voice Mail Plan
- Churn by Customer Service Calls

**2. Customer Behavior & Churn Drivers**

Examines:

- Average customer service calls by churn status
- Average day minutes by churn status
- Day, evening, and night usage patterns
- Relationship between day minutes and customer service calls

**3. Geographic & Segment Risk**

Analyzes:

- Churn rate by state
- Highest-churn states
- Customer population versus churn rate
- Geographic concentration of churn risk

#### Key Findings

- Customers with an **International Plan** showed a substantially higher churn rate than customers without one.
- Customers without a **Voice Mail Plan** showed a higher churn rate than customers with one.
- Churn increased significantly among customers with repeated customer-service contacts, particularly at higher call counts.
- Churned customers had higher average daytime usage than retained customers.
- Several states showed comparatively high churn rates, although state-level customer volume should also be considered when interpreting geographic risk.

#### Interactive Features

The Power BI report includes:

- State slicer
- International Plan slicer
- Voice Mail Plan slicer
- Page navigation
- Interactive filtering
- Cross-filtering between visuals
- Geographic tooltips

---

## Skills Demonstrated

Across the six projects, I applied:

- Exploratory Data Analysis
- Data Cleaning and Preparation
- Statistical Analysis
- Data Visualization
- Regression Analysis
- Unsupervised Machine Learning
- Classification Modeling
- Model Evaluation
- Hyperparameter Tuning
- Business Intelligence
- DAX
- Power Query
- Dashboard Design
- Business Insight Communication

## Repository Structure

```text
Codveda-Data-Analytics-Internship/
│
├── Level1_Task2_Iris_EDA.ipynb
├── Level1_Task3_Stock_Data_Visualization.ipynb
│
├── apple_average_open_close_by_year.png
├── apple_open_vs_close_scatterplot.png
├── apple_stock_price_trend.png
│
├── Level2_Task1_Regression_Analysis.ipynb
├── Level2_Task3_KMeans_Clustering.ipynb
│
├── Level3_Task1_Churn_Classification.ipynb
├── Level3_Task2_Build_BI_Dashboard.pbix
│
data/
├── 1) iris.csv
├── 2) Stock Prices Data Set.csv
├── 4) house Prediction Data Set.csv
└── Churn/
    ├── churn-bigml-20.csv
    └── churn-bigml-80.csv
|
├── .gitignore
└── README.md
```

## About This Repository

This repository documents my practical learning and project work in data analytics, machine learning, and business intelligence.

The projects demonstrate my experience using Python and Power BI to explore data, build analytical models, evaluate results, and communicate findings through visualizations and dashboards.
