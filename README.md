# Project Shark Attack #

## Data ##
Source: https://www.sharkattackfile.net/ <br />
Dataset: https://www.kaggle.com/teajay/global-shark-attacks <br />

## Objectives
#### Primary: ####
* to verify if there is an obvious trend in the number of attacks per year in the last 10 years of collected data; <br />
* to determine the top 10 most dangerous areas and activities; <br />

#### Secondary: ####
* to find the acttack fatality rate for the top 10 activities (as a single variable) <br />

## Background ##
The dataset *attacks.csv* was sourced from the [**Shark Research Institute**](https://www.sharks.org/). The file contains extensive data, collected for centuries, about shark attacks in the entire World. The method of data collection is ignored, thus, inherent bias cannot be avoided. Moreover, there is significant data heterogeneity for most of the variables, in particular those necessary for the purpose of this study. 

## Methods ##
Targetted data cleaning and analysis was performed under *Python* and *Pandas*. The entire process was carefully worked in order to allow statistical analysis as accurate as possible.

## Results ##

#### Trend of attacks throughout the last 10 years ####
The analysis was initially made for the period from 2009 to 2018. However, the number of attacks computed in 2018 significant lower compared to the previous 9 years. The cause of this extreme variation was due by the fact that in 2018 the data has been collected only for the first six months (from January to June). The analysis was then readjusted to reject data from 2018 and to add those from 2008, keeping a 10-year interval. The next table shows the total number of attacks per year from 2008 to 2018: <br />

| year |	attacks |
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
 
For the purpose of data validation , 
