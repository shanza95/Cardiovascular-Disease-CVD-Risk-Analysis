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




### Phase 5: Visualize the correlation matrix using the HeatMap
### Phase 6: Logistic Regression
### Phase 7: Conclusion


