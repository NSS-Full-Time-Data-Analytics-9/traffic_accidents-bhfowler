# Nashville Traffic Accidents

For this exercise, you have been provided a dataset of traffic accidents that occurred in Davidson County which was retrieved from https://data.nashville.gov/Police/Traffic-Accidents/6v6w-hpcw. 

This spreadsheet has been divided into the following sheets:
* Accidents: Contains the raw data for each accident. For a description of each column, you can see the Metadata, available here: https://data.nashville.gov/api/views/6v6w-hpcw/files/3af9281b-fa4f-4044-83f8-1b9a46cc6e95?download=true&filename=Traffic-Accidents-Metadata-v2.pdf. 
* Analysis: This sheet will hold most of your answers.
* Zero Car Crashes: This sheet will be used in question 3.
* Collision Types: Contains the text description of each collision type. You will fill in your answers for question 5 here.
* Weather Types, Illumination Types, and Harmful Types: Contain descriptions for the other three codes. Not used in this exercise.

Use formulas to answer each question. Unless otherwise stated, fill in your answers in the "Analysis" tab.

1. How many total accidents are contained in this dataset?

	218319

2. What are the earliest and latest records that appear in this dataset?

	Earliest : 01/01/2015 0:00
	Latest : 06/21/2022 20:06

3. a. Create a new column to the right of the "Number of Motor Vehicles" column called "Single or Multiple". This column should contain "Single" if the number of vehicles is 1 and "Multiple" if it involved more than one vehicle.  
b. Are there any rows that involved zero vehicles? How many? Make sure that your formula accounts for these cases.  
c. Investigate the rows that have zero vehicles using the FILTER function in the "Zero Car Crashes" sheet. What do you find?  
d. What percentage of crashes are single-car?

	a. Excel
	b. Yes, 8556
	c. ???
	d. 15.7416441%

4. How many accidents occurred which are hit and run and had at least one injury?

	7535

5. a. What is the overall average number of injuries?  
b. Go to the "Collision Types" sheet and fill in the table to find the total number of crashes, average number of injuries, and total number of injuries per collision type. For each calculation, write a single formula and copy it down the table. What do you find? (Hint: If you're not sure how to answer this question, revisit the "Conditional functions and lookups" chapter of [Data Analysis in Spreadsheets](https://app.datacamp.com/learn/courses/data-analysis-in-spreadsheets).)

	a. 0.388591923
	b. Collision Type Code 11 "Front to Rear" is the most common type of collision and causes the most total injuries. And Collision Type Code 2 "HEAD-ON" has the highest average injuries by nearly 2 times more than 2nd highest.


6. a. Add three new columns, Month, Year, and Hour to the right of the Date and Time column. Use the [TEXT function](https://support.microsoft.com/en-us/office/text-function-20d5ac4d-7b94-49fd-bb38-93d29371225c) to extract out the Month, Year, and Hour from the "Date and Time" column.  
b. Add one more new column, Weekday, and use the WEEKDAY function to extract out the day of the week from the Date and Time column. Use the TEXT function in combination with the WEEKDAY function to display the result as the name of the weekday (eg. Monday).

	a. Excel
	b. Excel

7. Fill in the Hour table in the Analysis spreadsheet to find the number of accidents that occurred for each hour of the day. Again, write a single formula and copy it down the table. Do you see anything unusual? What might be the explanation for this?

	Excel

	More accidents happened during evening rush hour(15:00-19:00). Compare to lower cases of accident during morning rush hour(06:00-10:00), I suspect there is correlation between how tired the drivers are and the numbers of accidents. That goes to show that numbers of accident increase through the weekday.
	The numbers of traffic would help to get more indepth analyse.

8. Do the same for the year and day of the week. What stands out?

	The numbers of accident increase through the weekday.

	There was significant drops of the numbers of accident during pandemic.

9. Add a column to the right of the Collision Type Code called "Collision Type". Use the table contained in the Collision Types sheet to fill in this column. 

	Excel

10. Which interstate has the most accidents between I-24, I-40, I-65, and I-440? Answer this by counting the number of accidents that contain the strings "I 24", "I 40", "I 65", or "I 440" in their Street Address. Hint: You may need to make use of [wildcards](https://support.microsoft.com/en-us/office/using-wildcard-characters-in-searches-ef94362e-9999-4350-ad74-4d2371110adb) in combination with the CONCAT function to answer this. Then do the same but search for "I24", "I40", "I65", and "I440" and then "I-24", "I-40", "I-65", and "I-440". Sum the results to get a total count. Bonus: Rather than doing three separate counts and adding, get the total count using a single formula for each interstate. 

	I-40