# Customer Churn Analysis Prediction Using KNN

## Overview

This project focuses on predicting customer churn for a call center using the K-Nearest Neighbors (KNN) algorithm. Churn prediction is crucial for businesses as it helps identify customers who are likely to leave, allowing companies to take proactive actions to retain them. In this project, I aimed to understand patterns and which factors led to a high likelihood of the customer churning such factors being;
total_day_minutes               
number_customer_service_calls    
total_intl_charge                
total_intl_minutes               
total_night_minutes              
total_day_calls                  
total_night_calls               
total_intl_calls                
number_vmail_messages           
account_length .

The primary goal was to use historical customer data, transaction records, and behavioral patterns to train a KNN model to predict the likelihood of churn. This type of analysis is valuable for businesses in sectors like telecommunications and subscription services, where customer retention is critical.

## Methodology

The approach for this project was as follows:

1. **Calculated churn statistics and percentages**

To begin, I calculated the overall churn rate within the dataset. This involves determining the proportion of customers who had churned versus those who had remained with the company.I found that 60% did not churn and 40% churned.By calculating the churn percentage, I gained an initial understanding of the overall customer retention rate, which would help me assess the predictive accuracy of my model.

2. ** Calculated correlation matrix**: 

Next, I created a correlation matrix to identify relationships between the features in the dataset. A correlation matrix helps to determine if there are any strong linear relationships between variables. In the context of churn prediction, this step allowed me to understand how different variables relate to each other. A high correlation between certain features may indicate potential redundancies or important relationships for the prediction model.

3. **Extracted the correlation with the churn column**:

After calculating the full correlation matrix, I extracted the correlation values between the various features and the churn column specifically. This step was important because it allowed me to identify which variables had the strongest positive or negative correlation with customer churn. Features with strong correlations to churn were more likely to serve as important predictors, and they would be prioritized during model training. This information informed my feature selection process, ensuring that only the most impactful variables were used.

4. **Selected the top predictors and the churn column**: 
Based on the correlation analysis, I selected the top predictors that had the most influence on the likelihood of churn. I picked the variables like account length, total day in minutes, number of customer service calls, number of vmail messages and total international charges which were highly correlated with churn, and these features were included for training the k-NN model. I ensured that the churn column was also included as the target variable to predict the outcome.


5. **Defined features and target variable**: 

In this step, I explicitly defined the features (independent variables) and the target variable (dependent variable). The target variable was the churn column, indicating whether a customer had left or remained. The features included variables like account length, total day in minutes, number of customer service calls, number of vmail messages and total international charges.

6. **Normalize the data**: 

Since k-NN is a distance-based algorithm, it is sensitive to the scale of the data. I normalized the dataset to ensure that all features had the same scale, preventing features with larger ranges from dominating the distance calculation. 
7. **Split the data into training and test sets (60% training, 40% test)**

To evaluate the model’s performance, I divided the dataset into a training set and a test set. The training set, consisting of 60% of the data, was used to train the k-NN algorithm and learn the relationship between the features and the target variable. The remaining 40% of the data was reserved as the test set to evaluate how well the model generalizes to unseen data. This split was essential for assessing the model's predictive accuracy and avoiding overfitting to the training data.

8.**Evaluate k-NN for k values from 1 to 10 using the elbow method**

For k-NN, selecting the optimal value of k (the number of neighbors) is crucial. To determine the best k, I evaluated the k-NN model for k values ranging from 1 to 10 using the elbow method. This method involves plotting the model’s error rate (or accuracy) for each k value and identifying the “elbow,” where increasing k no longer significantly improves the model's performance. This helped me find the optimal k value for my model which was at 7, 0.1383333333333333 as shown in the graph below.


9. **Best k based on the elbow method**

Based on the elbow method, I identified the optimal value of k that resulted in the lowest error rate and the highest predictive accuracy. The best k value was chosen to ensure the k-NN model was neither overfitting nor underfitting. For this project, k=7 was determined to be the most effective value, balancing model complexity and prediction accuracy.



10.Build and evaluate the final k-NN model with k=7

With the optimal k value selected, I built the final k-NN model using k=7. The model was trained on the training dataset and then evaluated on the test set. I assessed its performance based on key metrics, including accuracy, precision, recall, and F1-score. These metrics allowed me to gauge how well the model predicted churn and its ability to correctly identify customers who would leave.

11. Predicted on the test set

Using the trained k-NN model with k=7, I made predictions on the test set. These predictions indicated whether each customer in the test set was likely to churn or not. The test set was kept unseen during training, providing a true evaluation of how the model performs on new, real-world data. The output indicated 0.1383333333333333 showing that the model was indeed effective in predicting customer churn.


12.Calculated the misclassification rate

To evaluate the model's prediction accuracy, I calculated the misclassification rate. I correctly predicted 346 not churning and 171 churning. while 14 were misclassified as not churners when they were and 69 churners when they were not.

13.Compute ROC curve and ROC area

To further evaluate the model’s classification performance, I computed the Receiver Operating Characteristic (ROC) curve and the Area Under the Curve (AUC). The ROC curve shows the trade-off between the true positive rate and the false positive rate, while the AUC represents the model’s ability to distinguish between churned and non-churned customers.The AUC was 0.89 which  indicates the model was performing well.




## Tools and Technologies Used

- **Python**: For data analysis, machine learning, and model building.
- **K-Nearest Neighbors (KNN)**: To build the churn prediction model.
- **Pandas and NumPy**: For data manipulation and analysis.
- **Matplotlib and Seaborn**: For data visualization and EDA.
- **Scikit-learn**: For implementing the KNN algorithm and evaluating model performance.
- **Jupyter Notebooks**: For organizing the analysis and visualizations.

## Key Findings and Results

- The KNN model provided good predictions with a relatively high accuracy score after tuning the value of K.
- Key features that influenced churn included **Account length**, **total day in minutes**, **number of vmail messages** and **total International charge**.
- Customers with a high frequency of service interactions and a decrease in product usage were more likely to churn.
  
## Conclusion and Recommendations

Based on the churn prediction model, businesses can take proactive steps to reduce customer churn by focusing on high-risk customers. By offering personalized promotions, improving customer support, and engaging with customers more effectively, companies can retain valuable customers and improve customer lifetime value
