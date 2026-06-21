
# Dummy Variable Approach

The dataset contains categorical variables that cannot be used directly in regression analysis. To incorporate categorical information into the regression model, dummy variables were created.

## Region Dummy Variables

The variable **region** contains four categories:

* East
* North
* South
* West

To avoid the dummy variable trap, one category was selected as the reference category.

### Reference Category

East

### Dummy Variables Created

* North_Dummy
* South_Dummy
* West_Dummy

Coding approach:

| Region | North_Dummy | South_Dummy | West_Dummy |
| ------ | ----------- | ----------- | ---------- |
| East   | 0           | 0           | 0          |
| North  | 1           | 0           | 0          |
| South  | 0           | 1           | 0          |
| West   | 0           | 0           | 1          |

## Interpretation

The coefficient of each dummy variable represents the expected difference in monthly sales compared with stores located in the East region while holding other variables constant.

For example:

* A positive coefficient for North_Dummy indicates that North region stores are associated with higher monthly sales than East region stores.
* A negative coefficient indicates lower monthly sales compared with East region stores.

The East region serves as the baseline category against which all other regions are compared.
