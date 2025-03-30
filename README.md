# A-B-Testing-Analysis-Campaign-Performance-Evaluation

## Project Overview

### Objective

The goal of this analysis is to evaluate the effectiveness of a new marketing campaign by comparing the conversion rates of a Test Group (new campaign) versus a Control Group (existing campaign). Using A/B testing methodology, we determine whether the new campaign performs significantly better or worse in terms of conversion rates.

### Key Metrics

- Conversion Rate = (Number of Conversions / Total Visitors) * 100

- Z-Score = Measures how many standard deviations the difference between the test and control groups is from zero.

- P-Value = Determines statistical significance of the results.

### Hypothesis 

- Null Hypothesis (H₀): The "Existing Campaign" strategy has a higher conversion rate compared to the "New Campaign" strategy.

- Alternative Hypothesis (H₁): The "New Campaign" strategy has a higher conversion rate compared to "Existing Campaign."


### Dataset Description

The dataset consists of two groups:

- Control Group: Users exposed to the existing campaign.

- Test Group: Users exposed to the new campaign.

Columns in the Dataset:

Campaign Name | Date | Spend (USD) | Impressions | Reach | Website Clicks | Searches | View Content | Add to Cart | Purchase |

### Data Preparation & Cleaning

Steps Taken:

- Checked for missing values and handled appropriately.

- Converted date format where necessary.

- Ensured numerical consistency in monetary values and conversion rates.

## Analysis

### Summary Statistics

- Control Group
![image](https://github.com/user-attachments/assets/7d8fdb4f-affa-417d-901a-a9f65d0b68e8)


- Test Group
![image](https://github.com/user-attachments/assets/02057fbf-0c31-4ac5-941f-cea987c42f7e)


### A/B Testing Methodology

#### 1. Calculating the Conversion Rates

- Control Group Conversion Rate = (Purchases in Control / Website clicks in Control) * 100
- Test Group Conversion Rate = (Purchases in Test / Website clicks in Test) * 100

![image](https://github.com/user-attachments/assets/0ba999fb-8774-452e-9b47-900817c9d335)


#### 2. Computing the Pooled Proportion (p)

- Pooled proportion represents the overall conversion rate across both groups. 

![image](https://github.com/user-attachments/assets/23f4567a-2577-4f50-bcd7-e7f973fb19fb)


#### 3. Computing Standard Error (SE)

- Measures variability in conversion rates.

![image](https://github.com/user-attachments/assets/1f6724dd-54b9-4450-98bd-5957d2cc58f9)


#### 4. Computing Z-Score

- Quantifies how many standard deviations the difference between conversion rates is from zero.

![image](https://github.com/user-attachments/assets/e6b576f2-eae0-496d-ada3-ed5377a1ba09)


#### 5. Calculating P-Value

- Indicates whether the results are statistically significant. 

![image](https://github.com/user-attachments/assets/9b68dab6-15eb-4469-8e07-e8bd2972bc6c)


## Interpretation of the A/B Test Results

### Conversion Rates:
- Control Group Conversion Rate = 10%
- Test Group Conversion Rate = 9%
The test group performed worse than the control group (by 1 percentage point).

### Z-Score (11.84):
- A Z-score of 11.84 means the difference between the two conversion rates is 11.84 standard deviations away from zero.
This is an extremely large Z-score, indicating a highly significant difference.

### P-Value (0):
- The p-value of 0 (or close to 0) means there is almost no chance that this difference happened due to random chance.

#### Decision: The new campaign negatively impacted conversion rates and should not be implemented. Therefore, we can confidently fail to reject the null hypothesis (which assumes that the existing campaign outperforms the new campaign).


## Conclusion & Business Recommendations

### Key Takeaways:
- The new campaign resulted in a lower conversion rate.
- The results are statistically significant.
- Sticking with the control campaign is the best decision.

### Next Steps:
- Investigate Possible Causes of lower conversion rates (e.g., ad design, messaging, targeting).
- Optimize the Test Group Strategy before re-running the campaign.
- Explore Alternative Campaign Variations for future testing.
