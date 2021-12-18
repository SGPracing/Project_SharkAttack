# Project Shark Attack #

## Data ##
Source: https://www.sharkattackfile.net/ <br />
Dataset: https://www.kaggle.com/teajay/global-shark-attacks (attacks.csv) <br />

## Objectives
#### Primary: ####
* to verify if there is an obvious trend in the number of attacks per year in the last 10 years of collected data; <br />
* to determine the top 10 most dangerous areas and activities; <br />

#### Secondary: ####
* to stablish the case fatality rate (CFR) for the top 10 activities (as a single variable) <br />

## Background ##
The dataset *attacks.csv* was sourced from the [**Shark Research Institute**](https://www.sharks.org/). The file contains extensive data, collected for centuries, about shark attacks in the entire World. The method of data collection is ignored, thus, inherent bias cannot be avoided. Moreover, there is significant data heterogeneity for most of the variables, in particular those necessary for the purpose of this study. 

## Methods ##
Targetted data cleaning and analysis was performed under *Python* and *Pandas*. The entire process was carefully worked in order to allow statistical analysis as accurate as possible.

## Results ##

#### **Trend of attacks throughout the last 10 years** ####
The analysis was initially made for the period from 2009 to 2018. However, the number of attacks computed in 2018 significant lower compared to the previous 9 years. The cause of this extreme variation was due by the fact that in 2018 the data has been collected only for the first six months (from January to June). The analysis was then readjusted to reject data from 2018 and to add those from 2008, keeping a 10-year interval. The next table shows the total number of attacks per year from 2008 to 2018: <br />

| Year |	Attacks |
| :-:  | :-----: |
|	2018 | 53      |
| 2017 |	136     |
| 2016 |	130     |
| 2015 | 143     |
|	2014 |	127     |
| 2013 |	122     |
| 2012 |	117     |
| 2011 |	128     |
| 2010 |	101     |
| 2009 |	120     |
| 2008 |	122     |

Anual trend line for the period from 2008 to 2017: <br />
 <br /> *insert plot here

##### Key variations: #####
* overall, there has been a small increase of around 11,5% in attacks from 2008 to 2017; <br />
* the biggest decrease in attacks was registered in 2010, showing a variation of -15,8% compared to 2009; <br />
* The biggest increase in attacks was of 26,7%, registered in 2011. <br />
 <br />
 
After a non exhaustive reserch for similar data available in the web, a very reputed website called [**Our World in Data**](https://ourworldindata.org/grapher/total-shark-attacks-per-year) used the same source of data and shows almost identical results. A second exemple, a website called [**Statista**](https://www.statista.com/statistics/268324/number-of-shark-attacks-worldwide/), shows relative significant lower numbers of attacks overall, but its source of data is not disclosed for non-members. <br />

#### Top 10 most susceptible activities to shark attacks ####

The variable 'activity' in the dataframe is extremelly heterogeneous and extensive. Although effort has been made to minimize the impact of such variations, inumerous activities are described in many different ways, sometimes in a composite manner. Particularly, 'swimming', which is the second most susceptible out from this analysis, has inumerous attributes, which means this activity was undoubtly under estimated. <br />

The table below shows the total number of attacks per activity throughout the entire dataset: <br />

| 
surfing          972
swimming         916
fishing          431
spearfishing     333
free diving      173
bathing          162
wading           149
body boarding    109
standing          99
scuba diving      90


