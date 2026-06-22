
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


# Model Comparison

## Overview

Three regression models were developed to understand the factors associated with monthly sales performance.

### Model 1: Simple Regression – Marketing Spend

**Dependent Variable:**

* monthly_sales

**Independent Variable:**

* marketing_spend

### Model 2: Simple Regression – Footfall

**Dependent Variable:**

* monthly_sales

**Independent Variable:**

* footfall

### Model 3: Multiple Regression

**Dependent Variable:**

* monthly_sales

**Independent Variables:**

* marketing_spend
* footfall
* inventory_availability_pct
* customer_rating
* North_Dummy
* South_Dummy
* West_Dummy

---

## Model Comparison Table

| Model               | Variables Used                                                                                             | R-Squared | Significant Variables                                                                           | Business Usefulness                                                                                    | Limitations                                                                               |
| ------------------- | ---------------------------------------------------------------------------------------------------------- | --------- | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------- |
| Simple Regression 1 | monthly_sales ~ marketing_spend                                                                            | 0.167     | marketing_spend (p < 0.05)                                                                      | Shows the relationship between marketing investment and sales                                          | Explains only 16.7% of sales variation and ignores other business factors                 |
| Simple Regression 2 | monthly_sales ~ footfall                                                                                   | 0.736     | footfall (p < 0.05)                                                                             | Strong predictor of sales and useful for understanding customer traffic impact                         | Does not account for marketing, inventory, customer satisfaction, or regional differences |
| Multiple Regression | monthly_sales ~ marketing_spend + footfall + inventory_availability_pct + customer_rating + region dummies | 0.814     | marketing_spend, footfall, inventory_availability_pct, customer_rating, South_Dummy, West_Dummy | Provides the most comprehensive explanation of sales performance and supports business decision-making | Cannot prove causation and may exclude external business factors                          |

---

## Comparison of Explanatory Power

The R-squared value increased substantially across the models.

* Marketing Spend Model: **0.167**
* Footfall Model: **0.736**
* Multiple Regression Model: **0.814**

The marketing spend model explains only 16.7% of variation in monthly sales and therefore has limited explanatory power when used alone.

The footfall model explains 73.6% of variation in sales and is a much stronger individual predictor.

The multiple regression model explains 81.4% of variation in sales, making it the strongest model overall because it incorporates multiple business drivers simultaneously.

---

## Significant Variables

The multiple regression model identified the following statistically significant variables:

* marketing_spend
* footfall
* inventory_availability_pct
* customer_rating
* South_Dummy
* West_Dummy

These variables had p-values below 0.05 and provide strong evidence of association with monthly sales.

The following variable was statistically weak:

* North_Dummy

Its p-value exceeded 0.05, suggesting limited evidence that North region stores perform differently from East region stores after controlling for other factors.

---

## Business Usefulness

### Marketing Spend Model

Useful for understanding the direct relationship between marketing investment and sales. However, it is too limited for strategic decision-making because many other factors influence sales.

### Footfall Model

Provides strong insight into the importance of customer traffic. This model can help leadership evaluate initiatives designed to increase store visits.

### Multiple Regression Model

Provides the most useful business insights because it evaluates multiple factors simultaneously. It identifies the strongest sales drivers and supports decisions regarding marketing investment, inventory management, customer experience, and regional strategy.

---

## Limitations

All regression models have limitations:

* Regression identifies association, not causation.
* External factors such as economic conditions, competitor actions, and local events are not included.
* Historical relationships may not remain constant in the future.
* Some important business variables may not be captured in the dataset.
* Regional differences may be influenced by factors not measured in the model.

---

## Final Model Selected

The Multiple Regression Model was selected as the final model because:

* It has the highest R-squared value (0.814).
* It includes multiple business drivers.
* It identifies statistically significant predictors.
* It provides the strongest support for business decision-making.
* It explains a much larger proportion of sales variation than either simple regression model.

Therefore, the multiple regression model is the preferred model for understanding and improving monthly sales performance.

# Model Equations

## Purpose

Regression analysis was performed to identify the business factors most strongly associated with monthly sales performance and to support data-driven decision-making.

Three regression models were developed and compared:

1. Simple Regression Model – Marketing Spend
2. Simple Regression Model – Footfall
3. Multiple Regression Model

---

# Simple Regression Model 1

## Monthly Sales vs Marketing Spend

### Regression Equation

Monthly Sales = 560,777.35 + 2.13 × Marketing Spend

### Coefficient Explanation

#### Intercept (560,777.35)

The intercept represents the estimated monthly sales when marketing spend is zero.

Although stores rarely operate without marketing activity, the intercept provides the baseline value from which the effect of marketing spend is measured.

#### Marketing Spend Coefficient (2.13)

