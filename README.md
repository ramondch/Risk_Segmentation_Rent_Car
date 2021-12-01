# Risk_Segmentation_Rent_Car
Analyzing the possible risks creating an algorithm to detect which segmentation suits better for the risks model

Nalisha Men | Ramon Denia Chavarri | Disha Saxena | Elias Theodoropoulos | Jan Philip Thoma

**Video Demo**: https://youtu.be/9hbsn3EJezg

**PythonAnywhere** 

# About
The project is to build a class to perform risk-based segmentation and test it for car loans’ customers based on given historical data of customer behavior. Customer Risk Segmentation for car loans aims to help a company to avoid delayed/unpaid car loans by making better program selection/approval based on identified customers' characteristics for risk profile.

# Pre-requisite
Before running the codes in the notebook, please **_install expelliarmusBANANA pacakge_**. 

nmenclass.py can be accessed by **_import pip install expelliarmusBANANA as nm_**

https://pypi.org/project/expelliarmusBANANA/


# Approach
A point to note is Risk based segmentation is different to a typical customer or market segmentation.

In this study, the logistic regression technique is used to predict the outcome of target variable, "BUCKET", which indicates the number of unpaid installements at this reporting date.

Objective (supervised)segmentation method,Chi-square Automatic Interaction Detector (CHAID), is applied, taking binary transfromed "BUCKET" as the basis for segmentation. Separate logistic regression models are created for separate segments and for the whole population, with GINI Coefficient on the probability of being "1" as the evaluation criteria. As the objective-based segments must have a higher degree spread between 1/0 for the target variable, a variance threshold of 0.1 is set in the method to further verify if a segmentation point identified by CHAID method is meaningful.
 

# Dataset AUTO_LOANS_DATA.csv

| Feature   | Details |
|  :----  |    :----         |
|Reporting date|Last working day in month|
|Account Number |Loan Identification Number|
| Customer ID| Customer Identification Number in Credit Agricole|
|Program Name| Name of program under car loans product|
|Loan Open Date | Date of opening the loan|
|Expected Close Date |The date at which the loan should be closed (end of tenor)|
|Original Booked amount | Loan Amount that the customer takes|
|Outstanding| Remaining amount of the loan that is not paid yet at this reporting date|
|Bucket|Number of unpaid installements at this reporting date|
|Sex |Customer's gender as per the national ID|
|Customer Open Date| Date of opening the relation with the customer (Can be before opening the loan)|
|Birth date |Customer's birth date as per the national ID|
|Profession|Customer's profession|
|Car Type|Car Brand|
