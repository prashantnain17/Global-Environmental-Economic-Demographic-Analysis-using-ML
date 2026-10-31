# 🌍 Global Environmental, Economic & Demographic Analysis Using Machine Learning

## 📌 Project Overview

This project analyzes relationships between environmental conditions, economic development, energy consumption, and demographic characteristics across countries using historical data from the World Bank.

The primary objective is to analyze global CO₂ emission patterns and investigate how economic, environmental, and demographic indicators can help predict CO₂ emissions using machine learning.

The project includes data cleaning, preprocessing, exploratory data analysis (EDA), statistical visualization, regression model development, and performance evaluation.

## 🎯 Project Objectives

- Analyze global CO₂ emission trends across different years.
- Identify countries with the highest CO₂ emissions.
- Investigate the relationship between GDP and CO₂ emissions.
- Examine the association between energy consumption and CO₂ emissions.
- Analyze the relationships between population, freshwater withdrawals, and CO₂ emissions.
- Explore correlations among environmental, economic, and demographic indicators.
- Develop and compare five machine learning regression models.
- Evaluate model performance using standard regression metrics.

## 📊 Dataset and Data Source

The datasets used in this project are based on the World Bank's World Development Indicators.

**Data Source:** [World Bank Open Data – World Development Indicators](https://databank.worldbank.org/source/world-development-indicators)

The project uses two CSV files containing country-level indicator information and yearly observations from 2000 to 2024.

### Selected Indicators

| Indicator | Description |
|---|---|
| CO₂ Emissions | Target variable for prediction |
| GDP | Gross Domestic Product |
| Energy Use | Energy consumption per capita |
| Population | Total population |
| Freshwater Withdrawals | Annual freshwater withdrawals |
| Birth Rate | Births per 1,000 people |
| Death Rate | Deaths per 1,000 people |

These indicators help examine relationships between emissions, economic activity, energy consumption, and population characteristics.

## 🧹 Data Cleaning and Preprocessing

The project includes the following data preparation steps:

1. Load both CSV datasets using Pandas.
2. Inspect dataset dimensions, column names, data types, and missing values.
3. Select the required environmental, economic, and demographic indicators.
4. Remove records with missing country or indicator identifiers.
5. Identify and remove duplicate country-indicator combinations.
6. Merge the datasets and resolve duplicate records according to the notebook's cleaning logic.
7. Convert yearly columns into a suitable format for analysis.
8. Combine the selected indicators into a consolidated country-year dataset.
9. Convert indicator values to numeric data types.
10. Handle missing values and prepare features for machine learning.
11. Apply feature standardization where required by the model.

## 📈 Exploratory Data Analysis (EDA)

The notebook explores the dataset through statistical analysis and visualizations, including:

- **CO₂ Emissions Over Time:** Examines changes in emissions across years.
- **Top 10 CO₂-Emitting Countries:** Identifies the highest-emitting countries in the selected year.
- **GDP vs CO₂ Emissions:** Examines the relationship between economic output and emissions.
- **Energy Use vs CO₂ Emissions:** Explores the association between energy consumption and emissions.
- **Population vs CO₂ Emissions:** Investigates the relationship between population size and emissions.
- **Freshwater Withdrawals vs CO₂ Emissions:** Examines patterns between water-resource use and emissions.
- **Correlation Heatmap:** Visualizes correlations among numerical indicators.
- **Yearly Emissions Distribution:** Uses box plots to compare emissions distributions across years.

These analyses help identify patterns and associations in global environmental data. Correlation does not necessarily imply causation.

## 🤖 Machine Learning Models

Five supervised regression models are used to predict CO₂ emissions.

### 1. Simple Linear Regression
Uses GDP as a single predictor to estimate CO₂ emissions.

### 2. Multiple Linear Regression
Uses multiple indicators, including GDP, population, freshwater withdrawals, energy use, birth rate, death rate, and year, to estimate emissions.

### 3. Decision Tree Regressor
Models relationships between input features and emissions through decision-based splits.

### 4. K-Nearest Neighbors (KNN) Regressor
Predicts emissions based on the values of nearby observations in feature space.

### 5. Support Vector Regression (SVR)
Uses support vector methods to estimate continuous numerical outcomes.

The models are compared using an 80:20 training-testing split with `random_state=42`. The notebook uses default model settings unless otherwise specified in the code.

## 📏 Model Evaluation Metrics

The models are evaluated using three standard regression metrics:

- **R² Score:** Measures predictive performance relative to a mean-based baseline.
- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values.
- **Root Mean Squared Error (RMSE):** Measures prediction error while penalizing larger errors more heavily.

The notebook compares model performance, visualizes evaluation metrics, identifies the model with the lowest test RMSE, and plots actual versus predicted CO₂ emissions.

The best model and its final scores should be taken from the results produced by executing the notebook.

## 🛠️ Technologies Used

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Development Environment:** Jupyter Notebook

## 📁 Project Structure

```text
Global Environmental, Economic & Demographic Analysis Using Machine Learning/
│
├── data/
│   ├── part-1.csv
│   └── part-2.csv
│
├── Global_Environmental_Analysis.ipynb
├── README.md
└── .gitignore
```

### File Description

- **`data/part-1.csv`** – First part of the dataset used for the analysis.
- **`data/part-2.csv`** – Second part of the dataset used for the analysis.
- **`Global_Environmental_Analysis.ipynb`** – Main notebook containing data cleaning, preprocessing, EDA, visualizations, model development, and evaluation.
- **`README.md`** – Project documentation.
- **`.gitignore`** – Specifies files and directories Git should ignore.

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Global-Environmental-Analysis.git
```

Replace `YOUR-USERNAME` with your GitHub username.

### Step 2: Open the Project Directory

```bash
cd Global-Environmental-Analysis
```

### Step 3: Install Dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

### Step 4: Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `Global_Environmental_Analysis.ipynb` and execute the cells sequentially.

**Important:** Ensure both CSV files are inside the `data/` directory and that the notebook uses these relative paths:

```python
df1 = pd.read_csv("data/part-1.csv")
df2 = pd.read_csv("data/part-2.csv")
```

## ⚠️ Limitations

- The analysis depends on the availability and quality of the selected indicators.
- Missing observations may affect the amount of data available for model training.
- The dataset may contain regional aggregates or income-group records in addition to individual countries.
- A random train-test split may place observations from the same country in both sets.
- The project estimates emissions from available indicators; it is not designed as a dedicated future-year forecasting system.
- Model performance may change with different feature selections, data preparation methods, and hyperparameters.

## 🏁 Conclusion

This project applies data analysis and machine learning techniques to a real-world environmental problem: understanding and estimating global CO₂ emissions.

By combining environmental, economic, and demographic indicators, the project explores relationships among development, resource consumption, population, and emissions.

The five regression models are evaluated using R², MAE, and RMSE to compare their predictive performance. The results demonstrate how machine learning can support environmental data analysis and help identify patterns that may inform further research into sustainable development.

## 🔗 References

- [World Bank Open Data](https://data.worldbank.org/)
- [World Development Indicators](https://databank.worldbank.org/source/world-development-indicators)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)

---

**Project Domain:** Environmental Data Analysis | Predictive Analytics | Machine Learning
