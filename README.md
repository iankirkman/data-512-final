# data-512-final
## Influential Characteristics of Opinion: A Basic Income Study
Released by: Ian Kirkman ikirkman@uw.edu 11/9/2017

### Project Goal
The goal of this project is to gain insight into the characteristics of people with varying levels of support for basic income, and predict which factors may have the greatest influence on an individual's opinion of basic income.

### License Info
 - The content of this project directory is released under the [MIT license](LICENSE.md).

### Data Sources
The core dataset used capture demographic information and quantify opinion of Basic Income is the publicly available ([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)), qualitative survery data conducted by Dalia in April 2016. We have accessed the dataset from [Kaggle](https://www.kaggle.com/daliaresearch/basic-income-survey-european-dataset) and saved it to the project [DATA](/DATA/basic_income_dataset_dalia.csv) folder, along with the associated [documentation](/DATA/codebook_basicincome). 

The Dalia survey data includes basic income opinion responses and demographic (age, gender, education level, full-time employment status, urban/rural residence, and presence of children in household) data for nearly 10K individual respondents in 28 EU countries. 

As a supplement to the Dalia data, we will also explore economic and quality of life issues in each of the represented countries. Some publicly available datasets that have been preliminarily identified to assist in this endeavor include:
 - [IHME Global Burden of Disease Study 2016](http://ghdx.healthdata.org/gbd-2016)
 - [World Bank - World Development Indicators](https://www.kaggle.com/worldbank/world-development-indicators)
 - [World Bank - Youth Unemployment Rates](https://www.kaggle.com/sovannt/world-bank-youth-unemployment)
 - [World Happiness Report](https://www.kaggle.com/unsdsn/world-happiness)

### Methodology
We plan to make a first pass at the Dalia survery data with cluster analysis, grouping respondents into similar responses. From this analysis, we hope to determine which demographic features of the Dalia survey are the most indicative of the respondent's opinion.

We also hope to uncover clusters of countries that espouse similar views, most likely by using K-means analysis. For this portion of the analysis, we would summarize the response proportions for each country over all demographic data, and then group the countries by their response proportions. If there are strong dilineations by country or groups of countries, then we can further explore potential confounding factors within supplemental data on health/disease burden, economic indicators, and the happiness report.

Exploring additional datasets for confounding factors by country would likely take the shape of a regression model, with the response being a classification of opinion on basic income. Early steps may include using PCA to reduce dimensions and identify the most impactful features on the supplemental datasets. This stage of analysis would contribute to finding additional potentially impactful features not included in the Dalia survey, as well seeking to understand any trends uncovered in the early explorations via clustering. 

### Expected Results
We anticipate that we will identify some correlated features to opinion of basic income, including features of the Dalia survey as well as features on from the supplemental country data. 

From the Dalia survery data, we hypothesize that:
 - Younger people will view basic income more favorably. We anticipate this because younger people are planning for a longer future, and have earning potential at stake as automation is replacing jobs.
 - Urban-dwellers will view basic income more favorably. We anticipate this because urban dwelling tends to be more expensive, and workers are more likely involved in service economies than rural workers.
 - People with children in their household will view basic income more favorably than those without. We anticipate this because people with children are likely to be anticipating the future on the behalf of their children.
 
 From the supplemental data, we hypothesize that:
  - Healthier countries will have a more favorable view overall of basic income. We posit that countries that are healthier have successfully implemented social care programs.
  - Happier countries will have a more favorable view overall of basic income. We posit that happier countries are likely to have a culture of work/life balance that values life and social contributions beyond work.
  - Economically burdened countries will have a more negative view overall of basic income. While counterintuitive that economically burdened countries may seek relief, we anticipate that signs of struggle may indicate failed social programs and/or negative views/blaming for failures.

### Impact of Results
We are in period of rapidly changing economies, and basic income is likely to become a necessity within our lifetimes. (Some would argue that it already is). Tracking public opinion on the matter is not limited to the interest of government or politic, but to any constituent that is aware of what automation and globalization mean for our future. Shaping public opinion of basic income will be a key component of making that transition as smooth as politically possible, while continuing to measure and predict that opinion will inform when success of implementation is feasible. 
