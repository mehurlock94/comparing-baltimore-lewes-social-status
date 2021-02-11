# This document outlines the workflow of data collection and analysis in Excel for Mini Project #1, labeled 

Raw data for this project were taken from the Opportunity Atlas [database](https://www.opportunityatlas.org/). All sets are organized by tract, which are areas that have a few thousand inhabitants.

Data were imported into Excel and filtered based on two locations: 
1. Baltimore, MD
1. Lewes, DE

Data from Baltimore locations were further processed to include only locations which exist within Baltimore city limits. Some data points were designated as Baltimore, MD but truly occurred outside these boundaries. The raw data compiled for analysis are included [here](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Mini_Project_1_raw_data.xlsx). The Excel file with manupulated data is inlcuded [here](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/comparing-baltimore-lewes-social-status.xlsx).

Once the data had been organized by true Baltimore locations and Lewes locations, a heat map was used to quickly observe trends in the data. 

![alt text](https://github.com/mehurlock94/comparing-baltimore-lewes-social-status/blob/main/Baltimore_Lewes_metric_heatmap.png)

From this, I decided to investigate two main relationships:
1. Teen mohters/single parents and poverty
1. Remaining in one's childhood commuter zone as an adult and income

# Teen mothers/single parents and poverty
Frequencies associated with each of these metrics were used to generate pairwise scatter plots. Baltimore data was colored blue and Lewes data was colored orange. Trendlines were added to quickly visualize potential correlation. A pivot table was also generated to look at the average of these three metrics as well as average median income and average median rent for the two locations. Standard deviations were also calculated below the table of heat map data

# Remaining in one's childhood commuter zone as an adult and income
Since the median household income of individuals who live as adults where they were raised was always lower than the unfiltered median household income, the ratio of the former over the latter was taken in Excel to determine what percent of the potential whole income "stayers" were receiving. This was included in a Pivot table along with the average number for each metric and the % of individuals who stayed for each location.
