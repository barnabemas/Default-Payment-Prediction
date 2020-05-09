This project's target was to build a model to predict default payment knowing some characteristics of the client. To do so, I had access to a dataset with 5380 clients and 19 covariates (8 were categorial, 7 quantitative and 4 were dates) describing each client's situation. To build our model I split the dataset in a training set on which we built our models and a test set. I used different metrics to compare the efficiency of our model. As the default payment represented less than 10% of the total client I used confusion matrix, AUC, ROC shape in addition to the most classical classification error. I filled missing values with -1 (as the quantitative covariates only took positive values). I used one-hot encoding to handle categorial covariates. Finally, before training I centered and scaled the train and test dataset.

I trained and compared several models covering a large diversity of ML techniques:
- Random Forests
- LightGBM
- XGBoost
- CatBoost
- Fully Connected Neural Network
- Ridge classification
- Logistic Regression

When possible, I used Crossed Validation (on a parameter Grid) to optimize the hyper parameters.
I also compared the performances of our models when trained on more engineered datasets:
- While removing the covariates with less impact on our models
- While removing outliers
- By compensating the fact that "Non default payment clients" where far more numerous than "default payment clients" using oversampling, undersampling and a combination of both techniques

My approach followed these steps:
- Data Reading, Preparation
- Exploratory Data Analysis
- First Machine Learning Models
- Machine Learning Models with Engineered datasets
- Results Comparison
