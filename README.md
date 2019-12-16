
# Module 5 Final Project - Classification

## Dataset

This project was an exploration of NYC’s Department of Buildings Permit Issuance Data collected from the NYC.gov API. using classification algorithms. The dataset contains all DOB permits issued in NYC from 2013-2019, with 3.6 million rows and 60 total features. Documentation exists on various DOB websites. The dataset contains primarily categorical features relating to types of permits, locations, and other  information about specific permits issued.

## Question

Predicting whether a property is **Residential** or **Not Residential (Commercial)** - binary classification.

![Image description](link-to-image)


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

**Decision Tree**	
- Accuracy: 0.68	
- AUC: 0.64	

F1 and Recall:
- N	0.57	0.45	
- Y	0.74	0.88	

**Random Forest**	
- Accuracy: 0.72	
- AUC: 0.77	

F1 and Recall:
- N	0.66	0.59	
- Y	0.76	0.83	

**AdaBoost**	
- Accuracy: 0.68	
- AUC: 0.70	

F1 and Recall:
- N	0.62	0.55	
- Y	0.73	0.79	

**Gradient Boosting**
- Accuracy: 0.70	
- AUC: 0.69	

F1 and Recall:
- N	0 .62	0.54	
- Y	0.75	0.84	

**Logistic Regression**	
- Accuracy: 0.69	
- AUC: 0.75

F1 and Recall:
- N	0.64	0.60	
- Y	0.73	0.77	

**SVM**
- Accuracy: 0.69
- AUC: 	Not Run	

F1 and Recall:
- N 0.64	0.59	
- Y	0.72	0.77	

## Final Model

Random Forest was selected as the final model because of it's combination of high accuracy and AUC. This project was interested in exploring the prediction of both Residential and Non-Residential properties, so balancing the precision and recall is important for the overall predictive ability of this model. 

## Feature importances:

The following details the top important features identified in the Random Forest model:

- City Council District 4
- Mechanical and Other work permit types
- New Buildings and Demolitions
- Manhattan 
- Self certification
- Nonprofit (NYCHA)

## Limitations

This was a large dataset, and it suffered from many of the disadvantages in processing speed both in obtaining the data from the NYC API, and in run time of the tests. Many of the tests had to be run on a substantial subset, and even then processesing speed could not full incorporate gridsearch into several of the models. Additionally, though there were meany features present at the outset, many had to be dropped because of missing values, messy data collection, and data leakage issues. 


## Next steps

To improve the function of this model, I would like to incorporate SMOTE to improve the model's recall (and balance the dataset).





