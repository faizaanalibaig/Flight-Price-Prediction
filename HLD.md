Project Analysis Report: Flight Price Prediction

This is HLD file that is High level design of this project, and everything regarding implementation is present in jupyter source file

1. Introduction:
The aim of this project was to create a predictive model that helps customers predict future flight prices and plan their journeys accordingly.
The dataset contains various features related to airlines, dates, sources, destinations, flight duration, and additional information. But all the input features are objects and we were converting them into
numerical features. 

3. Domain Analysis:
The domain analysis provided insights into each feature:
- Airline: Different airlines offer varying levels of service and pricing.
- Date_of_Journey: Captures seasonal patterns and day-of-week effects in flight prices.
- Source and Destination: Departure and arrival locations can influence ticket prices.
- Route: Describes the flight path, affecting ticket prices.
- Dep_Time and Arrival_Time: Departure and arrival times may impact pricing based on traveler preferences.
- Duration: Total time taken for the flight journey, influencing ticket prices.
- Total_Stops: The number of stops in the flight journey may affect pricing.
- Additional_Info: Provides additional details about the flight that could influence ticket prices.
- Price: The target variable representing the flight ticket price.

3. Data Preprocessing:
   Data preprocessing involved dropping duplicate records, dropping Null records and Label Encoding categorical features, extracting relevant information from date and time features,
and One-Hot Encoding some categorical variables. Additional_Info feature was manually encoded, replaced price above 40000 to mean of the price, because it's very rare to have price above 40000.
* In this dataframe we had 11 Features in which 10 are independent and one is out output feature or we can say it is dependent feature.
* Now the problem was all the 10 features were objects and we need to convert them into numerical columns. 
* Those 10 features contains dates, time, source location, destination location etc, but the pronlem was no feature contains correct format of anything like time or date
* every feature needs different approach to extract the values from those object or categorical columns.
* From every single feature we are creating many features like for example, in Dep_Time it contains unstructured format of time and we were extracting seperately minute like Dep_minute and Dep_Hour


4. Exploratory Data Analysis (EDA):
EDA provided insights into the distribution of features, correlations, and counts of different categories.
Countplots helped understand the distribution of airlines, sources, destinations, and more. Heatmap showed correlations between certain features like Source_Channai, Cochin and Kolkata.
* Extracting insights from the object columns were like challanging, but with help of some research and analysis we found some insights regarding this data and in detail about the insights is present in
  jupyter source file below every plot i have written the insights which i found from the plots.

6. Model Evaluation:
Various regression models were trained and evaluated using R2_score, MSE, RMSE, and MAE metrics. Models evaluated were Linear Regression, SVR, KNN, Decision Tree, Random Forest,
Bagging for Decision Tree, Bagging for Random Forest, Gradient Boosting, XGradient Boosting (XGB), and Tuning for XGB.

8. Model Selection:
The XGradient Boosting (XGB) model emerged as the best performer with an R2_score of 0.907 and the smallest MAE of 714.15. The Random Forest model also performed well with the smallest MSE and RMSE.

9. Challenges Faced:
Data preprocessing challenges included converting object datatypes, extracting meaningful information from date and time features, and dealing with categorical variables.
Improving model performance required careful feature engineering, hyperparameter tuning, and manual encoding.

11. Conclusion:
The project successfully developed a predictive model for flight price prediction.
The XGradient Boosting (XGB) model was identified as the best performer, achieving a 90% R2_score and demonstrating potential for accurate price predictions.
The Random Forest model also exhibited strong performance.

13. Recommendations:
- Further explore feature engineering and consider feature interactions to potentially improve model performance.

10. Project Summary:
The project achieved the business objective of creating a predictive model to help customers forecast future flight prices.
The XGradient Boosting (XGB) model demonstrated the highest accuracy and is recommended for deployment to assist customers in planning their journeys effectively.

<br>
**Note:** Detailed technical specifications, algorithms, and code implementation details are typically provided in separate ipynb file sections of the project repository.


