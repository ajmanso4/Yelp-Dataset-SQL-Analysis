# SQL for Data Science UC Davis (Coursera) final - December 2023:

Data Scientist Role Play: Profiling and Analyzing the Yelp Dataset Coursera Worksheet

This is a 2-part assignment. In the first part, you are asked a series of questions that will help you profile and understand the data just like a data scientist would. For this first part of the assignment, you will be assessed both on the correctness of your findings, as well as the code you used to arrive at your answer. You will be graded on how easy your code is to read, so remember to use proper formatting and comments where necessary.

In the second part of the assignment, you are asked to come up with your own inferences and analysis of the data for a particular research question you want to answer. You will be required to prepare the dataset for the analysis you choose to do. As with the first part, you will be graded, in part, on how easy your code is to read, so use proper formatting and comments to illustrate and communicate your intent as required.

For both parts of this assignment, use this "worksheet." It provides all the questions you are being asked, and your job will be to transfer your answers and SQL coding where indicated into this worksheet so that your peers can review your work. You should be able to use any Text Editor (Windows Notepad, Apple TextEdit, Notepad ++, Sublime Text, etc.) to copy and paste your answers. If you are going to use Word or some other page layout application, just be careful to make sure your answers and code are lined appropriately.
In this case, you may want to save as a PDF to ensure your formatting remains intact for you reviewer.

## Part 1: Yelp Dataset Profiling and Understanding

1. Profile the data by finding the total number of records for each of the tables below:

SELECT * FROM [table name]
^^^ To find the total number of records
	
<img width="194" height="155" alt="Screenshot 2026-02-16 at 22 54 56" src="https://github.com/user-attachments/assets/9f49af1b-196b-4e04-a7fb-d297c5e158e2" />


## 2. Find the total distinct records by either the foreign key or primary key for each table. If two foreign keys are listed in the table, please specify which foreign key.

I just did:
SELECT DISTINCT [primary or foreign key column name] FROM [table name]
^^ to find the total amount of distinct records from each table's primary and/or foreign key

<img width="499" height="155" alt="Screenshot 2026-02-16 at 22 55 26" src="https://github.com/user-attachments/assets/41a45e98-cad8-4d55-af04-6d30e2cd4fe5" />

Note: Primary Keys are denoted in the ER-Diagram with a yellow key icon.	


## 3. Are there any columns with null values in the Users table? Indicate "yes," or "no."

	Answer:
No

<img width="312" height="313" alt="Screenshot 2026-02-16 at 22 56 36" src="https://github.com/user-attachments/assets/cba5f3b4-e614-4d18-a555-cceedc7570bd" />

## 4. For each table and column listed below, display the smallest (minimum), largest (maximum), and average (mean) value for the following fields:
<img width="428" height="238" alt="Screenshot 2026-02-16 at 22 56 58" src="https://github.com/user-attachments/assets/31ec09ce-6fc5-4aff-8e83-1cc189a8d6d8" />


## 5. List the cities with the most reviews in descending order:
<img width="213" height="52" alt="Screenshot 2026-02-16 at 22 59 40" src="https://github.com/user-attachments/assets/51ae4540-bedf-48aa-9b38-707d2c2fe15b" />

<img width="531" height="602" alt="Screenshot 2026-02-16 at 23 00 00" src="https://github.com/user-attachments/assets/730344c4-51f7-403f-a0bd-dc0bb197e1b9" />


## 6. Find the distribution of star ratings to the business in the following cities:
<img width="514" height="457" alt="Screenshot 2026-02-16 at 23 03 29" src="https://github.com/user-attachments/assets/54f1e394-a83e-4e8b-944e-0adcdc244773" />


## 7. Find the top 3 users based on their total number of reviews:
<img width="277" height="166" alt="Screenshot 2026-02-16 at 23 04 07" src="https://github.com/user-attachments/assets/13c28cc2-b66b-489d-96ac-3ae0d9c67648" />


## 8. Does posing more reviews correlate with more fans? Please explain your findings and interpretation of the results:
Technically yes. But a very weak correlations. As the people who posted 0 or very few reviews have little to no fans, whereas the people who at the least started posting a lot of reviews start to gain more fans.
HOWEVER, as we see with the users ranked by the most fans below, The Average review_count for the people who have over 100 fans is 891.5, versus an average of a 22.9 review_count for the people who have less than 100 fans. 


More reviews does not mean the more fans. 

<img width="315" height="386" alt="Screenshot 2026-02-16 at 23 05 15" src="https://github.com/user-attachments/assets/066c4c32-709f-4d8e-a3e5-680b693b1acc" />

The Average review_count for the people who have over 100 fans is 891.5, versus 22.9 reviews for the people who have less than 100 fans. 

