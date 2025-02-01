# Titanic-Data-Cleaning-and-Analysis-Project

Overview
This project demonstrates data cleaning, handling missing values, memory optimization, and exploratory data analysis (EDA) on the Titanic dataset. The goal is to provide insights into the data and prepare it for further analysis or modeling.

Dataset
The dataset used is the Titanic dataset, which includes passenger information from the Titanic shipwreck, such as whether they survived, their class, sex, age, fare, and other features.

Steps Performed
1. Data Loading
The dataset is loaded using seaborn's built-in function:
import seaborn as sns
titanic = sns.load_dataset('titanic')
2. Exploring the Dataset
Shape of Dataset: The dataset consists of 891 rows and 15 columns.
Columns: The dataset includes features such as survived, pclass, sex, age, fare, etc.
Data Types: Various data types such as int64, float64, object, bool, and category are present in the dataset.
3. Missing Value Handling
age: 19.86% of the values were missing. These were filled with the median value.
embarked and embark_town: 0.22% of values were missing. These were filled with the most frequent value (mode).
deck: 77.2% of the values were missing, so the column was dropped.
4. Data Type Conversion and Memory Optimization
To reduce memory usage and improve performance:

Integer Columns: Converted pclass, survived, sibsp, and parch to int8.
Float Columns: Converted age and fare to float32.
Categorical Columns: Converted columns like sex, embarked, who, embark_town, and alive to category data type.
5. Exploratory Data Analysis (EDA)
Descriptive Statistics: Summary statistics for both numerical and categorical columns were explored.
Correlation Analysis: A heatmap was used to show correlations between numerical features.
Survival Rate by Pclass: A count plot was generated to analyze the survival rate by passenger class.
Age and Fare Bins: Age and fare were binned into categorical groups for better visualization of survival rates.
Survival by Embarked and Pclass: A bar plot was used to explore survival rates based on the embarkation port and passenger class.
6. Visualizations
Age Distribution: A histogram and KDE plot were created to visualize the age distribution.
Fare Distribution: A histogram and KDE plot were created to visualize the fare distribution.
Survival Rate: Multiple count plots and bar plots were created to visualize the survival rate across different groups such as pclass, age_group, and fare_group.
7. Memory Usage Optimization
Optimized the memory usage by converting columns to more efficient data types, significantly reducing the dataset’s memory footprint.
8. Final Dataset
After data cleaning and optimization, the dataset is now ready for further analysis, such as building predictive models.

Technologies Used
Python
Pandas
Seaborn
Matplotlib

Conclusion
This project showcases the steps of cleaning and preparing data for further analysis, with a special focus on memory optimization. By performing these steps, we ensured that the dataset is in optimal form for subsequent modeling tasks.
