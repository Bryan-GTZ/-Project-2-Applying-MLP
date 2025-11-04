# -Project-2-Applying-MLP
## By: Bryan Gutierrez and Zach Lanter

## Introduction  
This project explores and compares the linear machine learning classifiers we went over in class on and tested them on the **UCI Adult Income dataset**. Our goal is to predict whether an individual’s income is over \$50K per year based on demographic and employment attributes.  



| Attribute          | Attribute        |
|--------------------|------------------|
| Age                | Occupation       |
| Workclass          | Relationship     |
| Education          | Race             |
| Marital Status     | Sex              |
| Capital Gain        | Hours Per Week   |
| Native Country     |    Capital Loss              |


## Multi-Layer Perceptron (MLP) Project

### Part 1: MLP

a) load and preprocesses the dataset
* Loaded project_adult.csv and project_validation_inputs.csv, replacing ? with nulls
* Target variable income converted to binary (1 = >50K, 0 = <=50K)
* Used a ColumnTransformer
* Ensured all missing values were handled

b) Train and test MLP (Split data into 70% training / 30% testing)

* Built an MLPClassifier pipeline with:
* max_iter=500, early_stopping=True, validation_fraction=0.1.
* Used GridSearchCV (3-fold) to tune hyperparameters:
* Hidden layers: (50,), (100,), (50,50), (100,50)
* Activation: relu, tanh
* Alpha: 0.0001, 0.001
* Learning rate: 0.001, 0.01

c) Evaluate models using appropriate metrics

* Best model metrics on test set:
* Accuracy: 0.8482
* Precision: 0.6771
* Recall: 0.6652
* F1-Score: 0.6711

d) Select most promising model

* Best model:
* hidden_layer_sizes=(50,)
* activation='relu', alpha=0.001
* learning_rate_init=0.001


e) Predict response variable for validation inputs

* Applied final model to validation dataset
















