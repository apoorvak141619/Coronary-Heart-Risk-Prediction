# Coronary-Heart-Risk-Prediction
Project that judges whether a person will be at heart disease risk after 10 years based on current lifestyle and medical history

## Background 
This is a part of data from an ungoing study being conduted in Framingham, Massachusetts, USA. It includes 15 columns and around 4200 rows, where each row presents a person's behavioural, demographic and medical (history and current) information. Each column is a potential risk factor. 

Demographic:

• Sex: male or female(Nominal)

• Age: Age of the patient;(Continuous - Although the recorded ages have been truncated to whole numbers, the concept of age is continuous)
Behavioral:

• Current Smoker: whether or not the patient is a current smoker (Nominal)

• Cigs Per Day: the number of cigarettes that the person smoked on average in one day.(can be considered continuous as one can have any number of cigarettes, even half a cigarette.)

Medical( history):

• BP Meds: whether or not the patient was on blood pressure medication (Nominal)

• Prevalent Stroke: whether or not the patient had previously had a stroke (Nominal)

• Prevalent Hyp: whether or not the patient was hypertensive (Nominal)

• Diabetes: whether or not the patient had diabetes (Nominal)

Medical(current):

• Tot Chol: total cholesterol level (Continuous)

• Sys BP: systolic blood pressure (Continuous)

• Dia BP: diastolic blood pressure (Continuous)

• BMI: Body Mass Index (Continuous)

• Heart Rate: heart rate (Continuous - In medical research, variables such as heart rate though in fact discrete, yet are considered continuous because of large number of possible values.)

• Glucose: glucose level (Continuous)

Predict variable (desired target):

• 10 year risk of coronary heart disease CHD (binary: “1”, means “Yes”, “0” means “No”)

## Objective
For The dataset provides the risk factors associated with heart disease for the patients and whether they have a risk of coronary heart disease in the next 10 years. 
Based on the dataset provided:
1.	Predict the probability of a patient suffering a coronary heart disease in the next 10 years
2.	Identify the most important factors that influence heart disease
3.	Come up with recommendations for
  a.	Preventing / reducing chances of getting a heart disease
  b.	Extrapolated applications of the model you build and its findings
  
## EDA Conclusions

<u> Summary of Study Group </u> : The study consists of 4,240 borderline-overweight Middle-Aged to Older patients, with the sex ratio slightly skewed towards Women, consisting of an almost even split between smokers and non-smokers. There are no diabetics in the group, and  only 25 people or 0.6% of the study group have had a history of strokes. Everyone in the study has high cholestrol levels.


<u> Results of EDA </u> : 85% of people are at a very low risk of heart failure by the end of 10 years. Older Women are more at risk of heart attacks. 

<u> Data Insights </u> :
1. Data is unbalanced. 

2. Education level does not seem to be related to the heart risk. If we had any data related to their occupation, then it might provide context to analyse the education data Vs Heart Risk. 

3. Systolic BP & Diastolic BP are highly correlated to each other.


## <u>Most Important Features</u>

The most important features that affect the 10-year Heart Risk factor:

1. Systolic BP
2. Age
3. Cigerattes Per Day
4. Total Cholestoral
5. Prevalent Hypertension
6. Diastolic BP
7. Diabetics
8. BP Medicines
9. Sex
10. Prevalent Stroke

The features to be ignored are education, BMI, heart rate and current smoker. We did not have any information about education to begin with and EDA analysis supported the fact that education was not a relavent factor. BMI seemed important at first glance but I will go with Univariate Feature Selection Analysis results. Same for heart rate and current smoker. 


## <u>Recommendations</u>

### Recommendations for Preventing or Reducing Chances of Heart Attack

The recommendations from the models show that there are 2 factors under our control to reduce chance of heart attack and 1 factor that is not. 

The 2 factors that we can control are: 

1. Systolic <u>BP</u> is one of the most important factor to determine risk of heart attack. So keeping BP in check is essential. 

2. The number of <u>cigarettes</u> smoked per day is directly proportionate to the probability of heart attack. So smoking kills!

The factor not under our control, that increases chance of heart attack is <u>Age</u>. As we age, the probability of getting a heart attack increases as well. So regular excercises and a healthy lifestyle is the only way to reduce chance of heart attack.



### Extrapolated applications of the model you build and its findings

1. The data overall, is highly imbalanced. Additional data, especially for the minority class will improve the accuracy of prediction.


2. The Gradient Boosting Model has the highest accuracy at 81% so if there are high-level decisions to be made, such as resources to be allocated to hospitals, support for patients or long-term health budget allotments, then this is the model to use. 


3. The Support Vector Machine (SVM) was the best performing model in terms of F1, Precision and Recall scores. So, if any individual assessment is to be made, based on the demographic, behavioural and medical information, then SVM is the method to use
