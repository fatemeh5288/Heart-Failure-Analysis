# Heart-Failure-Analysis

Explanation of data:

Cardiovascular diseases (CVDs) are the number 1 cause of death globally, taking an estimated 17.9 million lives each year, which accounts for 31% of all deaths worldwide. Four out of 5CVD deaths are due to heart attacks and strokes, and one-third of these deaths occur prematurely in people under 70 years of age. Heart failure is a common event caused by CVDs and this dataset contains 11 features that can be used to predict a possible heart disease.

This dataset was created by combining different datasets already available independently but not combined before. In this dataset, 5 heart datasets are combined over 11 common features which makes it the largest heart disease dataset available so far for research purposes. 

Features list: 
#Age: age of the patient [years]
#Sex: sex of the patient [M: Male, F: Female]
#ChestPainType: chest pain type [TA: Typical Angina, ATA: Atypical Angina, NAP: Non-Anginal Pain, ASY: Asymptomatic]
#RestingBP: resting blood pressure [mm Hg]
#Cholesterol: serum cholesterol [mm/dl]
#FastingBS: fasting blood sugar [1: if FastingBS > 120 mg/dl, 0: otherwise]
#RestingECG: resting electrocardiogram results [Normal: Normal, ST: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV), LVH: showing probable or definite left ventricular hypertrophy by Estes' criteria]
#MaxHR: maximum heart rate achieved [Numeric value between 60 and 202]
#ExerciseAngina: exercise-induced angina [Y: Yes, N: No]
#Oldpeak: oldpeak = ST [Numeric value measured in depression]
#ST_Slope: the slope of the peak exercise ST segment [Up: upsloping, Flat: flat, Down: downsloping]

Target variable:
HeartDisease: output class [1: heart disease, 0: Normal]Source

Steps of data cleaning and visualization:
This data needed minimum cleaning. I changed cp, slope, and thal to dummy variables since they are not ordinal in nature. They are just different types, that should not be numerically ordered, hence converted to dummies.

Training the dataset:
Data was split into train and test set and different classification algorithms were applied. 

Summary of training:
Logistic regression yielded 90% accuracy
K-nearest neighbors resulted in 70% accuracy which is a poor performance. The n_neighbors was optimized using the accuracy vs. #k plot. Although I used optimal value of n_neighbors as 10, still the model performed poorly on test set.
SVM and Decision tree both yielded a 85% accuracy.
