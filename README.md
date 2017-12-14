# data-512-final
## Influential Characteristics of Opinion: A Basic Income Study
Released by: Ian Kirkman ikirkman@uw.edu 11/9/2017

## Project Goal
The goal of this project is to gain insight into the characteristics of people with varying levels of support for basic income, and predict which factors may have the greatest influence on an individual's opinion of basic income.

## License Info
 - The content of this project directory is released under the [MIT license](LICENSE.md).

## Data Sources
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


## Methodology
Aggregate Dalia data was analyzed by voter versus non, and support versus opposed among voters. Aggregate data was analyzed by both demographic and opinion data. Ultimately, we used scikit-learn's kbest fit with an f_classif classifyer for categorical data to identify most impactful features.

We then calculated population weights for the Dalia data from the GHDx Population Estimates, and joined a country proportion of support with other country index metrics described in the data section below. We applied k-means with k=2 to group countries by similar features, and concluded that support for basic income was inversely responding to other country-level social service metrics.

See jupyter notebook for full methodology details.

## Expected Results
We anticipate that we will identify some correlated features to opinion of basic income, including features of the Dalia survey as well as features on from the supplemental country data. 

From the Dalia survery data, we hypothesize that:
 - Younger people will view basic income more favorably. We anticipate this because younger people are planning for a longer future, and have earning potential at stake as automation is replacing jobs.
 - Urban-dwellers will view basic income more favorably. We anticipate this because urban dwelling tends to be more expensive, and workers are more likely involved in service economies than rural workers.
 - People with children in their household will view basic income more favorably than those without. We anticipate this because people with children are likely to be anticipating the future on the behalf of their children.
 
 From the supplemental data, we hypothesize that:
  - Healthier countries will have a more favorable view overall of basic income. We posit that countries that are healthier have successfully implemented social care programs.
  - Happier countries will have a more favorable view overall of basic income. We posit that happier countries are likely to have a culture of work/life balance that values life and social contributions beyond work.
  - Economically burdened countries will have a more negative view overall of basic income. While counterintuitive that economically burdened countries may seek relief, we anticipate that signs of struggle may indicate failed social programs and/or negative views/blaming for failures.

## Impact of Results
We are in period of rapidly changing economies, and basic income is likely to become a necessity within our lifetimes. (Some would argue that it already is). Tracking public opinion on the matter is not limited to the interest of government or politic, but to any constituent that is aware of what automation and globalization mean for our future. Shaping public opinion of basic income will be a key component of making that transition as smooth as politically possible, while continuing to measure and predict that opinion will inform when success of implementation is feasible. 
