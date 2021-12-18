# Project Shark Attack #

## Data ##
Source: https://www.sharkattackfile.net/ <br />
Dataset: https://www.kaggle.com/teajay/global-shark-attacks (attacks.csv) <br />

## Objectives
#### Primary: ####
* to verify if there is an obvious trend in the number of attacks per year in the last 10 years of collected data; <br />
* to determine the top 10 most dangerous activities; <br />
* to identify the top 10 most dangerous areas in the last 10 years (2009 to 2018). <br />

#### Secondary: ####
* to stablish the case fatality rate (CFR) for the top 10 activities (as a single variable) <br />

## Background ##
The dataset *attacks.csv* was sourced from the [**Shark Research Institute**](https://www.sharks.org/). The file contains extensive data, collected for centuries, about shark attacks in the entire World. The method of data collection is ignored, thus, inherent bias cannot be avoided. Moreover, there is significant data heterogeneity for most of the variables, in particular those necessary for the purpose of this study. 

## Methods ##
Targetted data cleaning and analysis was performed under *Python* and *Pandas*. The entire process was carefully worked in order to allow statistical analysis as accurate as possible.

## Results ##

#### 1. Trend of attacks throughout the last 10 years ####
The analysis was initially made for the period from 2009 to 2018. However, the number of attacks computed in 2018 significant lower compared to the previous 9 years. The cause of this extreme variation was due by the fact that in 2018 the data has been collected only for the first six months (from January to June). The analysis was then readjusted to reject data from 2018 and to add those from 2008, keeping a 10-year interval. The next table shows the total number of attacks per year from 2008 to 2018: <br />

| Year |	Attacks |    
| :--: | :-----: |
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


The graphic below illustrates well the significant data disparity in 2018 compared to previous years: <br />
<br />
<img width="391" alt="image" src="https://user-images.githubusercontent.com/92320460/146643892-240be8b1-3971-4354-98df-5c6d70ffefe7.png">


After exclusion of year 2018, the anual trend line for the period from 2008 to 2017: <br />
<br />
<img width="379" alt="image" src="https://user-images.githubusercontent.com/92320460/146643766-67b3f96b-520c-440a-af0e-2851c77fbf34.png">

##### Key variations: #####
* overall, there has been a small increase of around 11,5% in attacks from 2008 to 2017; <br />
* the biggest decrease in attacks was registered in 2010, showing a variation of -15,8% compared to 2009; <br />
* The biggest increase in attacks was of 26,7%, registered in 2011. <br />

##### Data validation: #####
After a non exhaustive reserch for similar data available in the web, a very reputed website called [**Our World in Data**](https://ourworldindata.org/grapher/total-shark-attacks-per-year) used the same source of data and shows almost identical results. A second exemple, a website called [**Statista**](https://www.statista.com/statistics/268324/number-of-shark-attacks-worldwide/), shows relative significant lower numbers of attacks overall, but its source of data is not disclosed for non-members. <br />

#### 2. Top 10 most susceptible activities to shark attacks ####
The variable 'activity' in the dataframe is extremelly heterogeneous and extensive. Although effort has been made to minimize the impact of such variations, inumerous activities are described in many different ways, sometimes in a composite manner. Particularly, 'swimming', which is the second most susceptible out from this analysis, has inumerous attributes, which means this activity was undoubtly under estimated. <br />

The table below shows the total number of attacks per activity and their representation ratio to the entire dataset: <br />

| Activity      | Attacks | Ratio  |
| :------:      | :-----: | :----: |
| surfing       |   972   | 16.88% |
| swimming      |   916   | 15.90% |
| fishing       |   431   |  7.48% |
| spearfishing  |   333   |  5.78% |
| free diving   |   173   |  3.00% |
| bathing       |   162   |  2.81% |
| wading        |   149   |  2.58% |
| body boarding |   109   |  1.89% |
| standing      |    99   |  1.71% |
| scuba diving  |    90   |  1.56% |

The figure below illustrates the number of attacks per activity:<br >
<br />
<img width="395" alt="image" src="https://user-images.githubusercontent.com/92320460/146644488-3f1cb95a-6aad-4bcf-952e-9418f1e3a654.png">


The 10 most recorded activities represents nearly 60% of the all dataset. Only surfing and swimming accounts for at least around 33% of all attacks recorded.<br />

#### 3. Most dangerous areas from 2009 to 2018 ####
The variable 'area' in the dataset is extensive (**826 different areas**), with fairly little heterogeneity. Most variations were typos, which were easily detected, and adressed accordinly. <br />
A verification was made to make sure that data was collected throughout the period for the ares in question. <br />

The table below shows the total number of attacks per area and their representation ratio:

|         Area  	       | Attacks |   Country    |  Ratio |
| :-------------------: | :-----: |   :-----:    | :----: |
| florida 	             |  1038   | usa          | 17.75% |
| new south wales 	     |  486 	  | australia    |  8.31% |
| queensland 	          |  311 	  | australia    |  5.31% |
| hawaii 	              |  298 	  | usa          |  5.09% |
|	california            | 	290 	  | usa          |  4.95% |
|	kwazulu-natal         |  213 	  | south africa |  3.64% |
|	western cape province |	 195 	  | south africa |  3.33% |
|	western australia     | 	192 	  | australia    |  3.28% |
|	eastern cape province |	 163 	  | south africa |  2.78% |
|	south carolina 	      |  161 	  | usa          |  2.75% |

The figure below illustrates the number of attacks per area:<br >
<br />
<img width="403" alt="image" src="https://user-images.githubusercontent.com/92320460/146644536-f39bfc16-f385-463e-b5da-af0c4e3b9bac.png">


The top 10 areas where attacks occured represent nearly 60% of all attacks recorded. Nearly 18% of all attacks happened in the state of Florida (USA), followed by New South Wales (Australia) with around 8%. As such, almost 28% of all attacks happened in the USA.

#### 4. Shark attacks fatality per activity ####
The dataset brought information about the fatality of almost all attacks. The activities' fatality were analysed comparing them to each other, showed as **'Fatality Ratio'** and the intrinsic fatality rate as the **Case Fatality Rate (CFR)**. <br />

The table below shows the analysis for the top 10 activities per absolute number of attacks: <br />

|    Activity   |	Total Fatalities |	Fatality Ratio |	  CFR  |
| :-----------: | :--------------: | :------------: |   :-:  |
|	surfing 	     |       49 	       |      3.81% 	   |  5.04% |
|	swimming      |	     325 	       |     25.33%	    |	35.48% |
|	fishing       |	      47         |	     3.66% 	   |	10.90% |
|	spearfishing  |	      41         |	     3.19%	    |	12.31% |
|	free diving   |	      26         |	     2.02%	    | 15.02% |
|	bathing       |	      71         |	     5.53% 	   |	43.82% |
|	wading 	      |       13         |	     1.01%	    | 8.72%  |
|	body boarding |	      17         |	     1.32% 	   |	15.59% |
|	standing 	    |       16         |	     1.24% 	   |	16.16% |
|	scuba diving 	|       14         |	     1.09% 	   | 15.55% |

The figure below illustrates the number of fatalities per activity and their CFR: <br >
<br />
<img width="386" alt="image" src="https://user-images.githubusercontent.com/92320460/146645804-f9ad153b-a1c2-4635-80cf-5544e78a15b5.png">

##### Some interesting considerations: #####
* swimming accounts for a quarter (25%) of all attacks recorded. If you're attacked while swimming, you have a non-survival chance of 35%;
* while surfing accounts for the biggest number of attacks (see point 2 above), the CFR for this activity is 5%, the lowest among the top 10 deadliest activities;
* the highest CFR among the top 10 is *bathing*: 43.8%
* the mean CFR of all activities is 17.9%

## Discussion ##
An extensive and extremelly heterogenous dataframe was available. With clear objectives in mind, target data cleaning was performed in order to maximise accuracy of the results. <br />
<br />
Of the 3 main variables for this analysis, by far, the most problematic was the *'activity'* variable. The recordings were many times composed of multiple words, not always related to each other, or even full 'complex' sentences. Out of the most represented activities, 'swimming' seemed to show the most number of variation in its description. Skiming the list of activities, some of these variations were addressed. However, it is clear that there has been an underestimation of the total number of attacks in this category, and consequently, an overestimation of its CFR. A thorough evaluation of the activity list would be necessary to minimise this issue.<br />
<br />
Within the variable *'area'*, one could question if there has been a bias in the data collection. The fact that around 28% of all attacks recorded from 2009 to 2018 were in areas in the USA, one could suspect that collection resources might be more available in that country compared to others. Further investigation is needed. In addition, when solely analysing the dataset, every non recorded attack for a certain 'area' in a certain year cannot be certanly attributed to a true null result or a faillure in the data collection. <br />
<br />
It is also important to note that the variables 'area' and 'activity' were analysed independently of each other. For example, the fact that 'surfing' accounts for the biggest number of total attacks, it doesn't necessary mean it is the most dangerous activity in Florida, the area where most of the attacks happened in the last 10 years. Such cross checking (rankig the 'activity' for a specific 'area') is possible with the data availale, but it remains out of the scope of this particular analysis.

## Conclusion ##
##### Taking in consideration the numerous dataset limitations and targeted analysis of a global shark attack dataframe, this study demonstrates: #####
* an uptrend in the number of shark attacks, with an overall increase of around 11,5% from 2008 to 2017;
* a ranking of the most dangerous areas in the World;
* the top 10 most susceptible activities to shark attacks;
* the CFR for each activity.<br />






