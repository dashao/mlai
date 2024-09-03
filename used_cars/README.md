# Used Cars Price Analysis

## Problem Statement

This project aims to develop a predictive model to identify the key factors that drive the price of used cars. By analyzing a dataset of used cars, we aim to uncover the relationships between various attributes, such as make, model, year, mileage, condition, and other features, and their impact on car prices, ultimately informing data-driven recommendations for used car dealerships.

Please use the following notebook to go through the analysis: https://github.com/dashao/mlai/blob/main/used_cars/used_cars_analysis.ipynb

## Key Findings

1. Year of Manufacture. The most significant factor affecting used car prices is the year of manufacture. Vehicles manufactured after 2012 are generally priced higher than older models.

2. Odometer Reading. The odometer reading, or mileage, is another critical factor. Cars with lower mileage are typically priced higher, reflecting their lesser wear and tear.

3. Condition of the Car. Vehicle condition significantly impacts pricing. Cars in “excellent” or “good” condition fetch higher prices compared to those in “fair” or lower conditions.

4. Fuel Type and Cylinders. Cars with different fuel types and engine configurations (number of cylinders) show varied pricing. Diesel vehicles and those with more cylinders generally have different pricing patterns, influenced by fuel economy, engine performance, and market demand.



## Next Steps and Recommendations

1. Focus on acquiring vehicles that are newer (post-2012) and have lower mileage. These cars tend to command higher prices and are likely to sell quicker. Investing in well-maintained cars could result in better margins. 
2. Look at trends in fuel efficiency and consider vehicles that are economical or have lower environmental impact, as consumer preferences are shifting in this direction. 
3. Perform further analysis to segment the market based on region, fuel type, and specific models. This can help identify niche markets or regional preferences that could be lucrative.
4. Use the existing data to explore price elasticity within different segments, helping to set more competitive pricing strategies.
5. Ensure that all vehicle attributes are accurately recorded in the inventory management system. Missing data, as observed in the initial dataset, can lead to less precise pricing and inventory decisions.
6. Regularly update the decision tree model and other predictive models with new data to keep insights relevant and accurate.
7. Experiment with more advanced machine learning models, such as random forests or gradient boosting machines, which might capture more nuanced patterns in the data.