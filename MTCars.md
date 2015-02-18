Covariates Prediction Accuracy Calculator
========================================================
author: kittiba
date: 17 February 2015


Some Background
========================================================

The application I built is doing a simple calculation for 
$R^2$ * 100 to get the Prediction Accuracy % for the 
covariate an user picks. 

- This uses the 'lm' method in r to predict 'MPG' (Miles per gallon) as outcome 
- It uses the covariate selection on the side panel. 

Data being used in this app is from MTCARS data set in r. 
All the covariates from this dataset are displayed for selection on the side
panel of the application.


Inputs and outputs
========================================================
There are two inputs
1. Desired prediction accuracy % - a reference value for comparision
2. You can select any one covariate (only) to have the app calculate the prediction accuracy for it. 

Outputs - Prediction accuracy desired is displayed. The prediction accuracy that was calculated by the app is displayed. 

For example, when 'cyl' was selected the following gets calculated


```r
round(summary(lm(mpg ~ cyl, data=mtcars))$r.squared*100,1) 
```

```
[1] 72.6
```

How can this app be helpful?
========================================================

I see the following uses for this application
- This is useful when one is trying to build a model (exploratory data analysis)
- This helps to know which covariate has how much significance in prediction.

What does the app not do today?
========================================================

Unfortunately the functionality is kept to a minimum where 
multiple covariates are not allowed at this time (maybe in Version 2.0).

Also the desired % that is being selected is only for reference and the 
application does not do a comparision automatically.

