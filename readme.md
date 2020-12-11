# Ford GoBike Data Exploration
## by Marwan Abdellattif


## Dataset

 The dataset contains 183,412 Ford GoBike  trips from February to March 2019 and 16 features about each trip. Each trip is described by the following:duration_sec, start_time, end_time, start_station_id, start_station_name, start_station_latitude, start_station_longitude, end_station_id, end_station_name, end_station_latitude, end_station_longitude, bike_id, user_type, member_birth_year, member_gender, bike_share_for_all_trip. 
 - The columns types are mostly numerical with two date format columns (start time and end time), three nominal categroical columns (member gender, user type, and bike_share_for_all_trip), two string columns (Start station name and end station name). However, three columns have been changed from numerical to string which are (start_station_id, end_station_id, and bike_id).
- The dataset has different columns with different missing values count, 197 and 8265. The 197 missing values occured with the station name and ID columns, while the 8265 missing values took place with information about the member's gender and age.

The following features are of interest (some of them are constructed):
- Age/Age groups of the users. ***New categorical feature***
- Type of User. 
- User's Gender. 
- Time  of day at which the trip started. ***New categorical feature***
- Time of day at whih the trip ended. ***New categorical feature***
- Days of the month for both start and end time. ***New numerical feature***


## Summary of Findings

I anticipated that some features of the data will be relatively connected to the main variable of interest (trip duration), which are:

Age/ Age groups: I had to transform the member birth year to two newly constructed features, the first is the member age (numerical), and the second is the age group of the member(categorical). This led to better visualization, and more intuitive interperetation. The Age groups column showed higher frequency for younger ages, and the frequency decrease as the age increases.
Type of user: I changed this feature to be of a ctegory type. The univariate visualization of this feature showed a signficant superiority of subscribers in terms of trips count.
Member's gender: Similar to the type of user, I changed this feature to be categorical type. It is visualization showed a very high frequency of male users, while the female group were only one third of the male groups' count. On the coontrary, the others group had no significant count.
Time of day (start/end): This is a newly constructed feature from the trip start time/ end time features. I used the mentioned features to categorize the times of day at which the trips took place. This was to know if a time of day has more trips than the other times, whih can be related to the crowd or the weather. From the visualization of this feature, I found that most of the users tended to have their trips between 6 am to 6 pm.
Days of the month: This feature was also constructed from the start/end time features. Yet, its visualization showed no significant conclusion.


## Key Insights for Presentation

For the presentation, I display the influence of the following features: (user type and user age) on the Users' GoBike trip duration. Firstly, I introduced each feature alone alonw with the main variable of interest (trip duration).

In the next step, I visualized each of the relationship in violin plots. Finally, I showed the relationship between the three features together in bar plot. 
