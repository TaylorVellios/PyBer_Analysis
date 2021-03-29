# PyBer_Analysis
Python - Pandas and MatPlotLib - A Look Into Ride Sharing Data

# Overview:
Taking a deep-dive into ride sharing data to highlight the potential differences in service and earnings between the three City Types: Urban, Suburban, and Rural.
By dividing the data around the types of cities, I will be highlighting the distribution of customer cost and company profit between them. 
<br><br>
# Results:
<br>
The dataset used for this analysis is 2,374 rows of ride data merged from DataFrames based off of two separate .CSV files.<br>
Items included in this dataset:
* The city a ride took place in
* The date and time the ride took place
* the total cost to the user
* The unique ride ID number
* The total driver count of the city each ride took place in
* The "type" of city, or the categorization it falls under: Urban, Suburban, or Rural
<br>

![dataset_snap](https://user-images.githubusercontent.com/14188580/112877554-8409fb80-908c-11eb-92b1-0287266302b2.PNG)

<br>

After confirming the data is NaN-Free, I used groupby functions to find useful data.<br>

## Total Rides by City Type
Using .groupby() on the "type" column, I used the .count() method on unique Ride ID's to get a simple Pandas Series of ride counts for each city type.<br>
Plotted as a pie chart, it is very apparent that the Urban city type gets the largest amount of usage for this ride sharing platform.<br>
![rides](https://user-images.githubusercontent.com/14188580/112891129-5ed1b900-909d-11eb-883c-4fae022d6a87.png)
<br><br>

## Total Drivers by City Type


There is a description of the differences in ride-sharing data among the different city types. total drivers, total fares, average fare per ride and driver, and total fare by city type. (7 pt)
<br><br>

Summary:
<br>
There is a statement summarizing three business recommendations to the CEO for addressing any disparities among the city types. (4 pt)
