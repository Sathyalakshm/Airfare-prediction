# Airfare Prediction Project  
****A model designed to predict the airfare with an r2_score of 0.984781

Welcome to the Airfare Prediction Project! This project aims to predict airfare prices based on historical data and various features. Whether you're a traveler looking to plan your next trip or a data scientist interested in exploring airfare prediction models, this project has something for you.

• To find the best fit model to analyse and predict ticket prices for upcoming flights.
• To help customers in selecting the optimum time to book and the cheapest flight to
the desired destination.
• To study the factors which influence the fluctuations in the airfare prices and how
they are related to the change in the prices.
Techniques:
1. Exploratory Data Analysis (EDA):
**Descriptive Analytics **
Duration Analysis: The average duration of flights in the dataset is approximately 12.22 hours, with a standard deviation of 7.19 hours. This indicates a considerable variability in flight durations.
Price Analysis: The average ticket price in the dataset is approximately 20,889.66, with a standard deviation of 22,697.77. This indicates a significant variation in ticket prices.

**Missing Data Analysis**: Our dataset do not have any null/nan/missing values.

**Outliers Detection**: For the 'duration' column, there are 722 outliers, which are flights with a duration greater than 30 hours. These outliers might be a result of layover stops between flights, including overnight layovers and flight cancellations. It is reasonable to have such outliers, so there is no need to remove them.
For the 'price' column, there are 602 outliers. These outliers might be due to natural price surges that occur, and they are not necessarily erroneous data points. Therefore, it is also not necessary to remove these outliers.It seems that the outliers detected in the 'duration' and 'price' columns are valid and represent natural occurrences in flight durations and pricing.

**Feature encoding**
One-Hot Encoding for Nominal Data- 'airline', 'source_city', 'departure_time', 'arrival_time', and 'destination_city'
Label Encoding for Ordinal Data-'Stops' and 'Class'
Feature Selection

**Correlation Analysis**: There is strong correlation with Class and Price.
**Mutual information** : The top features with higher mutual information scores were
ExtraTreesRegressor: feature importance based on how much they contribute to the overall performance of the model.
**Data Splitting **
The dataset was divided into training and testing sets to assess the model's performance effectively 

**Normalization for Model Evaluation**
Min-Max normalization was applied.
Hyperparameter tuning
## Models
**Model Building and Evaluation:** Three models, namely Linear Regression, Decision Tree,
and Random Forest, were built and evaluated to predict flight prices. The evaluation included
the calculation of mean absolute error (MAE) and R-squared (R2) score for each model. The
results are summarized below:
• **Linear Regression**:The Linear Regression model yielded an MAE of approximately
4,485.83 and an R2 score of 0.90982.The MAE represents the average absolute
difference between the predicted flight prices and the actual prices. In this case, a
lower MAE indicates better model performance.The R2 score represents the
proportion of the variance in the flight prices that can be explained by the model. A
value closer to 1 indicates a better fit to the data.
• **Decision Tree**: The Decision Tree model resulted in an MAE of around 1,183.92 and
an R2 score of 0.975269.Compared to Linear Regression, the Decision Tree model
achieved a lower MAE, indicating improved prediction accuracy.The higher R2 score
suggests that the Decision Tree model explains a larger portion of the variance in the
flight prices.

• **Random Forest**:The Random Forest model exhibited the lowest MAE of
approximately 1,082.35 and the highest R2 score of 0.984828.The Random Forest
model outperformed both Linear Regression and Decision Tree models in terms of
both MAE and R2 score.The lower MAE indicates better prediction accuracy, and the
higher R2 score signifies that the Random Forest model explains a larger proportion
of the variance in the flight prices.
Based on these findings, the Random Forest model emerged as the most promising for
predicting flight prices, as it achieved the lowest MAE and highest R2 score among the three
models. However, it is crucial to note that model performance may vary depending on the
specific dataset and problem domain. It is recommended to conduct further evaluation, fine-
tuning, and validation to ensure the robustness and generalizability of the selected model.

**Hyperparameter tuning**
The hyperparameter tuning and evaluation Was done for three different regression models
(Linear Regression, Decision Tree, and Random Forest) using the RandomizedSearchCV
function from scikit-learn. The results show the mean absolute error (MAE) and R2 score for
each model after hyperparameter tuning. The Linear Regression model has an MAE of
approximately 4482.29 and an R2 score of 0.909839. The Decision Tree model has an MAE
of around 1184.61 and an R2 score of 0.975359. The Random Forest model has the lowest
MAE of approximately 1083.51 and the highest R2 score of 0.984781.
Based on these results, the Random Forest model with hyperparameter tuning performs the
best, as it has the lowest MAE and highest R2 score.
Based on these findings, the Random Forest model emerged as the most promising for predicting flight prices, as it achieved the lowest MAE and highest R2 score among the three models.
