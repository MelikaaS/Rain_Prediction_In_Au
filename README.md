<p style="text-align:center">
    <a href="https://skills.network/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkillsNetworkML0101ENSkillsNetwork20718538-2022-01-01" target="_blank">
    <img src="https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/assets/logos/SN_web_lightmode.png" width="200" alt="Skills Network Logo">
    </a>
</p>

<h1 align="center"><font size="5">Final Project: Classification with Python</font></h1>




<hr>

# Introduction
Rain prediction is a critical task in meteorology, with significant implications for various sectors, including agriculture, disaster management, transportation, and 
everyday life. Accurately forecasting whether it will rain tomorrow helps farmers plan irrigation, prevents weather-related accidents, and aids in disaster preparedness 
for floods and landslides. Given the complexity of weather patterns, predicting rain is challenging and requires sophisticated models that can analyze a multitude of 
factors, such as humidity, wind patterns, and temperature.

# Instructions
In this project, the goal is to develop and evaluate machine learning models to predict the likelihood of rain tomorrow using historical weather data from Australia. By comparing the performance of different algorithms like K-Nearest Neighbors, Logistic Regression, Decision Trees, Support Vector Machines and Linear Regression, we aim to identify the most accurate model for this task. Effective rain prediction can enhance decision-making processes and improve outcomes in sectors reliant on weather conditions.

Below, is where we are going to use the classification algorithms to create a model based on our training data and evaluate our testing data using evaluation metrics learned in the course.

We will use some of the algorithms taught in the course, specifically:

1. Linear Regression
2. KNN
3. Decision Trees
4. Logistic Regression
5. SVM

We will evaluate our models using:

1.  Accuracy Score
2.  Jaccard Index
3.  F1-Score
4.  LogLoss
5.  Mean Absolute Error
6.  Mean Squared Error
7.  R2-Score

Finally, you will use your models to generate the report at the end.

# About The Dataset
The original source of the data is Australian Government's Bureau of Meteorology and the latest data can be gathered from [http://www.bom.gov.au/climate/dwo/](http://www.bom.gov.au/climate/dwo/?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkillsNetworkML0101ENSkillsNetwork20718538-2022-01-01).

