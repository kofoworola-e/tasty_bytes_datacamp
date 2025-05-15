# 🍽️ DataCamp Data Scientist Certification: Tasty Bytes Practical Exam

This repository contains my solution to the DataCamp **Data Scientist Certification Practical Exam**, built around the **Tasty Bytes** case study.

The business goal was to help the product team predict which recipes are likely to be popular, so they can promote them more confidently and drive more user engagement on their website.

## 📌 Project Brief

Tasty Bytes, a food-focused tech company, aimed to:

* **Predict which recipes will drive high web traffic.**
* **Correctly identify popular recipes at least 80% of the time.**
* **Minimize the chances of featuring unpopular recipes.**

As a data scientist, I was tasked with exploring the data, developing predictive models, evaluating their effectiveness, and recommending a solution that supports confident business decisions.

## 📁 Repository Contents

* `notebook.ipynb` – Jupyter notebook containing data validation, EDA, model building, evaluation, and conclusions. It served as the report document for the Data Science team manager,
* `presentation.pdf` – Slide deck prepared for the product team (8–10 slides).
* `data/` – Folder containing all datasets.

## 📊 Dataset Description

The dataset contains over 900 recipes, with each row representing a recipe and including several associated features:

| Column Name    | Description                                     |
| -------------- | ----------------------------------------------- |
| `recipe`       | Numeric ID of the recipe                        |
| `calories`     | Calories per serving                            |
| `carbohydrate` | Carbohydrate in grams                           |
| `sugar`        | Sugar in grams                                  |
| `protein`      | Protein in grams                                |
| `category`     | Recipe type/category (e.g., Lunch, Dessert)     |
| `servings`     | Number of servings                              |
| `high_traffic` | Whether the recipe led to high traffic ("High") |

## 🧪 Analysis Steps

### 1. 🔍 Data Validation

* Checked for missing, inconsistent, or invalid values.
* Standardized categorical values and handled duplicates.
* Confirmed consistency between data and project context.

### 2. 📊 Exploratory Data Analysis

Key insights from the data exploration:

- **Traffic is heavily skewed**: 60% of recipes drive most of the traffic.
- **Category matters**: Potato and Vegetable recipes are more likely to be high-traffic.
- **Statistical confirmation**: Chi-square tests show significant relationships between category and high_traffic.

*Visualizations and summaries are included in the notebook to support these findings.*

### 3. 🤖 Model Development and Evaluation

* **Problem Type**: Binary classification.
* **Models**: Logistic Regression (baseline) vs. Random Forest (final)
* **Evaluation Focus**: Precision, Recall, and F1-Score to align with business goals
* **Result**: Random Forest achieved 80% precision, meeting the business target



## 📌 Business Metric: Promotion Hit Rate (PHR)

We introduced a tailored metric called 

> **Promotion Hit Rate (PHR)** = Proportion of promoted recipes that were actually popular
>
> **Formula**:
>
> $$
  \text{PHR} = \frac{\text{Number of promoted recipes that became popular}}{\text{Total number of promoted recipes}} \times 100
  $$
> 
> **Estimated Starting PHR = Precision of Model = 80%**

This metric helps the business track ongoing success after model deployment.

## 💡 Recommendations

* Deploy the model to recommend recipes for homepage display.
* Use predictions to assist human decision-making rather than fully automate at first.
* Continuously monitor model performance and retrain with new data.
* Collect more data (e.g., prep time, ingredients) to improve prediction accuracy.
* Run A/B tests to optimize promotional strategies

## 📢 Presentation

A slide deck was prepared for the product manager covering:

* Project overview and objectives
* Summary of analysis and modeling
* Key metrics and results
* Clear, actionable business recommendations

--- 

## Final Note
This project showcases my ability to handle the full data science lifecycle—from cleaning and exploring data, to building models, communicating insights, and making actionable recommendations.

**Completed by Kofoworola Egbinola with ❤️**
