## BostonHousePred

### Software And tools Requirements

1. [Github Account](https://github.com)
2. [VS Code IDE](https://code.visualstudio.com/)
3. [Heroku Account](https://id.heroku.com/login)
4. [GitCLI](https://git.com)

Create a new environment

```
python -m venv .venvpython -m venv .venv

```
### Relevant Information:

   Concerns housing values in suburbs of Boston.

### Number of Instances: 506

Number of Attributes: 13 continuous attributes (including "class" attribute "MEDV"), 1 binary-valued attribute.

### Attribute Information:

    1. CRIM      per capita crime rate by town
    2. ZN        proportion of residential land zoned for lots over 
                 25,000 sq.ft.
    3. INDUS     proportion of non-retail business acres per town
    4. CHAS      Charles River dummy variable (= 1 if tract bounds 
                 river; 0 otherwise)
    5. NOX       nitric oxides concentration (parts per 10 million)
    6. RM        average number of rooms per dwelling
    7. AGE       proportion of owner-occupied units built prior to 1940
    8. DIS       weighted distances to five Boston employment centres
    9. RAD       index of accessibility to radial highways
    10. TAX      full-value property-tax rate per $10,000
    11. PTRATIO  pupil-teacher ratio by town
    12. B        1000(Bk - 0.63)^2 where Bk is the proportion of blacks 
                 by town
    13. LSTAT    % lower status of the population
    14. Price     Median value of owner-occupied homes in $1000's

### Feature Observation:

The following behavioral trends are expected from the data:

* RM : The prices increase with increase in the average number of rooms among homes in the neighborhood. Larger homes have higher prices. 

* LSTAT : Lower the LSTAT, higher should be the prices in the neighborhood ie. a lower LTSAT indicates people with higher incomes in the neighborhood as compared to others. More affluent families tend to have more expensive homes.

* PTRATIO : Lower the studentt teacher ratio, higher the quality of education and therefore, the neighborhood would be more sought after and have a higher price.

## Conclusion :

* Linear Regression : RMSE= 4.638689926172821 
                       R^2 Score= 0.7112260057484932
                       Adjusted R^2 Score= 0.6840226584639308

* Decision Tree Regressor : RMSE= 4.331676471371284 
                            R^2 Score= 0.7481862629698195
                            Adjusted R^2 Score= 0.7244646790466865


* K Neighbors Regressor :   RMSE= 4.339935422755068
                            R^2 Score= 0.7472251108326438
                            Adjusted R^2 Score= 0.7234129835922406


* Gradient Boosting Regressor RMSE= 2.8917840102807286
                              R^2 Score= 0.8877725492628508
                              Adjusted R^2 Score= 0.8772003981064527

* Random Forest Regressor:  RMSE= 3.15182368679334
                            R^2 Score= 0.8666812527794711
                            Adjusted R^2 Score= 0.8541222403601458

Here we can clearly see that our Gradient Boosting Regressor model perform better (as it is giving lowest rmse and highest R^2 )