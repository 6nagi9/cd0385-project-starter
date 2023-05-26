# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
After getting the predictions, I realized that all predictions were positve, so no correction to 0 was required. Also, only datetime and count columns needed to be extracted (rest all removed) for submission to Kaggle.

### What was the top ranked model that performed?
WeightedEnsemble_L3

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
The exploratory analysis found the distribution of the features for the whole dataset. I also added additional features as month, day, hour derived from datetime feature using pd.to_datetime.

### How much better did your model preform after adding additional features and why do you think that is?
My score improved from 1.79445 to 0.68935 because of creation of in more relevant month day and hour features instead of just datetime.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
My hyperparameters when to use which is not clear so I used only once, researching online. Alas!, it didn't change the score.

### If you were given more time with this dataset, where do you think you would spend more time?
I would probably remove month from the features and see the result. Than I would like to learn to tune hyperparameters more.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.

model	hpo1	hpo2	hpo3	score
0	initial	NA	NA	NA	1.79445
1	add_features	NA	NA	NA	0.68935
2	hpo	GBM	GBM	GBM	0.68935

### Create a line plot showing the top model score for the three (or more) training runs during the project.

![model_train_score.png](model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

![model_test_score.png](model_test_score.png)

## Summary
The default Autogluon intial run set a benchmark against which we can compare later iteration of feature engineering and model tuning.
