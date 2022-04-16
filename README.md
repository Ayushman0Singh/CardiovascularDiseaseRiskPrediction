# CardiovascularDiseaseRiskPrediction
The dataset is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has a 10-year risk of future coronary heart disease (CHD). The dataset provides the patients’ information and other details. 

To do EDA on the data set, we first have to clean and prepare the data set. For that, I did Null Value Treatment and Data type check. Once the data was ready for EDA I went on ahead to see the distribution of our dependent variable(10 year CHD) alongside other features. I came up with certain Hypotheses for the problem and verified them using different tools(Hypothesis-driven EDA). The EDA gave me some idea of the data set and relevant features.
I plotted the correlation of all the features and dv. This helped me in feature selection and further data processing. Next, I applied Random Forrest and Decision tree algorithms to the data set after a test-train split. I used these to calculate feature importance. I also found that the accuracy of these tree-based algorithms was very very poor. Probably because of the high-class imbalance. I dropped certain irrelevant and highly correlated features using the correlation graph and feature importance calculations. 

I decided to apply SMOTE(synthetic minority oversampling technique) to my data set to balance the minority class. After applying smoot the data set was much more even. I also undersampled the majority class(not by much since I didn't want to lose any information). The next step was to apply different models to the data. 

I applied Logistic regression, K-nearest neighbours, Support Vector Machines(experimented with multiple kernels and chose the best one-Radial) and XG-Boost.  Since this is an imbalanced data set, I used evaluation metrics such as balanced accuracy, f1-score and AUC.

The Support vector machine with the radial kernel was the best performing model in terms of accuracy and the F1 score followed by XG-Boost. Its high AUC and this shows that it has a high true positive rate.
