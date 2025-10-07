# 📚 Student Performance Analysis Dataset (2024)

## Dataset Purpose

This dataset contains **1,000 anonymized records** tracking various demographic, social, and academic factors for a group of students. The primary goal of this dataset is to facilitate the analysis of **student performance** (measured by math, reading, and writing scores) and to identify potential correlations between performance and external factors such as parental education, lunch type, and test preparation.

The accompanying files, identified by their Arabic names (translated below), contain **pre-calculated pivot tables** for quick analysis of key relationships.

---

## 📂 Main Dataset: `Students_2024.xlsx - Main.csv`

The core dataset is structured with 12 columns covering student demographics, preparation, and academic results.

### Column Descriptions

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `gender` | Categorical (Object) | The student's gender (e.g., 'female', 'male'). |
| `ID` | Integer | A unique identifier for each student. |
| `race/ethnicity` | Categorical (Object) | The student's race or ethnic group (e.g., 'group A', 'group B', etc.). |
| `parental level of education` | Categorical (Object) | The highest level of education attained by the student's parents (e.g., 'bachelor\'s degree', 'some college', 'high school'). |
| `lunch` | Categorical (Object) | The type of lunch received by the student (e.g., 'standard', 'free/reduced'). |
| `test preparation course` | Categorical (Object) | Whether the student completed the test preparation course (e.g., 'completed', 'none'). |
| `math score` | Integer | The student's score in the math test (out of 100). |
| `reading score` | Integer | The student's score in the reading test (out of 100). |
| `writing score` | Integer | The student's score in the writing test (out of 100). |
| `Score Avg` | Float | The average of the three subject scores. |
| `Pass/Fail` | Categorical (Object) | A binary indicator of overall performance (e.g., 'Pass', 'Fail'). |
| `Kind of Student` | Categorical (Object) | A more granular performance rating (e.g., 'Excellent', 'Good', 'Acc', 'Failed'). |

### Example Rows

| gender | ID | race/ethnicity | parental level of education | lunch | test preparation course | math score | reading score | writing score | Score Avg | Pass/Fail | Kind of Student |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| female | 1 | group B | bachelor's degree | standard | none | 72 | 72 | 74 | 72.67 | Pass | Good |
| female | 2 | group C | some college | standard | completed | 69 | 90 | 88 | 82.33 | Pass | Good |
| male | 4 | group A | associate's degree | free/reduced | none | 47 | 57 | 44 | 49.33 | Fail | Failed |

---

## 📈 Pre-calculated Summary Tables

The following files contain **pivot table summaries** derived from the main dataset, offering immediate insights into specific factors.

| Filename (Original Arabic) | English Translation | Summary Content |
| :--- | :--- | :--- |
| `... - تأثير مستوى تعليم الوالدين على .csv` | **Effect of Parental Education Level** | Sum of Math, Reading, and Writing scores grouped by `parental level of education`. |
| `... - تأثير الاكل على حاله الطالب.csv` | **Effect of Lunch Type on Student Status** | Count of students categorized by `Pass/Fail` status versus `lunch` type (`free/reduced` vs. `standard`). |
| `... - الجموعه التى اعدت ل الاختبار.csv` | **Average Scores by Group and Test Prep** | Average `Score Avg` grouped by `race/ethnicity` and `test preparation course` completion status. |
| `... - توزيع أداء الطلاب داخل كل مجموع.csv` | **Performance Distribution within Each Group** | Count of students for each `Kind of Student` performance category, grouped by `race/ethnicity`. |

---

## 🛠️ Possible Use Cases and Analysis

This dataset is ideal for various statistical analysis and machine learning tasks:

1.  **Exploratory Data Analysis (EDA):** Visualize the distribution of scores and categorical variables.
2.  **Hypothesis Testing:** Test for significant differences in scores between groups (e.g., males vs. females, standard lunch vs. free/reduced lunch).
3.  **Predictive Modeling:** Build a model to predict:
    * **Score:** Use demographics to predict the `Score Avg` (Regression).
    * **Pass/Fail Status:** Use all factors to predict `Pass/Fail` (Classification).
4.  **Feature Importance:** Determine which factors (e.g., parental education, test prep) have the greatest impact on student success.
