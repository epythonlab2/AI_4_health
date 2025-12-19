# Mini Project(Health Dataset): Pima Indians Diabetes Dataset
Dataset: [Diabetes dataset CSV](https://raw.githubusercontent.com/jbrownlee/Datasets/master/pima-indians-diabetes.data.csv)

**Columns: ['Pregnancies', 'Glucose', 'BloodPressure', 'SkinThickness', 'Insulin', 'BMI', 'DiabetesPedigree', 'Age', 'Outcome']**

**Objective:** Explore the dataset using descriptive statistics and basic visualizations to understand health patterns.


# Pima Diabetes Descriptive Statistics Assignment – Student Guide

Part 1: Load and Inspect Data
- Look at the first 5 rows. What do the columns represent?
- How many rows and columns are there?
- Are there any missing values? If yes, mention wich columns?

Part 2: Summary Statistics
- For each numerical column (Pregnancies, Glucose, BloodPressure, SkinThickness, Insulin, BMI, DiabetesPedigree, Age):
    - Compute mean, median, min, max, range, standard deviation, variance.
    - Observations: 
        - Which features vary the most (largest std/variance)?
        - Any surprising min or max values?

Part 3: Distribution & Visualization
- Histograms & KDE: 
    - Observation: Is it symmetric, skewed left or right?
- Boxplots: identify potential outliers.
    - Observation: Which features have extreme values?
- Comparison by Outcome: Compare distributions of Glucose and BMI for Outcome = 0 vs 1.

    - Observation: Which group tends to have higher or lower values?

Part 4: Skewness & Kurtosis
- Skewness >0: right-skewed, <0: left-skewed.
- Kurtosis >0: heavy tails, <0: light tails.
    - Observation: Which features are close to normal? Which are skewed?

Part 5: Outliers
- Use the IQR method or boxplots.

- Observation: Which extreme values might affect the mean and standard deviation?

Part 6: Apply Data Cleaning Strategy Based on Insights
