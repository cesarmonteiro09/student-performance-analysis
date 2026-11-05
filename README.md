# Student Academic Performance Analysis 📊

## Overview
This project analyzes student demographic data and daily habits to identify key factors impacting exam performance (`exam_score`). Using statistical techniques, hypothesis testing, and data visualization, the analysis evaluates variables such as study hours, sleep habits, social media usage, part-time employment, and gender distribution.

## Key Insights & Findings
* **Part-Time Employment (`part_time_job`):** Working part-time does not significantly reduce sleep hours, nor does it have a statistically significant impact on achieving above-average exam scores.
* **Study Hours (`study_hours_per_day`):** A strong positive association was identified between high daily study hours and academic performance.
* **Social Media Usage (`social_media_hours`):** Evaluated across binned intervals (`0-2h`, `2h-4h`, `4h-6h`, `6h+`) to analyze thresholds where screen time negatively impacts grades.
* **Gender Distribution (`gender`):** Male and female students represent the vast majority of the dataset with identical score distributions. The "Other" category represents ~4% of the sample, making it insufficient for robust statistical comparison.

## Tech Stack & Tools
* **Language:** Python 3.11
* **Data Manipulation:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Statistical Analysis:** `scipy`

## Project Structure
```text
├── data/
│   └── student_habits_performance.csv
├── notebooks/
│   └── students_performance_analysis.ipynb
├── .gitignore
├── README.md
└── requirements.txt