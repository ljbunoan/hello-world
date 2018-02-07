# Question 4: Take a look at the trends in number of clicks per product over time. Describe anypatterns that you notice. This data can be found in the tracks dataset.

# Approach part 1: SQL querying

Since the data is contained in the Tracks table, I worked under the assumption that the abbrevations (first few characters) in the event column helped highlight the different products (syn, ins, alrt, mtbls, and bynd). 

When querying for this, I wanted to pull the distinct product abbreviation, the count of occurrences of that particular product event by the dates of occurence. The data needed to be grouped by the distinct abbrevations and the date, while ordered by the date the click took place (recieved_at) in ascending order.

# Approach part 2: Graphing in Excel

Taking the data from the query, I createdline charts in Excel relative to each product. JPG files of the graphs are attached in the branch. 

# Results (as a whole)

- Overall, clicks were low during the weekends (Sat, Sun) as expected since people are not in the office. In addition, Tues-Thurs tend to be the most popular days where activity took place. Clicks by day of week below:

Day     Count
Sunday  493
Monday  1512
Tuesday   1813
Wednesday 1940
Thursday	2151
Friday	1504
Saturday	587

Oddly enough, there is no increase/growth in activity over time. Clicks by product tend to be within a certain rage over the course of nearly 8 months. The next question would be to see how we can increase user behaviors and assess its value to them.

# Results (by product) 
- SYN (New Relic Question 4 SYN.jpg): During the week, clicks ranged between 20-40 per day. No signs of progressive growth over the 8 months. Most popular product that was utilized/clicked on across accounts.
- INS (New Relic Question 4 INS.jpg): generally 10-20 clicks per day durng the week. This stayed constant over the 8 months. Significant spikes took place on 4/19/17, 4/20/17, and 5/4/17. Why did these take place? Was this tied to the (or any) security breach? Was this a key promotional period for certain accounts?
- ALRT (New Relic Question 4 ALRT.jpg): Clicks per weekday ranged anywhere from 5-20. There is very minimal increse in the number of clicks as time progresses, but also there are bigger swings in number of clicks by day as we approach June.
- MTBLS (New Relic Question 4 MTBLS.jpg): not as popular of a product, as number of clicks during weekdays range anywhere from 1-6. No signs of growth over time.
- BYOND (New Relic Question 4 BYOND.jpg): Least popular product out of the 5. Will register a click or two scattered over a few days. 




