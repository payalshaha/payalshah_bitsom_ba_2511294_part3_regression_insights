
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
