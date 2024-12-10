# Analyzing the Relationship Between Urban Heat Islands (UHIs) and Local Climate Factors

**Daria Oskomova**

## Executive summary


## Rationale
Urban Heat Islands (UHIs) are areas within urban environments that experience significantly higher temperatures than their surrounding rural areas. Figuring out what causes UHIs is important because it helps to address a range of interconnected challenges — public health, energy efficiency, environmental sustainability, etc.

## Research Question
How urbanization characteristics and specific local climate factors (such as vegetation cover, building density, land use, and proximity to water bodies) contribute to the Urban Heat Island (UHI) effect in different cities.

## Data Sources
1. Land Surface Temperature: [MODIS/Terra Land Surface Temperature/Emissivity Daily L3 Global 1 km SIN Grid](https://lpdaac.usgs.gov/products/mod11a1v061/)
2. Vegetation Index: [MODIS/Terra Vegetation Indices 16-Day L3 Global 1 km SIN Grid](https://lpdaac.usgs.gov/products/mod13a2v061/)
3. Meteo data on zip level: [DAYMET](https://daymet.ornl.gov/getdata)
4. Wind and atmosphere pressure: [Meteostat](http://meteostat.net/)
5. Zipcode geo shapefile: [US Census Bureau](https://www2.census.gov/geo/tiger/TIGER2024/ZCTA520/tl_2024_us_zcta520.zip)
6. Population density: [US Census Bureau](https://data.census.gov/table/DECENNIALDHC2020.P1?q=All%205-digit%20ZIP%20Code%20Tabulation%20Areas%20within%20United%20States%20Populations%20and%20People)
7. Land Cover and Fractional Impervious Surface: [Multi-Resolution Land Characteristics Consortium](https://www.mrlc.gov/data)

## Methodology
1. Modeling and hyperparameter tuning:
    - Classification models:
      - RandomForestClassifier
      - Support Vector Classifier (SVC)
      - K-Nearest Neighbors (KNeighborsClassifier)
    - GridSearchCV was used to optimize the hyperparameters for each model using cross-validation (CV). This technique helps find the best combination of hyperparameters by evaluating model performance across multiple folds.

3. Cross-validation and evaluation:
    - The models were trained using a cross-validation strategy (`cv=5`) to evaluate how well each model generalizes to unseen data.
    - The best models were further evaluated on the test data to generate classification metrics, including accuracy, precision, recall, f1-score, and confusion matrix.

4. Feature Importance Analysis:
    - For the RandomForest model, feature importance was calculated to determine which features contributed the most to the prediction of UHI.
    - The importance scores were plotted using Seaborn to provide a visual representation of the most influential features.

5. Decision Tree Visualization:
    - One of the decision trees from the RandomForest was visualized using Graphviz to provide insights into the model's decision-making process.
    - The tree structure was presented with key features at each split to show how different factors affect the UHI prediction.

## Results
Urbanization characteristics and specific local climate factors contribute significantly to the Urban Heat Island (UHI) effect in different cities:.

- Vegetation matters most. Areas with low greenery, measured by avg_ndvi, are much more likely to experience UHI. Trees and plants play a huge role in cooling urban areas.
- Urban development. High-density development (like big buildings and paved areas) is strongly linked to UHI. Open spaces with more grass and vegetation help reduce these effects.
- Hot surfaces. Land surface temperature (avg_lst_c) is a key indicator of how hot an area gets, especially in urban zones.
- Day length and weather. Longer days and calm weather (low wind speeds) can make UHI worse since there’s less opportunity for heat to dissipate.
- Forest cover. Forested areas, especially evergreen trees, are very effective at keeping temperatures lower.
- Features like rainfall, population density, and certain types of land cover (like farmland) don’t play as big of a role but still provide some context.

The findings emphasize the interplay of vegetation, urbanization, and climate in driving UHI effects. Urban planners and policymakers should focus on increasing vegetation, reducing impervious surfaces, and adopting sustainable designs to mitigate UHI, improving urban resilience to climate change.


## Next steps
1. **Model Deployment**:
   - Deploy the best-performing model (e.g., RandomForest) as a web service using frameworks like **Flask** or **FastAPI**. This will allow users to input relevant features and predict the likelihood of UHI occurrence in real-time.

2. **Model Monitoring and Maintenance**:
   - Implement a monitoring system to track the model's performance over time. Metrics like **accuracy**, **precision**, and **recall** should be tracked to identify any drift in model performance. Tools such as **MLflow** or **Prometheus** can be used for this purpose.

3. **Data Collection and Updating**:
   - Regularly update the dataset with new data to ensure the model remains accurate and relevant. New data will help the model adapt to changes in urbanization patterns, climate, and other contributing factors.

4. **Feature Engineering**:
   - Explore additional features that could improve the model, such as **building material types**, **surface albedo**, or **proximity to water bodies**. This may enhance the model's ability to accurately predict UHI.

5. **Explainability and User Interface**:
   - Develop an interactive dashboard using tools like **Dash** or **Tableau** to provide stakeholders with an easy-to-understand visual representation of the model's predictions and feature importances.

6. **Integration with Urban Planning Tools**:
   - Collaborate with urban planners to integrate the model with tools used in city planning to support decision-making related to green spaces, building density, and other urban design features that can mitigate UHI.

7. **Further Model Evaluation**:
   - Consider additional evaluation metrics like **ROC-AUC** or **PR-AUC**, particularly if the dataset is imbalanced. These metrics provide a more nuanced understanding of model performance beyond accuracy.

8. **Testing in Real-World Scenarios**:
   - Conduct pilot projects in collaboration with city authorities to apply the model's predictions in real-world scenarios. This could help validate the model's utility and gather insights for further improvement.

## Outline of project

- [Data Preparation](https://github.com/dashao/mlai/blob/main/Urban_Heat_Islands/1_uhi_data_preparation.ipynb)
- [Data Exploration](https://github.com/dashao/mlai/blob/main/Urban_Heat_Islands/2_uhi_data_exploration.ipynb)
- [Modeling](https://github.com/dashao/mlai/blob/main/Urban_Heat_Islands/3_uhi_modeling.ipynb)


### Contact and Further Information
[Email](mailto:oskomova@gmail.com)