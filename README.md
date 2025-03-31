# A-B-Testing-Analysis-Campaign-Performance-Evaluation

## Project Overview

### Objective

The purpose of this analysis is to assess how well the new marketing campaign performs compared to the existing one. By comparing the conversion rates— the percentage of people who make a purchase after clicking on the website—between the Test Group (new campaign) and the Control Group (existing campaign), we can determine whether the new campaign is more or less effective

### Key Metrics

#### Conversion Rate:
- This tells us how successful each campaign is. (Number of Purchases / Total Website clicks) × 100

#### Z-Score (How Big is the Difference?) This helps us measure the gap between the two campaigns.
- A higher Z-Score means a bigger difference between the campaigns.
- A low Z-Score means the difference might be small or due to chance.

#### P-Value (Is the Difference Real?) This tells us if the difference is just luck or a real trend.
- A p-value below 0.05 means the difference is significant, and we can trust it.
- A p-value above 0.05 means the difference could be random, and we can’t be sure.

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

### Control Group
![image](https://github.com/user-attachments/assets/7d8fdb4f-affa-417d-901a-a9f65d0b68e8)

General Campaign Performance
- Ad Spend: The average ad spend per campaign is $2,288, with campaigns reaching an average of 88,844 people.
- Website Clicks: On average, 5,321 people click on the ads, but engagement gradually drops through the conversion funnel.
- Purchases: The final conversion (purchase) is significantly lower, averaging 523 purchases per campaign.
- Key Issue: There is a large drop-off between website visits and actual purchases, indicating potential conversion inefficiencies.

  
### Test Group
![image](https://github.com/user-attachments/assets/02057fbf-0c31-4ac5-941f-cea987c42f7e)

General Campaign Performance (Test Campaign)
- Ad Spend: The average ad spend per campaign is $2,563, with campaigns reaching an average of 53,491 people.
- Website Clicks: On average, 6,032 people click on the ads, but this gradually drops through the conversion funnel.
- Purchases: The final conversion (purchase) is significantly lower, averaging 521 purchases per campaign.
- Key Issue: There is a large drop-off between website visits and actual purchases, indicating potential conversion inefficiencies


### A/B Testing Methodology

#### 1. Calculating the Conversion Rates

We compare how well each campaign gets people to make a purchase.
- Control Group Conversion Rate = (Purchases in Control / Website clicks in Control) * 100
- Test Group Conversion Rate = (Purchases in Test / Website clicks in Test) * 100

![image](https://github.com/user-attachments/assets/0ba999fb-8774-452e-9b47-900817c9d335)


#### 2. Computing the Pooled Proportion (p)

- Pooled proportion represents the overall conversion rate across both groups. 

![image](https://github.com/user-attachments/assets/23f4567a-2577-4f50-bcd7-e7f973fb19fb)


#### 3. Computing Standard Error (SE)

- We check how much the results might naturally fluctuate to ensure we’re making a fair comparison.

![image](https://github.com/user-attachments/assets/1f6724dd-54b9-4450-98bd-5957d2cc58f9)


#### 4. Computing Z-Score

We calculate a number (Z-Score) that tells us how big the difference is between the two campaigns.

A Z-Score of 11.84 means the difference is extremely large and unlikely to be random.

![image](https://github.com/user-attachments/assets/e6b576f2-eae0-496d-ada3-ed5377a1ba09)


#### 5. Calculating P-Value

We calculate a p-value to check if the difference happened by luck or if it’s a real pattern.

A p-value of 0 means this is not random—the new campaign truly performed worse.

![image](https://github.com/user-attachments/assets/9b68dab6-15eb-4469-8e07-e8bd2972bc6c)


## Interpretation of the A/B Test Results

### Conversion Rates:
- Control Group Conversion Rate = 10%
- Test Group Conversion Rate = 9%
The test group performed worse than the control group (by 1 percentage point).

### Z-Score (11.84):
- A Z-score of 11.84 means the difference between the two conversion rates is 11.84 standard deviations away from the mean of the distribution.
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
