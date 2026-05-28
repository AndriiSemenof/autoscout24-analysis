
# German Used Car Market Analysis - AutoScout24

Analysis of the German used car market based on real AutoScout24 listings data (2011–2021).

## Project Overview

This project explores what drives used car prices in Germany. Using a dataset of 46,000+ listings, I cleaned the data, analyzed key trends, and built machine learning models to predict car prices.

## Key Questions Answered

- Which car makes are most popular on the German market?
- How do price, mileage, and horsepower relate to each other?
- What fuel types and gearboxes are most common?
- Can we predict a car's price from its features?

## Dataset

- **Source:** - provided as part of the Data Analytics course (Data Science Institute, 2026)
- **Size:** 46,405 listings
- **Period:** 2011–2021
- **Features:** make, model, fuel type, gearbox, mileage, horsepower, year, price

## Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python | Data analysis and ML |
| Pandas, NumPy | Data cleaning and processing |
| Matplotlib, Seaborn | Data visualization |
| Scikit-learn | Machine learning models |
| Tableau | Interactive dashboard |

## Project Structure

```
autoscout24-analysis/
│
├── autoscout24.ipynb          # Main analysis notebook
├── autoscout24.csv            # Raw dataset
├── autoscout24_top5.csv       # Filtered top 5 makes
├── model_results.csv          # ML model comparison results
└── README.md
```

## Analysis Steps

**1. Data Cleaning**
- Removed rows with missing values (46,405 → 46,071 rows)
- Filtered to top 5 makes for ML modeling

**2. Exploratory Data Analysis (EDA)**
- Price distribution across makes and years
- Correlation between price, horsepower, mileage, and year
- Fuel type and gearbox distribution

**3. Key Findings**
- Horsepower is the strongest price predictor (correlation: +0.75)
- Newer cars are significantly more expensive (correlation: +0.41)
- Higher mileage lowers price (correlation: -0.30)
- Petrol is the most popular fuel type
- Automatic gearbox cars cost noticeably more than manual

**4. Machine Learning Models**

Three regression models were trained and compared:

| Model | MAE (€) | R² |
|-------|---------|-----|
| Linear Regression | 2,704 | 0.80 |
| Random Forest | 1,615 | 0.91 |
| Gradient Boosting | ~1,643 | 0.91 |

Random Forest achieved the best balance of accuracy and speed.

## How to Run

```bash
# Note: the dataset is not included in this repository
# as it was provided as part of a private course.
# The notebook and analysis code are fully available.

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

# Launch Jupyter
jupyter notebook autoscout24.ipynb
```

## Author

**Andrii Semenov** — Junior Data Analyst  
[GitHub](https://github.com/AndriiSemenof) | [LinkedIn](https://www.linkedin.com/in/andrii-semenov-6453233b6)
