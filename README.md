# UserTrendsinPowerBI

The Google Data Analyst Professional Certificate provided a large dataset for the capstone project. The idea is to ensure that all aspects of data analysis process are applied on a business problem to produce actionable insisghts.

## Graphs
For Graphs Open the Accompanying PDF file

## 1. Situation
Cyclistic: A bike-share program that features more than 5,800 bicycles and 600 docking stations. The Dataset has data about the time and station that the ride was started and the time and station that the ride was ended. 
## 2. Scenario/Task
You are a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director
of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore,
your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights,
your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives
must approve your recommendations, so they must be backed up with compelling data insights and professional data
visualizations

## 3. Strategy for Identifying User Trends
I performed exploratory Data analysis on 12 months Data of 2021 to figure out the differences in bahaviors of the Casual users vs Annual users.
I performed the following analysis:

1. Number of rides vs
- Day of week
[](1.jpg)
- Month of year
- Time of Day
- Length of trip
2. Quarter wise change in total number of rides
3. Type of bike used vs
- Day of the week
- Month of the Year
4. Average Length of trip Vs time of the day
5. Number of trips by Quarter for Casual users vs Annual(member) users 
6. Total Time spent on Trips by Quarter

## 4. Data Cleaning and Data Processing

- The data was in 12 CSVs and directly loaded to POWER BI
- I deleted extra columns including the latitude and longitude of the start and end station.
- Extracted the duration of trip as time and as a decimal number seperately
- Extracted names of days,months, quarter number
- Extracted the date and the time of day seperately from the time of ride starting (column started_at)

#### NOTE:
I did not delete rows with nulls, I only filtered them out. After the model was transformed and loaded. I sorted the date via different columns to study the data patterns. I discovered that some of the ride durations were negative so we filtered those ones out.

## 5. Insights and Reccomendations

### 5A. Insights
- There is strong seasonality in the use of bicycles as Chicago is too cold in the winter months so total use drops. Summer has very pleasant weather and casual users (perhaps tourists) also flock to this service in the summer months
- There is strong seasonality in the use with the time of day as well. 6AM to 6PM time slot experiences a steady increase in the number of rides and then drops sharply after that upto 5 30 AM
- Casual users are mostly weekend users and Annual(member) users are mostly weekdy users.
- There is a predictable seasonality in the number of total rides based on the day of the week (weekday vs weekend)
- Regular users take longer ride on average and casual users take shorter rides
- Casual users stop taking rides steeply right after summer ends but regular users tend to use them more in post summer months
- From Mid October to End of December the use of Electric bikes is more than the use of Classic and docked bikes combined
- Annual users are more predictable than casual users thus demand prediction would be easier for annual members




###  5B. Specific Reccomendations
- The current casual users who are using the service atleast X times per year (Decide X based on further analysis) can be targetted to market that using this service is a substitue for going to the gym -  this will achieve the **business goal of converting casual users to Annual users** 
- Casual user trips have a strong peak from 7 30 Am to 9 AM this means they are using the bikes for getting to work. Thus by **marketing to people to use this service for work the company can get more annual users** 
- The company can launch a buddy program where annual members get a discount if they get someone to sign up for an annual membership

### 5C. General Reccomendations
- In general marketing efforts should be focused Feburary and onwards as that is the start of enjoyable weather
- Electric bikes have very low utilisation hence they need to be marketed, Specially in the winter months starting Sept till mid December. ( After Dec the weather may be unfeasible for bike rides)
- Docked bikes are not being used a lot hence company needs to figure out **if it's profitable to have docked bikes**
- 3AM to 6AM is the best time to repair the bikes as demand is minimum
- The average annual member goes for longer rides hence it may be useful to build/encourage local communities around cycling to encourage neighbourhoods to participate in this as a healthy bonding activity
- Companies can be given special rates for Annual memberships to increase the total number of annual users
- Due to High demand in the winter months the company should to hire seasonal workers in the summer months instead of full time employees
- There is unused capacity in the system on weekdays(lower demand) so targetting annual members is a great business decision.

## 6. Major Learnings
1. Some operations are O(n^2), so we need to delay these steps till after the data model is ready. For e.g. Sorting and Deleting rows with blanks, nulls etc.  Meaning that once the index has been assigned to rows it is a compute-heavy task to delete unwanted rows and then refresh the index for every row deleted.
2. Documenting the steps of your work is mroe important than doing the work once and forgetting what you did the last time.
3. It's too complicated to share your report in Power BI, Tableau is faster and smoother for this task.


### Referrences: 
1. Case Study for Google Data Analyst Professional certificate and the accompanying data
