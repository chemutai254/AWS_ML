# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Nancy Chemutai

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
The accuracy of the model kept increasing.

### What was the top ranked model that performed?
WeightedEnsemble_L3

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
I added three columns, i.e., year, month, and date, by extracting the three columns from the datetime column.

### How much better did your model preform after adding additional features and why do you think that is?
The WeightedEnsemble_L3  model performed well, followed by RandomForestMSE_BAG_L2 and LightGBM_BAG_L2.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
The accuracy of the model kept improving as I re-trained using new features in the dataset.

### If you were given more time with this dataset, where do you think you would spend more time?
Fine-tuning the dataset using different algorithms to ensure an efficient model.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
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

The more the model was fine-tuned, the more the model performed better.