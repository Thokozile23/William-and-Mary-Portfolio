**HEART ATTACK PREDICTION PROJECT**

**Overview**

For our machine learning project we analyzed patient data for heart attack disease prediction.The dataset had thirty-five different columns with patient data. 
These columns include a unique patient id, state of residence, sex, self reported health status, age group, height, weight, BMI, history of stroke, asthma indicator, skin cancer indicator, chronic obstructive pulmonary disease indicator, depressive disorder indicator, kidney disease indicator, arthritis indicator, diabetes indicator, hearing impairment indicator, vision impairment indicator, walking difficulties indicator, dressing difficulties indicator, smoking status indicator, e-cigarette usage indicator, chest scan indicator, race, alcohol consumption indicator, HIV test indicator, flu vaccine status, pneumococcal vaccine status, identified as high risk in past year, tested positive for COVID-19 indicator, and whether the patient had a heart attack. 

**Research Question**

Can we predict whether or not an individual will experience a heart attack based on medical history, demographic data, lifestyle factors?

**Potential Analyses**

For this project we would like to create a model to help predict whether an individual will have a heart attack or not. This analysis can include both explanatory to determine which variables have more of an influence and predictive to apply the model with the most accurate predictions. We can also test multiple models that we learn throughout this course such as logistic regression and KNN classification, to see which yields the most accurate results.

**Significant Predictors**

1. Sex
Male increases odds
2. General Health
Higher level decreases odds
Self survey - mention this
3. Age
Higher age increases odds
4. Weight
Higher weight increases odds
5. Angina
Having angina increases odds
6. Stroke
Having stroke increases odds
7. Arthritis
Having it increases odds
8. Diabetes
Having it increases odds
9. Deaf or Hard of Hearing 
Having it increases odds
10. Blind or Vision Difficulty 
Having it increases odds
11. Flu
Vaccination over the last 12 Days increases odds
12. Pneumonia Vaccination
Having the vaccination in the past increases odds
13. Tetanus Vaccination
Having the vaccination increases odds

**Best Models** 
Our strongest model was the Centered and Scaled Quadratic Discriminatory Analysis model with the thirteen predictors listed above. This model has more adaptable decision boundaries then the other models, and is therefore more flexible to the data. Since we found our numeric variables did not have linear relationships with the classification, the quadratic model was well suited for this dataset. Quadratic Discriminatory Analysis also requires more data than other models since it has more parameters to learn. The sufficient size of the data set allowed for this model to accurately predict without overfitting. This model resulted in an overall accuracy of 0.7179, a sensitivity of 0.84186, and a specificity of 0.71065. For this model, the most important measure of accuracy is the sensitivity, since it is the proportion of actual heart attacks that are correctly identified by the model. If a heart attack is misclassified as not predicted to take place, this may result in a life threatening situation for a patient. 

**Introduction**

**Context**

Cardiovascular disease remains a leading cause of mortality worldwide, with heart attacks serving as a critical public health concern. Identifying individuals at heightened risk and understanding the contributing factors behind heart attacks could have profound implications for early prevention, medical interventions, and resource allocation. Contemporary healthcare datasets offer a wealth of patient-specific information, including demographic details, medical histories, and lifestyle indicators. By leveraging these datasets, we can employ statistical machine learning models to better understand how various factors interplay to increase the likelihood of a heart attack.
Research Question: 
To what extent can an individual’s medical history, demographic attributes, and lifestyle factors predict the probability of experiencing a heart attack?

**Objective**

The primary goal is to develop a predictive model that estimates whether a patient will experience heart attack based on a combination of health indicators, behavioral patterns, and demographic characteristics. This includes determining which features most significantly contribute to heart attack risk and comparing predictive accuracy of different classification approaches, such as logistic regression. Ultimately, this model aims to inform preventative strategies, guide clinical decision-making, and improve patient outcomes.
Approach
For this analysis we tested 6 different models and compared the predictions for each of them. The first model we tested was a logistic regression analysis with all the predictor variables included. Logistic Regression uses a mathematical function to combine the features into a probability of a heart attack ranging between 0 and 1. We then tested a logistic regression model with only predictors that were calculated to be significant. Next, we tested linear discriminatory analysis, a method that takes predictor variables and combines them into new variables that maximize the differences between classes. First, we ran a linear discriminatory analysis with all the predictor variables, and then we ran a linear discriminatory analysis with only the variables we had found to be significant within logistic regression. Finally, we tested quadratic discriminatory analysis, a method that also takes predictor variables and combines them into a new variable that maximizes the differences between classes, without assuming linear boundaries between the classes. While the Logistic Regression provided the highest overall accuracy, accuracy is heavily influenced by the imbalance in the number of patients who actually had a heart attack in the data set, so we chose to focus on finding the model with the highest sensitivity instead. This is the proportion of actual heart attacks that are correctly identified by the model.

**KEY INSIGHTS**

Our group picked the dataset called “Patients Data” used for heart disease prediction from the Virginia open data portal. This dataset had 35 columns (33 predictors) and approximately 237,000 rows (unique patients). We sampled 70% for our training set and 30% for our test set. After cleaning the data, we graphed each predictor against whether they had a heart attack to see which one had the most influence on the likelihood of a patient having had a heart attack. Based on our graphs, it looked like our strongest predictors would be whether someone has had Angina or not, whether someone has had a stroke before, and the age of the patients. These graphs provided an initial understanding of the proportional breakdowns of our dataset. All three of these predictors were found to be significant in our later models.

**Conclusion**

This project demonstrated that using demographic, lifestyle, and medical history data can help predict an individual’s risk of experiencing a heart attack. By applying models such as logistic regression, linear discriminant analysis (LDA), and quadratic discriminant analysis (QDA), we identified several key factors that appear to influence heart attack risk. While our models achieved promising results in terms of classification accuracy and interpretability, there is still room for refinement and broader applicability.
Moving forward, several steps can enhance both the utility and credibility of our findings. One important direction is to develop a more user-friendly, front-end interface. Such an interface would allow individuals, without deep technical or medical expertise, to input their health information and receive immediate insight into their potential risk level. This direct access could empower patients to take more proactive measures, such as seeking a cardiology consultation if their risk appears elevated.
In addition, collaborating closely with healthcare professionals and domain experts can provide valuable context and validation. Cardiologists, clinical researchers, and epidemiologists can help interpret why these variables were found to be the most meaningful and advise how to incorporate domain-specific knowledge. Their expert feedback might illuminate additional factors that could be added such as blood pressure, resting heart rate, and others that may help capture the inaccuracies in our model.
Lastly, continuously monitoring and refining the model after putting it into production are both key next steps. This moves us closer to a tool that can genuinely support patient empowerment, early intervention, and improved cardiovascular outcomes in everyday practice.

Accessed via Kaggle: Sample from the 2022 Annual CDC Adult Survey                    Contributors: Fiona Basewitz, Augie Cooper, Margaret Shepard, Thoko Muthali
