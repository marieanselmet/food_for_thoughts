# Project P4 milestone

```project.ipynb``` is our final notebook.

```plots.ipynb``` is a notebook that produces our html plots with the plotly library.
## Data story can be found [here](https://sofiadandjee.github.io).

## HTML rendered Jupyter notebook can be found [here](https://nbviewer.jupyter.org/github/SofiaDandjee/food_for_thought/blob/main/project.ipynb).

## 1. Title: Food (and money) for thought


## 2. Abstract
Keeping a good and balanced diet is fundamental to having a healthy life as it helps avoiding food-related illnesses such as diabetes, obesity and cardiovascular diseases. However, the price of the food products influences greatly the decisions of individuals in purchasing them or not. There is a strong belief amongst consumers that more expensive products are healthier than cheaper ones, even this is not always true. Thus, we ask ourselves: do people have an equal chance in maintaining a nutritious diet and thus a healthy life?

Our goal is to provide insight on the food consumption discrepancies between different boroughs of Greater London. We explore the link between the economic situations of households and their food purchases. To measure the level of wealth in each area, we study the income and children poverty per borough provided by the London Datastore. We compare them to the nutritional properties of each borough’s typical product given in the Tesco Grocery 1.0 dataset. 


## 3. Research questions
- What is the average diet of a Londoner?
- What constitutes a healthy diet?
- What is the proportion of food related expenditure in each borough? How does it relate to its economic situation?
- How does a healthy diet relates to the borough's economic situation? Is this connection area-dependent?


## 4. Datasets used
- [Grocery purchases](https://figshare.com/articles/dataset/Area-level_grocery_purchases/7796666?backTo=/collections/Tesco_Grocery_1_0/4769354) from the Tesco Grocery 1.0 dataset presented in the paper:  aggregated information on food purchases, enriched with information coming from the census at the level of boroughs.
- [Prevalence of overweight and obese children](https://data.london.gov.uk/dataset/prevalence-childhood-obesity-borough) from the English National Health Service (NHS): fractions of overweight and obese primary school children in Reception class (aged 4 to 5) and year 6 (aged 10 to 11), sampled across wards in the 2013–2014 school year.
- [Prevalence of overweight and obese adults](https://data.london.gov.uk/dataset/obesity-adults) from the Active People Survey (APS): fractions of overweight 
and obese individuals among a statistical sample of borough residents in 2012
- [Diabetes prevalence](https://digital.nhs.uk/data-and-information/publications/statistical/quality-and-outcomes-framework-achievement-prevalence-and-exceptions-data/quality-and-outcomes-framework-qof-2016-17) from the English National Health Service (NHS): fraction of adults among those registered 
at a GP practice in England who are affected by type-2 diabetes. This data has been collected for year 2015 at ward level.
- [Earnings by Place of Residence](https://data.london.gov.uk/dataset/earnings-place-residence-borough): gross earnings of employees by place of residence. We only considered the full-time weekly earnings per borough in 2015.
- [Children poverty](https://data.london.gov.uk/dataset/children-poverty-borough): numbers and percentages of children in poverty for Borough and London Wards (at 31 August each year). We only took into accout the children (dependent children under the age of 20) in child benefit families per borough in 2015.
- [London Consumer Expenditure Estimates - Detailed Borough Base](https://data.london.gov.uk/dataset/london-consumer-expenditure-estimates-2011-2036): consumer expenditure data to 2036 broken down by London borough. We transformed the data concerning food expenditure in percentage of the total expenditure over the year 2015.
- [Statistical GIS Boundary Files for London](https://data.london.gov.uk/dataset/statistical-gis-boundary-files-london): geolocalization of London's areas. We used the boundaries of the boroughs as at 2011 for visualization purposes.


## 5. Methods
- Visualize the average diet of a Londoner.
- Compute a healthy diet score based on the nutritional properties of each borough’s typical product.
- Visualize the healthy diet score differences between areas.
- Compute and visualize the proportion of food related expenditure in each borough.
- Visualize the wealth differences between areas based on gross earnings and child poverty.
- Compute the Spearman rank correlation between the food health score and the earnings of employees, the percentage of children in poverty and the percentage of food expenditure. 
- Run a linear regression to predict the food health score from the highest correlated factors found previously and other control variables accounting for demographics and store penetration. If a high goodness of fit is obtained regarding the <i>R<sup>2</sup></i> coefficient, it will indicate that these economic factors are representative of the food diet quality. 


## 6. Timeline
- 27th of November - 4th of December: creative extension analysis
- 4th of December - 11th of December: creative extension analysis + individual update of the replication notebook 
- 11th of December - 18th of December: creative extension plots + data story
-18th of December - 23rd of December: video pitch


## 7. Organization within the team
- Marie: computing the health diet score + plotting the results + data story
- Sofia: wrangling the data + map visualization + data story
- Héloïse: computing the correlations and fitting the linear regressions + plotting the results + data story

## 8. Packages to install

```conda create --name ada_project
conda install -n ada_project pandas geopandas matplotlib plotly scikit-learn scipy seaborn pyshp shapely
conda install -n ada_project -c conda-forge descartes
conda install -n ada_project -c plotly plotly-geo
conda install -n ada_project xlrd
pip3 install jupyterlab "ipywidgets>=7.5"
jupyter labextension install jupyterlab-plotly@4.13.0
