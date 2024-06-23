# Cyclistic Bike_Share Analysis

# Tool Used:
PowerBI

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

# Data Manipulation
- converted started at and ended at to datetime
- getting the start and end time in date (ymd)
- getting the start time and end time in hour
- getting the ride length in hour
- getting the ride length in minutes
- remove rows that have trip equal to zero and less than 0
- getting days of the week from the start and end date
-  removed unused columns such as start and end station name, start and end station id, start and end latitude and start and end longitude as instructed.
-  get minimum and maximum date of rides
