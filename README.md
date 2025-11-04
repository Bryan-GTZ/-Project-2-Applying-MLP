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

b) Train and test MLP
*












