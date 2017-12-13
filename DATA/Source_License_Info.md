This file contains location and license info for all data utilized in the root project.

### Dalia Basic Income Data:
Raw [Basic Income Survey (2016)](/DATA/Dalia/basic_income_dataset_dalia.csv) data and [documentation](/DATA/Dalia/codebook_basicincome.pdf) codebook were accessed from [Kaggle](https://www.kaggle.com/daliaresearch/basic-income-survey-european-dataset), under the publicly available creative commons license [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).


### World Bank Youth Unemployment Rate Data:
The [Youth Unemployment Rate](/DATA/worldbank_API_ILO_country_YU.csv) data was accessed form [Kaggle](https://www.kaggle.com/sovannt/world-bank-youth-unemployment) and is released under the World Bank's [Open License](https://data.worldbank.org/summary-terms-of-use).


### Sustainable Development Solutions Network World Happiness Report Data: 
The [World Happiness Report](/DATA/world_happiness_2016.csv) data was accessed from [Kaggle](https://www.kaggle.com/unsdsn/world-happiness) and is released under [CC0: Public Domain](https://creativecommons.org/publicdomain/zero/1.0/).


### Global Health Data Exchange (GHDx) Data:
IHME's [Population Estimate](/DATA/GHDx/IHME_GBD_2016_POP_ESTIMATES/) data, [Socio-Demographic Index](/DATA/GHDx/IHME_GBD_2016_SDI_0/) data, and [Retrospective Health Spending](/DATA/GHDx/IHME_RETROSPECTIVE_HEALTH_SPENDING_1995_2014/) data were all accessed directly from the [Global Health Data Exchange](http://ghdx.healthdata.org), under the linked [terms and conditions](http://www.healthdata.org/about/terms-and-conditions). 

Unused datasets (such as those representing historical year ranges) in each source folder were excluded from the github upload. However, all codebook and readme files were included from the original source. 

The Socio-Demographic Index dataset was converted from xlsx to csv format, using the export feature in Excel 2013.

To allow for upload to github, the size of the Population Estimates dataset was manually restricted by limiting to only years 2014-2016. This restriction was done in Excel 2013 via Data > Filter > year_id > select [2014, 2015, 2016]. The restricted csv was saved under the same naming convention as the original dataset, with the 2014 replacing the start year.

All GHDx datasets are publicly available under the [Open Data Commons Attribution License](https://opendatacommons.org/licenses/by/summary).

### DataHub Country Codes:
The [Country Code](/DATA/country_codes_datahub.json) json file was accessed from [datahub](https://datahub.io/core/country-list), and is released under the [Public Domain Dedication and License](https://opendatacommons.org/licenses/pddl/summary). 


