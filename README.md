# heart_failure_dashboard
 
[Kaggle-- Heart Failure Clinical Records](https://www.kaggle.com/datasets/aadarshvelu/heart-failure-prediction-clinical-records)

The dataset comprises the medical data of 5000 patients who experienced heart failure, gathered throughout their monitoring period. Each patient's profile encompasses 13 clinical characteristics.

There are 13 features, 6 numerical, 7 categorical (6 boolean):

| Feature               | Description                                                    |
|-----------------------|----------------------------------------------------------------|
| age                   | Age of the patient (years)                                     |
| anaemia               | Decrease of red blood cells or hemoglobin (boolean)            |
| creatinine phosphokinase (CPK) | Level of the CPK enzyme in the blood (mcg/L)           |
| diabetes              | If the patient has diabetes (boolean)                          |
| ejection fraction     | Percentage of blood leaving the heart at each contraction (percentage) |
| high blood pressure   | If the patient has hypertension (boolean)                     |
| platelets             | Platelets in the blood (kiloplatelets/mL)                      |
| sex                   | Woman or man (binary)                                          |
| serum creatinine      | Level of serum creatinine in the blood (mg/dL)                 |
| serum sodium          | Level of serum sodium in the blood (mEq/L)                     |
| smoking               | If the patient smokes or not (boolean)                         |
| time                  | Follow-up period (days)                                        |
| DEATH_EVENT           | If the patient died during the follow-up period (boolean)      |




The dataset likely contains features collected during the follow-up period after the patients experienced heart failure. These features could include various clinical measurements and health indicators taken at different points in time during the monitoring period.

There is a bit of a logic issue regarding the follow-up and whether the patient has died. e.g. if a patient dies, they're automatically given the follow-up period and metrics are recorded. However, if a patient hasn't died, the time of follow-up is a bit more arbitrary. 

-------------------

- change binary data to appropriate text labels, e.g. 0 becomes 'Alive' and 1 becomes 'Dead'
- needed to prep binary data:
    - give each column an extra column (for pivot tables & charts)
    - create a third column for the string label (for slicer)

-delete all 'label' rows with strings and one column out of each set of "binary" value columns 
-use resulting table with only numerical data to investigate correlation etc to guide graphs 

--------------------------
1. first, consider which features are numerical and categorical (and binary)
2. format numerical values accordingly with appropriate number of decimal places etc, clean up strings for categorical values
3. binary features--> create a second column where the second condition is true, create a third column for the string representation of the feature
4. create pivot table with values that become the KPIs, add slicer for each CATEGORICAL value
5. subsequent pivot tables should be copied from the first one so that the slicers are connected to them
6. use correlation, pca, etc to find patterns
7. use the found patterns to guide which graphs to include in dashboard 
