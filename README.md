# Amex Dataset Analysis

## Overview

This project analyzes the Amex dataset, focusing on default prediction based on various financial and risk factors. The dataset contains information about different financial metrics, credit risk scores, acquisition channels, and default indicators for each customer.

## Dataset Description

The dataset consists of **61 columns** and **62,484 rows**. It includes various fields such as:

- **unique_identifier**: A unique ID for each record.
- **appl_month**: Month of application.
- **prod_name**: Product name associated with the customer.
- **acq_channel**: Acquisition channel of the customer.
- **state_code**: The state in which the customer resides.
- **bureau_score**: Credit score provided by the bureau.
- **risk_scores**: A series of risk scores (1 to 11) that estimate the probability of default.
- **limit**: Credit limit.
- **income**: Reported income.
- **default_ind**: Indicator of whether the customer defaulted (1) or not (0).

There are some missing values in columns like `trust_identity` and `addr_mismatch` which were filled appropriately to avoid data loss.

## Steps in Analysis

1. **Data Cleaning**:
   - Missing values in categorical columns like `trust_identity` and `addr_mismatch` were filled with 'Unknown'.
   - For numerical columns, missing values were filled with the column's median.
2. **Exploratory Data Analysis (EDA)**:
   - Several key visualizations were generated to extract insights, including distribution plots, bar plots, and box plots.

## Visualizations and Insights

1. Distribution of Default Indicator: A count plot of default cases shows that the majority of the samples are non-default cases.
2. Risk Score 1 Distribution for Default and Non-Default: Higher risk scores tend to be associated with default cases.
3. Income Distribution for Default and Non-Default: There is no significant difference in income distribution between default and non-default cases.
4. Acquisition Channel vs Default Rate: Certain acquisition channels have a higher default rate, indicating a possible risk factor based on acquisition sources.
5. Product Name vs Default Rate: Some products exhibit higher default rates, suggesting that product type could be an important factor in assessing default risk.
6. Default rates vary significantly by state, which could be due to regional economic factors.
7. Limit Distribution for Default and Non-Default: Lower credit limits are more associated with default cases.
8. Bureau Score vs Default Indicator: Bureau scores are generally lower for customers who defaulted.
9. Risk Score 2 vs Default Indicator: Higher values in `risk_score_2` are associated with an increased likelihood of default.
10. Address Mismatch Distribution for Default and Non-Default: Address mismatches are slightly more frequent in default cases, which could indicate instability or fraud.

## Conclusion

This analysis provides valuable insights into the risk factors contributing to default in the Amex dataset. By exploring various financial and risk-based metrics, we can identify patterns and trends that help predict defaults. The analysis suggests that certain products, acquisition channels, and risk scores are strong indicators of default risk.

## Files

- **amex_data_analysis.ipynb**: Jupyter Notebook containing the full analysis and visualizations.
- **datadet.csv**: Original dataset file.

## Requirements

- Python 3.x
- Pandas
- Seaborn
- Matplotlib
