# Wildfire_Prediction_Model
For more information on the project and method procedures, refer to the ArcGIS StoryMap website: https://storymaps.arcgis.com/stories/f53d780418ad4cc6bb2386db05165ed4
## Repository Information
This repository contains four Jupyter notebooks:
1. **Combining_Wildfire_Climate_Data.ipynb**: This notebook process and merges wildfire and climate data. The climate data is a daily summary of the average temperature (TAVG), average wind speed (AWND), and precipitation (PRCP) within each county.
2. **Decision Tree Modeling.ipynb**: This notebook creates a decision tree model of different conditions (one-variable, two-variable, etc.) and comapares it with a random classification model. A hypothesis test is applied to see if all the decision tree models have a significantly higher accuracy versus the random classification model.
3. **Random Forest Modeling.ipynb**: This notebook creates a random forest model and compares it with a random classification model (dummy classifier). A hypothesis test is applied to see if the random forest model has a significantly higher accuracy versus the random classification model.
4. **Wildfire_Dataset_Variable_Methods.ipynb**: Contains data processing and visualization instructions regarding adding variables to our wildfire dataset.

This repository contains the following visualization attachments:
1. **V4_WDF_OFFICIAL.csv**: This CSV file is the cleaned and processed database already provided. If you want to skip to the decision tree and random forest modeling, ignore the Combining_Wildfire_Climate_Data notebook.
2. **ML_Model_Tables.pdf**: Contains two readable tables. One table is the scikt-learn parameters applied in our code. The other table is the accuracy and p-values for each tested model.
3. **dt_all.png**: Graphviz image of a decision tree that factors in all our variables (AWND, PRCP, TAVG, DURING_A_DROUGHT, WATERSHD, POP_BY_COUNTY). Max depth of tree is 6.
4. **dt_awnd.png**: Graphviz image of a decision tree that factors in only AWND. Max depth of tree is 3.
5. **dt_climate_all.png**: Graphviz image of a decision tree that factors in our climate variables (AWND, PRCP, TAVG). Max depth of tree is 1.
6. **dt_pop_by_county.png**: Graphviz image of a decision tree that factors in only POP_BY_COUNTY. Max depth of tree is 13.
***
## Datasets
### Dataset #1: Spatial Wildfire Occurrence Data for the United States, 1992-2015 [FPA_FOD_20170508] (4th Edition)
This data publication contains a spatial database of wildfires that occurred in the United States from 1992 to 2015.<br>
**Project Goal**: Extracted Southern California wildfires from 2000-2015.<br>
**Source**: [USDA](https://www.fs.usda.gov/rds/archive/catalog/RDS-2013-0009.4)
### Dataset #2: Cal Fire Incident Archive
CAL FIRE contains an archive of wildfire incidents from 2013. <br>
**Project Goal**: Extracted Southern California wildfires from 2016-September 2020.<br>
**Source**: [CAL FIRE](https://www.fire.ca.gov/incidents/)
### Dataset #3: Climate Data Online Search (Daily Summaries)
Contains climate summaries for the average temperature (TAVG), average wind speed (AWNG), and precipitation (PRCP).<br>
**Project Goal**: Extracted daily climate summaries from 2000-September 2020.<br>
**Source**: [NOAA](https://www.ncdc.noaa.gov/cdo-web/search)
### Dataset #4: Population By County
Population by counties were collected from the census.<br>
**Project Goal**: Acquired the population data and appended it our wildfire database.<br>
**Source**: [U.S. Census Bureau](https://www.census.gov/data/)
### Dataset #5: California High Hazard Zones (Tier 2)
Tier Two High Hazard Zones are based on watersheds and represent areas for forest health restoration and fire planning.<br>
**Project Goal**: Extracted watershed data in Southern California using ArcGIS Pro's intersection tool.<br>
**Source**: [CAL Fire](https://www.arcgis.com/home/item.html?id=e50b7577426c4367a518b80b38e9b5d8)
### Dataset #6: Weeks In Drought
The Consecutive Drought Dataset for California was collected from the National Drought Mitigation Center in the form of a CSV file.<br>
**Project Goal**: Extracted the counties in our study area and confirmed which wildfires occurred during a drought.<br>
**Source**: [NDMC](https://droughtmonitor.unl.edu/Data/DataDownload/WeeksInDrought.aspx)

**Note**: Watershed, drought, and population data was appended to our merged wildfire and climate database using Microsoft Access. Refer to Wildfire_Dataset_Variable_Methods.ipynb for further instructions on this data processing step.
