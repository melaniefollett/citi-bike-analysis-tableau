# Cycling in the City: Citi Bike Analysis Using Tableau

Since 2013, the Citi Bike Program has implemented a robust infrastructure for collecting data on the program's utilization. Through the team's efforts, each month bike data is collected, organized, and made public on the Citi Bike Data webpage.  However, while the data has been regularly updated, the team has yet to implement a dashboard or sophisticated reporting process. City officials have a number of questions on the program, so my task for this project was to build a set of data reports to provide the answers.

# Overview of Project
My first task was to aggregate the data found in the Citi Bike Trip History Logs and find two unexpected phenomena.  I followed this by designing 3-4 visualizations for each discovered phenomena (7 total). I then created a dashboard for each phenomenon and an overall story using Tableau, as well as compiled a report describing and explaining the phenomena observed.

# Data Source
The data used for this analysis was collected from the Citi Bike Data webpage. In order to determine the effect of season on bike use, the data from June, July, and August 2019 were compiled to use as the summer months and the data from December 2019,  and January and February 2020 were compiled as the winter months. 

# Data Cleaning
The data was cleaned using pandas in Jupyter Notebook. The 6 CSV files (one for each month) were combined into one data frame. A new Season column was created based on month and a new Age column was created by subtracting the Birth Year column from the year 2020.
Once the data was imported into Tableau, several outliers became obvious. A significant number of users classified their Gender as “Unknown” and their age as “50”. This data was likely fabricated so all Gender Unknown datapoints were excluded. The Age range also included several outliers, with a particularly long bike trip being found in the age 16 category and several users claiming to be over 100 years old. So, the data was filtered to only include users whose age fell between 17-80.

# Dashboard 1: The Effect of Season on Citi Bike Use
Question: Does the number and duration of Citi Bike trips vary between summer and winter months?
Observation 1: There are a larger number of bike trips made during the summer months and trip duration tends to be longer.
Observation 2: Many cyclists are using bikes to commute to and from work regardless of season.
Observation 3: Stations further away from the city center are used more frequently in the summer months.

# Dashboard 2: Difference in Citi Bike Use Between Subscribers and Customers
Question: Do annual subscribers and short-term customers vary in their use of Citi bikes?
Observation 1: Subscribers use Citi bikes more frequently, but customers use Citi bikes for longer periods of time.
Observation 2: Subscribers use Citi bikes for commuting to and from work. Customers use Citi bikes for recreation.
Observation 3: There are more male subscribers and customers than female, but there is a much larger difference between the number of male and female subscribers than customers.

# Dynamic Map Analysis
The dynamic map of the locations of all bike stations and their popularity across months clearly shows that the most popular bike stations are all in the city center.  Bike stations outside of the city center are used less frequently, particularly in the winter months.

# Tableau Story
Please go to https://public.tableau.com/profile/melanie.follett#!/vizhome/tableau-challenge_15875944466250/CityOfficialMap to view the entire Tableau Story and please see the report in this repo for further discussion on the trends observed.