The dataset to be used has extra columns like 'RainToday' and our target is 'RainTomorrow', which was gathered from the Rattle at [https://bitbucket.org/kayontoga/rattle/src/master/data/weatherAUS.RData](https://bitbucket.org/kayontoga/rattle/src/master/data/weatherAUS.RData?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkillsNetworkML0101ENSkillsNetwork20718538-2022-01-01)

This dataset contains observations of weather metrics for each day from 2008 to 2017. The **weatherAUS.csv** dataset includes the following fields:

| Field         | Description                                           | Unit            | Type   |
| ------------- | ----------------------------------------------------- | --------------- | ------ |
| Date          | Date of the Observation in YYYY-MM-DD                 | Date            | object |
| Location      | Location of the Observation                           | Location        | object |
| MinTemp       | Minimum temperature                                   | Celsius         | float  |
| MaxTemp       | Maximum temperature                                   | Celsius         | float  |
| Rainfall      | Amount of rainfall                                    | Millimeters     | float  |
| Evaporation   | Amount of evaporation                                 | Millimeters     | float  |
| Sunshine      | Amount of bright sunshine                             | hours           | float  |
| WindGustDir   | Direction of the strongest gust                       | Compass Points  | object |
| WindGustSpeed | Speed of the strongest gust                           | Kilometers/Hour | object |
| WindDir9am    | Wind direction averaged of 10 minutes prior to 9am    | Compass Points  | object |
| WindDir3pm    | Wind direction averaged of 10 minutes prior to 3pm    | Compass Points  | object |
| WindSpeed9am  | Wind speed averaged of 10 minutes prior to 9am        | Kilometers/Hour | float  |
| WindSpeed3pm  | Wind speed averaged of 10 minutes prior to 3pm        | Kilometers/Hour | float  |
| Humidity9am   | Humidity at 9am                                       | Percent         | float  |
| Humidity3pm   | Humidity at 3pm                                       | Percent         | float  |
| Pressure9am   | Atmospheric pressure reduced to mean sea level at 9am | Hectopascal     | float  |
| Pressure3pm   | Atmospheric pressure reduced to mean sea level at 3pm | Hectopascal     | float  |
| Cloud9am      | Fraction of the sky obscured by cloud at 9am          | Eights          | float  |
| Cloud3pm      | Fraction of the sky obscured by cloud at 3pm          | Eights          | float  |
| Temp9am       | Temperature at 9am                                    | Celsius         | float  |
| Temp3pm       | Temperature at 3pm                                    | Celsius         | float  |
| RainToday     | If there was rain today                               | Yes/No          | object |
| RainTomorrow  | If there is rain tomorrow                             | Yes/No          | float  |

Column definitions were gathered from [http://www.bom.gov.au/climate/dwo/IDCJDW0000.shtml](http://www.bom.gov.au/climate/dwo/IDCJDW0000.shtml?utm_medium=Exinfluencer&utm_source=Exinfluencer&utm_content=000026UJ&utm_term=10006555&utm_id=NA-SkillsNetwork-Channel-SkillsNetworkCoursesIBMDeveloperSkillsNetworkML0101ENSkillsNetwork20718538-2022-01-01)


# Conclusion


| Model               | Accuracy | Jaccard Score | F1 Score | Precision (Rain) | Recall (Rain) | Confusion Matrix (label=[1,0])             |
|---------------------|----------|---------------|----------|------------------|---------------|--------------------------------------------|
| **KNN**             | 0.80     | 0.46          | 0.63     | 0.69             | 0.58          | [[TP = 107, FN = 77], [FP = 48, TN= 423]]  |
| **Decision Tree**   | 0.78     | 0.51          | 0.68     | 0.58             | 0.83          | [[TP = 152, FN = 32], [FP = 110, TN= 361]] |
| **Logistic Regression** | 0.81     | 0.55          | 0.71     | 0.63             | 0.83          | [[TP = 152, FN = 32], [FP = 90, TN= 381]]  |
| **SVM**             | 0.81     | 0.53          | 0.69     | 0.65             | 0.75          | [[TP = 138, FN = 46], [FP = 74, TN= 397]]  |

Logistic Regression Log Loss = 0.42

### Model Performance Overview:

#### KNN (K-Nearest Neighbors):
Accuracy (0.80): 80% of the predictions were correct.

Jaccard Score (0.46): Moderate similarity between predicted and actual classes.


F1 Score (0.63): Balanced performance considering both precision and recall.


Precision (0.69): 69% of the days predicted as rainy were actually rainy.


Recall (0.58): The model correctly identified 58% of all actual rainy days.


Confusion Matrix:
TP = 107 (correctly predicted rainy days)
FN = 77 (actual rainy days missed)
FP = 48 (incorrectly predicted rainy days)
TN = 423 (correctly predicted non-rainy days)

----
#### Interpretation:
 
KNN has good precision but lower recall, indicating it is better at avoiding false alarms (wrongly predicting rain) but misses more actual rainy days.

#### Decision Tree:

Accuracy (0.78): 78% of the predictions were correct.


Jaccard Score (0.51): Better similarity between predicted and actual classes compared to KNN.


F1 Score (0.68): Higher than KNN, indicating a more balanced model.


Precision (0.58): Lower precision, meaning it has more false alarms.


Recall (0.83): High recall, catching 83% of the actual rainy days.


Confusion Matrix:
TP = 152, FN = 32, FP = 110, TN = 361

----
#### Interpretation: 
The Decision Tree is more aggressive in predicting rain, leading to higher recall but lower precision. It correctly identifies most rainy days but at the cost of more false alarms.

#### Logistic Regression:

Accuracy (0.81): 81% of predictions were correct, the highest along with SVM.


Jaccard Score (0.55): Best similarity between predicted and actual classes.


F1 Score (0.71): Best balance between precision and recall among all models.


Precision (0.63): Good precision, fewer false alarms than the Decision Tree.


Recall (0.83): Same recall as Decision Tree, capturing most actual rainy days.


Confusion Matrix:
TP = 152, FN = 32, FP = 90, TN = 381

----
#### Interpretation: 
Logistic Regression offers the best overall balance with high accuracy, F1 score, and a good balance between precision and recall. 
It’s effective at both catching rainy days and minimizing false alarms.

#### SVM (Support Vector Machine):

Accuracy (0.81): Matches Logistic Regression for the highest accuracy.


Jaccard Score (0.53): Slightly lower than Logistic Regression but better than KNN and Decision Tree.


F1 Score (0.69): High, indicating balanced performance.


Precision (0.65): Better than Decision Tree, close to Logistic Regression.


Recall (0.75): Lower than Decision Tree and Logistic Regression, but still high.


Confusion Matrix:
TP = 138, FN = 46, FP = 74, TN = 397

----
#### Interpretation: 
SVM is another well-balanced model with good precision and recall. It’s slightly less aggressive in predicting rain compared to Logistic Regression,
 
leading to fewer false alarms but also missing more rainy days.

### General Interpretation:
Logistic Regression and SVM are the best performers overall, offering high accuracy and a good balance between precision and recall.
 
Logistic Regression slightly edges out SVM in balancing both precision and recall.

KNN is more conservative, with fewer false alarms but more missed rainy days.

Decision Tree is more aggressive, capturing almost all rainy days but at the cost of more false alarms.

For an imbalanced dataset like this, where predicting rain (minority class) is important, Logistic Regression and SVM are preferable 

due to their higher F1 scores and better overall balance in performance.

### **Conclusion for Linear Regression in the Rain Prediction Problem:**

In this rain prediction problem, the performance of the Linear Regression model is summarized by the following metrics:

- **R² Score: 0.4271**: This indicates that the model explains approximately 42.7% of the variance in the target variable (`RainTomorrow`). 
- While this shows some degree of predictive capability, it also suggests that over half of the variability in the data is not captured by the model, indicating a moderate fit.
  
- **MAE (Mean Absolute Error): 0.2563**: On average, the model's predictions differ from the actual values by about 0.2563 units. Given that the target is binary (0 or 1), this error might be considered significant, as it represents a considerable discrepancy between predicted and actual values.

- **MSE (Mean Squared Error): 0.1157**: The MSE is relatively low, indicating that, on average, the squared difference between predicted and actual values is not large. However, since the target variable is binary, the relevance of this metric is limited.

#### **Interpretation:**
Linear Regression, which is inherently designed for continuous data, struggles with this binary classification problem. The moderate R² score suggests that while the model captures some patterns, it's not well-suited for predicting a binary outcome like rain or no rain. The MAE and MSE further indicate that the model's predictions are not particularly accurate.

#### **Conclusion:**
Given these results, Linear Regression is not the most effective model for this classification task. Models specifically designed for classification, such as Logistic Regression, SVM, or Decision Trees, would be better suited to capture the nuances of predicting rain tomorrow.
