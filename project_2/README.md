# Project 2: Ames Housing Data and Kaggle Challenge

## Contents:
* Problem Statement
* EDA
* Preprocessing and Modeling
* Model Comparison
* Diving into Lasso Model
* Kaggle
* Conclusions and Recommendations

## Problem Statement
Being a personal assistant to an ultrarich family, my new task is to help them increase their vacation house value.
Hence, I've gathered data from 2006 to 2010 to determine which features can help to increase the house value.
Additionally, to advise on which features to avoid to prevent decreasing the house value.

## EDA
First step is to split the columns between numerical and categorical

### Diving into numerical columns

The numerical features with at least 50% correlation to saleprice

* Overall Qual
* Mas Vnr Area
* Total Bsmt SF
* 1st Flr SF
* Gr Liv Area
* Full Bath
* TotRms AbvGrd
* Garage Cars
* Garage Area
* SalePrice
* Age
* Remod Age

**Heatmap Plotting**

Features with high correlation with another features
Garage Cars - Garage Area = 0.9
Gr Liv Area - TotRms AbvGrd = 0.81
Total Bsmt SF - 1st Flr SF = 0.79

Diving into categorical columns
Have a basic overview of the categorical columns

**Boxplot plotting**

Based on the box plots, the following 6 features were extracted out due to the lack of variance in the feature itself to be deterministic:

* Utilities
* Lot Config
* Land Slope
* Bldg Type
* Roof Style
* Paved Drive

**Barchart plotting**

Bar chart will be plotted for the 6 features above to further investigate on the frequency in the features.

Since there are value with more than 50% of the distribution in the data, these features will not be deterministic.

The final number of features after doing EDA is 42.


## Preprocessing and Modeling

### Baseline Model
Baseline model used for this project is simply the mean.
RMSE = 77296.52524199558

### Linear regression model
Linear Regression R2 score for train set = 0.9210311522106592
Linear Regression R2 score for test set = 0.8967747047452289
RMSE = 3.993135068877397e+17

### Ridge Model
Linear Regression R2 score for train set = 0.9197730300942619
Linear Regression R2 score for test set = 0.9003549223225601
RMSE = 25990.10524928891

### Lasso Model
Linear Regression R2 score for train set = 0.9173230965842667
Linear Regression R2 score for test set = 0.90228759693215
RMSE = 25811.4265917059

### Model comparison
|        Model Type | Cross Val Score | Train |  Test |      RMSE |      α |
|------------------:|----------------:|------:|------:|----------:|-------:|
| Baseline          |      NA         | NA    | NA    | 7.729653e+04 |     NA |
| Linear Regression | -22856105640160602429063168.0 | 0.921031 |  0.896775| 3.993135e+17 |     NA |
|       Ridge Model |           0.892504 | 0.919773 | 0.900355 |  2.599011e+04 |  27.049597 |
|       Lasso Model |           0.894031 | 0.917323 | 0.902288 |  2.581143e+04 | 186.492609 |

**Observations from the comparison above:**
* Cross Validation Score for Lasso is slightly better compared to Ridge.
* Lasso test score is slightly better compared to Ridge.
* The RMSE is lower for Lasso compared to Ridge as well.
* Using the RMSE, Lasso has performed way better compared to the baseline model.
* Based on the results above, Linear model oversimplifies. A linear model was used to plot on data that is non-linear. The R2 score is 0.89 due to the high number of features utilized in the modeling.
* The difference between Ridge and Lasso score is not huge. This is because the Ridge model reduce the coefficients of the features to near zero but never zero. While, Lasso assign a zero to features that are not useful for prediction
* Hence, Lasso Model performed best among the models and will be the chosen model

Diving into Lasso Model

After lasso modeling, there are 130 features left.


Top 3 features that are positively correlated with sale price

* Gr Liv Area, correlation = 25937.302896
* Total Bsmt SF, correlation = 12249.713710
* Overall Qual, correlation = 10621.941265


Top 3 features that are negatively correlated with sale price

* Exter Qual_TA, correlation = -12974.329643
* Kitchen Qual_TA, correlation = -12847.974994
* Kitchen Qual_Gd, correlation = -11624.083276


Top 3 Features with the greatest magnitude

* Gr Liv Area
* Exter Qual_TA
* Kitchen Qual_TA


## Conclusion and Recommendations
### Conclusion
With the findings above, the above ground living area square feet is the most important feature to increase the salesprice. Followed by the total basement square feet, then the overall quality (material and finish of the house).
* With 1 square feet increase in the ground living area, the sale price will increase by ~26,000.
* With 1 square feet increase in the total basement, the sale price will increase by 12,230.
* With 1 rating increase in the overall quality, the sale price will increase by 10,734.

On the contrary, the features that will reduce the sale price are kitchen quality, basement quality, age of the house and the quality of the material in the exterior.

### Recommendations
The recommendation is to sell the house as soon as possible once the appropriate enhancements to the house have been done.

The appropriate enhancements:

* Increase the ground living area
* Increase the basement square feet
* Improve on the material and finish of the house
* Improve the kitchen quality
* Improve on the basement quality