# BA 545 Course Project 1: Advanced Preparation of Financial Data
## Spring 2020

## Overview of the Competition

Understanding pricing strategies in the context of the Initial Public Offering (IPO) process has been receiving much attention. Most prior studies have however focused on information sources from post issuance periods, and understanding such strategies from the management’s perspective during the IPO process is still an open research issue. Form 424 variants, as finalized IPO prospectus approved by Security Exchange Committee (SEC), contain rich and genuine information about the issuing firms. In this study, we analyze the inter-relationships between the management’s confidence (through the proxy of sentiments expressed in textual contents in the Management’s Discussion & Analysis (MD&A) sections in the prospectus) and the pre-/post-IPO valuations.

In this competition, you are provided with data regarding successful U.S. IPOs from __more than 600 companies__. Your client is seeking advanced and novel methods to __prepare the collected data__, for further predictive analysis of the “underpricing” phenomenon. You will mainly focus on the data understanding and data preparation phases in the CRISP-DM model. Advanced preparation and modeling techniques will be needed for extra points.

 
### Evaluation Rules
- Submissions are evaluated on __two evaluation metrics__ of the modeling results; each part takes up to __100__ points:
  - _Prediction Accuracy_: we will use F-1 score as the measurement of how close the predicted values are to the factual outputs – please refer to [this Wikipedia article](https://en.wikipedia.org/wiki/Precision_and_recall) for the computation of F-1 score;
  - _Predictive Power_: we will use __ROC curve__ (Receiver Operating Characteristics), or similarly, AUC (Area Under ROC Curve), is a graphical representation that demonstrate the predictive performances of models. Note that ROC/AUC can only be applied to __binary targets__. The rule-of-thumb for ROC is as follows (the higher the better):
  
 | AUC Value | Interpretation |
:--- | :---
| 1.0 | Perfect Analysis |
| 0.9 - 0.99 | Excellent Analysis |
| 0.8 - 0.89 | Good Analysis |
| 0.7 - 0.79 | Fair Analysis |
| 0.5 - 0.69 | Poor Analysis |
| 0.5 and Below | Worthless Analysis |


  
## Guidelines

### Research Question
The overarching research question is “ _What are the determinants of IPO underpricing phenomena?_ ” In this competition, your main purpose is to prepare the data for predictive models answering the overarching research question.

### Data Dictionary
See attached ‘Data Dictionary’ Document.

### Suggested Tasks
Following tasks are normally conduct in data preparation phase. __Not all steps are required/available in this particular dataset__ – and __not in this particular order__. Some additional step(s) might be required – which you might need to research on. Keep in mind that your decisions on different strategies below will determine the results.

1. __Descriptive statistics__ – describing the data using minimum, maximum, 1st & 3rd quartile, mean, median, standard deviation, number of records, number of missing records, ...
2. __Imputation__ – dealing with missing data, you can choose from following strategies: 
  i) drop the record with missing (highly discouraged); 
  ii) replace the missing with mean/median/mode, determined on the data type; 
  iii) replacing missing values in continuous field with linear regression predictions;
3. __Normalization__ – You need to manipulate all continuous fields to follow normal distribution: which contains two steps: 
  i) removing skewness (using logarithm, square root, etc.) 
  ii) make sure the residual is randomly distributed;
4. __Correlation analysis__ – you need to select predictor variables with low pair-wise correlation (i.e. spearman’s) values – usually the threshold is __0.5__ – one variable from the pair should be excluded from the model;
5. __Standardization__ – you need to convert the values at the same numeric level; one way of doing this is to use the z-score standardization, which is calculated as shown on [this page](https://www.statisticshowto.datasciencecentral.com/probability-and-statistics/z-score/).
6. __Recoding__ – for categorical data, you might want to recode them. For instance, since you need to use AUC as the evaluation metric, you should convert the target(s) to binary (two classes). Also, you should recode any categorical variable(s) with no more than 5 classes.


