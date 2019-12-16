
# Module 5 Final Project


## Introduction

In this lesson, we'll review all the guidelines and specifications for the final project for Module 5.

## Dataset

This project was an exploration of NYC’s Department of Buildings Permit Issuance Data collected from the NYC.gov API. using classification algorithms. The dataset contains all DOB permits issued in NYC from 2013-2019, with 3.6 million rows and 60 total features. Documentation exists on various DOB websites. The dataset contains primarily categorical features relating to types of permits, locations, and other  information about specific permits issued.

## Question

* Predicting whether a property is Residential or Not Residential (Commercial) - binary classification.

## Feature Engineering

- self certification (Y, N, NA)
- borough
- nonprofit (Y, N) 
- work type (recoded) 
- job type (recoded) - A2, A3, A1, NB, DM, SG
- permit type (recoded) - EW, PL, EQ, AL, NB, FO, SG, DM
- permittee license type (recoded) - GC, MP, FS, OB, SI, NW, OW, RA, PE
- owner business type (recoded)
- permit sequence 
- council district (26)

All categerical variables were One Hot Encoded prior to modeling.

### Modeling

**Decision Tree**	
- Accuracy: 0.68	
- AUC: 0.64	
- N	0.57	0.45	
- Y	0.74	0.88	

**Random Forest**	
- Accuracy: 0.72	
- AUC: 0.77	
- N	0.66	0.59	
- Y	0.76	0.83	

**AdaBoost**	
- Accuracy: 0.68	
- AUC: 0.70	
- N	0.62	0.55	
- Y	0.73	0.79	

**Gradient Boosting**
- Accuracy: 0.70	
- AUC: 0.69	
- N	0 .62	0.54	
- Y	0.75	0.84	

**Logistic Regression**	
- Accuracy: 0.69	
- AUC: 0.75	
- N	0.64	0.60	
- Y	0.73	0.77	

**SVM**
- Accuracy: 0.69
- AUC: 	Not Run	
- N 0.64	0.59	
- Y	0.72	0.77	

## Final Model

Selected Random Forest as the final model.
Parameters: 

## Feature importances:
- City Council District 4
- Mechanical and Other work permit types
- New Buildings and Demolitions
- Manhattan 
- Self certification
- Nonprofit (NYCHA)

## Limitations

- Data leakage
- API slow
- Processing speed low with so much data
- Could not use GridSearch or run most models on full dataset
- Disproportionate data 
- Too many related categorical variables (dropped)
- Messy government dataset 
- Make sure to update your Sklearn





