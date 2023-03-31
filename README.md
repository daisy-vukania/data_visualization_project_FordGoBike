# FordGoBike Data Exploration

## by Daisy Vukania


## Dataset

The **'201902_fordgobike_tripdata.csv'** dataset was downloaded from the Udacity classroom workspace for the purposes of exploratory and explanatory data analysis through visualizations to communicate findings in the data. 
 
This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area. The original dataset contained **183412** rows and **16** columns. The data required some amount of tidying up of issues such as incorrect data types, misleading columns names, missing data and others. The cleaning process involved creating new columns, renaming columns, dropping rows with null values in the specific columns and dropping excess columns, all in effort to made the dataset clean and uesr friendly. The copy was saved to a new notebook; **'wrangled_201902_fordgobike_tripdata.csv'**.

After wrangling and tidying processes, the dataset contained **183,215** entries (rows) and **16** columns. These are the list of columns and their informations;

**trip_duration**(float64): duration each trips in ***'minutes'***, calculated from **duration_sec** column(dropped afterwards).

**trip_distance**(float64): distance of each trip in ***'miles'***, created for values calculated using *numpy* from **start_station_latitude**, **start_station_longitude**,**end_station_latitude**, **end_station_longitude**( all were dropped afterwards).

**day_of_week**(object): day of the week the trip was taken; created for values calculaed from **start_time**.                   

**trip_start_date**(datetime): date when trip was started; created for values calculaed from **start_time**.

**trip_start_hour**(int64): hour of the day trip was taken; created for values calculaed from **start_time**.

**trip_end_date**(datetime): date when trip was ended; created for values calculated from **end_time**.

**trip_end_hour**(int64): hour of the day trip was ended; created for values calculated from **end_time**.

**bike_id**(int64): identification numbers of bicycles used for trips.

**membership_type**(object): renamed **user_type** column; casual(Customer) or regular(Subscriber) type of user.created for values calculated from **member_birth_year**; dropped afterwards.

**gender**(object): renamed **member_gender** column; gender of user - Man, Woman, Other and Unknown(user did not provide, or not properly recorded).

**age**(int64): created for age values of users, calculaed from **member_birth_year**(dropped afterwards).

**start_station**(object): renamed **start_station_name** column; contains names of docking stations where users began rides.

**end_station**(object): renamed **end_station_name** column; contains names of docking stations where users ended rides.

**trip_start_time**(datetime): renamed **start_time** column; contains date and time information on trips as they begin. Used for extaction of data into individually created columns.

**trip_end_time**(datetime): renamed **end_time** column; contains date and time information on trips after they have ended. Used for extaction of data into individually created columns.

**bike_share_for_in_city_trips**(object): renamed from **bike_share_for_all_trip**;Whether or not (Yes/No) user relys on bike-share service fo all trasnportation in city.


## Summary of Findings

Most bike trips are taken on weekdays with fewer rides on weekends.
Bike usage is high during morning and afternoon rush hours, with peak usage at 4 AM and at 7 PM.
The majority of bike riders are aged between 20 to 40 years.
Most riders are subscribers as opposed to single or casual users.Most bike trips are less than 60 minutes. Around 90% of the riders do not opt for the only the bike-sharing service for either in-city or out-of-station trips. They use other means of transport.
There is a positive correlation between trip duration and distance, as shown by the scatter plot.
There are more male riders than female and other gender riders. The average trip duration is similar for all genders but is slightly longer for other genders.
Members tend to ride longer trips than casual riders.
The average duration and distance per trip do not vary significantly by hour.
There are more male riders and subscribers than female riders and casual riders in all age groups.
There is no significant difference in the distribution of age by gender.
The number of bikes used by male and female riders is similar, but the number used by other gender riders is much lower. Subscribers tend to use the bikes more than casual riders.



## Key Insights for Presentation

Popularity and Use of the Bike-Share system based on the following;

Peak time travel information

Types of memberships

Age of patrons

Gender of the patrons

Locations for the assessing the Bike-Share system for users, casual (customers) or regular (subscribers), of the service.
