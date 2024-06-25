# Cyclistic Bike_Share Analysis

### Introduction 
I'm tasked with analyzing a public dataset for Cyclistic, an imaginary bike-share company located in Chicago. Throughout this case study, I'll utilize the PowerBI  for data analysis and visualization.

### About the Company
<br> Cyclistic was launched in 2016 and has since expanded its program, boasting a fleet of 5,824 bicycles meticulously tracked through geotracking technology and securely stationed across a network of 692 locations throughout Chicago.
<br> Cyclistic distinguishes itself by providing a range of options beyond traditional bicycles, including reclining bikes, hand tricycles, and cargo bikes. This inclusive approach aims to cater to individuals with disabilities and those unable to use standard two-wheeled bikes, making bike-sharing accessible to a broader audience.
<br> The majority of riders opt for traditional bikes, but approximately 8% of riders use the assistive options.
<br> Cyclistic users are more likely to ride for leisure, but about 30% use the bikes to commute to work each day.

<br> Customer categprization:
-  Casual Riders: Customers who purchase single-ride or full-day passes are referred to as casual riders.
- Cyclistic Members: Customers who purchase annual memberships are Cyclistic members.

<br> Cyclistic’s finance analysts have concluded that annual members are much more profitable
than casual riders.

### Current Challenge:
<br> Business Focus: The company's future prosperity hinges on maximizing the number of annual memberships.
<br> Marketing Goal: The marketing team seeks to discern the varying usage patterns between casual riders and annual members of Cyclistic bikes in order to craft a fresh marketing strategy. The objective is to convert casual riders into annual members.

### Tool Used:PowerBI

### Problem Statement: How does a bike-share navigate speedy success?
- Disribution by member types.
- Bike type used by different riders.
- Total Rides by Rider Type.
- Total Rides  by Bike Type.
- Rider distribution by Month and Rider Type
- Rider distribution by Weekday and Rider Type
- Rider distribution by start time and Rider Type.
- Total Number of rides.
- Total rides by bike type and Rider type.



## Prepare
### Data Sources: Link to Cyclistic Data:https://divvy-tripdata.s3.amazonaws.com/index.html

### Dataset Downloaded
- 202304-divvy-tripdata.csv
- 202305-divvy-tripdata.csv
- 202306-divvy-tripdata.csv
- 202307-divvy-tripdata.csv
- 202308-divvy-tripdata.csv
- 202309-divvy-tripdata.csv
- 202310-divvy-tripdata.csv
- 202311-divvy-tripdata.csv
- 202312-divvy-tripdata.csv
- 202401-divvy-tripdata.csv
- 202402-divvy-tripdata.csv
- 202403-divvy-tripdata.csv

### Steps Followed after Downloading the Dataset into my Computer:
I downloaded dataset covering bike rides between April 2023 to March 2024 for the purpose of this analysis.
<br> The data is in CSV format.

### Data Cleaning
- Open PowerBI
- Get data > From folder
- Locate and select the folder from pc
- Select transform data; this will open power query editor.
- Select content column, right click and select remove other columns.
- Click on double arrow beside content[combile files] to preview other headers
- To preview the quality of the data, go to view, select to check column quality , distribution and profile.
- After the preview, click to uncheck the column quality, distribution and profile.
- Select started at column and duplicate it twice
- Select ended at column and duplicate twice
- Rename the started at copy to startdate, rightclick and change type to date.
- Rename the started at copy1 to starthour, rightclick, select transform to hour.
- Rename the ended at copy to enddate, rightclick and change type to date.
- Rename the ended at copy1 to endhour, rightclick, select transform to hour.
- Added a custom column to get the ride in minutes. to do this;
- Go to add column
- choose custom colum and rename it to ride in minutes
- Where you see equal sign complete it by writing = endedat - started at
- Transform rideinminute to minutes; right click on right in minute column, select tranform and choose minutes.
- Select to filter start station name column, uncheck select all and select blanks, lod complete,go to tranform and select count rows.There are 874450 blanks station.
- clear the count row filter
- Select to filter ride in minute column, select number filter, lessthan/=0, go to transform and count row which sum up to 148807
- Add a custom custom name is abs_trip where abs mean absolute trip = Number.Abs([rideinminutes])
- Rightclick ride in minutes column and delete it
- Rename  abs_trip to rideinminutes.
- Add a custom column to get month from date and weekday with the formulars = Date.MonthName([startdate]) and Date.DayOfWeekName([startdate])
- Rename member-casual to rider type
- Rename rideable type to bike type
- Remove unused columns such as start and end station name, start and end station id, start and end latitude and start and end longitude as instructed.
- Select close and apply.
  

### Data Manipulation
- converted started at and ended at to datetime
- getting the start and end time in date (ymd)
- getting the start time and end time in hour
- getting the ride length in hour
- getting the ride length in minutes
- remove rows that have trip equal to zero and less than 0 
- getting days of the week from the start and end date
- removed unused columns such as start and end station name, start and end station id, start and end latitude and start and end longitude as instructed.
- 

### Recommendation
To accomplish the objective of converting casual riders into annual members, you can consider the following recommendations:
- Develop targeted marketing campaigns aimed at casual riders, highlighting the benefits of becoming annual members.
- Offer discounts or incentives to encourage casual riders to sign up for annual memberships. This could include discounted membership fees, rewards for signing up.
- Encourage annual members to share their positive experiences with others, creating social proof and word-of-mouth referrals.
- Increase awareness through targeted educational campaigns and social media outreach.

By putting these suggestions into action, you can successfully motivate occasional riders to become annual members, thereby increasing 

