# Student Performance Analysis

## Project Overview

This notebook performs an exploratory data analysis (EDA) and cleaning process on a dataset containing student performance information. The goal is to understand various factors influencing student performance, identify patterns, and prepare the data for further machine learning tasks or detailed reporting.

## Dataset

The dataset `student_performance_messy_data.csv` contains various attributes related to students, including:

*   **Demographic Information:** Student_ID, Student_Name, Gender, Age, City
*   **Academic Performance:** Department, Year, Assignment_Score, Internal_Marks, Final_Score, Grade, Pass_Fail
*   **Study Habits & Lifestyle:** Study_Hours_Per_Day, Attendance_Percentage, Sleep_Hours, Screen_Time_Hours, Commute_Time_Minutes, Extracurricular_Hours, Internet_Access, Internet_Quality, Study_Method, Stress_Level, Library_Books_Issued
*   **Financial & Placement:** Scholarship, Fees_Paid, Internship, Projects_Completed, Placement_Status, Starting_Salary_LPA
*   **Dates:** Enrollment_Date, Last_Exam_Date

## Analysis Performed

This notebook covers the following key data science steps:

1.  **Data Loading & Initial Inspection**: Loading the dataset into a Pandas DataFrame and performing initial checks (e.g., `df.info()`, `df.describe()`, checking for missing values).
2.  **Data Cleaning - Missing Values Handling**: Imputing missing values in numerical columns (e.g., `Age`, `Final_Score`) with the median and categorical columns (`Gender`, `Department`) with the mode. `Starting_Salary_LPA` missing values were filled with 0.
3.  **Data Transformation**: Creation of new features, such as `Study_Efficiency` (Final_Score / Study_Hours_Per_Day), and `Scaled_Study_Hours`. Also, categorizing students into `Performance_Category` using conditional logic.
4.  **Data Selection**: Demonstrations of various methods to select specific columns and filter rows based on conditions (e.g., high-scoring students).
5.  **Grouping and Aggregation**: Summarizing data by grouping it based on categorical features like `Department` and `Gender` to calculate statistics (e.g., mean `Final_Score`).
6.  **NumPy Operations**: Applied direct NumPy functions for statistical calculations and element-wise operations on DataFrame columns.
7.  **Data Visualization**: Using Matplotlib to create:
    *   A histogram of `Final_Score` to show its distribution.
    *   A scatter plot of `Study_Hours_Per_Day` vs. `Final_Score` to explore their relationship.
    *   A bar plot of `Mean Final Score by Department` to compare performance across departments.
8.  **Merging and Combining DataFrames**: Examples of how to combine different datasets using `pd.merge()` (inner and left joins) and `pd.concat()`.

## How to Use

1.  **Open in Google Colab:** You can open this notebook directly in Google Colab.
2.  **Run Cells:** Execute each code cell sequentially to reproduce the analysis. Ensure you have the `student_performance_messy_data.csv` file in your Colab environment or adjust the path in the first cell accordingly.
3.  **Explore and Modify:** Feel free to experiment with the code, change parameters, or add new analysis steps.

## Resources

*   [Pandas Documentation](https://pandas.pydata.org/docs/)
*   [NumPy Documentation](https://numpy.org/doc/)
*   [Matplotlib Documentation](https://matplotlib.org/stable/users/index.html)
*   [Google Colaboratory](https://colab.research.google.com/)
