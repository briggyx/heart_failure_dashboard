# heart_failure_dashboard
 
[kaggle data set](https://www.kaggle.com/datasets/aadarshvelu/heart-failure-prediction-clinical-records)

The dataset comprises the medical data of 5000 patients who experienced heart failure, gathered throughout their monitoring period. Each patient's profile encompasses 13 clinical characteristics.

There are 13 features, 6 numerical, 1 categorical, 6 boolean:

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