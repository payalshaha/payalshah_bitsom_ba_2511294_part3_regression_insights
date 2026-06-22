
# Residual Analysis

## Methodology

Predicted monthly sales were calculated using the final multiple regression model.

Residuals were calculated as:

Residual = Actual Sales − Predicted Sales

Positive residuals indicate that actual sales exceeded model predictions.

Negative residuals indicate that actual sales were lower than model predictions.

---

## Largest Positive Residuals

| Store ID | Region | Actual Sales | Predicted Sales | Residual |
|-----------|-----------|-----------|-----------|-----------|
| STR-1017 | West  | 685379.08  | 841678.3 | 156299.3 |
| STR-1012 | West  | 595467.6   | 729696.7 | 134229.2 |
| STR-1023 | South | 627171.9   | 757388.6 | 130216.7 |
| STR-1009 | North | 641865.03  | 762488.8 | 120623.8 |
| STR-1077 | South | 538376     | 648422.3 | 110046.3 |

### Interpretation

These stores performed substantially better than predicted.

Possible explanations include:

- Exceptional local management
- Strong local demand
- Successful promotions not captured in the dataset
- Unique competitive advantages
- Seasonal factors not included in the model

The model may be missing variables that explain these unusually strong sales outcomes.

---

## Largest Negative Residuals

| Store ID | Region | Actual Sales | Predicted Sales | Residual |
|-----------|-----------|-----------|-----------|-----------|
| STR-1028 | East  | 713611.16  | 585781.3| -127829.9 |
| STR-1026 | East  | 625514.04   |522797.2 | -102716.8 |
| STR-1051 | East | 787715.51   | 687127.0 | -100588.5 |
| STR-1073 | East | 813316.71  | 718839.5 | -94477.2 |
| STR-1064 | South | 799046.94     | 706026.9 | -93019.9 |

### Interpretation

These stores performed substantially worse than predicted.

Possible explanations include:

- Local operational issues
- Staffing shortages
- Stockouts not fully reflected in inventory metrics
- Competitive pressure
- Economic or demographic factors not captured in the model

The model may be overestimating sales potential for these locations.

---

## Under-Prediction Analysis

Stores with large positive residuals indicate that the model is under-predicting sales performance.

This suggests that some factors driving success are not currently included in the model.

Examples may include:

- Local marketing campaigns
- Strong store leadership
- Favorable store location
- Repeat customer behavior

---

## Over-Prediction Analysis

Stores with large negative residuals indicate that the model is over-predicting sales performance.

This suggests that some negative influences are not captured by the model.

Examples may include:

- Local competition
- Operational inefficiencies
- Poor customer experience
- Temporary business disruptions

---

## Overall Conclusion

Most residuals are relatively small compared with total sales, indicating that the model fits the data reasonably well.

However, the presence of large positive and negative residuals suggests that additional variables may further improve predictive accuracy.

The model explains approximately 81.44% of variation in monthly sales, but it does not capture every factor influencing store performance.
