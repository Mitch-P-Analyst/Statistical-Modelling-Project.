# Final-Project-Statistical-Modelling-with-Python

## CityBike Lisbon: Location Data Modelling with Python

### Project
This project explores relationships between bike availability at Lisbon’s CityBike stations and characteristics of surrounding locations/Points of interst, such as bars, cafes, restaurants. 

This process was completed using APIs of CityBike and Foursquare.

### Goals
- Identify predictor variables that influence bike availability at Lisbon CityBike stations.
- Visualise trends between station-level bike availability and surrounding locations
- Use multivariate regression analysis to determine the significance of nearby business categories types, buisness ratings and popularity.

# Process
## Step 1 
- city_bikes.ipynb

- Acquired CityBike Data from CityBike API
    - Resulting 195 bike station coordiantes
- Parsing JSON File data into Dataframes for cleaning

## Step 2
- yelp_foursquare_EDA.ipynb

- Acquired organisation/location data from FOURSQAURE APIs within 1,000metres of BikeStations 
    - Data parameters included;
        - Organisation Name,
        - Distance From CityBike Station,
        - Organisation Category,
        - Rating,
        - Popularity,
        - Hours, Hours Popular,
        - Price
    
    - 9,662 Locations/Organisations within 1,000 metres radii of BikeStations
        - Grouped by Bike Station, visualisation methods performed for cleaning, aggregation and modelling

- **Issue** Unable to access YELP API without Business Contact
    - **YELP API Step Ignored**

### SQL Database
- Created SQL Database for future access
    - Created, linked and stored data in normalised tables

## Step 3
- Exploratory Data Analysis
    - Conducted visual inspections with seaborn/matplotlib pairplots
        - Observed null or weak visual relatonships 
    - Generated Pearson R correlations for proposed linear relationships & variance inflation factor values for Multicollinearity
    - Observed weak linear correlations between x-variables and y-variables (free_bikes, total_slots)

## Step 4
- Statistical Modelling
    - Mulivariate Regression Models 
        - Dependent Variables
            - Free Bikes
            - Total Bike Slots
        - Full model with all business categories
        - Refined model using only top independent variables
            - bar_count 
            - cafe_counts
        - Adjusted R² improved in simplified model

    - Linear Regression Models
        - Independent Variable
            - Average Popularity of locations
        - Dependent Variables
            - Free Bikes
            - Total Bike Slots
        - Strong correlations
            - Statistically Insignificant
            - Maximum of 1.3% explanatory power on the variability of dependent variables

        
        
## Results
(fill in what you found about the comparative quality of API coverage in your chosen area and the results of your model.)
Results:




## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)