<img width="155" height="211" alt="Screenshot 2026-02-16 at 23 05 32" src="https://github.com/user-attachments/assets/1dcf1605-4fef-4aba-8cf8-688b9dfe3233" />



## 9. Are there more reviews with the word "love" or with the word "hate" in them?

	Answer: The word "Love"
<img width="336" height="834" alt="Screenshot 2026-02-16 at 23 06 41" src="https://github.com/user-attachments/assets/a63763ac-6dde-48c1-a973-46f95c40d8a7" />


## 10. Find the top 10 users with the most fans:
<img width="294" height="249" alt="Screenshot 2026-02-16 at 23 07 05" src="https://github.com/user-attachments/assets/d60c995f-16bd-4c46-a847-b27bf0985898" />

### Part 2: Inferences and Analysis
#### 1. Pick one city and category of your choice and group the businesses in that city or category by their overall star rating. Compare the businesses with 2-3 stars to the businesses with 4-5 stars and answer the following questions. Include your code.

I pick Las Vegas and shopping

<img width="619" height="794" alt="Screenshot 2026-02-16 at 23 08 19" src="https://github.com/user-attachments/assets/b22fd54e-3c4c-4d67-bda3-d36f70be259a" />

  i. Do the two groups you chose to analyze have a different distribution of hours?
 The 4-5 star group has from 8:00-16:30 (7 days a week) and 8:00-17:00 (Monday-Friday), which is 8.5-9 hours of being open each day.
- The 2-3 star group is open from 10:00-16/19:00 (Monday-Saturday) and 8:00-22:00 (7 days a week), which is 8-14 hours being open each day.

The businesses with the lower stores are open for longer times and for more days. 

##### ii. Do the two groups you chose to analyze have a different number of reviews?
Yes, the 4-5 star group has a higher average of reviews. Yet, the highest rated business with the only ranking of 5 stars only has 4 reviews.

##### iii. Are you able to infer anything from the location data provided between these two groups? Explain.

SQL code used for analysis: Above ^^

Not necessarily... there are only four businesses in Las Vegas under the category "Shopping"...

### 2. Group business based on the ones that are open and the ones that are closed. What differences can you find between the ones that are still open and the ones that are closed? List at least two differences and the SQL code you used to arrive at your answer.

Difference 1: There are more businesses Open than closed, the open businesses have a higher sum star rating.
         
Difference 2: The open businesses have a higher sum review count.
<img width="517" height="223" alt="Screenshot 2026-02-16 at 23 10 25" src="https://github.com/user-attachments/assets/94d4c38d-ca64-4068-be01-22a2d645f484" />

#### 3. For this last part of your analysis, you are going to choose the type of analysis you want to conduct on the Yelp dataset and are going to prepare the data for analysis.

Ideas for analysis include: Parsing out keywords and business attributes for sentiment analysis, clustering businesses to find commonalities or anomalies between them, predicting the overall star rating for a business, predicting the number of fans a user will have, and so on. These are just a few examples to get you started, so feel free to be creative and come up with your own problem you want to solve. Provide answers, in-line, to all of the following:

##### i. Indicate the type of analysis you chose to do:
Which city has the highest business ratings - and why.

##### ii. Write 1-2 brief paragraphs on the type of data you will need for your analysis and why you chose that data:
Performing the following query:

<img width="335" height="391" alt="Screenshot 2026-02-16 at 23 11 32" src="https://github.com/user-attachments/assets/7bb182b9-1eae-4789-97db-10f159b65923" />

---> ^^ Shows us that Las Vegas is the city with the sum highest amount of high rating businesses

Then, I did the code below with similar format for the next several cities with the highest sum of combined star ratings on Yelp. The trend is that Las Vegas simply has more businesses than the next couple, which obviously correlates to higher ratings. Las Vegas has over 400 businesses more than second place in star ratings, Phoenix, and has over 500 more than third place, Toronto.
Using this following code to find total number of businesses per city on this database:

<img width="169" height="42" alt="Screenshot 2026-02-16 at 23 11 53" src="https://github.com/user-attachments/assets/29b8b179-030a-4b4c-b034-f4a914e372d3" />

##### iii. Output of your finished dataset:
<img width="572" height="667" alt="Screenshot 2026-02-16 at 23 12 15" src="https://github.com/user-attachments/assets/0a116d4f-0ca4-4431-b5cd-00ac2aa789a1" />

##### iv. Provide the SQL code you used to create your final dataset:
<img width="349" height="116" alt="Screenshot 2026-02-16 at 23 12 35" src="https://github.com/user-attachments/assets/8242d0d2-5da2-4752-9aa3-f42c024b1a12" />














