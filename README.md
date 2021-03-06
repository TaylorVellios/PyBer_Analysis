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
* The date and time the ride took place. (Total range of this dataset is from Jan. 1 2019 - May 8 2019)
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
![rides_series](https://user-images.githubusercontent.com/14188580/112901570-8e3af280-90aa-11eb-8146-ab4328df287f.PNG)
<br><br>

## Total Drivers by City Type
Getting this metric required a revisit to one of the original .CSV files pre-merge. Merging both files together resulted in duplicate cities per row, whereas the city_data_df DataFrame object already contains unique rows for cities. By using .groupby() on the "type" column again, I was able to get sum of the driver counts based on the grouped column.
<br>
Plotted as a pie chart, it is easy to see how the Urban city-type eclipses the other two in terms of Drivers.<br>

![drivers](https://user-images.githubusercontent.com/14188580/112899125-52525e00-90a7-11eb-8e50-93fa615d54c2.png)
![drivers_series](https://user-images.githubusercontent.com/14188580/112901592-972bc400-90aa-11eb-9ad1-beebf103ab8f.PNG)
<br><br>

While is should come as no surprise that there is certainly a correlation between city population and number of drivers, the key takeaways from this plot are as follows:

#### During the timeframe of this dataset (1/1/2019 - 5/8/2019):

* There were more drivers onboarded to service Urban cities than there were rides given.
* Both Suburban and Rural city types had fewer drivers than rides.
<br><br>

## Sum of Fares by City Type
My last pie chart, I promise.<br>
The following graph is showing the sum of all fares for each city type. Please take note of how much the Suburban and Rural city types start to push back against the ever-dominant Urban city type. <br>
As soon as we start looking at dollars and cents we can see the importance of ride-sharing services in these areas.<br>
It is very impressive to see Suburban cities earning almost 50% of what Urban cities brought in with when the number of rides for Suburban cities was 38.4% of the Urban count.
<br>

![sumoffares](https://user-images.githubusercontent.com/14188580/112903264-e07d1300-90ac-11eb-8915-8cc72b6efc4b.png)
![faresby_type](https://user-images.githubusercontent.com/14188580/112903275-e4109a00-90ac-11eb-9d8b-35e697cb322d.PNG)
<br><br>

# Average Fare per Driver/Ride
![avgfareperdriver](https://user-images.githubusercontent.com/14188580/112909911-f17f5180-90b7-11eb-9428-eea4d697d3fa.png)
![avgfareperride](https://user-images.githubusercontent.com/14188580/112909917-f2b07e80-90b7-11eb-87f6-bf1928998384.png)
<br>
Above are visualizations for the average fare by Driver and per Ride grouped by City Type.<br>
It is very easy to see just how drastically more expensive Rural and Suburban rides are in comparison to Urban ones.<br>
There are many possible reasons for this:
* Rural rides most likely have to travel longer distances to get passengers from point A to point B, coupled with the cost premium from a lack of available drivers.
* Urban areas have an overabundance of drivers, simple supply and demand. I'm confident looking at data in Summer/Fall months would yield very different results.
* Suburban rides may not have to travel as far as Rural rides, but most certainly shorter distances than Urban ones. 
<br><br>

# Summary:
![PyBer_fare_summary](https://user-images.githubusercontent.com/14188580/112912629-98b2b780-90bd-11eb-9bdb-5450964cff05.png)

<br>
There is no doubting the foothold that Urban cities have for the bottom line of this company, but there is work to be done to secure a larger user-base.
<br>

### I believe the high cost of Rural rides is limiting our reach to service those communities.

* By lowering the base fare while keeping the driver's cut intact, it could encourage a greater number of people to join the platform: creating more cash flow.

### Based on our driver counts, it comes as no surprise that there is a direct relationship between city population and number of onboarded drivers.
* By creating an incentive for drivers to service city types other than the ones they reside in, it would be possible to help our supply-heavy Urban drivers operate more rides to keep them as part of the system longer, while alleviating any issues that Suburban and Rural users might have with wait times.

### Other Markets:
* No matter how you look at it, this service seems to be better at employing drivers than garnering interest for their services. If we have a labor force as strong as this one - without an equal or greater demand of their services, it would be beneficial to look into additional means of pulling in revenue. Should something happen to impact the ride-sharing market, like a global pandemic for instance, this business would be crippled. Breaking into the grocery/restaurant delivery service market would give our drivers more incentive to stay active for our users throughout the day while bringing in more revenue.

<br>
