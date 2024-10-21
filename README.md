# Business Understanding
A company is expanding in to new industries to diversify its portfolio. Specifically, they are interested in purchasing and operating airplanes for commercial and private enterprises but do not know anything about the potential risks of aircraft. This analysis will aid in determining which aircraft are the lowest risk for the company to start this new business endeavor.

# Data Understanding
We will be using the  NTSB aviation accident database contains information from 1962 and later about civil aviation accidents and selected incidents within the United States, its territories and possessions, and in international waters.https://www.kaggle.com/datasets/khsamaha/aviation-accident-database-synopses/data

There are 31 columns and 88889 rows. These are some areas we'll consider cleaning or analyzing:
* Injury Severity gives us similar information to Total Fatal Injuries, Serious Injuries, Minor Injuries, and Uninjured. We may consider splitting Injury Severity so it just has the word classification and the number of injuries will be kept in the other columns.
* Unknown: There are values included in some columns like 'Unknown, UNK, and Unavailable that are the same thing as Nan. We will note this for later.
* Ensure data types are correct for each column.
*Ensure there are no duplicates and that value formatting is standardized.
*Drop columns that do not give us relevant information.

## Data Preparation
Here is a recap of the steps we took for data preparation:
* Changed Event Date to datetime format.
* Checked for duplicates.
* Checked for null values and decided to drop columns that contained over 30% null values.
* Dropped columns that we did not need for this particular analysis.
* Split Injury Severity column to only contain the first word since the exact number is contained in the other columns.
* Renamed columns to simplify analyses.
* Replaced variations of value Unknown with a standardized version.
* Limited data set to just USA.
* Split location into city and state columns.
* Create simplified Model column containing zero to three digits or letters of Model to contain larger groups of Models and give us the ability to drill down if needed.
* Created column with total number of passengers.
* Limited data to Airplanes with fewer than 20 passengers
* Limited data to exclude amateur-built airplanes
* Limited data to exclude entries from after the year 2000.
* Dropped Report Status column
* Dropped the rest of the null values.

# Exploratory Data Analysis

# Conclusion

## Limitations
* Limited to the United States.
* Limited to accidents reported in the the Aviation Accident Database & Synopses.
* This analysis excludes Amateur Built aircraft and incidents before the year 2000. Use the Aviation Accident Database & Synopses dataset. The NTSB aviation accident database contains information from 1962 and later about civil aviation accidents and selected incidents within the United States, its territories and possessions, and in international waters.
## Recommendations
### Engine
* It is not recommended to buy planes with less than two engines becuase it is smart to have a backup engine if one fails.
* Avoid reciprocating engines as they are associated with the most accidents.
### Make and Model
* Beech and Cessna are the makes of the airplanes with the most accidents.
* Specifically, the Beech-200, Cessna-550, and Beech-C90 are the private aircrafts with the most accidents.
## Next Steps
* The main source of data for this analysis was an accident database which is a specific set of information that is going to include “riskier” investments by the nature of the database. I recommend exploring other data points that will also inform this investment decision such as market share, reviews, awards, and data from outside the US. 
* To explore potential commercial aircraft investments, find a dataset that contains more information on commercial planes as this may yield more robust results in this category. Further research is required.
# Links
* More details on the analysis can be found here. https://github.com/hannahdallas/aviation_strategy
* The presentation can be found here.https://docs.google.com/presentation/d/1b_scnhp-Di3wnTscorX9necAMQr6c6b707tKXBXExGo/edit?usp=sharing
* The Tableau dashboard can be found  here https://public.tableau.com/views/StatsonCrashedAirplanes/StatsonCrashedPrivateAirplanes?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link.

```
├── code
│   ├── __init__.py
│   ├── data_preparation.py
│   ├── visualizations.py
│   └── eda_notebook.ipynb
├── data
├── images
├── __init__.py
├── README.md
├── presentation.pdf
└── notebook.ipynb
```
