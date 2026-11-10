# Student Academic Performance Analysis 📊

## Overview
This project is an exploratory data analysis of 1,000 students, combining demographic data and daily habits to identify which factors are most associated with exam performance (`exam_score`). The analysis uses descriptive statistics, correlation analysis, and data visualization.

## Dataset
* **Source file:** `student_habits_performance.csv`
* **Size:** 1,000 students and 16 columns
* **Age range:** 17 to 24 years old (mean of 20.5), so the findings describe **young students (17-24)** only and should not be generalized to other age groups.
* **Missing values:** only `parental_education_level` has missing values (91 rows); all other columns are complete.
* **Target variable:** `exam_score` (ranging from 18.4 to 100.0)

## Key Insights & Findings
* **Study Hours (`study_hours_per_day`):** Study hours show a very strong positive correlation with exam score (0.83 in the correlation heatmap). Students who study more than 5 hours per day average ~90.8 points, while students who study less than 2 hours per day average ~45.6 points.
* **Mental Health (`mental_health_rating`):** It has the second highest correlation with exam score (0.32), and higher ratings show higher median scores in the boxplot.
* **Social Media Usage (`social_media_hours`):** Evaluated across the intervals `0h-2h`, `2h-4h`, `4h-6h`, and `6h+` (labeled `6h-8h` in the notebook, since the maximum is 7.2h) using boxplots. Average scores decrease as usage increases, although the `6h+` group has only 4 students. Correlation with exam score is weak and negative (-0.17).
* **Part-Time Employment (`part_time_job`):** 21.5% of students have a part-time job. The share of students scoring 70 or above is similar between groups (47.9% with a job vs. 52.0% without), suggesting little difference. No formal statistical test was applied.
* **Healthy Habits:** Boxplots suggest that more frequent exercise and higher mental health ratings are associated with better scores, while diet quality shows only a small difference.
* **Gender (`gender`):** Female (48.1%) and male (47.7%) students make up most of the dataset, with very similar mean scores (about 69.7 and 69.4). The "Other" category represents ~4% of the sample, which is too small for a robust comparison.

## Limitations
* The analysis is exploratory: it identifies associations, **not causation**.
* No hypothesis tests or predictive models were applied.
* The dataset covers only ages 17 to 24.

## Tech Stack & Tools
* **Language:** Python 3.11
* **Data Manipulation:** `pandas`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Environment:** Jupyter Notebook

## Project Structure
```text
├── data/
│   └── student_habits_performance.csv
├── notebooks/
│   └── students_performance_analysis.ipynb
├── .gitignore
├── README.md
└── requirements.txt
```

## How to Run
```bash
pip install -r requirements.txt
jupyter notebook notebooks/students_performance_analysis.ipynb
```