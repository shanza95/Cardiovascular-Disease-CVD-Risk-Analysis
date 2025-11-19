# Cardiovascular Disease Analysis

## Project Overview:
Cardio-Vascular Diseases are the leading cause of death globally. To identify the causes and to develop a system to predict heart attack in an effective manner is necessary. This project explores the relationship between heart-related metrics and the occurrence of heart attacks.

## Insights
- Datasets can be found [here](Dataset/)
- Python implementation for the data cleaning and EDA phases can be reviewed in the [notebook](Python.ipynb/)

### Tools & Technologies
| Category               | Tools                            |
| ---------------------- | -------------------------------- |
| Programming & Cleaning | Python (Pandas, NumPy, Datetime) |   
| Visualization          | Seaborn, Matplotlib              |
| Data Storage           | CSV files                        |
| Version Control        | GitHub                           |

## Project Phases

### Phase 1: Data Cleaning
- Find any missing/null/duplicate entries in the dataset.
  
### Phase 2: Exploring the Data
- Standardized features tags 
- Separate categorical features and numerical features for data modeling.
  
### Phase 3: Statistical Summary
- Optimize data types and features labels.

### Phase 4: EDA on Categorical & Numerical Features

<img width="562" height="433" alt="image" src="https://github.com/user-attachments/assets/9bca49c9-3a27-4c78-8e03-d9696f3e9b4d" />

The bar chart indicates that heart attacks appear more common among younger people, but this trend may be influenced by additional aspects like stress levels, lifestyle habits, or the characteristics of the sample group.

<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/4d75395f-eb8b-4959-9901-9ff783e043ac" />

In both heart attack and non–heart attack cases, males make up a larger share of the sample. This could be due to the dataset having a greater number of male entries.

<img width="686" height="547" alt="image" src="https://github.com/user-attachments/assets/d9cd728a-09a7-4746-b490-ee70f537d9f5" />

The data shows a peak in heart attack cases among individuals with low blood pressure. This is unusual because high blood pressure is typically considered a greater risk factor for heart attacks.

<img width="695" height="509" alt="image" src="https://github.com/user-attachments/assets/2f0ada03-d91f-43ea-b774-ded51a020480" />

The **“Yes”** group has four clear outliers, meaning a few patients had unusually high or low cholesterol, but most heart-attack patients still had similar cholesterol levels.
The **“No”** group shows clustered outliers, meaning some patients had high cholesterol but no heart attack, possibly due to protective factors. This group also shows more overall variation.
Overall, cholesterol alone is not a strong predictor of heart attacks and should be considered together with other risk factors.

<img width="695" height="509" alt="image" src="https://github.com/user-attachments/assets/50f4f581-40f9-42a4-a7ed-2c0213fb406c" />

The boxplot shows that people who had a heart attack often reached a higher maximum heart rate than those who didn’t — but this doesn’t mean a high heart rate causes heart attacks.
It may happen because:
- High heart rates can come from exercise or stress tests.
- Younger or fitter people naturally reach higher heart rates.
- Heart rate may be recorded during the heart attack itself, which raises it.
Low heart rate outliers:
Some people in both groups have very low maximum heart rates. While a low rate can mean good fitness, it may also indicate poor fitness or blocked arteries.

Conclusion:
Maximum heart rate alone is not a reliable indicator of heart attack risk. It’s more useful when combined with other factors like age, blood pressure, ECG results, and medical history.

<img width="573" height="433" alt="image" src="https://github.com/user-attachments/assets/d95166c3-28b7-4d0b-b85b-9b655f5b8492" />

- Fixed defect type of thalassemia is strongly associated with heart attacks.
- People with normal or reversible types seem less likely to have heart attacks.
- Having no thalassemia doesn't clearly impact risk, since both groups are similar.

Conclusion: Thalassemia type, especially fixed defect, could be a significant factor when assessing heart attack risk and should be considered in diagnosis or prediction models.

<img width="571" height="433" alt="image" src="https://github.com/user-attachments/assets/916a827b-597c-4838-bc98-9883228ebb54" />

- Downsloping ST slope is the most risky and highly associated with heart attacks in this case.
- Flat slope is more common in people without heart attacks but can still carry some risk.
- Upsloping appears safest, with most individuals not experiencing heart attack but very close to "yes" plot so still needs to be considered.

Medically, downsloping ST segments often indicate ischemia or serious heart issues, so this aligns with clinical knowledge also. 

### Phase 5: Visualize the correlation matrix using the HeatMap

<img width="924" height="842" alt="image" src="https://github.com/user-attachments/assets/87373461-2ae3-406b-99a0-22421f9ebdaa" />

| Feature                     | Correlation with Heart Attack | What it means                                                                                   |
| --------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------- |
| **max_heart_rate_achieved** | **+0.42**                     | Higher max heart rate is linked to heart attack.                                                        |
| **exercise_induced_angina** | **-0.44**                     | Angina during exercise is linked, but here shows a negative number—could be a coding or data quirk.     |
| **st_depression**           | **-0.43**                     | ST depression usually means risk, but negative here suggests complex relations.                         |
| **num_major_vessels**       | **-0.41**                     | Number of blocked vessels shows a negative link—unexpected, might need data check.                      |
| **thalassemia_type**        | **-0.53**                     | This blood disorder type shows negative correlation—might be about how data was encoded.                |
| **age**                     | **-0.22**                     | Older age usually increases risk, but here shows a slight negative link—could be specific to the data. |


### Phase 6: Logistic Regression --- ***Model Performance Summary***

**Accuracy:** 87% — The model correctly predicts heart attack status in 87% of cases.
**Precision:**
 - No Heart Attack: 84% — When the model predicts “No,” it is correct 84% of the time.
 - Yes Heart Attack: 90% — When the model predicts “Yes,” it is correct 90% of the time.
**Recall:**
  - No Heart Attack: 90% — The model correctly identifies 90% of patients without a heart attack.
  -  Yes Heart Attack: 84% — The model correctly identifies 84% of patients with a heart attack.
**F1-Score:** Balanced at 87% for both classes, reflecting a good trade-off between precision and recall.

### Phase 7: Conclusion --- ***Integrated Insights on Heart Attack Risk***

- **Strongest Indicators:** Max heart rate achieved, thalassemia type (especially fixed defects), and downsloping ST segments show the clearest associations with heart attacks, both in correlations and visual analysis.  
- **Unexpected Correlations:** Features like exercise-induced angina, ST depression, and number of major vessels show negative correlations despite being medically relevant, likely due to dataset quirks or encoding issues.  
- **Weak or Inconsistent Factors:** Age, cholesterol, and blood pressure show weak or counterintuitive correlations, indicating they are not reliable predictors on their own in this dataset.  
- **Takeaway:** Heart attack risk is multifactorial; combining ECG results, blood disorders, heart rate, and lifestyle factors provides a more accurate and clinically meaningful assessment than any single feature alone.


