# machine-learning
# Electric Vehicle Population Analysis

This project analyzes the electric vehicle (EV) population data to understand trends and factors influencing EV adoption.

## Data

The source of the dataset used in this project kaggle kernels output vencerlanz09/electric-cars-eda-with-feature-engineering -p /path/to dest ("Electric_Vehicle_Population_Data.csv"). 

**Key Columns:**

*   `Electric Range`: The estimated range of the electric vehicle on a single charge.
*   `Base MSRP`: The Manufacturer's Suggested Retail Price of the vehicle.
*   `County`: The county where the vehicle is registered, used here as a proxy for geographic distribution and adoption.
*   `importance_score`: A calculated score based on 'Electric Range' and 'Base MSRP' (`Electric Range` * `Base MSRP`).
*   `predicted_ev_adoption_rate`: A calculated rate based on the proportion of vehicles in a given county relative to the total number of vehicles in the dataset.

## Analysis

The project performs the following analysis:

1.  **Importance Score Calculation:** An 'importance\_score' is calculated based on 'Electric Range' and 'Base MSRP' to understand the potential impact of these factors.
2.  **Predicted EV Adoption Rate:** A 'predicted\_ev\_adoption\_rate' is calculated for each county based on the distribution of EVs in the dataset.
3.  **Visualizations:** The project generates several visualizations to explore the data:
    *   Histogram of 'importance\_score' to visualize its distribution.
    *   Bar plot of 'predicted\_ev\_adoption\_rate' for the top 20 counties to show regional adoption trends.
    *   Scatter plot of 'importance\_score' vs. 'predicted\_ev\_adoption\_rate' to examine the relationship between these two metrics.

## Results and Insights

Based on the analysis, the following key results and insights were observed:

*   The 'importance\_score' distribution shows a wide range, indicating varying combinations of electric range and MSRP across different vehicles.
*   The bar plot of 'predicted\_ev\_adoption\_rate' by county highlights significant regional disparities in EV adoption. Certain counties show considerably higher adoption rates than others. 
*   The scatter plot of 'importance\_score' vs. 'predicted\_ev\_adoption\_rate' helps visualize any correlation between these two calculated metrics. Further analysis could explore this relationship in more detail.
*   The presence of many vehicles with a 'Base MSRP' of 0 in the dataset warrants further investigation, as this might impact the 'importance\_score' calculation.

## Code

The analysis is implemented in a Python script using libraries such as pandas, matplotlib, and seaborn. The script includes steps for data loading, data wrangling, and generating visualizations.

## Getting Started

1.  Ensure you have the "Electric\_Vehicle\_Population\_Data.csv" file in the same directory as the script.
2.  Run the Python script to perform the analysis and generate the plots.

## Dependencies

*   pandas
*   matplotlib
*   seaborn
*   numpy
*   geopandas
*   plotly
*   shapely
*   missingno
