
# Module 5 Final Project - Classification

## Dataset

This project was an exploration of NYC’s Department of Buildings Permit Issuance Data collected from the NYC.gov API. using classification algorithms. The dataset contains all DOB permits issued in NYC from 2013-2019, with 3.6 million rows and 60 total features. Documentation exists on various DOB websites. The dataset contains primarily categorical features relating to types of permits, locations, and other  information about specific permits issued.

## Question

Predicting whether a property is **Residential** or **Not Residential (Commercial)** - binary classification.


![Image description](https://github.com/mellymillionz/Classification_Project/blob/master/total_counts.png, img width=200)


## Feature Engineering

- self certification 
- borough
- nonprofit 
- work type (recoded) 
- job type (recoded) 
- permit type (recoded) 
- permittee license type (recoded)
- owner business type (recoded)
- permit sequence 
- council district

All categerical variables were **One-Hot-Encoded** prior to modeling to convert all categorical variables to numeric values. 

### Modeling


![Image description](https://github.com/mellymillionz/Classification_Project/blob/master/Outcomes.png)

## Final Model

Random Forest was selected as the final model because of it's combination of high accuracy and AUC. This project was interested in exploring the prediction of both Residential and Non-Residential properties, so balancing the precision and recall is important for the overall predictive ability of this model. 

![Image description](https://github.com/mellymillionz/Classification_Project/blob/master/Randon_forest_ROC.png)


## Feature importances:

The following details the top important features identified in the Random Forest model:

- City Council District 4 (Midtown East and UES)
- Mechanical and 'Other' work permit types
- New Buildings and Demolitions
- Borough of Manhattan 
- Self certification
- Nonprofit (NYCHA)

## Limitations

This was a large dataset, and it suffered from many of the disadvantages in processing speed both in obtaining the data from the NYC API, and in run time of the tests. Many of the tests had to be run on a substantial subset, and even then processesing speed could not full incorporate gridsearch into several of the models. Additionally, though there were meany features present at the outset, many had to be dropped because of missing values, messy data collection, and data leakage issues. 


## Next steps

To improve the function of this model, I would like to incorporate SMOTE to improve the model's recall (and balance the dataset).