For every additional ₹1 spent on marketing, monthly sales are expected to increase by approximately ₹2.13.

### Business Interpretation

The model suggests that marketing investment is positively associated with sales performance. Increased marketing activity may help attract customers and generate additional revenue.

---

# Simple Regression Model 2

## Monthly Sales vs Footfall

### Regression Equation

Monthly Sales = 446,410.58 + 35.68 × Footfall

### Coefficient Explanation

#### Intercept (446,410.58)

The intercept represents estimated monthly sales when customer footfall equals zero.

Since stores cannot realistically generate sales without customers, the intercept primarily serves a mathematical function within the regression model.

#### Footfall Coefficient (35.68)

Each additional customer visit is associated with approximately ₹35.68 higher monthly sales.

### Business Interpretation

Footfall is strongly associated with monthly sales. Stores that attract more visitors generally achieve higher revenue levels.

---

# Multiple Regression Model

## Regression Equation

Predicted Monthly Sales =

80,972.67

* 1.2023 × Marketing Spend

* 33.9843 × Footfall

* 2,886.73 × Inventory Availability %

* 11,024.99 × Customer Rating

* 8,667.12 × North_Dummy

* 21,972.42 × South_Dummy

* 17,042.83 × West_Dummy

---

# Coefficient Interpretation

## Intercept (80,972.67)

The intercept represents the estimated monthly sales when all independent variables equal zero.

Because stores do not realistically operate with zero marketing spend, zero customers, and zero inventory availability, the intercept has limited practical business meaning and mainly serves as a baseline value within the equation.

---

## Marketing Spend (1.2023)

For every additional ₹1 invested in marketing, monthly sales are expected to increase by approximately ₹1.20 while holding all other variables constant.

### Business Meaning

Marketing investment contributes positively to sales growth and remains an important driver of store performance.

---

## Footfall (33.9843)

Each additional customer visit is associated with approximately ₹33.98 higher monthly sales while holding all other variables constant.

### Business Meaning

Customer traffic is the strongest sales driver in the model. Increasing store visits is likely to have a significant impact on revenue.

---

## Inventory Availability Percentage (2,886.73)

A one percentage-point increase in inventory availability is associated with approximately ₹2,886.73 higher monthly sales.

### Business Meaning

Stores that maintain better stock availability are more likely to satisfy customer demand and avoid lost sales opportunities.

---

## Customer Rating (11,024.99)

A one-point increase in customer rating is associated with approximately ₹11,024.99 higher monthly sales.

### Business Meaning

Improved customer satisfaction appears to contribute positively to revenue through repeat purchases and stronger customer loyalty.

---

# Dummy Variables

## Why Dummy Variables Were Used

The variable **region** is categorical and cannot be used directly in a regression model.

Dummy variables were created to convert the categories into numerical values that can be analyzed statistically.

---

## Reference Category

The selected reference category is:

**East Region**

No dummy variable was created for East.

All regional comparisons are measured relative to East region stores.

---

## North_Dummy

### Coding

* North = 1
* Otherwise = 0

### Coefficient

8,667.12

### Interpretation

North region stores are estimated to generate approximately ₹8,667 higher monthly sales than East region stores, holding all other variables constant.

However, this variable was not statistically significant and should be interpreted cautiously.

---

## South_Dummy

### Coding

* South = 1
* Otherwise = 0

### Coefficient

21,972.42

### Interpretation

South region stores are estimated to generate approximately ₹21,972 higher monthly sales than East region stores, holding all other variables constant.

This relationship was statistically significant.

---

## West_Dummy

### Coding

* West = 1
* Otherwise = 0

### Coefficient

17,042.83

### Interpretation

West region stores are estimated to generate approximately ₹17,043 higher monthly sales than East region stores, holding all other variables constant.

This relationship was statistically significant.

---

# Final Model Selected

## Selected Model

Multiple Regression Model

---

## Reason for Selection

The multiple regression model was selected as the final model because it provided the strongest explanation of monthly sales performance.

### Advantages

* Highest R-squared value (81.44%)
* Includes multiple business drivers simultaneously
* Identifies statistically significant predictors
* Incorporates regional differences through dummy variables
* Produces more reliable business insights than simple regression models

### Key Drivers Identified

The strongest factors associated with higher monthly sales were:

1. Footfall
2. Inventory Availability
3. Customer Rating
4. Marketing Spend
5. South Region
6. West Region

---

# Conclusion

The final model indicates that monthly sales are influenced by a combination of customer traffic, marketing investment, inventory management, customer satisfaction, and regional factors.

Among all variables, footfall emerged as the strongest predictor of sales performance. Therefore, leadership should prioritize strategies that increase customer visits while maintaining strong inventory availability and customer experience standards.



The East region serves as the baseline category against which all other regions are compared.
