# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Nancy Chemutai

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
The accuracy of the model kept increasing from 1.8014 to 0.4897 and 0.4952, respectively, after including hyperparameters.

### What was the top-ranked model that performed?
The best-performing model is WeightedEnsemble_L3, followed by WeightedEnsemble_L2, CatBoostCAT_BAG_L2, LightGBMXGB_BAG_L1, RandomForestRF_BAG_L2, LightGBMXGB_BAG_L2, CatBoostCAT_BAG_L1, and RandomForestRF_BAG_L1, respectively.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find, and how did you add additional features?
I added year, month, date, and hour by extracting the three columns from the datetime column.

### How much better did your model perform after adding additional features, and why do you think that is?
The model's accuracy improved to 0.4952, since the new features might have provided relevant information to the model, such as identifying patterns between different classes.

## Hyperparameter tuning
### How much better did your model perform after trying different hyperparameters?
There was no significant improvement after incorporating hyperparameters since the model scored 0.4952 from 0.4897, i.e., a 0.0055 difference.

### If you were given more time with this dataset, where do you think you would spend more time?
Fine-tuning the dataset using different algorithms to ensure an efficient model.

### Create a table with the models you ran, the hyperparameters modified, and the Kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|3.28|63.37|368.24|1.7962|
|add_features|16.31|195.42|629.10|1.4206|
|hpo|16.72|195.60|630.29|1.3670|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

https://rx4im9n1uveh8zr.studio.us-east-1.sagemaker.aws/jupyterlab/default/lab/tree/RTC%3And009t-c1-intro-to-ml-project-starter/model_test_score.png

![model_train_score.png](img/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

https://rx4im9n1uveh8zr.studio.us-east-1.sagemaker.aws/jupyterlab/default/lab/tree/RTC%3And009t-c1-intro-to-ml-project-starter/model_test_score.png

![model_test_score.png](img/model_test_score.png)

## Summary

The more the model was fine-tuned, the better the model performance.