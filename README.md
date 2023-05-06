
# Valorant Pro Match Analysis

> Predictive Modeling Based on Team Performance and Player Statistics
>
> Author(s): \
> [Mohammad Ryan Ur Rafi](https://github.com/DEF4LT-303) \
> Ahmed Zarir Siddique \
> Hasnat Md. Imtiaz

**I. INTRODUCTION**

>Predicting the outcomes of professional esports matches has become a critical problem, with substantial practical consequences such as aiding teams in strategic decisions, helping investors place wagers, and providing game developers with critical insights into the game's meta. Machine learning has emerged as a viable method for forecasting esports match outcomes because it can use massive amounts of data to identify patterns and relationships that people find difficult to detect.  In this project, we will use Python and its machine learning libraries to create a classification model that can accurately predict the winning team from a list of teams in a tournament, predict which team will win given a balance of 10 different players with 5 in each team, and judge players based on their average ACS, ADR, Econ, and other stats. By the end of this project, learners will have a good understanding of how to approach a machine learning problem and apply these techniques to real-world scenarios in the field of professional esports.


**Dataset:** [https://www.kaggle.com/datasets/visualize25/valorant-pro-matches-full-data](https://www.kaggle.com/datasets/visualize25/valorant-pro-matches-full-data "https://www.kaggle.com/datasets/visualize25/valorant-pro-matches-full-data")


 **II\. MODEL APPROACHES**



>In our experiment, we have used two of the most commonly used machine learning models, the Decision Tree Regressor and the Random Forest Classifier. The Decision Tree Regressor takes input data and produces a regression output. The architecture of this model is similar to that of a tree. The algorithm breaks down the dataset into smaller subsets, where each feature is reviewed and examined in order to make an informed decision based on the pattern made by the dataset. The Decision Tree Regressor is a powerful model for predicting numerical values. It can handle both categorical and continuous variables and is robust to outliers. It is also easy to interpret, making it a popular choice for data analysis.
>
>  
>
>The Random Forest Classifier works by creating a large number of decision trees and aggregating their predictions. Each decision tree is trained on a random subset of the input data, and a random subset of the features is selected at each split. This randomness helps reduce overfitting and make the model more robust. The Random Forest Classifier has several advantages. It is less prone to overfitting and can handle larger datasets with many features. It is also more accurate than a single Decision Tree, as the aggregation of multiple models helps reduce variance and improve prediction accuracy.
>
>
>
>To conclude, the Random Forest Classifier has shown significant improvement in the performance of the first two experiments. By modifying the work of [1] and using Random Forest Classifier instead of Decision Tree Classifier, we have achieved better accuracy in our predictions. Cleaning the data properly before feeding it to our model has also helped us improve the results significantly. However, for our third experiment, where we predict the outcome of matches played by defined teams, the Decision Tree Regressor shows better performance than the Random Forest Classifier. Because the data we provide here is smaller and more clustered than the original dataset. As Decision Tree Regressor is more prone to overfitting, it performs better on the small modified dataset.

**III\. PERFORMANCE METRICS**

| **Experiment**| **Model** | **Training Accuracy** | **Testing Accuracy** |
| -------- | -------- | -------- | -------- |
| **Predicting Winning Team** | Random Forest Classifier | 100% | 93% |
| **Predicting Top Players** | Random Forest Classifier | 100% | 60% |
| **Predicting Player Stats (kills)** | Decision Tree Regressor | 100% | 98% |

> <img src="https://raw.githubusercontent.com/DEF4LT-303/Valorant-Pro-Match-Analysis/main/Media/image1.png" alt="Confusion Matrix" style="width: 500px;"/>


**Fig-1: Confusion Matrix (Predicting Winning Team)** \
The confusion matrix shows a representation of he count of correct and wrong predictions.

><img src="https://raw.githubusercontent.com/DEF4LT-303/Valorant-Pro-Match-Analysis/main/Media/image2.png" alt="Density Plot" style="width: 500px;"/>


**Fig-2: Density Plot (Predicting Top Players)** \
The density plot graph shows the distribution of True ACS and Predicted kills of players.

><img src="https://raw.githubusercontent.com/DEF4LT-303/Valorant-Pro-Match-Analysis/main/Media/image3.png" alt="Density Plot" style="width: 500px;"/>



**Fig-3: Density Plot (Predicting Player Stats)** \
The density plot graph shows the distribution of True kills and Predicted kills of players.

**IV\. RESULTS**
>For the part where the model is able to predict the winning team in a tournament, On the test dataset, the machine learning model constructed in this research performed well, with an accuracy of 93%. A Random Forest Classifier with 100 estimators was utilized as the model. The training accuracy was determined to be 1.0, and the testing accuracy was determined to be 0.93. The model was used to forecast the winning team in a tournament given a balance of ten distinct players, with five on each team, as well as to rate players based on their predicted ACS. The results demonstrated that the model could correctly estimate the winning team from a list of teams in the competition. However, the accuracy of the model was lower when predicting a sample of top players in the future based on their ACS. Further improvements could be made by tuning the hyperparameters of the model or by using similar machine learning models that adopt the Tree machine learning model architecture. Overall, this model showed significant promise and could be a good alternative for predicting the winning team in a tournament.
