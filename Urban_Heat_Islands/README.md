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

1. **City-Level Influence**: The `city` feature is the most important factor, indicating that UHI effects vary significantly by city. Urban areas have unique characteristics like population density, building materials, and infrastructure that affect heat retention and distribution.

2. **Local Climate Factors**: Features such as `avg_lst_c` (Average Land Surface Temperature), `evergreen_forest_pct`, `day_length_sec`, and `max_air_temp_c` are highly influential in determining UHI. High land surface temperatures, reduced vegetation cover, and increased solar radiation exposure all contribute to elevated heat levels in urban areas.

3. **Vegetation and Land Cover**: The percentage of evergreen and deciduous forest cover, along with other vegetation types (e.g., `shrub_scrub_pct`), plays a crucial role in mitigating UHI effects. Areas with more vegetation tend to have lower UHI effects due to evapotranspiration and shade provided by plants.

4. **Wind and Atmospheric Conditions**: Factors like `wind_speed_kmh`, `wind_dir_degrees`, and `atm_pressure_hpa` also influence UHI intensity. Wind can disperse heat, while atmospheric pressure can affect local weather patterns, influencing temperature distribution.

5. **Built Environment**: Developed land features, such as `developed_open_space_pct` and `percent_impervious`, are also significant, reflecting how the built environment (e.g., buildings, roads) retains and radiates heat, exacerbating UHI.

In summary, urban heat islands are influenced by a combination of urban characteristics (e.g., building density, land use) and local climate factors (e.g., vegetation cover, temperature, wind). The presence of vegetation, local climate conditions, and city-specific infrastructure all contribute to how heat is retained and distributed within urban areas.


#### Next steps
What suggestions do you have for next steps?

#### Outline of project

- [Data Preparation](https://github.com/dashao/mlai/blob/main/Urban_Heat_Islands/1_uhi_data_preparation.ipynb)
- [Data Exploration](https://github.com/dashao/mlai/blob/main/Urban_Heat_Islands/2_uhi_data_exploration.ipynb)
- [Modeling](https://github.com/dashao/mlai/blob/main/Urban_Heat_Islands/3_uhi_modeling.ipynb)


##### Contact and Further Information
[Email](mailto:oskomova@gmail.com)