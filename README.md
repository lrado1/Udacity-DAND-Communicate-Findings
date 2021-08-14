# (Bay Wheels - Usage Pattern Analysis)
## by (Laszlo Rado)


## Dataset

> Bay Wheels's publicly available trip data downloaded from the following url:

https://www.lyft.com/bikes/bay-wheels/system-data

* The data was combined from 12 separat monhtly data file from 2019.
* The data required some slight wrangling before the analysis (handling missing values, standardizing station names and IDs and using the correct data types.
* Additional calculated columns was added to the dataset during analysis (separate column for year, hour, weekday, and area calculated from the GPS coordinates)
* For 2019 there were 2,506,983 unique trips recorded in the dataset (although 3.9% of the data was removed during data cleaning)
* Each trip is anonymized and includes the following columns
    * Trip Duration (seconds)
    * Start Time and Date
    * End Time and Date
    * Start Station ID
    * Start Station Name
    * Start Station Latitude
    * Start Station Longitude
    * End Station ID
    * End Station Name
    * End Station Latitude
    * End Station Longitude
    * Bike ID
User Type (Subscriber or Customer – “Subscriber” = Member or “Customer” = Casual)


## Summary of Findings

> I have found out during the analysis that there were significant difference between the usage patterns of the two user groups.

The Subscriber user group, who took 80% of the rides in 2019, typically using the service for commute to work, which was conclued from the following observations:
    * Peak usage hours for the group are the morning and afternoon rush hours.
    * There is a huge drop in the usage rate during weekends
    * There is a drop in usage rates during working hours
    * There is a drop in usage during the Holiday season in December.
    * The typical ride length is between 500-700 seconds (~10 minutes)
    
 While the Customer user group, who took 20% of the rides in 2019, are consists of more casual fun-rides and tourist, which was concluded from the following observations:
     * Peak usage hours are the evening rush hours, but usage rate also high during the morning.
     * Customer user group is also actively uses the service during the weekend and working hours.
     * December is the most active month of the year.
     * The typical ride length is longer than for the the Subscriber user group around 7-800 seconds. The tail of the ride length distribution is als fading off much longer.
     
3 clearly isolated service area was identified by plotting the rides startin station on a scatter plot using the longitude and latitude coordinates provided as part of the dataset.
    * Looking a the company's website we could confirm that they are indeed providing service in 3 main areas
        * San Francisco
        * East Bay
        * San Jose
    * There was a large difference between the usage rates of the different areas. San Franscisco leading with the largest portion of the rides, and San Jose is the last with only a fraction of the number of rides compared to San Francisco.
    * Additional column was aded to the dataset to make it easier to filter on the different areas for further analysis.
     



## Key Insights for Presentation

In the presentation I've focused on showing the difference between the usage patterns of the two user groups.
I have used the polished versions of my initial plots from the exploration phase but typically included them as multiple sub plots showing the same finding from different perspectives.
One additional plot was created that visualizes the difference in usage rate per area and per user type in a more simpler way than in the exploration.

