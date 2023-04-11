# Spaceship-Titanic

This project is based on data from Kaggle competition. I used it to test performance of several classification models, three methods of categories encoding and parameters tuning with Optuna.

The project consists of several notebooks.

In "DataAnalysis" I performed data visualisation, data cleaning and some data transformation. It allowed me to make some observations regarding correlation between independent variables and dependent variable. The features included numerical and categorical data of each of spaceship passengers. The target was boolean variable, meanning whether the passenger was transported to another dimension after a collision. Target variable was well balanced, so accuracy metric was used in models valuation.

In "FeaturesEngineering" I included functions preparing datasets for models and predictions. It contains in particular functions performing features extraction for three metods of categorical data encoding: one hot encoding (OHE), target encoding (TE) and leave one out encoding (LOOE). Functions from this notebook were imported to next ones.

"FinalDatasets" presents three datasets for classification models, that differ in categorical data encoding.

In "Optimisation" there are functions imported to next notebooks, related to use of classification models and Optuna for parameters tuning.

Notebooks starting with word "Model_" have the same structure. Each one imports appropriate model, defines range of values for parameters tuning, prepares three datasets, calculates initial accuracy (before tuning) for each dataset, performs parameters tuning (using train and validation data subsets) and finally tests tuned model on separate test data subset. Results are saved to the file for further comparison.

Notebook "Model_Pytorch" is a bit different. I implemented there a LogisticRegression model using Pytorch and used k-fold technique for training and testing model.

"Models_Summary" contains comparison of all results with observations and conclusions.
