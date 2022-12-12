# DATA 512 Project: COVID-19 and Mobility Analysis

## Project Goal
In Par 1 of this project, we want to answer the question "How did masking policies change the progression of confirmed COVID-19 cases from February 1, 2020 through October 1, 2021?"

To extend part 1,  we want to answer the question "How has the mask mandate affected mobility changes from February 2020 to October 2022?"

## About the Data

We use a total of 3 data sources and will be examining Cleaveland, Ohio (Cuyahoga County) specifically. 

```
County of interest: Cuyahoga, Ohio
Land area (km^2): 1,184.12
Land area (mi^2): 457.19
April 1, 2020 census: 1,264,817
July 1, 2021 estimates: 1,249,387
County seat: Cleaveland
FIPS: 39035
Lat: 41.424119
Long: -81.65918339
```

The first one is the [COVID-19](https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university?select=RAW_us_confirmed_cases.csv) data from John Hopkins University, which documents cumulative confirmed cases per county in the U.S since January 22nd, 2020. At the time of starting this project, data until October 29th, 2022 was used for the study. The original dataset contains attritbues listed below:

| Attributes | Description |
| --- | --- |
| Province_State | Name of the state|
| Admin2| Name of the county |
| UID | A unique identifier for each county|
| iso2| Two-letter country codes defined in ISO 3166-1|
| iso3 | Three-letter country codes defined in ISO 3166-1|
| code3| Standard country or region code for statistical use |
| FIPS | Federal Information Processing Standards code for the county |
| Country_Region| Name of the country for the region |
| Lat | Latitude of the region |
| Long| Longtitude of the region |
| Combined_Key| Indicate county, state, country |
| Dates| Cumulative number of confirmed cases for specific date |

The second dataset is the [mask mandates](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i) data from CDC. The attributes and their description is listed below:

| Attributes | Description |
| --- | --- |
| State_Tribe | Abbreviation of the state or the tribe|
| County_Name| Name of the county |
| FIPS_State | Federal Information Processing Standards for the state|
| FIPS_County| Federal Information Processing Standards for the county|
| date | Dates in the format of mm/dd/yy|
| order_code| Indicate if there is a order for mask policy|
| Face_Masks_Required_in_Public | A requirement for individuals operating in a personal capacity to wear masks 1) anywhere outside their homes or 2) both in retail businesses and in restaurants/food establishments. |
| Source_of_Action| Source where order was found |
| URL| URL of order language used to complete dataset|
| Citation|Citation for the order|

Data available from 4/10/20 to 8/15/21. This file is very large so it has been stored in a zip file and should be unzipped when used.

Note that where mask mandates are "N/A" is a time before mask mandates were recommended as a mitigation to Covid-19 spread.


The third dataset is the [mask usage by county](https://github.com/nytimes/covid-19-data/tree/master/mask-use) data from The New York Times. The attributes and their description is listed below:

| Attributes | Description |
| --- | --- |
| COUNTYFP | The county FIPS code |   
| NEVER | The estimated share of people in this county who would say never in response to the question “How often do you wear a mask in public when you expect to be within six feet of another person?”   
| RARELY | The estimated share of people in this county who would say rarely | 
| SOMETIMES | The estimated share of people in this county who would say sometimes | 
| FREQUENTLY | The estimated share of people in this county who would say frequently |  
| ALWAYS | The estimated share of people in this county who would say always |

Data obtained between July 2 and July 14, 2020.

The fourth data set is the [COVID-19 Mobility](https://www.google.com/covid19/mobility/) data from Google. The attributes used for the analysis and their description is listed below:

| Attributes | Description |
| --- | --- |
| country_region_code | the country region code |   
| country_region | the country name |   
| sub_region_1 | State Name | 
| sub_region_2 | County Name | 
| census_fips_code | Census FIPS code |  
| place_id | unique ID for the place |
| date | date reported | 
| retail_and_recreation_percent_change_from_baseline | percent change from baseline (January 2020) for retail and recreation locations | 
| grocery_and_pharmacy_percent_change_from_baseline | percent change from baseline (January 2020) for grocery and pharmacy locations |  
| parks_percent_change_from_baseline | percent change from baseline (January 2020) for park locations |
| transit_stations_percent_change_from_baseline | percent change from baseline (January 2020) for transit locations | 
| workplaces_percent_change_from_baseline | percent change from baseline (January 2020) for workplace locations |  
| residential_percent_change_from_baseline | percent change from baseline (January 2020) for residential locations |

Data obtained between February 1, 2020 and October 15, 2022.

## Project Structure

```
└── data-512-project
    ├── LICENSE
    ├── README.md
    ├── data
    │   ├── mask-use-by-county.csv
    │   ├── RAW_us_confirmed_cases.csv
    │   └── us_public_mask_mandate.zip
    ├── plots
    │   ├── daily_vs_total_cases.png
    │   └── infection_rate.png
    ├── submissions
    │   └── DATA 512 Project Part 1 Reflection.pdf
    └── src
        └──data-512-project-part1.ipynb

```

## Attribution

Charles Reinertson and Tharun Reddy suggested plotting change points for the change of infection rates using Facebook Prophet and the Ruptures library. Arik Shurygin and Charles Reinertson also showed how they preprocessed the data which greatly helped me get started with the project faster. I also got the idea to highlight the mask mandate period from Eli Corpron. I was also initially unclear about what to do for the derivative function of the change in rate of infection, but collaboration with Arik and Tharun cleared up the calculation for the rate of infection and they discussed how it would be best to apply a 7-day rolling/moving average to detect the infection rate more accurately.

## Licenses
Datasets used for this project is licensed under [MIT](LICENSE).

The COVID-19 data is licensed under [Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/legalcode).

As per [Q&A section](https://www.cdc.gov/Other/policies.html) in CDC, the second dataset is in the public domain and may be freely used or reproduced without obtaining copyright permission. 

According to the [linking and copyright information](https://www.bls.gov/bls/linksite.htm), the third dataset is in the public domain and is free to be used without specific permission but required to cite the U.S. Bureau of Labor Statistics as a source.
