# Turning Data Into Information: Evaluating Reimbursements #

## Summary of our Project and Findings ##

### The Data ###

Our project team examined a data set of three month's worth of reimbursement claim denials. Below is a quick description of our data set:
- Over 56k rows
- 20 features
- pre-labeled binary outcomes
- balanced sample with ~60/40 split between the two outcomes

### The Classifier Model ###

Each reimbursement denial was ultimately resubmitted for payment, or written off. 
Our team found that we could create a relatively strong Random Forest Classifier model (94% weighted average accuracy) predicting whether a claim would be written off or resubmitted. 

![](https://github.com/alexgwise/project_3/blob/main/Resources/model%203%20confusion%20matrix.PNG)

After three iterations, we created a parsimonious model that relied on a fraction of the original data features. The great thing about the final set of features was that all data points were available at the time of the denial, and did not have to be added as part of the resubmission or write off reconciliation step. This means that samples can be evaluated for potential resubmission in near real time.

![](https://github.com/alexgwise/project_3/blob/main/Resources/model%203%20top%20features.PNG)

92% recall accuracy may not be a high enough threshold for management on write off determination, but the 96% precision score for resubmitting has the potential to greatly speed up the time spent in resubmitting a reimbursement denial. 

**Our data showed an average of 35 days was spent before a resubmission was performed. Our classifier model could be used on a daily basis to identify which claims are predicted to be resubmitted, greatly reducing the time to collect. In the Q4 data set, that would result in working capital savings on $3.9M in resubmissions!**

### Visualizations ###

In addition, we created several visuals that allow the user to examine the data set through a number of lenses including, region, days to resolve, write off vs. resubmission, manufacturer data, customer data, and denial reason. These plots should aid the management team in knowing which contracts and manufacturers are causing the largest impacts to their business, so targeted actions and follow up conversations can take place. Below are a few examples

![](https://github.com/alexgwise/project_3/blob/main/Images/Manufacturer_Writeoff.png)

![](https://github.com/alexgwise/project_3/blob/main/Images/Contract_Plot.png)

![](https://github.com/alexgwise/project_3/blob/main/Images/Number_of_Days_to_Resolve.png)

***We're proud of using the principles and techniques we have learned in school to a real world problem, that leads to meaningful action. Thank you for your interest in our project!***

## Day 1 ##

**Our Dataset**

- Our team will use data representing McKesson's Q4 2020 write off vs. collected reimbursement amounts
- The data has been updated to mask the true names of the manufacturers and customers involved
- The dataset has over 56k records which will lend itself well to machine learning, and is pre-labeled with the binary "write off" or "resubmit" results

**The Questions We Will Ask**

- Can we transform this raw data set into more user-friendly visuals? 
- Are there any patterns shown in the data set?
- Can SK Learn help us predict which customers, suppliers, contracts, or drugs have a higher write off rate? 


**The Python Packages We Will Use**

- Pandas
- Panel
- Pathlib
- Plotly Express
- SKLearn
- Pydotplus
- HVPlot
- Mapbox API
- Dot ENV

## Day 2 ##

- Classifier model tuned to use fewer features, while still maintaining acceptable accuracy
- Good start on visuals
- PowerPoint shell started

## Day 3 ##
- PowerPoint nearly complete
- 2nd iteration of random forest classifier model created
- Continued work on visuals

## Day 4 ##
- 3rd and final iteration of random forest classifier model created
- Added more visuals
- created dashboard tabs to organize visuals

## Day 5 ##
- Finalized code
- Finalized PowerPoint
- Practiced our presentation
