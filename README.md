# DATA 512 Project Part 1: Common Analysis

## About the Data

We use a total of 3 data sources and will be examining Cleaveland, Ohio specifically.   

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


The third dataset is the [mask usage by county](https://github.com/nytimes/covid-19-data/tree/master/mask-use) data from The New York Times. The attributes and their description is listed below:

| Attributes | Description |
| --- | --- |
| COUNTYFP | The county FIPS code |   
| NEVER | The estimated share of people in this county who would say never in response to the question “How often do you wear a mask in public when you expect to be within six feet of another person?”   
| RARELY | The estimated share of people in this county who would say rarely | 
| SOMETIMES | The estimated share of people in this county who would say sometimes | 
| FREQUENTLY | The estimated share of people in this county who would say frequently |  
| ALWAYS | The estimated share of people in this county who would say always |

## Attribution

## Licenses
Datasets used for this project is licensed under [MIT](LICENSE).

The COVID-19 data is licensed under [Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/legalcode).

As per [Q&A section](https://www.cdc.gov/Other/policies.html) in CDC, the second dataset is in the public domain and may be freely used or reproduced without obtaining copyright permission. 

According to the [linking and copyright information](https://www.bls.gov/bls/linksite.htm), the third dataset is in the public domain and is free to be used without specific permission but required to cite the U.S. Bureau of Labor Statistics as a source.
