#  Car Price Prediction using Machine Learning

A machine learning project to predict car prices in the US market, 
built to help **Geely Auto** (a Chinese automobile company) understand 
the key factors that influence car pricing.

---

##  Business Problem

Geely Auto wants to enter the US market and needs to understand:
1. Which variables are significant in predicting car price?
2. How well do those variables describe car price?

---

##  Dataset

- **Source:** Car Price Dataset
- **Records:** 205 cars
- **Features:** 26 columns including CarName, fueltype, enginesize, 
  horsepower, mileage, carbody, drivewheel, and more
- **Target Variable:** `price`

---

##  Tools & Libraries

| Tool | Purpose |
|------|---------|
| Python | Programming language |
| Google Colab | Development environment |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib & Seaborn | Data visualization |
| Scikit-learn | Machine learning models |

---

##  Project Workflow

### 1. Data Inspection
- Loaded dataset and inspected shape, datatypes, and sample records
- Checked for null values and duplicates

### 2. Data Cleaning
- Extracted company name from CarName column
- Fixed typos in company names (e.g. "vokswagen" → "volkswagen")
- Categorized companies into budget, mid-range, and premium segments

### 3. Exploratory Data Analysis (EDA)
- Visualized price distribution
- Analyzed correlation between features and price
- Plotted heatmaps, boxplots, and scatter plots

### 4. Feature Engineering
- Label encoding for categorical variables
- One-hot encoding for multi-category columns
- MinMax scaling for numerical features
- Created `company_cat` feature (brand reputation category)

### 5. Model Building
Three regression models were built and compared:
- Linear Regression
- Ridge Regression
- Lasso Regression

### 6. Model Evaluation

| Model | R² Score | RMSE |
|-------|----------|------|
| **Lasso Regression** | **0.8920** | **2890.95** |
| Ridge Regression | 0.8905 | 2911.22 |
| Linear Regression | 0.8848 | 2985.91 |

 **Lasso Regression** performed best with R² of **0.89**

---

##  Key Findings

### Most Significant Variables:
1. **Company Category (Brand Reputation)** — biggest driver of price
2. **Engine Size** — larger engines = higher price
3. **Mileage (fuel efficiency)** — higher mileage = lower price segment
4. **Aspiration & Drivewheel** — moderate positive influence

### Variables eliminated by Lasso (insignificant):
- fueltype, symboling, body_hatchback, fsystem_mpfi

---

##  Recommendations for Geely Auto

- Focus on **engine size** as a key design parameter
- Invest in **brand reputation** — highest impact on pricing
- Target **mid-to-premium segment** for competitive positioning
- Balance **fuel efficiency** carefully — highly efficient cars 
  are perceived as budget vehicles in the US market

---

##  How to Run

1. Open `Regression_project.ipynb` in Google Colab
2. Upload `car_price_dataset.csv` to your Google Drive
3. Update the dataset path in the notebook
4. Run all cells sequentially

---

##  Files

| File | Description |
|------|-------------|
| `Regression_project.ipynb` | Main notebook with complete analysis |
| `car_price_dataset.csv` | Dataset used for training |

---

## 👤 Author

**Pankaj**  
[GitHub](https://github.com/pankajiam)
