# Coupon Acceptance Analysis

## Problem Statement

This project aims to analyze factors influencing the acceptance of different types of coupons (restaurants, coffee houses, bars, etc.) by drivers and various contextual attributes such as weather, time, and passenger type.

Please use the following notebook to go through the analysis: https://github.com/dashao/mlai/blob/main/customer_coupon/coupon_analysis.ipynb

## Key Findings

### Bar Coupon Analysis

1. Drivers who visit bars more frequently are more likely to accept bar coupons &rarr;  
**Target frequent bar-goers: Focus marketing efforts on individuals who visit bars more than once a month.**

2. Age plays a role in coupon acceptance &rarr;  
**Tailor campaigns to younger audiences: Drivers under 30 are particularly receptive to bar coupons.**

3. Passengers influence coupon acceptance &rarr;  
**Leverage social influence: Promote coupons when drivers have friends as passengers**

4. Marital status and parenthood affect acceptance rates &rarr;  
**Segment by lifestyle: Create separate strategies for single, young adults versus older, married individuals with children.**
   

### Carry Out & Take Away Coupon Analysis

1. Education level and destination significantly impact carry out coupon acceptance rates &rarr;  
**Target carry out coupon campaigns towards individuals with some high school education and associate degree holders, particularly when they are heading home or to work. Use marketing channels frequented by these demographics.**

2. Coupon acceptance rates vary by occupation and time of day &rarr;  
**Schedule coupon distributions at specific times to align with the peak acceptance periods for various occupations:**
   - 7am: Focus on service industry workers starting their day.
   - 10am: Target manual labor workers.
   - 2pm: Offer coupons to manual labor, service, transportation, and retired workers.
   - 6pm: Expand offers to include professional workers along with manual labor, service, and transportation workers.
   - 10pm: Prioritize service occupations and manual labor workers.

3.	Coupon expiration time influences acceptance rates, with one-day coupons generally more popular &rarr;  
**Implement longer expiration periods (one day) for carry out coupons to increase acceptance rates. This approach appeals to both frequent and infrequent bar visitors. Use two-hour expiration coupons strategically for infrequent bar visitors.**


## Next Steps and Recommendations

1. Investigate the impact of coupon expiration time on acceptance rates.
2. Analyze the effect of distance to the venue on coupon acceptance.
3. Develop a machine learning model to predict coupon acceptance based on user and contextual attributes.
4. Design and implement A/B tests to validate the effectiveness of targeted marketing strategies based on these findings.





