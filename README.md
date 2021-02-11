# Investigating young, single parent households and households existing near hometown and their relationship to income

## Background
A recent [article](https://www.nytimes.com/2015/05/04/upshot/an-atlas-of-upward-mobility-shows-paths-out-of-poverty.html) in The New York Times highlighted some key findings from the Opportunity Atlas [database](https://www.opportunityatlas.org/). One key finding showed that moving children from poor neighborhoods to middle-class neighborhoods greatly improved the childrens' likelihood for success in adulthood. While the prevalence of children from poor communities attending college is [increasing](https://www.insidehighered.com/news/2019/05/23/pew-study-finds-more-poor-students-attending-college#:~:text=The%20total%20share%20of%20undergraduate,to%2047%20percent%20in%202016.), growing up in poverty has [lasting effects](https://www.insightintodiversity.com/povertys-long-lasting-effects-on-students-education-and-success/) on an individual's ability to perform in college. The best effort to equalize all childrens' opportunity for pursuing the "American Dream" is therefore rooted in mitigating the factors that contribute to a child being raised in poverty. 

This investigation seeks to identify some of the key metrics that contribute to a child gainaing upward mobility based on data from two municipalities (Baltimore, MD and Lewes, DE). Both locations are situated on the east coast. Baltimore is a major city with a wide range of races, education systems and social status. Lewes is a small town with less diversity but better prospects for upward mobility. The results reported here demonstrate that income level is not always negatively affected by single parenthood, but teen pregnancy is associated with increased poverty rate. Additionally, the data suggest that moving away from one's original home may lead to better prosperity.

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

For detailed workflow, please see [data analysis](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/data-analysis-workflow.md)

## Data Question - Analysis
Microsoft Excel was used to answer the following:
1. __What socio-economic differences exist between Baltimore, MD and Lewes, DE?__ Key community metrics including % Non-White Individuals, Employment Rate, and Household Income were compared between the municipalities using Pivot Tables, mean and standard deviation.
1. __Do teen births and/or single parent homes put individuals at an economic disadvantage?__ Each metric was analyzed againsted the other and against poverty rate to find correlations. Trendlines were fit to scatterplots of the paired metrics.
1. __Does living where one was raised determine their economic prosperity?__ Household incomes for the full populations were compared against the household incomes of individuals who still live in the commuter zone from their childhood using Pivot Tables, mean and standard deviation.

## Data Answer
__What socio-economic differences exist between Baltimore, MD and Lewes, DE?__
![alt text](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Baltimore_Lewes_socioeconomic.png)

By summarizing the data into a Pivot Table, we can see that Baltimore, MD and Lewes, DE differ greatly in at least two different socio-economic metrics. First, the average employment rate in Baltimore is approximately 70% compared to 80% in Lewes. It's important to note that Baltiomre (15,450 people/sq. mile) is almost 40x more dense than Lewes (407 people/sq. mile). This means that while the difference between 70% and 80% does not seem large, this difference equates to thousands more people living unemployed. Additionally, the fraction of non-white individuals is approximately 10% in Lewes compared to 60% in Baltimore. It is worth noting that there is a high degree of variance between tracts in Baltimore and some of these have fractions of non-white individuals of 100%. This suggests that from a cultural standpoint, successful strategies used for poverty intervention may vary greatly between Baltimore and Lewes.

__Do teen births and/or single parent homes put individuals at an economic disadvantage?__
![alt text](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Teen_Poverty.png)

A scatterplot of Teen Birth Rate vs. Poverty Rate suggests a correlation for both locations. While we cannot conclude that there is some sort of causation, it is at least reasonable that giving birth as a teen would contribute to a higher prevalence of poverty. A teenager of any age has not had the time to seek education or establish a career and are therefore will have little to no dispensable funds following the birth of a child.

![alt text](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Teen_Single.png)

Interestingly, there is an apparent difference in the relationship between Teen Birth Rate and Single Parent Frequency when comparing Lewes to Baltimore. Baltimore shows a clear, positive linear relationship between Teen Birth Rate and Single Parent Frequency. By contrast, Lewes appears to show no relationship between these metrics, or even a slight negative correlation. This suggests that while many teen births in Baltimore result in single parent househoulds, Lewes may see a higher incidence of teen moms staying with their partner, perhaps getting married. 

![alt text](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Single_Poverty.png)

Another striking difference between Baltimore and Lewes is observed in the relationship between Single Parent Frequency and Poverty Rate. In Baltimore, single parenthood is positively correlated to poverty rate. This is contrary to what is observed in Lewes where the two are not correlated. As stated before, there are many things contributing to poverty rate, so the extent of causation is not clear. However, this does suggest that being a single parent in Lewes is easier than in Baltimore. Indeed, the average median income in Lewes is $31,290 (SD = 3,401) compared to $26,015 (SD = 5,485) in Baltimore, while the average median rent in Lewes is only $75 per month ($900 annually) higher than Baltimore. This means that single parents in Lewes are more likely to be able to sustain themselves than in Baltimore.

![alt text](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Baltimore_Lewes_single_teen_income_rent.png)

## __Does living where one was raised determine their economic prosperity?__
The [article](https://www.nytimes.com/2015/05/04/upshot/an-atlas-of-upward-mobility-shows-paths-out-of-poverty.html) in The New York Times pointed out that moving children into better neighborhoods increases their likelihood for upward mobility. We wanted to investigate whether remaining where one was raised is also a hinderance. To do this, we compared Median Household Income (MHI) to the MHI of those Staying in their Commuter Zone.

![alt text](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Baltimore_Lewes_CZ_data.png)

Strikingly, staying where one was raised is correlated with lower earnings. In Baltimore, the MHI of those who live near where they were raised is approximately $5,000 (-14%) below the unfiltered median income for the same area. For Lewes, this figure is approximately $10,000 (-21%) below. While it is difficult to speculate on what is the cause for this, one possibility is that people who stay where they were raised are limiting their opportunities. People who branch out may be doing so in pursuit of a higher-paying job or of better long-term economic prospects. The data also show that on average 78% of individuals from Baltimore remain in their childhood commuter zone compared to 65% from Lewes. As discussed above, this small difference in percentage amounts to thousands more people living near their childhood home in Baltimore.

## Data Interpretation

This analysis highlights some of the similiarities and differences between Baltimore, MD and Lewes, DE. While many of the basic demongraphics are quite different between the two, the both sets of data support the conslusions that teen birth rate is associated with poverty and that living near where one was raised is associated with lower median income. Since both teen birth rate and the percentage of individuals living near their childhood home are higher in Baltimore, these may be effective metrics to target for improving the upward mobility of Baltimore residents. For teen birth rate, providing affordable or free methods of contraception will give individuals better chances to establish their lives before having children. Likewise, providing supplemented resources like childcare and higher education to young mothers and single parents will increase their ability to thrive once they've had a child. The reduced income in individuals who live near their childhood home, is likely a reflection of not realizing or pursuing more prosperous alternatives. To mitigate this, providing adolescents programs to explore careers as well as new locations will inspire them to branch out. Doing so will increase the likelihood that they can earn more than they would have staying near home. These same efforts would be useful in Lewes, though the scale is far smaller. 

As a student, this analysis reminds me how different my childhood experiences have been from those who were raised in Baltimore. In my career, this means that I need to challenge my biases and actively work to understand the foundations for people's beliefs, motivations and ethics. It is also important to make concerted efforts to build up those around me and to do what I can to ensure that everyone is given equal opportunity to succeed.
