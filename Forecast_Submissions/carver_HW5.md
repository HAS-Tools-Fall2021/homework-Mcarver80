### Monique Carver
**Assigment 5**

**9/27/2021**

**Explanation for this week's predictions:**

I chose to look at data from 2010, 2018, 2019, and recent data. I took the averages of each week and chose the one that I thought was more repetitive.

**Assignment questions**


**1.	Provide a summary of the data frames properties.**

•	What are the column names? 

    -Index, agency, site_no, datetime, flow, code, year, month, day.

•	What is its index?

    -	# of rows: 11954

•	What data types do each of the columns have?
    -	Dataframe, str, series, int.

**2.	Provide a summary of the flow column including the min, mean, max, standard deviation and quartiles.**
-	mean: 340.9
-	max: 63400.0
-	min: 19.0
-	standard deviation: 1391.3
-	quartiles: 93.5, 157.0, 214.0

**3.	Provide the same information but on a monthly basis.**

- 

**4.	Provide a table with the 5 highest and 5 lowest flow values for the period of record. Include the date, month and flow values in your summary.**

- 

**5.	Find the highest and lowest flow values for every month of the year (i.e. you will find 12 maxes and 12 mins) and report back what year these occurred in.**

-	Initialize some 1D arrays to store your max and min values
-	Loop over the months
-	For each month grab out just the flow values of that month
-	Sort them ascending by flow
-	Grab the year for the first value and save it in your min array
-	Grab the year for the last value and save that in your max array

**6.    Provide a list of historical dates with flows that are within 10% of your week 1 forecast value. If there are none than increase the %10 window until you have at least one other value and report the date and the new window you used.**
  

