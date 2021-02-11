# Investigating young, single parent households and households existing near hometown and their relationship to income

## Background
A recent [article](https://www.nytimes.com/2015/05/04/upshot/an-atlas-of-upward-mobility-shows-paths-out-of-poverty.html) in The New York Times highlighted some key findings from the Opportunity Atlas [database](https://www.opportunityatlas.org/). One key finding showed that moving children from poor neighborhoods to middle-class neighborhoods greatly improved the childrens' likelihood for success in adulthood. While the prevalence of children from poor communities attending college is [increasing](https://www.insidehighered.com/news/2019/05/23/pew-study-finds-more-poor-students-attending-college#:~:text=The%20total%20share%20of%20undergraduate,to%2047%20percent%20in%202016.), growing up in poverty has [lasting effects](https://www.insightintodiversity.com/povertys-long-lasting-effects-on-students-education-and-success/) on an individual's ability to perform in college. The best effort to equalize all childrens' opportunity for pursuing the "American Dream" is therefore rooted in mitigating the factors that contribute to a child being raised in poverty. 

This investigation seeks to identify some of the key metrics that contribute to a child gainaing upward mobility based on data from two municipalities (Baltimore, MD and Lewes, DE). Both locations are situated on the east coast. Baltimore is a major city with a wide range of races, education systems and social status. Lewes is a small town with less diversity but better prospects for upward mobility. The results reported here demonstrate that income level is not always negatively affected by teen pregnancy, but single parenthood is associated with increased poverty rate. Additionally, the data suggest that moving away from one's original home may lead to better prosperity.

## Business Question
__Helping individuals ascend from poverty is beneficial to the economy as it reduces resources given to these individuals as aid while giving them the power to spend more. What key factors should be targeted to increase upward mobility in cities like Baltimore, MD?__

## Data Question - Open Data
All data from this analysis comes from the [Opportunity Atlas Project](https://www.opportunityatlas.org/) organized by tract. Files downloaded are as follows:

- [Household Income](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/tract_kfr_rP_gF_pall.csv)
- [Household Income of those who Stayed in their Commuter Zone](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/tract_kfr_staycz_rP_gP_pall.csv)
- [Individual Income Excluding Spouse](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/tract_kir_rP_gF_pall.csv)
- [Median Rent](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/tract_median_rent2016.csv)
- [% Non-White Individuals](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/tract_nonwhite_share2010.csv)
- [Fraction of Population in Poverty](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/tract_poor_share2016.csv)
- [Fraction of Single Parents](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/tract_singleparent_share2016.csv)
- [Fraction who Stayed in their Commuter Zone](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/tract_staycz_rP_gP_pall.csv)
- [Frequency of Teen Births](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/tract_teenbirth_rP_gF_pall.csv)
- [Employment Rate](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/tract_working_rP_gP_pall.csv)

Data were imported into excel and filtered based on two locations: 
1. Baltimore, MD
1. Lewes, DE

Data from Baltimore locations were further processed to include only locations which exist within Baltimore city limits. Some data points were designated as Baltimore, MD but truly occurred outside these boundaries. The raw data compiled for analysis are included [here](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Mini_Project_1_raw_data.xlsx).

## Data Question - Analysis
Microsoft Excel was used to answer the following:
1. __What key metrics are correlated with higher prosperity?__ Variables listed under "Data Question - Open Data" were analyzed in Excel using a heat map to quickly visualize relationships. Variables that appeared correlated were analyzed further using a combination of Pivot Tables, charts, statistics, and trendlines.
1. __What socio-economic differences exist between Baltimore, MD and Lewes, DE?__ Key community metrics including % Non-White Individuals, Employment Rate, and Household Income were compared between the municipalities using Pivot Tables, mean and standard deviation.
1. __Do teen births and/or single parent homes put individuals at an economic disadvantage?__ Each metric was analyzed againsted the other and against poverty rate to find correlations. Trendlines were fit to scatterplots of the paired metrics.
1. __Does living where one was raised determine their economic prosperity?__ Household incomes for the full populations were compared against the household incomes of individuals who still live in the commuter zone from their childhood using Pivot Tables, mean and standard deviation.

## Data Answer
__What key metrics are correlated with higher prosperity?__
![alt text](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Baltimore_Lewes_metric_heatmap.png)

Here we see some interesting metrics pulled from the [Opportunity Atlas Project](https://www.opportunityatlas.org/). Heat maps were generated using conditional formating to differentiate cells by increasing value. This highlights that higher incomes are anti-correlated to Fraction of Non-White Individuals, Frequency of Single Parents, and Frequency of Teen Moms. The data also show that living near one's hometown is associated with a lower household income.

__What socio-economic differences exist between Baltimore, MD and Lewes, DE?__
![alt text](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Baltimore_Lewes_socioeconomic.png)

By summarizing the data into a Pivot Table, we can see that Baltimore, MD and Lewes, DE differ greatly in at least two different socio-economic metrics. First, the average employment rate in Baltimore is approximately 70% compared to 80% in Lewes. It's important to note that Baltiomre (15,450 people/sq. mile) is almost 40x more dense than Lewes (407 people/sq. mile). This means that while the difference between 70% and 80% does not seem large, this difference equates to thousands more people living unemployed. Additionally, the fraction of non-white individuals is approximately 10% in Lewes compared to 60% in Baltimore. It is worth noting that there is a high degree of variance between tracts in Baltimore and some of these have fractions of non-white individuals of 100%. This suggests that from a cultural standpoint, successful strategies used for poverty intervention may vary greatly between Baltimore and Lewes.

__Do teen births and/or single parent homes put individuals at an economic disadvantage?__
![alt text](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Teen_Poverty.png)



