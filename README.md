# Inside Sephora Reviews: Understanding Drivers of High-Rated Products

## Project Overview
This project analyzes **Sephora skincare product reviews and product attributes** to identify the key drivers behind **high customer ratings (4–5 stars)**. By combining customer review data with product characteristics, we apply **machine learning and exploratory data analysis** to uncover which brands, categories, and review dynamics are most strongly associated with highly rated products.

The insights from this analysis help Sephora make **data-driven merchandising, promotion, and review strategy decisions**.

---

## Business Problem
Online reviews strongly influence customer purchasing behavior. However:
- Products with **few reviews** often show inflated ratings
- High ratings may not always reflect **true product quality**
- Sephora needs to identify which product attributes consistently lead to **reliable high ratings**

This project aims to help Sephora:
- Distinguish genuinely high-performing products  
- Understand how review volume impacts rating stability  
- Identify brands and categories most associated with high ratings  

---

## Data Source
- **Sephora Products and Skincare Reviews** dataset (Kaggle)
- Over **8,000 products** and **~1 million customer reviews**
- Data includes:
  - Product attributes
  - Pricing
  - Categories (primary, secondary, tertiary)
  - Review counts
  - Customer ratings

---

## Methodology

### 1. Data Cleaning & Preprocessing
- Removed missing and empty reviews
- Aggregated reviews at the product level
- Engineered review-based features such as:
  - Average rating
  - Number of reviews
- One-hot encoded categorical variables
- Scaled numerical features

### 2. Exploratory Data Analysis (EDA)
- Analyzed rating distributions and class imbalance
- Visualized:
  - Product category distributions
  - Review volume patterns
  - New vs existing products
  - Sephora-exclusive products
- Identified trends and biases affecting model performance

### 3. Modeling
- Built and evaluated:
  - **Logistic Regression** (baseline, interpretable model)
  - **Random Forest** (non-linear, high-performance model)
- Target variable:
  - `high_rating` = 1 if average rating > 4, else 0

### 4. Model Validation & Optimization
- Applied **5-fold stratified cross-validation** to prevent data leakage
- Addressed class imbalance using:
  - Balanced class weights
  - SMOTE (tested)
- Tuned Random Forest using **RandomizedSearchCV**

---

## Key Results & Insights
- **Number of reviews** is the strongest predictor of stable high ratings
- Certain brands (e.g., Caudalie, StriVectin, Dermalogica) consistently show higher predicted probabilities of high ratings
- Skincare and hydration-focused categories are more strongly associated with positive ratings
- Products with very low review counts tend to show inflated ratings

---

## Business Recommendations
- Promote consistently high-performing brands and categories
- Encourage review generation for low-review products to improve rating reliability
- Use review volume as a trust signal alongside star ratings

---

## Tools & Technologies
- Python
- pandas, NumPy
- scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook

---

## My Contributions
- Performed **exploratory data analysis** and created **data visualizations** to identify key patterns
- Engineered review-based features used in modeling
- Interpreted model outputs and translated results into **business insights**
- Contributed to deriving **actionable recommendations** for the Sephora business problem

---

## Team Members
- Christie Shin
- Shivani Vallamdas
- Gema Zhu
- Vishal Srivastava
- Shuai Zhao

---

## Future Work
- Incorporate sentiment analysis from review text
- Apply advanced NLP models for deeper review understanding
- Explore causal relationships between marketing exposure and ratings

